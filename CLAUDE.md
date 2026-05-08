# Long Covid Podcast — Indexed Knowledge Base

A separate knowledge base over the **Long Covid Podcast** (host: Jackie Baxter) — patient recovery stories, clinician interviews, researcher conversations. The LLM maintains a structured wiki layered on top of 211 episode transcripts; Eric asks questions about treatments, what helped/didn't help, and patterns across episodes.

**Why this is separate from `ercipedia/`.** Ercipedia is for peer-reviewed evidence — papers, trials, guidelines. The material here is **anecdote and clinical opinion**: individual recovery stories, practitioner experience, expert interviews not subject to peer review. Mixing the two would degrade the integrity of both. Keep them apart. Cross-reference by name when relevant (`See ercipedia: [[ldn]]`), but never copy podcast claims into ercipedia and never let podcast quotes update ercipedia's living pages (`mechanisms.md`, `definitions.md`, `overview.md`).

**This is a research-tracking system, not a substitute for care.** Any change to medication or activity plans belongs in a conversation with a clinician.

## Why It Exists

Eric has Long COVID with confirmed POTS and PEM (see `ercipedia/wiki/overview.md` for full clinical context). Patient stories and practitioner interviews are a *different kind of signal* than the trial data ercipedia tracks — they capture:

- What people actually try in the real world (off-label, behavioral, lifestyle)
- Which interventions show up repeatedly across many recoveries
- Practitioner perspectives that won't appear in journals for years
- Recovery trajectory patterns (timelines, setbacks, what mattered most)
- Negative experiences — things that *didn't* help or actively harmed

Whether any individual claim is **true** is downstream of the wiki. The wiki's job is to **surface and structure** the claims so Eric can examine them.

## The Theory (Karpathy-style LLM Wiki)

This setup follows Andrej Karpathy's "LLM Wiki" pattern:

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

The LLM doesn't re-read 211 transcripts on every question. Instead it builds a **persistent, compounding artifact** — a structured wiki — and queries that. Each ingest reads a transcript, extracts key information, updates relevant pages across the wiki, flags contradictions with prior episodes, strengthens cross-links. A single episode may touch 10–15 wiki pages. Over time the wiki becomes the synthesis of everything the podcast has covered, organized by intervention, theme, person, and recovery pattern — not by episode.

Sources used to inform this design:
- Karpathy's gist: <https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f>
- The Farzapedia thread: <https://x.com/karpathy/status/2040572272944324650>

## Directory Layout

```
long-covid-podcast/
├── CLAUDE.md             ← you are here
├── transcripts/          ← 211 .json + 211 .txt files (immutable; read-only)
│                           NNN_<slug>.json — full API response with timestamps
│                           NNN_<slug>.txt  — plain-text transcript (cheaper to read)
├── wiki/                 ← LLM-maintained. The LLM owns this layer entirely.
│   ├── index.md          ← content catalog, organized by category
│   ├── log.md            ← append-only ingest/query log
│   ├── overview.md       ← high-level synthesis: themes, host style, evidence quality
│   ├── episodes/         ← one short summary page per indexed episode (NNN-slug.md)
│   ├── interventions/    ← one page per single treatment/practice (LDN, mestinon, cold plunge…)
│   ├── programs/         ← named multi-component recovery programs (Gupta, DNRS, ANS Rewire,
│   │                       Visible, Curable…) — distinct from single interventions because they
│   │                       bundle education + somatic + community as a paid offering
│   ├── symptoms/         ← symptom-focused pages (brain fog, PEM, tinnitus, dizziness,
│   │                       dysautonomia…) — what helped/hurt for each, drawn across episodes
│   ├── trials/           ← named clinical trials discussed (STIMULATE-ICP, LISTEN, AXA1125,
│   │                       RECOVER, DecodeME, ReDIRECT…) — mirrors ercipedia/trials/, but
│   │                       captures patient/researcher commentary; cross-ref ercipedia for data
│   ├── recovery-stories/ ← patient recovery arcs (one page per story-teller; the journey)
│   ├── people/           ← guest experts: clinicians, researchers, practitioners, coaches,
│   │                       advocates. Role distinguished by frontmatter, not folder.
│   ├── themes/           ← cross-cutting concepts (pacing, trauma, mind-body, microbiome,
│   │                       autonomic dysfunction, viral persistence). NOT symptoms (→ symptoms/),
│   │                       NOT specific trials (→ trials/), NOT specific programs (→ programs/).
│   └── queries/          ← filed answers to substantial questions
└── _meta/
    ├── episode_list.json ← canonical list of 213 episodes with videoIds
    └── failures.json     ← episodes that couldn't be transcribed (#31, #157)
```

`transcripts/` is **immutable**. Never modify those files. Only the wiki gets written.

## Page Conventions

### Frontmatter

```yaml
---
title: Page Title
type: episode | intervention | program | symptom | trial | recovery-story | person | theme | query | overview
tags: [pem, autonomic, microbiome]
updated: 2026-05-04
episodes: [12, 87, 134]   # episode numbers this page draws from
---
```

Episode pages add:

```yaml
type: episode
episode_number: 87
guest: Dr Tania Dempsey
guest_role: clinician | patient | researcher | coach | advocate | author | host-solo
episode_date: 2024-...     # if discoverable from content
duration: 58:30
videoId: tg5jABbdkS4
interventions_mentioned: [ldn, hbot]
programs_mentioned: [gupta-program]
symptoms_discussed: [pem, brain-fog]
trials_mentioned: [recover]
themes: [mcas, autonomic-dysfunction]
```

Intervention / Program / Symptom / Trial pages all share an aggregate counts block (see "Outcome classification" below for the buckets). Counts are the **sum of evidence-log entries**, not editorial estimates — if a number changes, it's because the evidence log changed.

Intervention pages:

```yaml
type: intervention
intervention_type: drug | supplement | rehab | behavioral | dietary | device | care-model
mention_count: 14              # total episodes that name it
counts:
  key_to_recovery: 3           # someone credits it as a primary factor in their recovery
  helped_partial:  5           # tried, helped to some degree but not "the" answer
  no_effect:       2           # tried, no noticeable effect
  harmed:          1           # tried, made things worse / setback
  recommended:     4           # clinician/researcher recommends it (no own-recovery claim)
  mentioned_only:  2           # named in passing, no outcome data
sentiment_summary: mixed       # one-word vibe: helped-many | helped-some | mixed | mostly-unhelpful | harm-reported
```

Program pages (same `counts` schema):

```yaml
type: program
program_kind: brain-retraining | somatic | mind-body | tracker-app | community | clinic-protocol
official_url: https://...
mention_count: 7
counts:
  key_to_recovery: 4
  helped_partial: 1
  no_effect: 0
  harmed: 0
  recommended: 1
  mentioned_only: 1
sentiment_summary: helped-many
```

Symptom pages:

```yaml
type: symptom
symptom_cluster: fatigue-pem | cognition | autonomic-pots | sleep | breathing | smell-taste | pain | sensory
related_interventions: [ldn, mestinon, pacing]   # interventions tagged against this symptom
mention_count: 22
top_helpers: [pacing, mestinon, ldn]              # interventions whose evidence log links this symptom + outcome=key_to_recovery|helped_partial
```

Trial pages:

```yaml
type: trial
trial_name: STIMULATE-ICP
status: recruiting | completed | published | preprint | unknown
investigators: [Amitava Banerjee]
mention_count: 3
ercipedia_crossref: trials/stimulate-icp.md
```

Person pages add:

```yaml
type: person
role: clinician | researcher | practitioner | coach | advocate | journalist | author | patient-advocate
specialism: cardiology | autonomic | mcas | microbiome | nutrition | psychology | physio | …
affiliation: Imperial College, Bateman Horne Center, …
episodes: [40, 87, 142]
notable_claims: [short bullet list of positions/arguments this person makes]
```

### Formatting

- Internal links: `[[page-name]]` (Obsidian wikilinks)
- Episode references inline: `(ep #87)` — links resolve via filename `087-...md`
- Quotes from transcripts: blockquote with `— guest, ep #N`
- Every page ends with `## See also` listing cross-references
- Lowercase-hyphen filenames; no spaces

### Cross-referencing into ercipedia

When an intervention or concept already has a peer-reviewed page in `ercipedia/`, link out as text only:

> Cross-ref: see `ercipedia/wiki/interventions/ldn.md` for the trial evidence on this.

Don't import ercipedia content here, and don't push podcast content there.

### Outcome classification (the strength signal)

Every time an intervention, program, or trial appears in an episode, the agent must classify the **outcome** for that mention into one of six buckets. The aggregate counts in frontmatter are derived directly from these classifications.

| Bucket | When to use | Strength as evidence |
|---|---|---|
| `key_to_recovery` | A guest with a recovery story explicitly credits this thing as a primary factor in their recovery (top-3 things that mattered). Example: "Gupta was probably 60% of why I got better." | **Strongest** — patient with successful recovery names this. |
| `helped_partial` | Someone tried it and reports clear partial benefit (symptom relief, energy uplift, mood improvement) but doesn't credit it as primary. Example: "LDN took the edge off my pain but I still had PEM." | Strong — direct first-person benefit report. |
| `no_effect` | Someone tried it and reports no noticeable effect after a fair trial. | Important and frequently underreported — log it. |
| `harmed` | Someone tried it and got worse, had a setback, had a serious side effect, or had to stop. | Critical signal — log every instance. |
| `recommended` | A clinician/researcher recommends it from clinical/research experience but the speaker is **not** themselves a recovered patient using it. Example: Dr Khan saying "we see good results with X in our clinic." | Medium — expert opinion, no patient outcome attached. |
| `mentioned_only` | Named in passing, no outcome data ("I tried lots of things including X, Y, Z…"). | Weakest — useful only for completeness. |

**Rules:**
- One episode can produce multiple entries for the same intervention if multiple speakers express different outcomes.
- If a guest tried the same thing twice with different outcomes (e.g. "first attempt didn't work, second time it helped"), log both.
- **Same speaker, same intervention, same outcome, different episode = one row, not two.** When a guest reaffirms a previous intervention with the same outcome in a later episode (e.g. Jackie reaffirms breathwork as `key_to_recovery` in #94 having already done so in #64), **do not add a new row and do not increment `counts`**. Update the existing row's notes to reference the later episode and capture any new framing. The episodes-list frontmatter can include the later episode for cross-reference.
- `key_to_recovery` requires the guest to have an actual recovery (full or substantial). It is not used for "I'm hoping this will work."
- When in doubt between `helped_partial` and `mentioned_only`: if there's a specific benefit named, it's `helped_partial`; if it's a name-drop without consequence, `mentioned_only`.
- `recommended` and `key_to_recovery` are mutually exclusive for the same speaker on the same intervention. Patient who recovered using X = `key_to_recovery`. Clinician recommending X to others = `recommended`. Both can coexist on the same page from different speakers.

### Required body section: "Evidence log"

Every intervention / program / symptom / trial page must include this section near the bottom. It is the source of truth that frontmatter counts derive from. Format as a markdown table:

```markdown
## Evidence log

| Ep | Speaker | Role | Outcome | Indication | Notes |
|---:|---|---|---|---|---|
| #87 | Suzy Bolt | coach (recovered patient) | key_to_recovery | pem, fatigue, dysautonomia | "Gupta was the biggest single factor in my recovery." Combined with pacing + somatic work. |
| #102 | Dan Neuffer | coach (recovered, founder of ANS Rewire) | recommended | autonomic-dysfunction, fatigue | Argues nervous-system retraining is upstream of most LC symptoms. |
| #145 | Anonymous patient | patient | harmed | pem | Crashed after trying GET-style component too aggressively; had to stop. |
```

The agent updating this page on a new ingest **appends a row**, then recomputes the `counts:` block in frontmatter. Counts and rows must always agree.

#### `Indication` column (added 2026-05-04, batch #90–#99)

Comma-separated list of symptoms / mechanisms / patient-profile slugs that the row's outcome applies to. Lets Eric query "what helped people with my profile" instead of reading every log and filtering mentally.

**Controlled vocabulary** — match `wiki/symptoms/` slugs where possible:
- Symptom slugs: `brain-fog`, `breathing-pattern-disorder`, `dysautonomia`, `gi-dysfunction`, `mcas`, `pain`, `pem` (= post-exertional-malaise), `pots`, `smell-loss-parosmia`, `tinnitus`
- Common non-symptom indications: `fatigue`, `sleep`, `mental-health`, `hair-loss`, `joint-pain`, `anxiety`, `depression`
- Mechanism / patient-profile tags: `viral-persistence`, `autoimmunity`, `microclots`, `mitochondrial`, `hormonal-dysfunction`, `eds-hypermobility`, `vaccine-injury`, `severe-bedridden`, `paediatric`

**Filling rules:**
- Use what the speaker explicitly says the outcome applies to. If they say "X helped my fatigue and brain fog", indication = `fatigue, brain-fog`.
- If a clinician recommends an intervention for a specific patient profile (e.g., POTS), indication = `pots`.
- If indication is genuinely broad / unspecified, write `general-lc`.
- If you can't tell from the transcript, leave `—` and flag in lint.
- Older rows added before 2026-05-04 may have empty Indication cells (`—`). Backfill is a future task; don't blanket-fill from memory.

### Querying with these counts

When Eric asks "how often did X actually drive a recovery?", answer with the explicit breakdown — not a single number:

> ANS Rewire — discussed in 11 of 211 episodes.
> - **key_to_recovery: 4** (4 patients credited it as primary in their recovery arc)
> - helped_partial: 2
> - no_effect: 1
> - harmed: 0
> - recommended: 3 (including Dan Neuffer, the founder)
> - mentioned_only: 1
>
> **Read this as:** out of 211 episodes, 4 recovered patients name ANS Rewire as a key factor. That's a stronger signal than the raw mention count of 11 suggests, but still N=4. Cross-check against ercipedia for any RCT-level evidence.

Always lead with `key_to_recovery` and `harmed` — those are the two buckets Eric cares about most.

## Workflows

### Ingest (one transcript)

1. Read the `.txt` transcript (cheaper than `.json`; only use `.json` if you need timestamps for citation precision).
2. Identify, with explicit lists:
   - **Guest** + role (clinician / researcher / practitioner / coach / advocate / patient / author / host-solo)
   - **Single interventions** named (LDN, mestinon, breathing exercise, cold plunge, …)
   - **Named programs** mentioned (Gupta, DNRS, ANS Rewire, Visible, Curable, …)
   - **Symptoms** discussed at length (brain fog, PEM, tinnitus, dizziness, dysautonomia, …)
   - **Named clinical trials** referenced (STIMULATE-ICP, LISTEN, RECOVER, AXA1125, DecodeME, …)
   - **Themes** (cross-cutting concepts: pacing, trauma, mind-body, microbiome, viral persistence, …)
   - **Explicit "what helped"/"what didn't help"** claims, with attribution
   - **Did the guest recover?** (full / substantial / partial / no / not-discussed) — this gates whether their named interventions can earn `key_to_recovery`.
3. Write `wiki/episodes/NNN-slug.md` — short summary (≤300 words), structured, with quote pulls keyed to interventions/programs/symptoms/themes.
4. For each intervention/program/symptom/trial mentioned: open or create the page, **classify the outcome for this episode** (one of six buckets — see "Outcome classification" above), append a row to its Evidence log table, recompute `counts:` in frontmatter. Counts must always equal the row totals.
5. Update each affected `wiki/themes/<name>.md` similarly (themes don't have outcome buckets — they have prose summaries plus episode lists).
6. Create or update `wiki/people/<slug>.md` for the guest (and any third party named substantively, e.g. when guest A discusses guest B's work). Use frontmatter `role` to distinguish.
7. If the episode is a recovery story, create or update `wiki/recovery-stories/<name>.md` — focus on the *journey/arc* (timeline, triggers, low points, turning points). The intervention list lives on the intervention pages, not here.
8. Update `wiki/index.md`.
9. Append to `wiki/log.md`: `## [YYYY-MM-DD] ingest | #NNN — Title`.

### Bulk ingest

When indexing many episodes in one run, batch the per-episode work but write to disk after each episode (so a crash mid-run doesn't lose progress). Update `index.md` at the end of the batch, not after every episode.

### Query

When Eric asks a question:

1. Read `wiki/index.md` to find the relevant intervention/theme/recovery-story pages
2. Read those pages
3. **Pull supporting quotes from the underlying transcripts** — never invent quotes; if a page references ep #87 say "X helped," verify by reading the transcript snippet before quoting
4. Synthesize an answer. Required structure when reporting on an intervention:
   - **Mention frequency**: "discussed in N of 211 episodes"
   - **Sentiment breakdown**: who said it helped / didn't help / harmed
   - **Who said it**: patient with similar profile, clinician, researcher
   - **Caveats**: dose, duration, what else was happening
5. If the answer is substantial, file it as `wiki/queries/<slug>.md`
6. Always include this disclaimer in queries: "Based on podcast testimony — this is anecdotal evidence, not clinical proof. Cross-check against `ercipedia/` for peer-reviewed evidence before acting."

### Lint

- Episodes with no interventions/themes extracted (probably under-processed)
- Interventions mentioned in transcripts but not in the wiki
- Contradictions between episode pages
- Orphan pages with no inbound links
- Stale sentiment labels (e.g. an intervention now has 10 mentions, but the page summary still cites 3)
- **Count integrity**: `counts:` block in frontmatter must equal row totals in the Evidence log. Sum check: `sum(counts.values()) == mention_count == len(evidence_log_rows)`. Any mismatch is a lint failure to fix immediately.
- **Suspect `mentioned_only`**: if an intervention page is dominated by `mentioned_only`, re-read those transcripts — the agent may have under-classified. Real outcomes hide in lazy classifications.
- **Missing `harmed` evidence**: if a popular intervention shows zero `harmed` rows, double-check — null findings are often missed. Re-scan the relevant transcripts for negative experiences.

## Evidence Rules (different from ercipedia)

The whole point of the separation is that **the rules for trusting podcast content are different**. Be explicit:

1. **Default evidence grade is "anecdote/expert-opinion."** Never elevate this to "evidence" without an external citation.

2. **Track who said what.** A claim from a board-certified specialist (Dr Asad Khan, Dr Amy Proal, Dr Boon Lim) is weighed differently than a claim from a recovered patient or a coach. Tag `guest_role` accurately.

3. **Recovery stories are N=1.** Every "this helped me" is one data point. The interesting signal is the *pattern across many stories*, not any single account.

4. **Negative experiences matter.** When a guest says X didn't help or made them worse, log it with equal weight. Patients tend to over-report what worked; capture the failures explicitly.

5. **Distinguish "I tried it and it helped" from "research shows it works."** Guests often blur this. The wiki should not.

6. **No medical recommendations.** This wiki indexes claims; it doesn't endorse them. Eric makes treatment decisions with his clinicians.

7. **Date-context everything.** A 2021 episode discussing "the latest research" is now 5 years out of date. Note episode dates where they matter.

## Eric's Context (read before answering personal questions)

If Eric asks "would this help me?", you need to remember his clinical picture:

- POTS (confirmed via tilt) + PEM as defining features
- Currently on: ivabradine, mestinon, florinef, zyrtec/pepcid, bufomix p.r.n., D-vitamin
- Possible MCAS overlap (empirical antihistamine trial)
- See `ercipedia/wiki/overview.md` for the full picture

Prioritize episodes featuring guests with similar presentations (POTS, PEM, MCAS overlap) when filtering recommendations. De-prioritize unrelated symptom profiles.

## Accessibility / TTS

Eric prefers responses read aloud via TTS. Include `<!-- TTS: "spoken summary" -->` in every response. Keep TTS text concise and natural — write it as you'd say it, not as you'd read it. Skip markdown, URLs, long code, tables. Use `<!-- TTS: SILENT -->` only for purely technical output with no conversational content.

## Tone and Language

- Clinical but accessible. Eric is the audience.
- Default English. Swedish in parentheses where it lands more naturally.
- When summarizing a guest's claims, use direct attribution: "Dr Khan argues…" not "Research shows…"

## Source Material — Quick Facts

- **Channel**: Long Covid Podcast on YouTube (`@longcovidpodcast`)
- **Host**: Jackie Baxter — herself a long-hauler; recovered/recovering, advocates, runs support groups
- **Episodes covered here**: 211 of 213 (transcripts unavailable for #31 and #157 — see `_meta/failures.json`)
- **Total runtime indexed**: ~167 hours
- **Format**: most episodes are 30–60 min interviews; a handful are host-solo reflections
- **Auto-captions**: transcripts are YouTube auto-generated, so expect occasional misspellings of names and medical terms (e.g. "long C podcast" instead of "Long Covid podcast"). When extracting names, sanity-check against episode titles.

## Index and Log Conventions

### `wiki/index.md`

Organized by category (episodes by number, interventions A–Z, etc.). Each entry: `- [[page-name]] — one-line summary`. Update on every ingest (or at end of batch).

### `wiki/log.md`

Append-only. Each entry: `## [YYYY-MM-DD] verb | Title`. Verbs: `ingest`, `query`, `lint`, `update`, `init`. Parseable: `grep "^## \[" wiki/log.md | tail -10`.
