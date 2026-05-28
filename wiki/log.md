---
title: Log
type: log
---

# Log

Append-only. Each entry: `## [YYYY-MM-DD] verb | Title`. Verbs: `ingest`, `query`, `lint`, `update`, `init`.

## [2026-05-04] init | scaffolded long-covid-podcast knowledge base

- Created directory next to `ercipedia/`, kept fully separate (different evidence class).
- 211 of 213 episode transcripts copied into `transcripts/` (.json + .txt). Missing: #31 (Zoe Challenor & Long Covid Choir), #157 (Ellen Alden's Recovery) — YouTube has no captions for those videos.
- Wrote `CLAUDE.md` with Karpathy-style LLM-wiki workflow, schema, evidence rules.
- Wiki categories: episodes, interventions, programs, symptoms, trials, recovery-stories, people, themes, queries. (Refined from initial draft after reviewing what the podcast actually covers — interventions alone wasn't enough; symptoms, named trials, and named multi-component programs each deserve their own axis. `researchers/` renamed to `people/` because guests cross categories.)
- Added 6-bucket outcome classification (`key_to_recovery`, `helped_partial`, `no_effect`, `harmed`, `recommended`, `mentioned_only`) so the wiki distinguishes "actually drove a recovery" from "was named in passing." Every intervention/program/trial page now has a `counts:` block in frontmatter derived from a required Evidence log table in the body. Lint enforces count integrity.
- `wiki/` empty except for stubs — ready for first ingest.

## [2026-05-04] ingest | #001 — Barbara Melville from Long Covid Scotland

Advocacy/policy episode — no interventions to log. Created people pages for Barbara, Jackie (host), Claire Hastie. Theme stubs: advocacy, healthcare-gaslighting.

## [2026-05-04] ingest | #002 — Jackie's Personal Story

Host's own story. PEM clearly described without the term. Logged graded-exercise (harmed; PT-prescribed interval training pre-PEM-awareness), breathwork (helped_partial; Wibbs Coulson class), yoga (helped_partial). Created PEM symptom page, pacing theme, long-covid-breathing program (the host's own course — sponsor segment, treat as such).

## [2026-05-04] ingest | #003 — Chiara Berardelli (singer/former GP)

Headache-dominant LC; improving at recording. Logged radical-rest (helped_partial), counselling (helped_partial), yoga (helped_partial — second mention), wild-swimming (helped_partial). Migraine medication declined; not tested.

## [2026-05-04] ingest | #004 — Research projects / Glasgow Science Festival

Meta-research episode. Created trial stubs: LOCO-RISE, ReDIRECT, ZOE Covid Study. People: Jane Ormerod, Chris White (co-chairs of Long Covid Scotland research subgroup).

## [2026-05-04] ingest | #005 — Dr Amy Small (GP, long-hauler, advocate)

POTS-defining clinician-patient. Logged **beta-blockers (key_to_recovery)** — first key_to_recovery entry in the wiki. Pacing (helped_partial — second mention). Created POTS symptom page (highly relevant to Eric).

## [2026-05-04] ingest | #006 — Prof Nick Sculthorpe (UWS)

Researcher episode. Created TraPS and HEARTPACE trial pages. Important methodological framing: PEM per Canadian criteria (≥14h) only captures 40–50% of LC patients; HR-based pacing fails for POTS so steps are tracked instead.

## [2026-05-04] ingest | #007 — Suzy Bolt (mind/body/soul)

Major recurring figure. Recovered. Created suzy-bolt-recovery program page (founder's own recovery — caveated as expected-bias). Stasis breathing program (recommended). Many forward references to later episodes (Boon Lim, Melanie Dani, Wibbs Coulson, Vicky Jones).

## [2026-05-04] ingest | #008 — Rachel Whitfield (recovery story)

First full recovery arc indexed. Logged **Lightning Process (key_to_recovery)** — second key_to_recovery in the wiki, first brain-retraining program with a credited recovery on this podcast. Created Optimal Health Clinic program (recommended). First recovery-story page.

## [2026-05-04] ingest | #009 — Claire Hastie (Long Covid Support founder)

Origin story of the term *long covid* (with Elisa Perego, Italian archaeologist on Twitter, May 2020). Origin of the "rehab, research, recognition" slogan adopted by the WHO. Spinoffs: Long Covid Kids, Long Covid Wales, Long Covid Physio.

## [2026-05-04] ingest | #010 — Amanda Finley (Covid-19 Long-Haulers Discussion Group)

US-side advocate. Brings socio-economic and structural-barrier story sharply into focus — federal post-covid clinics require a positive PCR (locks out almost the entire first wave); FMLA is unpaid; many patients become homeless. References to Patient-Led Research Collaborative (Hannah Davis, Lisa McCorkell), Ziyad Al-Aly (Wash U), Ed Yong (Atlantic).

## [2026-05-04] checkpoint | first 10 episodes ingested

- 10 of 211 episodes done. Index.md updated with all created pages plus a "placeholder targets" section listing wikilinks-without-files for the next ingest pass to fill in.
- Counts so far: 10 episode pages · 11 people pages · 7 intervention pages · 5 program pages · 5 trial pages · 2 symptom pages · 3 theme pages · 1 recovery-story page.
- Recovery stories logged: 1 (Rachel Whitfield, ep #8). Self-reported recovered guests so far: Suzy Bolt (ep #7) and Rachel Whitfield (ep #8).
- key_to_recovery entries logged: 2 (beta-blockers in ep #5; Lightning Process in ep #8).
- harmed entries logged: 1 (graded-exercise in ep #2).

## [2026-05-04] ingest | #011 — Iain on partner-of-someone-with-chronic-illness

Carer perspective episode. No interventions to log. Created [[iain]] guest page; theme pages [[caregiver-burden]] and [[partner-support]] referenced as placeholders. Iain's "team" framing and oxygen-mask-first framing exported to caregiver-burden.

## [2026-05-04] ingest | #012 — Kelly Mitchell, the Breathing PT

Foundational breathing-pattern-disorder episode. Logged breathwork as `recommended` (Kelly), updated mention_count from 1→2 then on through #17 to 4. Cited paper: 74% of LC patients have low end-tidal CO₂. Created [[kelly-mitchell]]. First explicit cite of the dysfunctional-breathing → low-CO₂ → systemic-symptoms model.

## [2026-05-04] ingest | #013 — AJ ("Finding My Sparkle")

⚠️ **Cross-condition episode** — AJ has post-concussion-syndrome, not LC. Episode logged as parallel-wisdom; created [[aj-finding-my-sparkle]] guest page; introduced **happy list** concept. Logged yoga-nidra and meditation as `recommended` from her experience but explicitly tagged as cross-condition. TENS, acupressure mat, flotation tank documented in episode page only — not added to LC intervention pages because non-LC speaker (will revisit if these surface again from LC patients).

## [2026-05-04] ingest | #014 — Long Covid Creativity 2021

Compilation episode of 9 patient voices via poems/songs/art. No outcomes logged. Notable: John Kennedy's microclot-hypothesis rhyme is the first explicit microclot reference on the podcast (placeholder theme [[microclots]] flagged). Long Covid Choir (ep #31 has no transcript per `_meta/failures.json`) gets first podcast appearance via [[zoe-chalena]]. Light patient pages flagged for future creation.

## [2026-05-04] ingest | #015 — Festive Compilation

Clip reel of episodes #1–#13. No new content. Episode page created for navigation; no other wiki updates.

## [2026-05-04] ingest | #016 — ReDIRECT Study

Major update to [[redirect]] trial page with full design walkthrough — 200 pts, BMI > 27, 12-week TDR, 1:1 dietitian, **mosaic outcome design** (each pt nominates own primary symptom). Created [[david-blane]] and [[emily-combet]] guest pages. Anti-inflammatory-via-weight-loss is the explicit hypothesis; design accommodates LC heterogeneity.

## [2026-05-04] ingest | #017 — Wibbs Coulson — Breathing for Long Covid

Major breathwork episode. Logged as `recommended`; pushed mention_count to 4. Created [[wibbs-coulson]] guest page. Introduced [[bolt-score]] concept (Jackie's BOLT moved 6→24 sec). Yin yoga + yoga nidra explicit; Mount Sinai pattern named. Cross-references Patrick McKeown, Andrew Huberman, Justin Feinstein, Sapolsky. Paired with #12 — same physiological model from different professional roots.

## [2026-05-04] ingest | #018 — Louise Cummings — Cognitive & Linguistic Difficulties

First research-grade brain-fog episode. N=142 study, six matched groups. Three robust LC deficits: verbal recall, verbal fluency, discourse informativeness. ME/CFS comparison group matched controls on most measures except letter fluency — preliminary signal that fatigue alone may not drive LC cognitive deficits. **Coined "cognitive pacing"** on the podcast — created theme page [[cognitive-pacing]]. Created [[louise-cummings]] and [[brain-fog]] symptom page.

## [2026-05-04] ingest | #019 — Cass MacDonald — Life Adjustments for Chronic Conditions

Most operationally detailed episode in the wiki for daily-life management. Major update to [[pacing]] theme. Cass has EDS-hypermobility + chronic-pain + asthma + autism + MDD pre-LC, plus LC since April 2020. No interventions logged into intervention pages individually (gabapentin, antihistamines, asthma inhalers — all placeholder targets); the load-bearing content is the *framework* for pacing/aids/return-to-work/UK-benefits/communication. Created [[cass-macdonald]] guest page. Strong "boom-and-bust pacer" honesty.

## [2026-05-04] ingest | #020 — Amy Anker — Recovery & Positively Covid

⚠️ **Naming clarification:** this Amy is **not** Dr Amy Small (ep #5). Different person; correction logged on dr-amy-small.md and ep-005 page. Second full recovery in the wiki (after Rachel Whitfield ep #8). Strongly **neurological** LC presentation that resolved via neuroplasticity-rooted approach + 4-pillar daily routine + nervous-system-loop interruption. Created [[amy-anker]] and [[recovery-stories/amy-anker]]. Created [[positively-covid]] program page (1 key_to_recovery, founder's own recovery — caveat as expected-bias). Created [[walking]] intervention page (1 key_to_recovery from Amy). Created [[mind-body]] theme page (consolidates the recurring NS-regulation framing across #7, #8, #17, #20).

## [2026-05-04] checkpoint | episodes 11-20 ingested

- 20 of 211 episodes done. Index.md updated.
- Counts so far: 20 episode pages · 20 people pages · 10 intervention pages · 6 program pages · 5 trial pages · 4 symptom pages · 5 theme pages · 2 recovery-story pages.
- Recovery stories logged: 2 (Rachel Whitfield ep #8 — Lightning Process; Amy Anker ep #20 — neuroplasticity/NS-loop interruption + Positively Covid).
- key_to_recovery entries logged: 4 (beta-blockers ep #5; Lightning Process ep #8; walking ep #20; Positively Covid ep #20). Note: Amy Anker's recovery technically generates two key_to_recovery entries on different pages — walking is the one specific intervention she names; the four-pillar routine on Positively Covid is the meta-framework.
- harmed entries logged: 1 (graded-exercise ep #2).
- Cross-condition episode: 1 (AJ ep #13, post-concussion-syndrome — flagged, kept conservative on intervention buckets).
- Methodological note: Amy Anker recovery (#20) is the second mind-body-framework recovery in the wiki and reinforces — but does not yet establish — a pattern. Watch for more in eps 21+ and weigh against contradicting cases.

## [2026-05-04] ingest | #021 — Moira Newiss — Nutritional Therapist

Practitioner episode (no recovery). Created [[moira-newiss]], [[anti-inflammatory-diet]], [[low-histamine-diet]], [[keto-diet]], [[gut-health]], [[mitochondrial-dysfunction]] theme. Five LC mechanisms framed under inflammation; Naviaux cell-danger-response narrative introduced. Notable: Jackie's aside that low-histamine didn't help her → first `no_effect` row on [[low-histamine-diet]].

## [2026-05-04] ingest | #022 — Eddie Duncan & LOCO-RISE

Major update to [[loco-rise]]: full design walkthrough (4 boards, 100 patients each, mixed-methods, 3-month follow-up). PPI panel includes [[jane-ormerod]]. Created [[eddie-duncan]] guest page. Cautioned on HBOT → ongoing Karolinska RCT in Finland. £10M Scottish gov funding (highest per-capita UK).

## [2026-05-04] ingest | #023 — Sally Riggs — Psychologist & Long-Hauler

**Third recovery arc** (substantial). Created [[sally-riggs]], [[low-dose-naltrexone]], [[safe-and-sound-protocol]], [[polyvagal-theory]], [[immobilization]] themes. Multi-component recovery — LDN → keto → SSP → polyvagal frame. Notable: **second `no_effect` for low-histamine diet** (Sally explicit: "was not the diet for me"). Stasis-breathing tried twice and abandoned (logged as user-fit issue, not intervention failure). Strongest polyvagal-frame episode in the wiki so far.

## [2026-05-04] ingest | #024 — Alec Finlay — "I Remember"

ME-30-yrs-then-LC artist. Designed Scotland's national Covid Memorial in Pollok Country Park. Politically rich, no clinical content; no evidence-log rows. Created [[alec-finlay]], [[me-cfs-parallels]] theme. Strongest-yet ME↔LC parallel voice on the wiki ("if we'd spent 30 years researching ME we'd have medicine for LC now").

## [2026-05-04] ingest | #025 — Scottish Opera's Breath Cycle

New program page: [[breath-cycle]]. Lineage from 2013 cystic-fibrosis pilot (~14% lung-capacity uplift; n≈18). LC adaptation in pilot — three 12-week cohorts, online, lunchtime sessions, free. Created [[david-douglas]] and [[gareth-williams]] guest pages. Sits next to [[long-covid-breathing]] and [[stasis-breathing]] as the breath-focused programs in the wiki.

## [2026-05-04] ingest | #026 — Dr Jackie Maybin — Reproductive Health

First menstrual-and-LC episode. Created [[jackie-maybin]], [[ergo-menstrual-study]] trial page (covers all three studies — Edinburgh ERGO + Bristol app + Oxford closed survey). First analysis from Oxford survey: ~80% no menstrual change post-vaccination, ~20% had temporary disturbance, no long-term signal. Inclusion criteria require regular cycles → flagged as exclusionary; future studies will broaden.

## [2026-05-04] ingest | #027 — Jenny Ceolta-Smith — Aftermath of Leaving Work

First substantial **employment / benefits** episode. Created [[jenny-ceolta-smith]] guest page; [[employment]] theme page (UK-focused: ACAS 3-months-less-1-day, ESA £74.70/week, PIP appeal route, Permitted Work). Headline advice: **don't resign — wait to be dismissed**. Documentation discipline (bounce-back-in-writing) emphasised.

## [2026-05-04] ingest | #028 — Ziyad Al-Aly — Doctor & Researcher

Big-data systems-level epidemiology episode. Created [[ziyad-al-aly]], [[viral-persistence]] theme. NIH 44-person autopsy preprint cited (virus in brain/lung/kidney/liver months post-acute). LC = systemic infection, not respiratory. Vaccinated breakthrough = small risk reduction, not elimination (n≈33,000). Omicron not "mild" in absolute terms because of volume. Frames patient advocacy as the **Larry Kramers of LC**.

## [2026-05-04] ingest | #029 — Lorna Nicholson — POTS & Breathing

Most consolidated POTS-and-breathing episode in the wiki. Major updates to [[pots]] (third row); created [[lorna-nicholson]], [[buteyko-breathing]], [[pilates]], [[cold-water-exposure]] interventions; [[sirpa]] program; [[breathing-pattern-disorder]] symptom; [[trauma-and-illness]] theme. Cites a study identifying breathing-pattern disorder as a core feature of POTS. Strong upstream framing: covid is the trigger; the pre-existing nervous-system pattern is what makes it stick. Co-founder of POTS UK (2010).

## [2026-05-04] ingest | #030 — Dr Gavin Francis — GP & Author

Convalescence-as-lost-concept episode (his book *Recovery*). Created [[gavin-francis]], [[convalescence]] theme. "Doctors are gardeners, not mechanics." Key distinction: acceptance of *this moment* ≠ acceptance of *being-this-way-forever*. Snakes-and-ladders metaphor for non-linear recovery. No interventions logged — pure framing episode, but very high signal as a counterweight to the more interventionist episodes in the wiki.

## [2026-05-04] checkpoint | episodes 21-30 ingested

- **30 of 211 episodes done.** Index.md and log.md updated.
- **Counts now**: 30 episode pages · 31 people pages (added 11 new) · 18 intervention pages (added 8 new) · 8 program pages (added 2 new) · 6 symptom pages (added 2 new) · 14 theme pages (added 9 new) · 6 trial pages (added 1 new) · 2 recovery-story pages.
- **Recovery stories logged: 3** (Rachel Whitfield ep #8 — Lightning Process; Amy Anker ep #20 — neuroplasticity/NS-loop; Sally Riggs ep #23 — substantial recovery via LDN + keto + SSP + polyvagal). Sally's recovery is the first **multi-component, anti-glamour** recovery — explicitly no silver bullet, attribution split across many interventions.
- **key_to_recovery entries**: still 4 (no new ones in 21-30 — Sally frames her recovery as multi-component → `helped_partial` rows on multiple pages rather than `key_to_recovery`).
- **helped_partial entries added**: 3 (LDN ep #23, keto ep #23, SSP ep #23).
- **no_effect entries**: 2 new on **low-histamine diet** (Jackie ep #21 aside; Sally ep #23). Now 2/3 mentions of low-histamine on the wiki are no-effects — first intervention with an explicit *negative* signal of size.
- **harmed entries**: still 1 (graded-exercise ep #2).
- **Cross-cutting themes that came online**: polyvagal theory (Riggs, Nicholson, framing-adjacent in Anker); ME↔LC parallel (Finlay, Al-Aly, Nicholson — strongly attested now); trauma-and-illness upstream framing (Riggs + Nicholson); convalescence (Francis); employment / UK benefits (Ceolta-Smith). The mind-body cluster now has four named frameworks (NS-loop / polyvagal / SIRPA / convalescence) — same underlying terrain in different vocabularies.
- **Methodological note**: After three recoveries (Whitfield #8, Anker #20, Riggs #23), the pattern is *all three routes are different* — Lightning Process / neuroplasticity-routine / multi-component pharma+diet+SSP. Unifying thread is **NS-regulation framing**, not any single intervention. Continue to log negative findings with equal weight (Sally's no_effect on low-histamine; stasis-breathing user-fit failure).

## [2026-05-04] ingest | #032 — Esther's Recovery Story (TMS / Mind-Body)

The wiki's **fourth full recovery** and the first via the explicit **TMS / Mind-Body Syndrome** lineage (Sarno → Schubiner → Sachs). Recovery date precise: 2 June 2021, ~80% symptom drop within hours of listening to a Nicole Sachs podcast. Created [[esther-rotterdam]] guest page, [[recovery-stories/esther-rotterdam]], [[tms-mind-body-syndrome]] program (with the four-route comparison table), [[longcovidcured-com]] (her recovery-stories blog), [[self-compassion]] theme (gating piece for high-self-critic personalities). 30-year pre-COVID pattern of migraines / fatigue / pain — same nervous-system pattern, COVID was the trigger. First `key_to_recovery` of the batch.

## [2026-05-04] ingest | #033 — Resia Pretorius & Douglas Kell — Microclots

The wiki's **anchor microclot mechanism episode**. Created [[resia-pretorius]], [[douglas-kell]], [[microclots]] theme, [[endothelial-dysfunction]] theme. Documents amyloid-form fibrin microclots resistant to fibrinolysis; trapped inflammatory mediators (von Willebrand factor, plasminogen, antiplasmin); spike protein and LPS as triggers; capillary entrapment → systemic cellular hypoxia framework. Treatment principles via clinical collaborators: triple therapy (asp+clop+DOAC) + HELP-apheresis (Jaeger). UK adoption gated on local replication despite SA/EU work being well-published.

## [2026-05-04] ingest | #034 — Sam Munslow — *The Covid Coach*

The wiki's **fifth full recovery** and the first where the "what worked" wasn't an intervention but a sustained psychological-skill rebuild. Created [[sam-munslow]], [[recovery-stories/sam-munslow]], [[mental-self-harming]] theme, [[communication]] theme. Permanent chemical-sensitivity legacy (no hair dye / makeup) is a quiet MCAS pointer she doesn't frame as such. Onset 5 April 2020. Recovery via reapplying her own coaching toolkit — only effective once she could re-read her own writing months later.

## [2026-05-04] ingest | #035 — Axcella Therapeutics — AXA1125

The wiki's **first deep dive on a long-covid pharma candidate**. Created [[bill-hinshaw]], [[margaret-koziel]], [[axa1125]] intervention, [[axa1125-oxford]] trial. Endogenous metabolic modulator (composition of amino acids and derivatives). Oxford Phase 2A in flight at recording, MRS muscle-mitochondria readout, results mid-2022. Cross-track ercipedia for trial outcomes. Outcome class: `recommended` until trial reads out + recovered-patient testimony lands.

## [2026-05-04] ingest | #036 — Dr Mark Faghy — Derby Cohort & Patient Voice

The Derby research-infrastructure episode. Created [[mark-faghy]], [[derby-cohort-observation]] / [[derby-patient-voice-survey]] / [[derby-rehab-delphi]] trial pages. 16-week bi-weekly cohort UK+US+India; 70-question patient-voice survey designed by patients (185 responses; visual dissemination planned). Delphi for LC rehab blueprint with system-science underpinning. "Buffet" multi-component support model framed against fragmented status-quo (echoes Cass #19 + Khan #37). No `key_to_recovery` rows — strictly research-infrastructure.

## [2026-05-04] ingest | #037 — Dr Asad Khan — Apheresis & Triple Therapy

The wiki's **anchor clinical apheresis + triple-therapy episode**, paired with #033 mechanism. Created [[asad-khan]], [[helapheresis]], [[triple-therapy-anticoagulation]], [[omalizumab-xolair]], [[midodrine]], [[mestinon]] (real page, replacing placeholder), [[ivabradine]] (real page), [[fludrocortisone]] (real page), [[vagus-nerve-tens]], [[reinfection]] theme, [[vaccine-injury]] theme, [[jess-taylor]] (placeholder for now). Khan's pattern: HELP-apheresis (Jaeger Mülheim, 7-8 cycles Sep-Oct 2021) → triple therapy (asp+clop+dabigatran Nov 2021) → best baseline → reinfection knocks down. Reinfection serology pattern: undetectable Spike+N in Dec 2021 → both above-detectable May 2022, all PCR/LFT-negative. Major signal — first wiki documentation of reinfection-as-baseline-degrader. New `helped_partial` rows on apheresis (1) + triple therapy (1) + omalizumab (1) + midodrine (1) + mestinon (1) + vagus-nerve TENS (1). One `harmed` row on vaccine-during-LC. One `no_effect` on Paxlovid.

## [2026-05-04] ingest | #038 — Dr Tina Peers — MCAS & Long Covid

The wiki's **anchor MCAS-treatment-protocol episode**. Created [[tina-peers]], updated [[mcas]] symptom page (now 6 mentions; top helpers list updated). Created [[antihistamines]] (real page replacing placeholder), [[montelukast]], [[sodium-cromoglicate]], [[ketotifen]], [[arc-microtech-device]], [[gupta-program]] (real page replacing placeholder). Updated [[low-histamine-diet]] (now 4 mentions, 2 recommended), [[low-dose-naltrexone]] (now 2 mentions). Peers's protocol: low-histamine diet → H1 → H2 → mast-cell stabilisers → LDN → montelukast → diazepam (interesting: no addiction in MCAS because diazepam binds mast cells, not brain). Background co-morbidities critical (mold, EBV, Lyme, UTIs). New angle: gut SARS-CoV-2 persistence (added to [[viral-persistence]] theme). 17.5% MCAS population estimate; ~98% of LC patients have prior MCAS pattern in her clinic.

## [2026-05-04] ingest | #039 — Lynn Laidlaw & Tracy Ibbotson — PPI

The PPI / co-production anchor episode. Created [[lynn-laidlaw]] (4-year diagnostic odyssey patient-researcher; visiting fellow Bournemouth), [[tracy-ibbotson]] (PPI Lead Glasgow Medical School), [[patient-and-public-involvement]] theme. Power-and-tokenism critique — "the only power I have is the power to walk away." Goldilocks problem: experienced patient contributors get rejected as "too research-literate"; inexperienced ones as "not knowing enough." Pair with Faghy #36 for the practical-application companion. No interventions/outcomes; purely research-infrastructure.

## [2026-05-04] ingest | #040 — Dr Boon Lim — Autonomic Dysfunction

The wiki's **anchor autonomic-dysfunction episode**, replacing the previous patchwork. Created [[boon-lim]], [[autonomic-dysfunction]] theme (now centralised), [[diaphragmatic-breathing]], [[salt-loading]], [[compression-stockings]], [[head-of-bed-elevation]], [[gratitude-and-forgiveness]] theme, [[eno-breathe]] program. Updated [[pots]] (now 5 mentions). Tilt-cohort numbers (60-80 LC patients): ~25% full POTS, ~25% sub-threshold, most-of-rest oscillatory adrenergic — net 60-70% autonomic dysfunction. Mechanism walkthrough (baroreflex). Bottom-up toolkit + top-down (forgiveness > gratitude > compassion as autonomic-regulation hierarchy — unusually direct from a cardiologist). Endorses Suzy Bolt + ENO Breathe explicitly as community programs that converge on autonomic regulation in different vocabulary.

## [2026-05-04] checkpoint | episodes 32-40 ingested (39 of 211)

- **39 of 211 episodes done.** index.md and log.md updated.
- **Counts now**: 39 episode pages · 44 people pages (added 13 new) · 32 intervention pages (added 14 new) · 12 program pages (added 4 new) · 6 symptom pages (no new files; mcas updated) · 19 theme pages (added 9 new) · 10 trial pages (added 4 new) · 4 recovery-story pages (added 2 new).
- **Recovery stories logged: 5** (Whitfield #8 — Lightning Process; Anker #20 — neuroplasticity; Riggs #23 — multi-component pharma + diet + SSP; **Esther #32 — TMS / Mind-Body Syndrome**; **Munslow #34 — coaching / mental-skill rebuild**). Five different routes; convergent on NS-regulation as the substrate.
- **key_to_recovery entries added: 1** (TMS, Esther #32). Total now 5: beta-blockers (Amy Small POTS), walking (Whitfield), Lightning Process (Whitfield), Positively Covid (Anker — founder caveat), TMS (Esther). No `key_to_recovery` row from Munslow — recovery framed as gradual mental-skill rebuild, no specific intervention to credit.
- **helped_partial entries added: 6** (apheresis Khan #37; triple therapy Khan #37; omalizumab Khan #37; midodrine Khan #37; mestinon Khan #37; vagus-nerve TENS Khan #37). All from one patient — caveat as bias toward the stack he found.
- **no_effect entries added: 1** (Paxlovid Khan #37 third infection — n=1).
- **harmed entries added: 1** (vaccine-while-still-in-LC Khan #37 — careful framing: pro-vaccination, but acknowledging reactions).
- **recommended entries added: many** across antihistamines, low-histamine diet, sodium cromoglicate, ketotifen, montelukast, LDN (Peers), helapheresis (Pretorius/Kell), triple therapy (Pretorius/Kell), midodrine (Lim), fludrocortisone (Lim), ivabradine (Lim), salt-loading (Lim), compression (Lim), diaphragmatic breathing (Lim), head-of-bed elevation (Lim), AXA1125 (Axcella), arc-microtech device (Peers), Gupta program (Peers), ENO Breathe (Lim).
- **Anchor episodes laid down**: This batch deposits **four anchor episodes** that subsequent ingests will frequently reference back to — #033 (microclots mechanism), #037 (apheresis/triple-therapy clinical), #038 (MCAS protocol), #040 (autonomic dysfunction). Plus #032 (TMS recovery route) as a fifth recovery-route anchor.
- **Mechanism convergence**: The microclots theme (#033) and the autonomic-dysfunction theme (#040) and the MCAS theme (#038) are now linked as three distinct mechanism families that **co-occur in many patients** rather than competing. Khan #037 explicitly stacks all three (apheresis + MCAS drugs + POTS drugs).
- **PPI / research-infrastructure thread**: Faghy #036 + Laidlaw/Ibbotson #039 anchor the patient-led-research story, with the broader implication that LC is the field where this is being tested most aggressively.
- **Gaps deliberately left as placeholders**: chronic-urticaria, angioedema, propranolol, famotidine, plasmapheresis, BC007, immunoadsorption, nattokinase / lumbrokinase / serrapeptase, paxlovid, ozone, HBOT (will land properly when patient-outcome rows arrive in later episodes). Eric stack drugs (ivabradine, mestinon, fludrocortisone) now have real wiki pages.

## [2026-05-04] ingest | #041 — Joachim Gerlach — Vedicinals-9

Industry-founder episode. Created [[joachim-gerlach]], [[vedicinals-9]], [[nutraceuticals]] theme, [[polypharmacy-warning]] theme, [[bruce-patterson]] (placeholder). Vedicinals-9 is a 9-molecule plant nutraceutical formulation; phase-2 acute-COVID RCT in India (n=124, faster viral clearance, IL-6/TNF reduction, lung-x-ray improvement at day 12). No Long-Covid RCT yet. One `recommended` row (Gerlach as founder — bias caveat). Most useful take: targeted-not-stacked supplement framing; "natural ≠ safe" emphasis; categorical-rather-than-redundant heuristic.

## [2026-05-04] ingest | #042 — Dr Alison Twycross — LCNMUK

Advocacy + employment-rights episode. Created [[alison-twycross]], [[long-covid-nurses-and-midwives-uk]] (program), [[antidepressants]] (real page replacing placeholder). Updated [[employment]] theme with NHS-staff section + ill-health-retirement misuse pattern + Welsh half-pay reprieve. New `helped_partial` row on antidepressants for affect/sleep at 16-month mark. LCNMUK first-3-months wins: NHS England dismissal-clause removed; Welsh half-pay reprieve; RCN web hub; Parliament debate briefing; survey via *Evidence-Based Nursing*; CNO meetings. Ill-health-retirement now their next campaign focus.

## [2026-05-04] ingest | #043 — Dr Mohammad Bashashati — GI issues

The wiki's **anchor GI / DGBI episode**. Created [[mohammad-bashashati]], [[gi-dysfunction]] symptom (new symptom-cluster), [[post-infectious-ibs]] theme, [[low-fodmap-diet]] (real page). Updated [[gut-health]] with the DGBI clinical layer. Acute COVID GI prevalence (45% diarrhea / 35% nausea / 30% abd pain in his cohort); 9% develop persistent DGBI at 6 months in mixed populations; 40% of post-COVID DGBI patients had no acute-phase GI symptoms. Walkerton 2000 (E. coli + Campylobacter, 36% post-infectious IBS at 2 years) is the prognostic precedent — eventual favourable spontaneous remission.

## [2026-05-04] ingest | #044 — Moira Newiss (return) — How do we make our energy?

Newiss's second appearance. Created [[forest-bathing]], [[robert-naviaux]] (placeholder). Updated [[moira-newiss]], [[mitochondrial-dysfunction]] theme with explicit Powerhouse-vs-Battleship + iceberg + mitochondria-as-endocrine framing. Added `recommended` row to [[keto-diet]] (now 4 mentions). Episode is the deeper-dive companion to #21. ATP biochemistry walkthrough; CDR mechanism; toolkit (real food, easy meal-plan download, keto rationale, toxin reduction, gentle movement, forest bathing). Ancestral-metabolic framing + endurance-athlete fasted-keto evidence cited.

## [2026-05-04] ingest | #045 — Keith Littlewood — Hormones, the thyroid & more

**Heterodox bioenergetic episode** — flagged carefully. Created [[keith-littlewood]], [[hormonal-dysfunction]] theme, [[bioenergetic-framework]] theme (with explicit tension-against-keto framing), [[methylene-blue]], [[progesterone]], [[bag-breathing]]. Littlewood is a UK PhD candidate at Reading on pollutants + thyroid physiology with a Ray-Peat-adjacent stance: pro-saturated-fat, pro-glucose, anti-PUFA, pro-progesterone, pro-thyroid-via-fuller-panel. Body temperature + pulse on waking as a free clinical lever. Methylene blue with serious SSRI/MAOI interaction caveats.

## [2026-05-04] ingest | #046 — Gez Medinger — Patient Advocate, Researcher & Author

Created [[gez-medinger]], [[danny-altmann]] (placeholder), [[bindi-venel]] (placeholder), [[nad-niacin]], [[probiotics]]. Added `helped_partial` rows to [[antihistamines]] and [[low-histamine-diet]] (Medinger via Tina Peers #38). Anchor advocacy episode for the LC YouTube + Long Covid Handbook (Penguin, w/ Altmann) project. 4-category framework (metabolic / mast cell / dysautonomic / vascular). The 50% rule. NAD/niacin via Bindi Venel for ~20% energy envelope. Tilt-test as `harmed` (6-week crash from a diagnostic procedure). "If you've been ill 2+ years and don't change anything, expecting random improvement is unlikely."

## [2026-05-04] ingest | #047 — Darren Brown — Long Covid Physio

Created [[darren-brown]], [[long-covid-physio]] (program). Founding chair episode for the international physio-with-LC association. The **World Physiotherapy Briefing Paper** "Safe Rehabilitation Approaches for People Living with Long Covid" (June 2021, translated 11 languages) is the institutional bedrock for stability-not-progression rehab framing. Sept 2022 Long Covid Physio International Forum: 80 speakers, 17 countries, scholarship-funded for PWLC, sponsors (Kaiser Permanente, Visible, Toronto Temerty, Realize). "Just because you can doesn't mean you should."

## [2026-05-04] ingest | #048 — Saskia Mulder — Long Covid & a visit to South Africa

The wiki's **anchor Stellenbosch / SA triple-therapy patient case** + the most consequential mental-health episode. Created [[saskia-mulder]], [[jaco-laubscher]] (placeholder), [[mental-health-and-suicidality]] theme, [[hbot]], [[cranial-sacral-therapy]], [[serrapeptase-lumbrokinase]], [[fola-oyinlade]] (placeholder). Added `helped_partial` row to [[triple-therapy-anticoagulation]] (now 3 mentions, 2 helped_partial) + [[antidepressants]] (now 2 mentions). 27-month patient story: walking + cold-forest both `harmed`; SSRI started at 16-17mo stopped active suicidal ideation in days ("the best decision I made"); Stellenbosch route via Pretorius's lab in 3 weeks vs Mülheim 6+ months; triple therapy improvements (sleep, circulation, sensory, food intolerance, limb pain) but anaemia from heavy bleeding cut treatment short at 9 weeks. "Massive part of the puzzle, not the magic cure."

## [2026-05-04] ingest | #049 — Wild Swimming with Dr Adrian Baker & Leanne

Created [[adrian-baker]] (recovered-LC GP, North Scotland, lifelong cold-water swimmer). Updated [[wild-swimming]] significantly: now 3 mentions with mechanisms (endorphins, diving reflex, microcirculation, anti-inflammatory, cold-shock-adaptation 5-7 sessions, mental-health/social) and practical heuristics (1 min per °C; slow exhale breath training; **never hot shower afterwards**; slow rewarming; tow floats; read the water). Added `recommended` row (Baker) and `key_to_recovery` row (Leanne, for fibromyalgia/RA — note cross-condition framing). Costochondritis as the last-to-clear LC symptom (~18 months for Baker).

## [2026-05-04] ingest | #050 — Chrissi Kelly — AbScent & Parosmia

The wiki's **anchor olfactory-dysfunction episode**. Created [[chrissi-kelly]], [[simon-gane]] (placeholder, AbScent trustee + namer of olfactory perseveration), [[smell-loss-parosmia]] symptom (new smell-taste cluster), [[smell-training]], [[abscent]] (program). Taxonomy: anosmia / hyposmia / parosmia / phantosmia / **olfactory perseveration** (Gane). Three nerves: olfactory + gustatory + trigeminal; "flavour" is brain integration. Acute COVID early variants impaired all three; later variants spare gustation+trigeminal more. Parosmia = aberrant nerve regeneration; statistically *better* long-term outcome than pure hyposmia. Smell training as evidence-based recovery accelerant (compliance the main failure mode). **Critical food red flag**: parosmia patients drop high-protein foods → malnutrition risk → pharmacy-grade meal replacement (Huel + cinnamon + oat milk).

## [2026-05-04] checkpoint | episodes 41-50 ingested (49 of 211)

- **49 of 211 episodes done.** index.md and log.md updated.
- **New people pages**: 13 (Gerlach, Twycross, Bashashati, Littlewood, Medinger, Brown, Mulder, Adrian Baker, Chrissi Kelly + placeholders Bruce Patterson, Robert Naviaux, Danny Altmann, Bindi Venel, Jaco Laubscher, Simon Gane, Fola Oyinlade).
- **New intervention pages**: 11 (vedicinals-9, antidepressants, low-fodmap-diet, forest-bathing, methylene-blue, progesterone, bag-breathing, nad-niacin, probiotics, hbot, cranial-sacral-therapy, serrapeptase-lumbrokinase, smell-training).
- **New program/org pages**: 3 (LCNMUK, Long Covid Physio, AbScent).
- **New symptom pages**: 2 (gi-dysfunction, smell-loss-parosmia) — both new symptom clusters (gi, smell-taste).
- **New theme pages**: 6 (nutraceuticals, polypharmacy-warning, post-infectious-ibs, hormonal-dysfunction, bioenergetic-framework, mental-health-and-suicidality).
- **New evidence-log rows**:
  - `key_to_recovery: 1` — Leanne, wild swimming for fibro/RA (cross-condition).
  - `helped_partial: 12` — Medinger antihistamines + low-histamine-diet + NAD/niacin + probiotics; Mulder triple-therapy + SSRI + HBOT + cranial-sacral + serrapeptase-lumbrokinase; Twycross antidepressants; Adrian Baker (cold water — recommended; recorded under recommended technically).
  - `recommended: 13` (Gerlach Vedicinals; Twycross LCNMUK; Bashashati low-FODMAP; Newiss keto + forest bathing; Littlewood methylene blue + progesterone + bag breathing; Brown LC Physio; Baker wild swimming; Kelly smell training + AbScent).
  - `harmed: 2` — Medinger tilt test (6-week crash); Mulder walking + cold-forest-walk (multiple relapses).
- **No `key_to_recovery` for LC** in this batch — important. Total LC `key_to_recovery` count remains at 5 (beta-blockers Amy Small POTS, walking + Lightning Process Whitfield, Positively Covid Anker — founder caveat, TMS Esther). Leanne's wild-swimming key_to_recovery is for fibromyalgia/RA, not LC.
- **Anchor episodes laid down in this batch**:
  - **#43 — anchor GI / DGBI** episode (gut symptoms, post-COVID DGBI taxonomy)
  - **#44 — anchor mitochondrial / Naviaux CDR** deeper-dive episode
  - **#45 — anchor bioenergetic / Ray-Peat-adjacent** heterodox episode (held as live hypothesis, not endorsed)
  - **#48 — anchor Stellenbosch / SA triple-therapy** patient case + LC mental-health crisis episode
  - **#49 — anchor cold-water-exposure mechanism + practical** episode
  - **#50 — anchor olfactory-dysfunction / smell-loss / parosmia** episode
- **Mental health surfaced as a load-bearing wiki theme** — Mulder #48's suicidality story is the most clinically consequential single data point so far. Twycross #42 antidepressants for sleep/affect adds the second case. The wiki will now flag mental-health-and-suicidality wherever a patient describes prolonged unresolved illness.
- **Triple therapy now 2 patient cases (Khan #37 + Mulder #48), both `helped_partial`**. Convergent improvements pattern: sleep, circulation, sensory, anti-allergic, limb pain. Neither was `key_to_recovery`. Both started late (~14-24 months) — both indicate recovery ceiling is lower than for ≤6mo starters.
- **Bioenergetic frame (Littlewood #45) is in explicit tension with keto frame (Newiss #21+#44)** — the wiki now carries both, neither is endorsed. Eric should not adopt either as dogma.
- **Polypharmacy critique unified across Gerlach #41 + Littlewood #45 + Medinger #46** — three independent clinicians warning against the 15-supplement-stack pattern.
- **Long Covid Coalition (Gerlach), LCNMUK (Twycross), Long Covid Physio (Brown), AbScent (Kelly)** — 4 new advocacy/professional/peer-support orgs added to the org map. Plus Long Covid Handbook (Penguin, late 2022, Medinger + Altmann) as a forthcoming publishing event.
- **Eric-relevant signals worth re-reading**: #43 DGBI taxonomy (if Eric ever has GI flares); #45 thyroid-panel-not-just-TSH + body-temp-and-pulse self-test; #46 NAD/niacin and 50% rule; #48 mental-health-and-suicidality red flags + Stellenbosch alternative; #49 cold-water exposure as a free low-friction lever (with hot-shower-afterwards warning); #50 smell-training + nutrition red flag.

## [2026-05-04] ingest | #051 — Darren Brown discusses Disability

15-min follow-up to #47. Anchor episodic-disability framework episode. Disability-model arc: biomedical → social → WHO ICF → **Episodic Disability Framework** (Kelly O'Brien, U Toronto, originating in HIV). LC fluctuates → static benefits-assessment fails. **Episodic Disability Questionnaire** is the practical lever for benefits-assessment letters. Rehab redefined: education / equipment / pacing / monitoring; **explicitly NOT exercise alone**. Created [[episodic-disability]] theme, [[kelly-o-brien]] placeholder.

## [2026-05-04] ingest | #052 — Margaret Koziel — AXA1125 Phase 2a results

Follow-up to #35. **Major positive Phase 2a readout**: ~70% of AXA1125 arm had clinically significant improvement in physical fatigue vs basically zero placebo; 3/21 back to pre-COVID baseline; both physical+mental fatigue improved; six-minute walk distance moved with fatigue; baseline mitochondrial function was abnormal. **First placebo-controlled positive readout for a fatigue-targeted LC therapy** in this wiki. AXA1125 mention_count → 2; trial status → completed-positive.

## [2026-05-04] ingest | #053 — Dr Deepak Ravindran — LC & Pain

Berkshire LC service lead, 1800+ LC patients, pain specialist. **Anchor pain episode + anchor [[nociplastic-pain]] / central-sensitization theme.** Three-pain framework: nociceptive (drugs work) / neuropathic (gabapentin et al.) / **nociplastic** (drugs and injections rarely work; calm immune+nervous system instead). LC pain is dominantly nociplastic. >70% of his LC patients score ≥6/10 on Yorkshire Rehab Screen. >90% have clean MRI → reversible NS hypersensitivity. New pages: [[pain]] symptom, [[deepak-ravindran]], [[nociplastic-pain]] theme, [[tens]], [[cbd-cannabis]]. Existing pages updated with `recommended` rows: yoga-nidra, yoga, pilates, meditation, cold-water-exposure, anti-inflammatory-diet.

## [2026-05-04] ingest | #054 — Elizabeth Dreicer — Consuli & LC research

CEO of Consuli (US public-benefit research-recruitment platform). Meta episode about research equity. **1-4% of people ever participate in trials despite 83-84% willing.** La Jolla Institute LC neuro study recruiting (positive test required, San Diego in-person). New pages: [[elizabeth-dreicer]], [[consuli]] program, [[la-jolla-immunology-lc-neuro]] trial.

## [2026-05-04] ingest | #055 — Jacob Teitelbaum — SHINE Protocol

US recovered-CFS clinician; author *From Fatigued to Fantastic*. **Anchor SHINE protocol episode**: Sleep / Hormones+Hypotension / Infections / Nutrition / Exercise. Frames LC as post-viral CFS (cites Fauci). Hypothalamic-dysfunction circuit-breaker model. Strong LDN advocate. Low-dose Abilify 0.25mg (Stanford) for severe CFS. Famciclovir+Celebrex 6mo for EBV. Avoid PPIs; use Pepcid/cimetidine. **Embodies "treat everything at once" — opposite pole to [[polypharmacy-warning]] critiques in #41/#45/#46.** Caveat: commercial relationships with named supplements (Recovery Factors, HRG80, Smart Energy System). New pages: [[jacob-teitelbaum]], [[shine-protocol]] program, [[hypothalamic-dysfunction]] theme, [[ribose]], [[hrg80-red-ginseng]], [[abilify-low-dose]], [[famotidine-pepcid]] (Eric is on this), [[famciclovir-celebrex]], [[fluconazole]], [[ans-rewire]] program (formerly placeholder), [[dynamic-neural-retraining-system]] program, [[dan-neuffer]] person. Updated low-dose-naltrexone, walking, beta-blockers (with cautious-split note).

## [2026-05-04] ingest | #056 — Johanna Rayl — Recovery Story

US economics PhD student, 2.5-year LC, recovered. **5th full recovery story in the wiki** (after Whitfield #8, Anker #20, Esther #32, Munslow #34). Path: ANS Rewire (Dan Neuffer) + Curable app + paid medical leave + radical rest + "movement, not exercise." **First `key_to_recovery` for [[ans-rewire]]** on this podcast (now mention_count 3 with 1 KTR). New pages: [[johanna-rayl]], [[johanna-rayl-recovery]] story, [[curable-app]] intervention.

## [2026-05-04] ingest | #057 — Dr Sanjay Gupta — the POTS Specialist

UK York cardiologist, >1000 POTS patients. **Anchor Eric-relevant POTS episode.** POTS = wrong name; reframe as dysautonomia. Same litter as CFS / fibromyalgia / LC / FND / IBS. 30bpm criterion is man-made. Four-pillar treatment (lifestyle / physio / meds / advocacy), all simultaneously. **Ivabradine preferred over beta-blockers**; midodrine pairs with fludrocortisone; mestinon as "rest-and-digest enhancer"; LDN + DDAVP + clonidine + antihistamines. **IV saline transformative** ("wheelchair in, walks out"; 24-36hr) but not NHS-available. POTS is debilitating but not life-threatening — long-term cardiac safety reassurance. **Eric's existing stack overlaps almost completely with Gupta's preferred stack — independent corroboration.** Missing from Eric's stack: midodrine. New pages: [[sanjay-gupta-cardiologist]], [[iv-saline]], [[desmopressin-ddavp]], [[clonidine]]. Updated: ivabradine, mestinon, fludrocortisone, midodrine, pots symptom page.

## [2026-05-04] ingest | #058 — Fiona Jones — the LISTEN Trial

Co-PI (with Monica Busse, Cardiff) of NIHR-funded **LISTEN trial** — codesigned 1:1 self-management support for LC. n=550 RCT vs usual care. 6 remote sessions + co-designed book + 8-hour practitioner training. **No positive COVID test required** (open to early-2020 cohort). Anchor codesign / self-management episode. Sites: all Wales + parts of England. Results expected Autumn 2023. New pages: [[fiona-jones]], [[listen-trial]], [[bridges-self-management]] program.

## [2026-05-04] ingest | #059 — Vikki Jones — Trauma & Breathing

Co-founder of [[long-covid-breathing]] (with Jackie Baxter). Oxygen Advantage / Buteyko-trained under Patrick McKeown. **Anchor practical-breathwork-protocol episode.** Specific exercises (Control Pause test; Many Small Breath Holds; Cadence Breath; diaphragmatic breathing; modified box breathing; mouth-taping for sleep). Trauma-frame for LC: "the quickest way to change your biochemistry is to change your breath." Standard breathwork can WORSEN LC patients with low CP — adapted protocols essential. New pages: [[vikki-jones]], [[patrick-mckeown]] placeholder. Updated long-covid-breathing program.

## [2026-05-04] ingest | #060 — Reema Ahmad — Diagnosis, Gaslighting & Life with LC

Indian (Delhi) NLP coach, trauma counsellor, author. Three COVID infections + spinal surgery; ~2-year delayed diagnosis. **First non-Anglosphere LC patient voice in the corpus.** Practical adjuncts: bat-cave sensory withdrawal during flares, ice packs on neck/face for thermal-dysregulation episodes, breath work, weekly pacing. Articulated **comparison guilt** as a self-gaslighting pattern. Cross-cultural framing: "don't make a fuss" + women-coded "get on with it" delays diagnosis. Full LC family pattern (brother, father, multiple friends). New pages: [[reema-ahmad]], [[ice-packs-temperature]] intervention.

## [2026-05-04] checkpoint | episodes 51-60 ingested (59 of 211)

- **59 of 211 episodes done.** index.md and log.md updated.
- **New people pages**: 14 (Brown #51 was return; Koziel #52 return; Ravindran, Dreicer, Teitelbaum, Rayl, Gupta-cardiologist, Fiona Jones, Vikki Jones, Reema Ahmad + placeholders Kelly O'Brien, Dan Neuffer, Patrick McKeown).
- **New intervention pages**: 14 (tens, cbd-cannabis, ribose, hrg80-red-ginseng, abilify-low-dose, famotidine-pepcid, famciclovir-celebrex, fluconazole, iv-saline, desmopressin-ddavp, clonidine, ice-packs-temperature, curable-app — and existing AXA1125 / pain symptom heavily updated).
- **New program/org pages**: 5 (consuli, shine-protocol, ans-rewire, dynamic-neural-retraining-system, bridges-self-management).
- **New trial pages**: 2 (la-jolla-immunology-lc-neuro, listen-trial). AXA1125-Oxford trial status flipped to **completed (positive readout)**.
- **New symptom pages**: 1 ([[pain]] — anchor pain page with three-category framework).
- **New theme pages**: 4 (episodic-disability, nociplastic-pain, hypothalamic-dysfunction, central-sensitization aliased).
- **New recovery story**: 1 (johanna-rayl-recovery — 5th full recovery story).
- **New evidence-log rows by outcome bucket**:
  - `key_to_recovery: 1` — Rayl crediting ANS Rewire as primary in her recovery (#56). **First key_to_recovery for any brain-retraining program in this wiki.**
  - `helped_partial: 3` — Rayl Curable app, Reema ice packs, Vikki Jones breathwork (in long-covid-breathing).
  - `recommended: ~30` — across many existing intervention pages (Ravindran #53, Teitelbaum #55, Gupta #57, Brown #51, Dreicer #54, Fiona Jones #58, Margaret Koziel #52).
- **AXA1125 Phase 2a positive readout (#52)** is the **strongest placebo-controlled efficacy signal** in the wiki to date for a fatigue-targeted LC therapy. ~70% with significant physical-fatigue improvement; 3/21 back to baseline; biological mechanism (mitochondrial) corroborated.
- **Anchor episodes laid down in this batch**:
  - **#51** — episodic-disability framework / rehab-not-exercise
  - **#52** — AXA1125 Phase 2a positive readout
  - **#53** — pain / nociplastic-pain
  - **#55** — SHINE protocol (Teitelbaum)
  - **#57** — Eric-relevant POTS treatment (Gupta) — most directly Eric-relevant clinician episode so far
  - **#58** — codesigned self-management trial (LISTEN)
  - **#59** — practical breathwork protocol (Vikki Jones / Oxygen Advantage)
- **Eric-stack independent corroboration (#57)**: Gupta's preferred POTS medication stack (ivabradine + mestinon + fludrocortisone + antihistamines + midodrine) overlaps with Eric's current stack on 4/5. **Missing: midodrine.** Worth raising with Eric's clinician. **IV saline** is novel; private only; not on Eric's radar yet.
- **Brain-retraining family converging as a recovery vector**: ANS Rewire / DNRS / Gupta program / TMS / Lightning Process / Positively Covid all share neuroplasticity substrate. Now 4 of 5 full recovery stories in this wiki use a brain-retraining or NS-regulation program as a primary lever. Cluster signal: brain-retraining + structured-leave-from-work + radical-rest + mind-body-reframe.
- **Polypharmacy debate now has explicit poles**: Teitelbaum #55 (treat everything at once, SHINE) vs. Gerlach #41 / Littlewood #45 / Medinger #46 (don't stack 15 supplements). Both positions logged neutrally; neither endorsed.
- **Trauma-framing of LC** consolidated as a wiki position: Vikki Jones #59, Reema Ahmad #60, plus prior Riggs #23 / Nicholson #29 / Munslow #34 — all converge on trauma + nervous-system regulation as the lens.
- **Pain emerges as a wiki-load-bearing symptom (#53)** — was under-counted because not all clinics use pain-specific questionnaires. Three-pain framework (nociceptive / neuropathic / nociplastic) imported as a permanent lens.
- **Eric-relevant signals worth re-reading**:
  - #51 Episodic Disability Questionnaire as a benefits-letter lever
  - #53 Three-pain framework (nociplastic) — keep on file in case pain emerges
  - **#55 LDN strong recommendation** — re-evaluate for Eric (he's not on it)
  - **#57 Gupta POTS stack** — Eric's stack confirmed; midodrine to consider; IV saline novel
  - #59 Control Pause test as a 2-minute self-assessment Eric can repeat
  - #60 ice packs on neck for thermal-dysregulation episodes

## [2026-05-04] ingest | #061 — Rosie & Colin Pidgeon — paediatric LC

First paediatric-LC episode in the wiki. Rosie (17) bundled improvement: LDN + acupuncture + pacing started April 2022. Created [[rosie-pidgeon]] and [[colin-pidgeon]] people pages, [[acupuncture]] intervention page (helped_partial, attribution-bundled). Added [[long-covid-kids]] program page. LDN page gains first paediatric row.

## [2026-05-04] ingest | #062 — Prof Nisreen Alwan — public health + long-hauler

Strongest population-level signal in the wiki for **early rest** as a protective factor (n=2500+ survey). Created [[nisreen-alwan]] people page. Updated [[radical-rest]] intervention with second row (recommended) and the strong observational note. Added stigma-scale framing to [[healthcare-gaslighting]]. Cross-reference to [[stimulate-icp]] (inequalities arm).

## [2026-05-04] ingest | #063 — Dr Michael Bagnell — brain stem & long Covid

**New theme: [[brain-stem-dysfunction]]** — wiki anchor for the Avindra-Nath-aligned brain-stem-as-upstream-substrate hypothesis. Bagnell's vagal-rehab toolkit: gargling, singing, eye movements, cross-crawl, cold-water facial immersion, primitive-reflex check (Moro), gammaCore + clip-on aural devices. Created [[michael-bagnell]] people page. Updated [[vagus-nerve-tens]] (gammaCore + aural recommendation), [[cold-water-exposure]] (facial-immersion entry-point).

## [2026-05-04] ingest | #064 — 2022 Reflections (Jackie host-solo)

Jackie's **self-declared top-3** logged as `key_to_recovery` rows on three intervention pages: [[breathwork]] (#1 — fixing breathing pattern), [[yoga-nidra]] (#2 — deep rest), [[cold-water-exposure]] (#3). Updated [[counselling]] (12-month weekly counselling, helped_partial), [[safe-and-sound-protocol]] (still working through it). Logged food-intolerance test as cautionary — milk reintroduction caused acute Carnage worse than baseline.

## [2026-05-04] ingest | #065 — Long Covid Creativity 2022 compilation

Multi-contributor creativity episode. Created [[long-covid-choir]] (Zoe Chaler / Claire Hastie / Merrill Vaughan, online weekly choir) and [[long-covid-kids-choir]] (Nov 2022 collaboration with LC Kids charity). Cross-link with [[063-michael-bagnell|Bagnell #63]]'s singing-as-vagal-stim. Colin Pidgeon's poem *Stormy* logged as carer-perspective verbatim of paediatric gaslighting.

## [2026-05-04] ingest | #066 — Lauren Stiles — Dysautonomia International

**Most comprehensive single-source autonomic-treatment toolkit in the wiki.** Created [[lauren-stiles]] people page and [[dysautonomia-international]] org page. **Second authoritative POTS-stack episode aligning with Eric's prescription** (after [[057-sanjay-gupta-pots-specialist|Gupta #57]]). Stiles announces a forthcoming **long-Covid-POTS IVIG immunotherapy trial** funded by DI. Updated rows on [[ivabradine]] (recommended), [[mestinon]] (recommended, anti-inflammatory framing), [[midodrine]] (recommended — second authority), [[salt-loading]] (specific 8-10g + 3L target), [[compression-stockings]] (abdominal placement primary), [[antihistamines]] (recommended), [[famotidine-pepcid]] (recommended), [[beta-blockers]] (recommended), [[anti-inflammatory-diet]] (recommended with smaller-meals/grazing schedule).

## [2026-05-04] ingest | #067 — DecodeME (Chris Ponting + Andy Devereux-Cooke)

**New trial page**: [[decodeme]] — world's largest GWAS of ME/CFS, 25,000-person UK study with a deliberate **5,000-person post-COVID-ME/CFS arm**. Created [[chris-ponting]] and [[andy-devereux-cooke]] people pages. [[graded-exercise]] gains a second `harmed` row from the community-position context (NICE 2021 withdrew GET). [[me-cfs-parallels]] theme strengthened.

## [2026-05-04] ingest | #068 — Dr David Saperstein — MCAS / dysautonomia / EDS overlap

**Anchor "trifecta / pentad / septad" episode**. Created [[david-saperstein]] people page and [[quercetin]] intervention page (250-500mg+, thyroid-med caveat). Updated [[antihistamines]] (Saperstein recommends **higher-than-OTC dose, twice daily**), [[famotidine-pepcid]] (brain H2 receptors; cytokine role), [[sodium-cromoglicate]], [[ketotifen]], [[beta-blockers]], [[dynamic-neural-retraining-system]] (broken-alarm framing). Distinct claim: **post-COVID POTS may present differently** from classic POTS — racing-HR more dominant. **Mast-cell ↔ sympathetic feedback loop** as a treatment principle.

## [2026-05-04] ingest | #069 — Fiona Lowenstein — Body Politic founder

**Architectural-history of the LC patient movement.** Created [[fiona-lowenstein]] people page, [[body-politic]] program page, [[patient-led-research-collaborative]] (PLRC) program page, [[long-covid-sos-uk]] program page. The **Long Covid Survival Guide** (book) logged as a non-prescriptive patient-authored reference. **Racial gaslighting at the acute-care entry point** added to [[healthcare-gaslighting]]. Major contribution to [[advocacy]] and [[patient-and-public-involvement]] themes.

## [2026-05-04] ingest | #070 — Lorrie Rivers — Reclaiming life from chronic illness

**Strong-claim minority-position episode**. Lorrie's hidden-parasite/dysbiosis root-cause theory of all chronic illness. Created [[lorrie-rivers]] people page, [[lorrie-rivers-relief-and-transformation]] program page (with explicit cautions), [[recovery-stories/lorrie-rivers-recovery|Lorrie's recovery story]] (with explicit cautions). Updated [[keto-diet]] with `key_to_recovery` row (Lorrie's strict-low-carb-as-foundation framing) — the controversial part of her protocol logged neutrally with caveats. Updated [[gut-health]] and [[me-cfs-parallels]] themes.

## [2026-05-04] checkpoint | episodes 61-70 ingested (69 of 211; #31 missing transcript)

- **New people pages**: 11 (rosie-pidgeon, colin-pidgeon, nisreen-alwan, michael-bagnell, lauren-stiles, chris-ponting, andy-devereux-cooke, david-saperstein, fiona-lowenstein, lorrie-rivers).
- **New program/org pages**: 7 (long-covid-kids, long-covid-choir, long-covid-kids-choir, dysautonomia-international, body-politic, patient-led-research-collaborative, long-covid-sos-uk, lorrie-rivers-relief-and-transformation).
- **New trial page**: 1 (decodeme).
- **New theme page**: 1 ([[brain-stem-dysfunction]]).
- **New intervention pages**: 2 (acupuncture, quercetin).
- **New recovery story**: 1 (lorrie-rivers-recovery).
- **New evidence-log rows by outcome bucket**:
  - `key_to_recovery: 4` — Jackie's self-declared top-3 ([[breathwork]], [[yoga-nidra]], [[cold-water-exposure]]) + Lorrie's keto/carnivore foundation framing on [[keto-diet]]. **First wiki entries for Jackie's own credits.**
  - `helped_partial: 5` — paediatric LDN + acupuncture (#61), counselling and SSP (#64), Lorrie's rebooted attempts.
  - `harmed: 1` — graded exercise (#67 community-position corroboration).
  - `recommended: ~25` — across [[midodrine]] / [[mestinon]] / [[ivabradine]] / [[salt-loading]] / [[compression-stockings]] / [[antihistamines]] / [[famotidine-pepcid]] / [[beta-blockers]] / [[sodium-cromoglicate]] / [[ketotifen]] / [[dnrs]] / [[anti-inflammatory-diet]] / [[radical-rest]] / [[vagus-nerve-tens]] / [[cold-water-exposure]] (Bagnell) (Stiles #66 + Saperstein #68 + Bagnell #63 the high-volume contributors).
- **Anchor episodes laid down in this batch**:
  - **#62** Alwan — strongest population-level signal for early-rest in the wiki (n=2500+)
  - **#63** Bagnell — anchor [[brain-stem-dysfunction]] theme
  - **#64** Jackie's reflections — wiki's clearest single statement of "what the host credits"
  - **#66** Stiles — most comprehensive autonomic-treatment toolkit; **second authoritative Eric-stack corroboration** (after #57)
  - **#67** DecodeME — the largest ME/CFS GWAS with a 5k post-COVID arm
  - **#68** Saperstein — anchor MCAS-trifecta clinical episode; H1+H2 cocktail at higher-than-OTC dose; mast-cell↔sympathetic feedback loop
  - **#69** Lowenstein — architectural picture of the LC patient movement
  - **#70** Lorrie Rivers — strong-claim minority position logged neutrally
- **Eric-stack second corroboration (#66 Stiles)**: **second independent recommendation of midodrine** (after Gupta #57) — now the most strongly-recommended Eric-not-yet-on-it drug in the wiki. Stiles also confirms ivabradine, mestinon, fludrocortisone, antihistamines, salt+fluids; specific dose target 8-10g salt + 3L fluids/day (must do both).
- **Dysautonomia umbrella formalised** (#66): "dysautonomia is not a diagnosis — ask which subtype." Subtypes: POTS, OI, OH, hyperhidrosis, GI dysmotility, dry-eyes/mouth (Sjögren's overlap).
- **Mast-cell ↔ sympathetic feedback loop** (#68 Saperstein) consolidated as a treatment principle. Must treat both layers.
- **MCAS H1+H2 dosing** (#68): higher than OTC labels, twice daily — explicit recommendation. Quercetin (250-500mg+) added as OTC mast-cell stabiliser.
- **Brain-stem hypothesis** (#63 Bagnell): wiki gains an upstream-substrate frame that subsumes microclots / mitochondrial / dysautonomia camps as plausibly downstream of brain-stem inflammation. Aligns with Avindra Nath at NIH.
- **Long Covid POTS may present differently from classic POTS** (#68 Saperstein): racing-HR-dominant rather than orthostatic-intolerance-dominant. Subtype hypothesis logged.
- **Patient-movement architecture mapped** (#69 Lowenstein): Body Politic → PLRC + LC SOS UK + Long Covid Survival Guide. Race/class gating of acute care explicitly logged on [[healthcare-gaslighting]].
- **First strong-claim minority position logged neutrally** (#70 Lorrie Rivers): hidden-parasite / dysbiosis root-cause theory. Recovery attribution logged because Lorrie is a recovered patient, but explicitly **not endorsed**; cross-check with ercipedia.
- **Eric-relevant signals worth re-reading**:
  - **#62 Alwan**: rest-in-first-2-weeks is the strongest single rest-evidence signal in the wiki (n=2500+).
  - **#63 Bagnell**: at-home Eric-applicable rehab (gargling, primitive-reflex check, cross-crawl, cold-shower-on-head, gammaCore rentable in US).
  - **#64 Jackie's top-3**: breathing + yoga nidra + cold water — wiki's clearest summary of what the host credits.
  - **#66 Stiles**: **midodrine corroboration** (second authority) for Eric's clinician conversation; salt 8-10g + 3L fluids dose target.
  - **#68 Saperstein**: H1+H2 cocktail at higher-than-OTC dose, twice daily; quercetin as OTC mast-cell stabiliser; long-COVID POTS may present differently.

## [2026-05-04] ingest | #71-#79 batch — tinnitus, STIMULATE-ICP, William Li, NIH RECOVER, Jackie 3y, SGB, reinfection-fear, Gahan, Towers

- **9 new episode pages**: 071-nic-wray-tinnitus, 072-banerjee-stimulate-icp, 073-william-li, 074-koroshetz-recover-nih, 075-jackie-3-year-reflections, 076-dr-robert-groysman-sgb, 077-suzy-bolt-reinfection, 078-lucy-gahan-psychology, 079-michael-towers-superhero.
- **8 new person pages**: nic-wray, amitava-banerjee, william-li, walter-koroshetz, robert-groysman, lucy-gahan, michael-towers (Suzy Bolt updated for #77 return).
- **8 new intervention pages**: stellate-ganglion-block, dietary-nitrates, sildenafil-viagra, metformin, baricitinib, colchicine, rivaroxaban (antihistamines updated for #72 trial endorsement).
- **2 new trial pages**: recover-trial (NIH), stimulate-icp (UCL).
- **1 new symptom page**: tinnitus (anchor).
- **Themes updated**: reinfection (Bolt's 5%-stretch + brain-immune-priming + Li metformin prevention), endothelial-dysfunction (Li's microvascular-loss extension distinguishing endothelitis vs structural loss vs flowing microclots), smell-loss-parosmia (SGB as second-line treatment).
- **New evidence-log rows by outcome bucket**:
  - `key_to_recovery: 0` — no new ones in this batch (all clinician/researcher episodes; Lucy Gahan and Michael Towers still recovering)
  - `helped_partial: 0` — none
  - `recommended: ~14` — across [[antihistamines]] (STIMULATE-ICP arm), [[colchicine]], [[rivaroxaban]] (STIMULATE-ICP arms), [[dietary-nitrates]], [[sildenafil-viagra]], [[metformin]], [[baricitinib]] (Li #73), [[stellate-ganglion-block]] (Groysman #76), CBT/sound-therapy/hearing-aids for tinnitus (Wray #71)
  - `harmed: 0` — none
- **Anchor episodes laid down in this batch**:
  - **#71** Wray — anchor for tinnitus as a symptom; ~38% LC tinnitus prevalence (Irish cohort)
  - **#72** Banerjee — anchor for STIMULATE-ICP; UK's largest LC platform trial; **third independent endorsement of H1+H2 antihistamines for LC**
  - **#73** William Li — anchor for the **three-legs-of-the-stool model** (microvascular + autoimmune + chronic inflammation); **strongest single hopeful synthesis in the wiki to date**
  - **#74** Koroshetz — anchor NIH RECOVER episode; 14k+ cohort; 4 mechanism hypotheses; master protocols
  - **#75** Jackie 3y — clearest single statement of the host's recovery arc; reaffirms breathwork + yoga nidra + cold water
  - **#76** Groysman — anchor SGB episode; ~1800 SGBs; modified C4+C6 protocol; Eric POTS-caution flag
  - **#77** Bolt return — anchor fear-of-reinfection episode; "5% stretch" + "immune system as superpower" mantra
  - **#78** Gahan — anchor LC-psychology vocabulary episode; Weingarten's witnessing/self-loss/chronic-sorrow framings
  - **#79** Towers — anchor severe-cohort representation; 5-minutes-at-a-time principle for energy-limited creative output
- **Eric-relevant signals worth re-reading**:
  - **#73 Li metformin → for any reinfection**: cheap, safe, ~30%+ LC-incidence reduction in Bramante RCT — clinician-conversation candidate
  - **#76 Groysman SGB**: smell + brain fog + autonomic — but POTS-caution applies to Eric; not "go book one"
  - **#72 STIMULATE-ICP**: H1+H2 antihistamine arm = 3rd independent endorsement (after Khan #37, Saperstein #68) — wiki's strongest convergent signal on this lever
  - **#74 Koroshetz**: 4 mechanism hypotheses are the wiki's most authoritative consolidation of "what we don't yet know" — useful frame against single-mechanism overfitting
  - **#77 Bolt reinfection**: directly addresses Eric's reinfection fear; combines with #73 metformin to reduce catastrophe-frame
  - **#78 Gahan**: provides vocabulary (witnessing, self-loss, chronic sorrow) for talking about LC with family/friends and clinicians
- **Microvascular framework consolidation (#73)**: Li's three-legs model now sits at the centre of the wiki's mechanism story:
  - **Leg 1**: microvascular damage — extends [[endothelial-dysfunction]] with structural loss (capillary disappearance, not just inflammation)
  - **Leg 2**: autoimmunity — incidence of post-covid type 1+2 diabetes, lupus-like symptoms, increased thyroiditis
  - **Leg 3**: chronic inflammation — 43% increased fatal heart attack rate <44 with covid (including Omicron)
- **First formally-trialled LC anticoagulant logged (#72)**: rivaroxaban via STIMULATE-ICP. Distinct from Khan's empirical triple therapy; Banerjee's case for sequential single-agent trials before combination is a useful counterweight to "why not just try everything" Twitter framing.
- **First formally-trialled metformin LC-prevention strategy logged (#73)**: Bramante RCT — most actionable single fact in the wiki for "what to do if reinfected."
- **First wiki-anchor SGB practitioner logged (#76)**: Groysman's modified C4+C6 protocol; ultrasound-guided; Horner's-syndrome confirmation; 1,800 cases. **POTS-caution explicit** — not endorsed for Eric without clinician weighing.
- **First severe-cohort representation in the wiki (#79)**: Towers's 1-year fully-bedridden phase (couldn't feed/walk/talk/sit up). The cohort that's invisible even to most LC patients now has a voice on the wiki.

## [2026-05-04] ingest | batch #80–#84

5-episode batch:
- **#80 Anjali Agarwal** — Hyderabad-based physio specialising in EDS/hypermobility, advocacy co-director Long Covid Physio. Third independent endorsement of EDS/POTS/MCAS trifecta. Adds a structural/connective-tissue mechanism for POTS (hypermobile vessels can't pump blood against gravity) on top of Lim's #40 baroreflex story. "Father of the problem is the mast cell." Circadian + 7pm digital-detox as concrete MCAS levers. Paediatric MCAS signal (12-14 yo). Updated [[mcas]], [[pots]], [[hormonal-dysfunction]], [[pacing]], [[long-covid-physio]], [[diaphragmatic-breathing]], [[autonomic-dysfunction]].
- **#81 Liza DiLeo Thomas** — US ED physician + Certified Patient Experience Professional + long-hauler. Anchor clinician-side communication episode. Empathy as measurable + teachable. The "must be / sounds like" technique. The "great news, everything's normal" antipattern as iatrogenic. Body Politic Slack as a structured signal source. Updated [[communication]], [[healthcare-gaslighting]], [[body-politic]].
- **#82 Jay Wiles** — clinical health psychologist; HRV biofeedback specialist; Hanu Health CSO. Anchor HRV episode. Created [[hrv-biofeedback]] intervention page. Key framing: HRV is **relative not normative** — only personal trends matter. Reports LC patients have 15-30min HRV recovery time after walks (vs 2-5min healthy) — concrete pacing signal. PMS/ovulation HRV-suppression physiology added to [[hormonal-dysfunction]]. The data motivates; the breathwork heals. Updated [[breathwork]], [[diaphragmatic-breathing]], [[autonomic-dysfunction]].
- **#83 Ryan Prior** — journalist/author/patient with ME/CFS for a decade-plus before LC. Author of *The Long Haul* (Hachette 2022) and director of *Forgotten Plague*. Anchor expert-patient episode. The wiki's "lived experience as practical wisdom" framing now has a strong articulation (Aristotle's phronesis). Drug-repurposing framing via Fajgenbaum / *Chasing My Cure*. Naming critique: "long covid" works because it doesn't bury the lede. Updated [[me-cfs-parallels]], [[patient-and-public-involvement]], [[patient-led-research-collaborative]].
- **#84 Caroline Pover** — UK author/entrepreneur, AstraZeneca-vaccine-injured, co-founder UK CV Family. **First dedicated vaccine-injury patient-experience episode** (after #37/#38 clinician-side). Anchors social ostracism layer that's distinct from regular LC. Created [[therapeutic-phlebotomy]], [[copper-supplementation]], [[uk-cv-family]]. Therapeutic phlebotomy logged as her n=1 key_to_recovery — controversial, mainstream pushback, but wiki policy is to log every key_to_recovery claim. Updated [[vaccine-injury]], [[acupuncture]] (added Chinese-bloodletting variant), [[healthcare-gaslighting]].

Batch-level signals:
- **EDS/POTS/MCAS trifecta is now the wiki's single most-converged clustering** — three independent voices (Peers #38, Saperstein #68, Agarwal #80) plus indirect support from Khan #37, Stiles #66. Eric should have hypermobility self-assessment in his clinical picture.
- **HRV as autonomic guide** is now well-anchored alongside [[diaphragmatic-breathing]] and [[breathwork]]. The **15-30min post-walk recovery threshold** is the most actionable single signal (#82) for pacing decisions.
- **The "expert patient" framing (#83)** legitimises the wiki itself as an artefact — patient + technologist extracting structure from unstructured testimony is exactly the pattern Prior describes.
- **First vaccine-injury patient-experience anchor (#84)** alongside the existing clinician-framed pages gives the wiki coverage on social-ostracism dimension that didn't surface in #37/#38.
- **Communication episodes (#81)** provide vocabulary for both directions of the clinician-patient axis. The "must be / sounds like" + "I don't know but I believe you" patterns are concrete enough to deploy.
- **Acceptance vs hope (#84)** is a counter-frame to the wiki's recovery-narrative bias. Most stored stories are recovery-trajectory; Pover articulates a coherent acceptance-without-recovery posture worth holding alongside.

## [2026-05-04] ingest | batch #85–#89

5-episode batch:
- **#85 Fiona Agombar** — UK yoga therapist (Viniyoga lineage), recovered from 15y of ME, "rest activist". Trauma-informed yoga therapy for LC. Two key wiki contributions: (1) the **safe-resource anchor** as a workaround when breath-focus itself triggers air-hunger / trauma response — a real reason to seek trauma-informed practitioners, not generic yoga. (2) **Buteyko-style breath-holds and control pauses excluded for LC patients** until near-recovery — first explicit caveat in the wiki on the breathwork family. Updated [[yoga]] (now 5 mentions) and added [[fiona-agombar]] people page.
- **#86 Harry Leeming** — UK ex-F1-engineer-turned-CEO of [[visible|Visible Health]]; LC since Sept 2020. Anchor wearable-app episode. Frames **"digital biomarkers"** as a strategic pattern: wearable patterns that exist in sick people but not in healthy people. Visible's deliberate **screenless wearable** is a notable design decision against hypervigilance — pairs with [[082-jay-wiles-hrv]]'s "data is motivation only" framing. First peer-reviewed-track menstrual-cycle ↔ symptoms study (Imperial / Mehta) in ethics review using Visible data. Created [[visible]] program page; created [[harry-leeming]] people page.
- **#87 Mark Harper** — UK/Norway anaesthetist + cold-water researcher; ChillUK clinical-trials lead. **Anchor cold-water mechanism episode** — three layers (face-diving-reflex parasympathetic / sympathetic-attenuation with repetition / anti-inflammatory) and an explicit minimum-effective-dose recipe (**~6 exposures, water <20°C, even cold showers count, 2-3 minutes is enough**). Six rules + minimise-discomfort-maximise-fun. Hypothesises **water-buoyancy-as-PEM-protection** which would explain why Eric's cold swimming has been notably PEM-safe. Updated [[cold-water-exposure]] (now 5 mentions); added [[mark-harper]] people page.
- **#88 Tania Dempsey** — US integrative + functional medicine physician; MCAS specialist (AIM Center for Personalized Medicine, NY). **Vulnerability + trigger** unifying model with the iceberg metaphor — explains the trifecta clustering the wiki has tracked across [[038-dr-tina-peers-mcas|Peers]], [[068-dr-david-saperstein|Saperstein]], [[080-anjali-agarwal-eds-physio|Agarwal]] in a way that makes the underlying physiology coherent. Comorbid clusters slide with infection at centre. Practical excipient-reactivity insight: swap formulations before abandoning a molecule. **Notable revision**: she's moving endocrine/metabolic dysfunction up her own list as the biggest root cause candidate — pairs with [[045-keith-littlewood-hormones-thyroid|Littlewood #45]]. Updated [[mcas]] (now 10 mentions); added [[tania-dempsey]] people page.
- **#89 Gina Short** — US recovery story (Washington State; July 2021 → Dec 2022 declaration). **6th full recovery on the wiki.** Three new contributions: (1) **Declaration as inflection point** — she wrote, signed, dated, told people; the act itself shifted her felt sense. First wiki articulation of this technique. (2) **Designated-witness sentence** — her 16yo son told to give a hug + say "Mom you're getting better" daily; eventually he believed it before she did. (3) **Pre-planning crashes** — noticing she was unconsciously rehearsing future-crashes was itself a route out of the cycle. Recovery stack: Suzy Bolt's free yoga + Fern programme + [[stasis-breathing]] + radical inputs-strip + joy + declaration. Created [[recovery-stories/gina-short-recovery]] and [[gina-short]] people page; updated [[suzy-bolt-recovery]] (first independent participant key_to_recovery), [[stasis-breathing]] (now 3 mentions), [[yoga]].

Batch-level signals:
- **First independent-participant key_to_recovery on [[suzy-bolt-recovery]]** (#89). The original founder-bias caveat is partly resolved.
- **Cold-water now has an anchor mechanism episode (#87)** alongside [[049-wild-swimming-adrian-baker-leanne]]'s practical-and-recovery story and [[063-michael-bagnell]]'s brain-stem-stimulation framing. Three independent angles on the same intervention. Eric's wild-swimming practice has the deepest mechanistic backing of any single intervention in the wiki.
- **Wearable design now has two anchors with consistent guidance**: [[082-jay-wiles-hrv]] + [[086-harry-leeming-visible]] both argue *data is motivation only, breath/practice is the active ingredient, hypervigilance is iatrogenic*. Operationally: turn off the screen, watch trends not absolutes.
- **MCAS framing has tightened** with #88 — the vulnerability+trigger model accommodates LC + ME/CFS + Lyme + mould-illness + post-vaccination patterns under one umbrella. Useful wiki-level synthesis.
- **Two new recovery-narrative techniques (#89)** — Declaration and Designated-Witness Sentence — are both portable to Eric without infrastructure. Worth explicitly trialling.
- **Trauma-informed breathwork (#85)** is a useful refinement of the wiki's breathwork stack — explains why breath-focus can backfire for some patients, and how to scaffold around it.

## [2026-05-04] ingest | batch #90–#99

10-episode batch — large structural additions across cognitive rehab, microbiome, decentralised trial design, the host's full recovery, and the wiki's first philosophy-of-disability anchor.

- **#90 James Jackson** — US neuropsychologist (Vanderbilt). **Anchor "brain fog → brain injury" reframe** + **cognitive rehab** as the wiki's "best-kept secret" intervention. Goal Management Training (GMT) for executive dysfunction; BrainHQ-style brain training as adjunct. Specifically: processing speed / memory / executive function as distinct rehab targets. Created [[cognitive-rehab]], [[brain-training]] intervention pages; updated [[brain-fog]] symptom page significantly with the reframe; created [[james-jackson]] people page.
- **#91 Groysman Q&A pt 1** — Listener Q&A continuation of [[076-dr-robert-groysman-sgb]]. Adds **anchor LDN dosing protocol** to [[low-dose-naltrexone]] (1mg → 4.5mg over weeks; <$100/mo via compounding pharmacy; 1-3 month onset; primary effect = fatigue). Also covers indirect dysautonomia testing options, vagus-thickening (dysfunction-not-damage), tinnitus mechanism speculation (auditory neuropathy + vagal involvement), spike-protein agnosticism, ferritin trap (LC inflammation falsely elevates ferritin → masks iron deficiency), hair-loss treatment (minoxidil + GHK-Cu copper peptide), exercise within pacing tolerance.
- **#92 Groysman Q&A pt 2** — **Microclots-sceptic anchor on the wiki**. Groysman flags validation gap, clinical-relevance unproven, and explicit anti-coagulant bleed-risk warning. Updated [[microclots]] theme with Groysman's sceptical voice alongside the existing pro-microclot [[033-pretorius-kell-microclots]] / [[037-dr-asad-khan]] / [[072-banerjee-stimulate-icp]] anchors — three positions on one disputed mechanism is a feature. Also covers gut-barrier repair (BPC-157, KPV peptides), parosmia/dysgeusia "**brown-out reset**" mechanism framing for SGB, blood-test panel pragmatism (don't order tests that won't change treatment).
- **#93 Viki Male** — Imperial reproductive immunologist. **Anchor LC-menstruation immunology episode**. Survey n~450: 70% of LC menstruators report cycle-pattern; >3/4 of those say worse in late luteal + period. Frames second half of cycle as "mini-pregnancy" immunologically — analogous to MS/IBD cycle-coupling, suggesting autoimmune dimension. Hormonal contraception + HRT as candidate management levers (pre-RCT). LC-perimenopause symptom overlap flagged. Created [[wilco-imperial]] trial page, [[viki-male]] people page; updated [[hormonal-dysfunction]] theme.
- **#94 Jackie's recovery story** — **Host's full recovery**, interviewed by partner Mally. **7th full recovery on the wiki.** Big Three = breathwork (now in instructor training) + yoga nidra + cold water; counselling + career break + Fern programme as later layers. New articulations: **"breath as active autonomic-regulation tool"** (not just calm); **"perfectionism as recovery-blocker"** named explicitly; **"brain-body asynchrony"** principle (body permits more before brain trusts more). Created [[recovery-stories/jackie-baxter-recovery]]; updated [[suzy-bolt-recovery]] (Jackie helped_partial late-phase amplifier), [[breathwork]] (#64 row updated with #94 reaffirmation), [[jackie-baxter]] people page.
- **#95 Élaina Gauthier-Mamaril** — Edinburgh philosopher of disability; ME/CFS since age 10. **Anchor philosophy-of-LC episode**. Frames LC as "**mass disabling event**" (1.9M UK private households per ONS, 40k+ children). Introduces **cripistemology** — disabled lived experience as expert knowledge — into the wiki. Identity move: queercrip (cyclical/episodic/invisible illness, distinct from permanent-disability). 2021 NICE GET/CBT-→-pacing change + clinician backlash flagged. Podcasting-as-scholarship (her *Massively Disabled* mini-series). Created [[laina-gauthier-mamaril]] people page.
- **#96 Masha Makeeva** — US-trained naturopathic + integrative MD on Mediterranean coast; LC ~80% recovered. **Anchor HBOT clinical-side episode** alongside [[048-saskia-mulder-south-africa]]'s patient-side anchor. Mitochondrial-repair + biogenesis framing; 20-60 sessions; **MS Charity UK ~£15/session** flagged as cheapest LC-relevant access. Lectin-free diet (Plant Paradox); spoons + jar-of-chi pacing metaphors; **recovery-then-stress-relapse pattern**. Created [[brain-tap]], [[ozone-therapy]], [[red-light-therapy]] intervention pages; updated [[hbot]] significantly; created [[masha-makeeva]] people page.
- **#97 Harlan Krumholz** — Yale cardiologist; co-PI with Akiko Iwasaki. **Anchor decentralised-trial-design episode**. Yale **LISTEN** study (observational, ~2,200 enrolled — DISTINCT from UK NIHR LISTEN [[058-fiona-jones-listen-trial]]). **Pax LC trial** (15-day extended-dose Paxlovid; placebo includes ritonavir for blinding; 41 US states; results ~Feb 2024) — explicit **viral-persistence hypothesis test**. **Hugo Health** data-agency platform — participant retains permission control. Atlas of Long Covid project (Iwasaki deep immune phenotyping × symptom phenotype map). Created [[yale-listen-study]], [[paxlovid-lc-trial]], [[paxlovid]], [[hugo-health]], [[harlan-krumholz]] pages.
- **#98 Charlotte Hammond** — UK recovery story, ex-school-teacher, Oct 2021 → ~late 2022. **8th full recovery on the wiki.** Private doctor (had had LC himself) + sugar-free/gluten-free diet + cold showers + antihistamines + **charity-rate therapy at £25/session** explicitly articulating partner-can't-substitute-for-therapist principle (independent of Jackie's #94 articulation — second voice). Post-recovery hypervigilance + sensory-sensitivity residuals. **Two-phase recovery** framing: clearing LC vs rebuilding capacity. Created [[recovery-stories/charlotte-hammond-recovery]] and [[charlotte-hammond]] people page.
- **#99 Viola Sampson** — UK microbiome analyst; recovered ME/CFS via cranial-sacral therapy. **Deepest microbiome anchor on the wiki**. Pro vs anti-inflammatory microbiome states; SCFA / butyrate as anti-inflammatory mediators; microbiome ↔ vagus ↔ inflammation loop. **Prebiotics > probiotics for long-term shifts** — probiotics are transient (days/weeks), prebiotics drive lasting ecosystem change. Specific strain recommendations (Optibac Every Day for nervous-system, BioGaia Protectis for slow transit, Culturelle/L. rhamnosus GG for histamine-degradation + viral defense). GOS prebiotic for bifidobacterium. **Explicit warning against broad-spectrum antimicrobials** (berberine, oregano essential oil) — counter-voice to functional-medicine "kill bad bugs" framing and to [[070-lorrie-rivers]]'s aggressive-antiparasitic minority position. Created [[prebiotics-gos]] and [[viola-sampson]] pages; significantly extended [[probiotics]] and [[gut-health]].

Batch-level signals:
- **Two new full recoveries (#94, #98)** bring the wiki's recovered-cohort to 8. **Jackie's own (#94)** is the most operationally detailed for Eric — same UK setting, same severe breathing-pattern dysfunction, same dysautonomia spectrum, same Type-A starting profile. The "**brain-body asynchrony**" principle is portable.
- **Disputed-mechanism status of microclots is now logged with all positions** — Pretorius/Kell pro [#33], Khan clinical pro [#37], Banerjee formal-trial sequential-singles [#72], **Groysman sceptic [#92]**. The wiki holds the dispute rather than resolving it.
- **Brain-fog anchor reframe (#90)** — "brain injury" with sub-categorisation (processing speed / memory / executive function) opens specific [[cognitive-rehab]] (GMT) and [[brain-training]] (BrainHQ) pathways. Both clinician-side anchored. Explicit identification of cognitive rehab as "best-kept secret" is the strongest single new intervention signal in this batch.
- **Microbiome anchor (#99)** is the wiki's most detailed — strain-specific probiotic recommendations + prebiotics-as-better-lever framing + don't-broad-spectrum-antimicrobial warning. Eric-relevant: Optibac Every Day + Culturelle (LGG, histamine-degrading) + GOS prebiotic are concrete self-experiment candidates.
- **HBOT cost-access (#96)** — £15/session via MS Charity UK is the wiki's most actionable HBOT-access signal.
- **LDN dosing anchor (#91)** — 1mg → 4.5mg over weeks; <$100/mo via compounding pharmacy. The wiki's most explicit titration protocol.
- **LC-menstruation autoimmune coupling (#93)** is now the wiki's clearest physiological case for cycle-symptom patterns — Imperial substudy will deliver mechanism-level data over coming months.
- **Decentralised-digital-democratised trial design anchor (#97)** — Yale's Krumholz / Iwasaki Pax LC trial is the wiki's clearest articulation of how 21st-century LC trials should be built. Hugo Health data-agency model is the structural layer worth tracking.
- **Philosophy-of-LC anchor (#95)** — gives the wiki vocabulary for what it is doing (cripistemology) and for the political dimension (mass disabling event). Unusually theoretical, but legitimises the wiki's own existence as a knowledge-extraction artifact from lived experience.
- **Partner-can't-substitute-for-therapist principle is now double-anchored** — Jackie #94 and Charlotte #98 articulate it from independent angles. Both note charity-rate / sliding-scale therapy as the access pathway.
- **Eric-relevant signals worth re-reading**:
  - **#91 LDN dosing protocol** if Eric ever evaluates LDN
  - **#93 Male LC-menstruation immunology** if any female contacts have cycle-coupled LC
  - **#94 Jackie's recovery story** as the closest-fit recovery template available — same setting, similar profile
  - **#96 Makeeva HBOT mechanism + MS Charity UK access** if HBOT becomes a candidate
  - **#97 Krumholz Pax LC trial** for any reinfection-prevention conversations + Hugo Health as data-agency philosophy
  - **#99 Sampson Optibac Every Day + Culturelle/LGG + GOS prebiotic** as specific microbiome self-experiment candidates; counter-voice against aggressive-antimicrobial protocols


## [2026-05-04] ingest | batch #100–#109

Ten-episode batch — broadens the wiki across coaching frameworks, the dysautonomia-vs-viral-persistence-vs-mind-body axis, employment-policy research, mould-as-mechanism, and adds two more full recoveries (#107, #109) bringing the recovered cohort to 10.

- **#100 Michelle Irving** — Australian coach (autoimmune liver + vertigo, *not* LC). **Emotional Empowerment Map** — 4 stages (at sea / beach / forest / village) decoupled from physical recovery. "What helps?" as foundational re-usable practice. **Vertical-vs-horizontal life model** explains why village-re-entry feels disorienting (the same pattern Jackie #94 and Charlotte #98 named without a label). Created [[michelle-irving]]; updated [[self-compassion]] theme.
- **#101 Sally Riggs (return)** — psychologist, now "more or less recovered" (was substantial in #23). Refined polyvagal frame for LC: **most "calm your nervous system" content is built for people already in rest-and-digest; LC patients are in shutdown — opposite condition**. Track NS state, not symptoms. SSP **upgraded helped_partial → key_to_recovery** based on her now-recovered status; #23 row updated to reference #101 rather than adding a new row. New disclosure: she did DNRS in one day (perfectionism warning, logged as no_effect on the DNRS page). New e-course launched (3 modules: sensitivities/strategies/support). Orienting strategy demonstrated.
- **#102 Dan Neuffer (first proper guest)** — founder of [[ans-rewire]], previously named-but-not-interviewed. Anchor articulation of **dysautonomia-as-root-cause** for the post-viral cluster (ME/CFS, fibromyalgia, POTS, MCS, much of LC). **Multilateral / "somato-neurological" approach** rejects pure-brain-training and pure-biomedical purist camps. **Rejects "long covid" as a term** (logged as Dan's position; wiki holds it alongside [[ryan-prior]]'s opposing argument). Multi-sensory triggering as tell-tale heuristic. Created [[dan-neuffer]] proper page; updated ANS Rewire program with multilateral framing.
- **#103 Amy Proal — anchor viral-persistence episode**. PolyBio Research Foundation + Long Covid Research Consortium articulated for the first time on the wiki. Tissue biopsy + PET imaging methodology. **Spike protein in gut up to 676 days, in blood up to 16 months** (argues active replication). UCSF T-cell activation maps. **Combination antiviral therapy** as design principle (per HIV experience). Truvada trial planned at Mt Sinai with David Putrino. Anti-psychosomatic argument grounded in pathogen biology. Created [[amy-proal]], [[polybio]] pages; significantly extended [[viral-persistence]] theme with #103 content.
- **#104 Alison Larkman** — Bristol artist with severe ME (~11 years). *I Would Be Here If I Could* (Arts Council England funded) — touring mirror box plays absent-people's audio messages at the places they would go if they could. **Art-as-advocacy** anchor. UK numbers worth preserving: 2M LC self-reporting, 500k ME, 65k severe ME bedbound. Created [[alison-larkman]]; updated [[advocacy]] theme.
- **#105 Calum Carson** — Lancaster University (PI Holland) Inclusive Remote and Hybrid Working Study. UK-wide survey on disabled workers' remote/hybrid experience over 5 years; 50 interviews; employer + policy-maker engagement; **publicly accessible report + commissioned short film + employer best-practice guide**, all launching Dec 2024. **Self-defined disability framing** (LC included even though no legal definition). Anchor concern: **substitution-not-supplement risk** — home-working replacing in-office reasonable adjustments. Created [[calum-carson]]; updated [[employment]] theme with remote/hybrid section.
- **#106 Taylor Krick** — US functional-medicine chiropractor (*Autoimmune Doc*). **First strong mould-as-LC-mechanism voice** on the wiki ("mould piles up the logs, COVID drops the match"). **Organic Acid Test (OAT) — Mosaic Labs** as anchor LC lab (76 markers covering gut/mitochondrial/neurotransmitter/methylation). **Clostridia-gut-→-dopamine-conversion-block** as standout LC neurotransmitter pattern. **Sniper-not-machine-gun supplementation** philosophy ("4 things in high doses, all aimed at the same lab-confirmed mechanism, beats 20 things at sub-therapeutic doses"). Created [[taylor-krick]] page.
- **#107 Raelan Agle** — Canadian recovered ME/CFS (10 years ill, ~4 years recovered). YouTube-channel host of the largest single recovery-story archive. **9th full recovery on the wiki + the wiki's best meta-source for recovery patterns**. Three universal themes from 100+ recovery interviews: NS/fear-response (everyone), brain training/neural pathways (most), physical-mechanism work (some — many recovered patients have all-normal tests). **Scaffolding-first principle for graded movement** = re-frame of "GET doesn't work": gradual re-exposure works, but only after sleep/stress/gut/environment are dialled in. Created [[raelan-agle]] person + recovery-story pages.
- **#108 Vass + Vicky** — UEA cardiologists (Prof Vassiliou + Dr Tsampasian). **Meta-analysis of LC risk factors (41 studies, ~860k patients)**: older age, female (~+50% risk), higher BMI, smoking, hospitalization/ICU, comorbidities (CAD/CKD/diabetes). **Vaccination ~halves LC risk** — wiki's clearest single-number prevention summary. Argues UK booster eligibility too narrow (asthmatics under 65 specifically). Cardiac-MRI for structural ruling-out. "Normal tests de-risk prognosis, don't dismiss symptoms." Created [[vass-vassiliou]], [[vicky-tsampasian]] pages.
- **#109 Julie Black** — Scottish recovered LC patient, **10th full recovery on the wiki**, ~3-4 month mind-body / pain-reprocessing-therapy recovery. Stack: low-histamine diet (early relief) → validating doctor + ruling-out scans (permission to commit to mind-body frame) → Suzy Bolt yoga + yoga nidra (the actual rest she'd never had) → Alan Gordon's *The Way Out* audiobook ("replace pain with symptoms") → **Curable app all-in for hours/day for weeks**. **First key_to_recovery for Curable on the podcast.** "Submit now ≠ accept forever" anchor framing on acceptance. Doom-loop-Facebook-groups named as iatrogenic harm. Suicidal-ideation framing in early LC. Created [[julie-black]] person + recovery-story pages; updated Curable app + Suzy Bolt program with new evidence.

Batch-level signals:

- **The wiki's frame-axis is now properly populated.** #102 (dysautonomia-as-root-cause / Neuffer) + #103 (viral-persistence-as-root-cause / Proal) + #106 (mould-as-major-mechanism / Krick) + #107 (NS-hypersensitivity-as-root-cause / Agle synthesis) sit on a single pluralism axis. The wiki holds all four positions without resolving them. **Critical Eric-relevance**: depending on which frame a clinician is operating from, "what test do I run?" yields different answers — Proal's tissue biopsy / spike-protein-in-blood, Krick's OAT, Riggs's NS-state tracking, Agle's "tests came back normal because the body is normal."
- **Pain-reprocessing-therapy / mind-body route is now strongly anchored** (#109 Julie + #56 Johanna already + Alan Gordon as common reference point). The Curable app is now the wiki's clearest cheap, no-clinician-required, do-it-yourself entry point to the mind-body route — distinct from Gupta / DNRS / ANS Rewire (more expensive, more programmatic). For Eric, this is the most actionable cheapest test of whether the mind-body frame works for him.
- **Suzy Bolt's program now has 2 key_to_recovery + 2 helped_partial across 4 third-party participants** (founder bias is now firmly resolved). Pattern: prerequisite-scaffolding role (yoga nidra as actual rest, breathing classes as foundation) more than load-bearing recovery layer. Useful UK-based starting point for any LC patient with breathing-pattern + dysautonomia presentation.
- **#107 Agle's three-themes synthesis is the wiki's highest-evidence summary of what recovery requires** across 100+ interviews. Compatible with — and complementary to — #102 Neuffer's multilateral frame.
- **Mould-as-mechanism is a new wiki signal worth tracking forward.** Krick's claim is strong (most common standout finding across hundreds of LC patients tested) and currently has no podcast counter-voice. Eric should at least be aware of OAT testing as a screen.
- **Vaccination-as-prevention quantified at ~50%** (#108 meta-analysis) is the wiki's clearest single-number reinfection-prevention summary — directly portable to any conversation Eric has about boosters.
- **Suicidal-ideation framing in LC** is now anchored from two angles (#94 Jackie's recovery story already named the territory; #109 Julie articulates it as occurring early, scarily fast, and stigma-loaded by patients themselves). Important for the wiki's [[mental-health-and-suicidality]] theme.
- **"Submit now ≠ accept forever"** (#109 Julie) is the wiki's clearest articulation of why the standard "you must accept LC" advice often fails — counter-pattern to the wiki's existing acceptance vocabulary.

- **Eric-relevant signals worth re-reading**:
  - **#103 Proal viral persistence** as the upstream-cause hypothesis Eric should know — explains why his clinicians may be looking in the wrong place if they only blood-test
  - **#102 Neuffer multilateral framing** — his closest-fit operational synthesis of integrating brain-training work with his existing pharmacological stack (mestinon / ivabradine / florinef / antihistamines)
  - **#106 Krick OAT + mould screen** if he hasn't been screened — the single highest-value test in this batch for him
  - **#109 Julie's Curable + *The Way Out*** as the cheapest, most-self-administered mind-body route entry point
  - **#101 Riggs polyvagal-LC re-frame + state-not-symptom-tracking** — operationally portable everyday practice
  - **#108 Vass + Vicky vaccination ~50% LC-risk reduction** for any reinfection conversation
  - **#100 Irving's vertical/horizontal life model + 4-stage map** as the cleanest articulation of village-re-entry experience Eric is now in
  - **#107 Agle's scaffolding-first principle for movement** as the operational guidance for Eric's exercise reintroduction


## [2026-05-04] ingest | batch #110–#119

Ten-episode batch — broadens the wiki across the patient-led research architecture (PLRC), cross-condition ME/CFS recovery (Sophie #111), Jackie's post-recovery year (#112 + the new creativity #113), a UK private-GP-as-LC-specialist voice (Taylor #116), the heterodox-clinician Myhill protocol (#118 + its patient-side application in #114), the most comprehensive LC dysautonomia trials map yet (Stiles return #115), and the first detailed mechanism-targeted LC fatigue neuroimaging study (#119). Adds **2 more full recoveries (#111 pre-Covid ME/CFS, #114 LC)** bringing the on-wiki count to 12 (10 LC + 1 ME/CFS pre-Covid + 1 partial LC #117).

- **#110 Lisa McCorkell + Gina Assaf + Hannah Davis** — three of the four PLRC co-leads, in conversation. Detailed founder-side narrative + state of PLRC at 3.5 years. **$6M raised in 2023, $5M to biomedical research grants** (10 funded projects), 2023 Long Covid review paper >1M downloads, **scorecards for patient engagement** with Council of Medical Specialty Societies, return-to-work paper just published, **Infection-Associated Chronic Conditions umbrella coalition**. Created [[lisa-mccorkell]], [[gina-assaf]], [[hannah-davis]] pages; updated [[patient-led-research-collaborative]] with 3rd evidence row; updated [[body-politic]] with Body-Politic-as-disability-justice-frame.
- **#111 Sophie Reynolds** — UK ex-prison-officer; **pre-Covid ME/CFS recovery (March 2018 → 2-3 years)**. Recovery stack: Optimum Health Clinic STOP technique + **Pilates as key_to_recovery (first on the wiki)** + nervous-system understanding + breathwork integrated with movement. **First explicit no_effect signal for cold-water exposure** — counterweight to Jackie's #64 key_to_recovery; possible interpretation: timing/scaffolding-dependent. Created [[sophie-reynolds]] + [[recovery-stories/sophie-reynolds-recovery]]; updated [[pilates]], [[cold-water-exposure]], [[breathwork]], [[optimal-health-clinic]] (now 1 key_to_recovery + 1 recommended).
- **#112 Jackie 2023 Reflections** — host-solo. Recovery declared spring 2023. **Post-recovery adjustment is its own journey** anchor framing. Career break (Jan 2023) as inflection — structural stress of sick-pay was bigger than recognised. Johanna #56's "**95% crash warning**" credited as a load-bearing wiki principle. **Tiredness ≠ fatigue** named distinction. Running [[long-covid-breathing]] with Vikki — first cohort just completed. Updated [[long-covid-breathing]] with cohort-completion row.
- **#113 Long Covid Creativity 2023** — third in the annual creativity-compilation series (#14 → #65 → #113). 10 contributors across poetry / painting / nail art / memoir / collage / crochet / art workshops / music. Standout: **Jess Taylor's Restart Creative** (UK CIC; online low-demand art workshops + journaling for LC patients; grant-funded). Skye Yu's *Still Moving* memoir. Anne Wallace poetry collection forthcoming. Cross-cutting pattern: creativity displaces symptom focus + provides career-pivot path + builds online community. Created [[restart-creative]] program.
- **#114 Sarah / Lotus Path Yogi** — Sheffield UK yoga teacher; **11th full recovery on the wiki (March 2020 → ~spring 2022)**. Recovery is **the strongest single example of multi-stack integration** on the wiki: Body Politic Slack (validation) → beta blockers (first win) → 10-12× daily enforced rest (yoga nidra/meditations — single biggest factor) → **Dr Myhill protocol** (paleo keto + B12 injections + D-ribose + mitochondrial supplements) → **Raelan Agle's YouTube** (hope + scaffolding-first graded resistance, 1 minute body-weight resistance/day, increase weekly if no PEM) → **fermented foods microbiome rehab** (Herx 3 days then improvement) → daily yoga (the right kind: seated/lying, no inversions). Now teaches Lotus Path Yoga with **zero PEM in 400-500 students** and hosts the **Long Covid Hope Podcast**. **D-ribose felt within 1-2 weeks** = strongest single anecdote on wiki for [[ribose]]. Created [[sarah-lotus-path-yogi]] + [[recovery-stories/sarah-lotus-path-recovery]] + [[lotus-path-yoga]] + [[long-covid-hope-podcast]] pages; updated [[ribose]], [[probiotics]] (added no_effect for capsules + helped_partial for fermented foods), [[keto-diet]], [[yoga]], [[yoga-nidra]], [[breathwork]], [[beta-blockers]], [[body-politic]].
- **#115 Lauren Stiles return** — second appearance from the Dysautonomia International president; **most comprehensive single-source LC dysautonomia research-pipeline episode** to date. **Anchor mechanism update**: animal-model SARS-CoV-2 damages the autonomic ganglia structurally before respiratory symptoms; ME/CFS autopsy literature already showed ganglionitis. **Trials map**: NIH IVIG + ivabradine arm; **argenx VYVGART (efgartigimod) phase-3** (FcRn inhibitor; FDA-approved for myasthenia gravis); Walter Reed/DoD ivabradine; Sweden EECP + iodine; **Harvard Peter Novak IVIG (broader than POTS criteria)**; **3 VNS trials with positive emerging results** (Kevin Tracy lineage; reduces orthostatic tachycardia + improves overall QoL). Vanderbilt RCT now confirms low-carb POTS benefit — "anecdote → research-priority → evidence" cycle complete. Stiles personally uses VNS before bed for sleep; lost IVIG access when her doctor went to pharma but uses VNS instead. Created [[nih-ivig-pots-lc]], [[argenx-vyvgart-pots-lc]], [[eecp-pots-sweden]], [[vagus-nerve-stim-pots-trials]], [[mri-fatigue-mass-gen-mit]] trial pages; updated [[lauren-stiles]], [[ivabradine]] (5 mentions now, two NIH trial arms), [[vagus-nerve-tens]], [[dysautonomia-international]] with #115 evidence row.
- **#116 Dr Claire Taylor** — UK private-GP LC + ME/CFS + MCAS + POTS specialist; expert advisor for World Health Network. **First practising-GP-as-LC-specialist voice on the wiki**. **79% of LC patients have POTS** per latest study; argues "nearly everyone has dysautonomia." 30bpm threshold misses many. 10-min stand test in clinic. **Salt graph** — 10-15bpm reduction per step-up (cleanest dose-response on wiki). Vagus nerve thickening + diaphragm flattening on imaging in ~1/5 LC patients. Pragmatic MCAS consensus (treat empirically). Cytokine + chemokine panels (IL-6, IL-10, TNF-α, CCL5, VEGF). **Third UK clinical voice confirming Eric's exact stack** (ivabradine + mestinon + fludrocortisone + antihistamines), after Gupta #57 and Stiles #66/#115. Created [[claire-taylor]] page; updated [[ivabradine]], [[mestinon]], [[fludrocortisone]], [[antihistamines]], [[salt-loading]], [[compression-stockings]], [[beta-blockers]], [[midodrine]], [[pots]], [[mcas]] with #116 rows.
- **#117 Leela O'Brien** — US aerospace engineer (PhD; ex-NASA contractor). LC with cognitive + motor symptoms. **Recovered substantially once, then re-flared**; partial recovery. **Belief-without-pressure** as recovery mindset (cleanest articulation on wiki — believing in healing AND removing pressure to heal simultaneously). **Ego-fuel as relapse mechanism** — initial recovery + ego-return → re-flare. **Hot-chocolate-on-the-couch** as can-rather-than-cant anchor. Stephen Hawking framing — physical capacity sets the frame, not the quality of life inside it. Created [[leela-obrien]] page; updated [[meditation]] with #117 evidence row.
- **#118 Dr Sarah Myhill** — heterodox UK GP since 1981 (in regulatory dispute history). **Coherent heterodox-clinician framework**, frequently cited in patient recovery communities. Car-analogy framework: fuel + oxygen + mitochondria + thyroid + adrenals + inflammation, in order. **Paleo ketogenic diet (PKD)** = non-negotiable starting point. **Vitamin C 5g + Lugol's iodine 3 drops/night** for upper fermenting gut (UFG). **UFG → MCAS** strong-claim alternative mechanism. Mitochondrial supplements only AFTER UFG fixed (Mg / Vit D / CoQ10 / B3 / acetyl-l-carnitine / D-ribose). Thyroid glandulars (DIY); Epsom salt baths; **methylene blue + DMSO + photodynamic therapy** as antimicrobial trio (logged but the wiki does not endorse self-administration). **Groundhog Basic / Acute / Chronic** protocol framework. The wiki holds this as a coherent framework — selectively endorses the cheap-low-risk pieces (D-ribose, vitamin C, Buteyko, Epsom baths, continuous glucose monitor as diagnostic), flags the high-risk pieces. Created [[sarah-myhill]] page; updated [[methylene-blue]], [[buteyko-breathing]], [[keto-diet]], [[ribose]], [[mcas]] with #118 rows.
- **#119 Daniel Gomez + Ewa Beldzik** — Mass Gen Hospital + MIT (Laura Lewis lab) postdocs. **First detailed mechanism-targeted neuroimaging study for LC fatigue specifically**. fMRI with 3 tasks per participant: 15s breath-hold (vascular control), simple visual task (sensory baseline), Stroop-style color-word matching (12-min cognitive task; expects performance degradation in LC patients). **Hypothesis**: sub-lesional oxygenation impairment as the LC fatigue mechanism (compatible with [[microclots]]). Methodologically novel combo of vascular + neural + cognitive in LC fatigue cohort at high resolution. **Tests-should-exclude-not-identify** anchor framing for LC clinical practice. Recruiting Boston only; results mid-late 2025. Created [[daniel-gomez]], [[ewa-beldzik]], [[mri-fatigue-mass-gen-mit]] pages.

Batch-level signals:

- **Eric's stack architecture is now triple-confirmed at UK-clinical level**: Gupta #57 + Stiles #66/#115 + Taylor #116 — three independent UK voices recommending the exact same architecture (ivabradine + mestinon + fludrocortisone + antihistamines). This is the strongest possible non-RCT signal that Eric is on the right architecture. **Midodrine remains the single highest-evidence gap** (4 wiki-anchor recommendations vs Eric not on it).
- **Multi-stack integration as the recovery template**: Sarah / Lotus Path Yogi #114 is the wiki's clearest example of a recovery built by combining frameworks (Myhill biochemical + Raelan scaffolding-first + microbiome work + her own yoga background). **No single protocol fixed it**; the integration was the recovery. Reinforces — and operationalises — Raelan's #107 three-themes synthesis.
- **The dysautonomia trial pipeline is now real**. Stiles #115 documents 6+ active LC dysautonomia trials. **Ivabradine** (Eric's drug) is in two NIH-funded LC POTS trials. **VYVGART** (efgartigimod) for LC POTS is in phase-3 expansion — closest to a near-term FDA-approval pathway for an LC drug.
- **VNS / vagus-nerve-stimulation accumulated significant evidence in this batch**. 3 funded VNS-in-POTS trials with positive emerging results (#115); Kevin Tracy lineage anchors mechanism (vagal anti-inflammatory pathway → cytokine suppression → drug-resistant Crohn's + RA in remission); Stiles personally uses it for sleep. Eric should know **VNS exists as a tool**.
- **Pilates → key_to_recovery on the wiki for the first time** (Sophie #111). Combined with [[029-lorna-nicholson-pots-breathing]] (clinician recommendation) and [[053-deepak-ravindran-pain]] (pain-specialist recommendation), Pilates is now the wiki's most evidence-supported POTS-friendly movement modality.
- **Cold-water exposure now has its first no_effect signal** (Sophie #111). The wiki holds both Jackie's #64 key_to_recovery AND Sophie's #111 no_effect — same intervention, different patient, different outcome. Probable interpretation: timing / scaffolding / immersion-vs-shower.
- **The MCAS mechanism debate is now three-way**: mast-cell-first (Peers #38, Saperstein #68, Dempsey #88) vs **upper-fermenting-gut-first (Myhill #118)** vs nervous-system-driven mast-cell-instability (Riggs #101, Nicholson #29). Wiki holds all three; treats each as a coherent alternative hypothesis.
- **Patient-Led Research Collaborative is now properly anchored** as a wiki entity rather than a referenced organisation. PLRC's $5M funded research grants will produce results 2024-2025 — material follow-up batch.
- **#119 fMRI study + Stiles #115 ganglia advocacy + Iwasaki/Putrino LISTEN/Pax-LC/Atlas of LC** form three parallel mechanism-mapping efforts. The wiki should track all three for next-generation LC mechanism evidence; results land 2024-2026.
- **The "tests-should-exclude-not-identify" framing** (Gomez #119; parallel of [[081-liza-dileo-thomas-patient-experience]]'s "great news, everything's normal" antipattern) — useful for any clinical conversation where Eric encounters "your tests came back normal."
- **Post-recovery adjustment is now anchored** (Jackie #112 + Charlotte #98 + Leela #117 partial). The wiki should hold "recovered" as the *start* of a separate phase, not an end-state.

- **Eric-relevant signals worth re-reading**:
  - **#116 Taylor's stack confirmation** — third UK clinical voice confirming Eric's exact medications; closes the loop on whether he's on the right architecture
  - **#115 Stiles trials map** — VNS, VYVGART, ivabradine, IVIG; the wiki's clearest single-shot map of where LC dysautonomia treatment is heading
  - **#114 Sarah / Lotus Path Yogi** — closest-fit POTS recovery template on the wiki; same drug architecture, similar profile, recovered in ~2 years; **D-ribose anecdote (felt in 1-2 weeks)** is the strongest single supplement-trial signal for Eric
  - **#118 Myhill** — selectively useful (D-ribose, vitamin C, Buteyko, Epsom baths, continuous glucose monitor); the broader framework is heterodox and shouldn't be self-administered without clinical oversight
  - **#117 Leela's belief-without-pressure** — operational mindset for Eric's post-recovery year
  - **#112 Jackie's post-recovery framing** — the "recovered ≠ pre-Covid me" template Eric is now living
  - **#111 Sophie's cold-water no_effect** — counterweight to existing key_to_recovery; cold water is dose / timing / context-dependent, not universally beneficial


## [2026-05-04] ingest | batch #120–#129

Ten-episode batch — 79 of 211 episodes now ingested (still missing #31). Strong batch on the **research-and-trials front** (#120 Faghy antiviral launch, #122 Cummings cognitive follow-up + employment, #128 McCracken/Knight T-cell exhaustion + Manchester cohort), a **major communication / mental-health theme strand** (#121 Pamela Rose, #125 Peter Burt, #126 Joshua Roman), the **first East Asian medicine deep-dive** on the wiki (#124 Elizabeth So), **2 more full recoveries on the wiki** (Rachael #127, Lily Spechler #129) plus 1 in-progress (Peter Burt #125), and one solo Jackie reflection (#123, 4-year mark).

- **#120 Mark Faghy** — research update; Derby cohort + CPETs + the **first UK long-Covid antiviral infusion trial** (£1.25m Gilead-funded; 5-day IV; targets viral persistence). Created [[gilead-antiviral-lc-uk]]; updated [[derby-cohort-observation]] (added follow-up findings — patient state can swing 180° in 48 hours, shouldn't be missed by 6/12-month cohorts), [[mark-faghy]], [[viral-persistence]] theme, [[episodic-disability]] theme.
- **#121 Pamela Rose** — fatigue coach (recovered ME/CFS pre-Covid). Anchored *difficult conversations* as a discrete skill set in chronic illness. Created [[pamela-rose]] + [[recovery-stories/pamela-rose-recovery]]; updated [[communication]] theme.
- **#122 Louise Cummings** (return) — 6-month follow-up of cognitive-linguistic study + first detailed **employment outcomes** in this cohort (only 1 of 37 returned to full pre-Covid role at 21 months). Updated [[louise-cummings]], [[brain-fog]] (added follow-up section), [[employment]] theme (with the empirical numbers).
- **#123 Jackie 4-year reflections** — host-solo. LC Awareness Day. Recovery-is-possible-AND-requires-the-right-environment. No new pages — episode page only.
- **#124 Elizabeth So** — DACM, recovered LC, NYC. **First East Asian medicine deep-dive on the wiki**. Created [[elizabeth-so]], [[gua-sha]], [[cupping]], [[chinese-herbal-formulas]]; updated [[acupuncture]] (new key_to_recovery row).
- **#125 Peter Burt** — recovering LC, 3+ years; men's-mental-health anchor. Created [[peter-burt]] + [[recovery-stories/peter-burt-in-progress]]; updated [[breathwork]] (helped_partial — first-agency-restoring tool), [[counselling]] (helped_partial — non-judgemental third-party), [[mental-health-and-suicidality]] theme, [[communication]] theme.
- **#126 Joshua Roman** — cellist; Mount Sinai LC clinic patient. Vulnerability as connection medium. Created [[joshua-roman]], [[mount-sinai-lc-clinic]] program; updated [[mind-body]] theme.
- **#127 Rachael (Rebound Athletic)** — **12th full recovery on the wiki**. Recovery sequence: stop-work + Suzy Bolt + Curable + countryside move + cold-water (second attempt). **Strongest single timing-matters data point on the wiki** — same patient, same intervention (cold water), no_effect at 6 months → key_to_recovery at ~18 months. Created [[rachael-rebound-athletic]] + [[recovery-stories/rachael-recovery]] + [[rebound-athletic]] program; updated [[curable-app]] (key_to_recovery #2), [[suzy-bolt-recovery]] (helped_partial — gateway), [[gupta-program]] (mentioned_only — chosen against on cost), [[cold-water-exposure]] (the timing-matters double row).
- **#128 Nigel McCracken + Sean Knight** — Virax Biolabs + Manchester (Lydia Becker Institute). T-cell exhaustion as an LC mechanism layered onto Amy Proal's tissue-reservoir model (different layers, not competing). Created [[nigel-mccracken]], [[sean-knight]], [[virax-tcell-exhaustion-lc]], [[ciro-manchester]]; updated [[viral-persistence]] theme (added cross-mechanism note + #128 episode link), [[me-cfs-parallels]] theme.
- **#129 Lily Spechler** — US RD; recovered LC. **Strong dietitian-side critique** of widely-recommended LC diets (low-histamine, keto/carnivore, blanket sodium) on malnutrition + mechanism-mismatch grounds. **13th full recovery on the wiki**. Created [[lily-spechler]] + [[recovery-stories/lily-spechler-recovery]] + [[energy-expansion-project]]; updated [[salt-loading]] (recommended-with-caveat — not blanket advice; subgroup-specific), [[low-histamine-diet]] (body-section critique, no count change), [[keto-diet]] (body-section critique, no count change), [[gut-health]] theme.

Batch-level signals:

- **Treatment-trial pipeline now visible end-to-end** for viral-persistence: tissue-imaging anchor (Proal #103) → cell-level mechanism (T-cell exhaustion #128) → diagnostic IVD in development (Virax) → first-in-UK antiviral RCT launching Easter 2024 (#120 Faghy/Strain). Multiple parallel angles into the same story; both researchers explicitly note LC is *several conditions* and the diagnostic should *identify the subgroup*, not relabel everyone.
- **Empirical employment data are now on the wiki** (#122 Cummings): only 1 of 37 LC patients returned to full pre-Covid role at 21 months. **Cognitive demand was the dominant return-to-work blocker, not physical symptoms.** Confirmed by mechanism: cognitive-only practice tasks empty Joshua Roman in 30–60 sec when full play-throughs take 20 min (#126).
- **Cold-water exposure timing/readiness thesis just got its strongest empirical anchor** — Rachael #127 same-patient no_effect → key_to_recovery in 18 months. Combined with Sophie #111 no_effect and Jackie #64/#94 key_to_recovery, the wiki now treats cold water as a **late-stage amplifier**, not a beginner intervention.
- **Suzy Bolt program now has 5 evidence rows** with a clear pattern: program reliably opens the door (community + breathwork + yoga nidra), but **load-bearing recovery driver varies by patient** (Bolt herself, Gina Short = key_to_recovery; Jackie, Julie Black, Rachael = helped_partial / scaffold to other interventions).
- **Curable app is now the highest-evidence accessible mind-body app on the wiki** (3 mentions: 2 key_to_recovery + 1 helped_partial). $50/year vs Gupta cost-prohibitive for many. Rachael #127 explicitly chose it *because* of cost.
- **Men's mental health is now an explicit thread** through Peter Burt #125. Therapy + breathwork is the wiki's clearest pattern for the male-and-pushing-through demographic. Pairs with Rachael's #127 same-arc-different-trajectory (resistance + finally accepting help + therapy was inflection point).
- **East Asian medicine on the wiki for the first time** (#124 Elizabeth So). 4 new intervention pages, all bundled to a recovered-patient practitioner. Wiki holds these but is neutral on EAM as a route — it's another integrative-stack candidate.
- **The "recommended_against" gap in the schema** is exposed by Lily Spechler #129. She has clinical critiques of low-histamine, keto, blanket sodium that don't fit any outcome bucket cleanly. Resolution: counts unchanged; body-text critique sections added. Worth flagging as a future schema discussion.
- **Eric-relevant signals worth re-reading**:
  - **#120 Faghy** — antiviral trial is moving fast. If results are positive, RCT could open up by 2025-2026. Eric should track Derby/Strain progress.
  - **#122 Cummings** — confirms cognitive load is the bigger LC return-to-work blocker than physical load. Reinforces the case for cognitive pacing as Eric continues.
  - **#125 Peter Burt** — the same perfect-storm setup as Eric's pre-Covid life. Both breathwork and therapy as recovery levers; both already in Eric's stack.
  - **#127 Rachael** — closest-fit timing-matters data on wiki. Same intervention can do nothing or be life-changing depending on the readiness of the system. Counts against rigid "this didn't work for me, cross it off" thinking.
  - **#128 McCracken/Knight** — T-cell exhaustion + Amy Proal's tissue-reservoir model are *layered*, not alternatives. The combination explains why single-drug antivirals tend to under-deliver and supports the combination-therapy frame.
  - **#129 Lily Spechler** — important counter to the Lorrie Rivers / Sarah Myhill keto framing already on the wiki. Eric's stack-and-experimentation should not slip into chronic under-eating during dietary restriction; check Chronometer.

## [2026-05-04] checkpoint | episodes 120-129 ingested (79 of 211; #31 missing transcript)

## [2026-05-04] ingest | batch #130–#140

Indexed 11 consecutive episodes covering Q1–Q2 2024 LC content. Two more **full recoveries** added (now 15 on wiki) and significant new infrastructure on hypothesis-driven mechanism work and movement-readiness frameworks.

Per-episode summary:

- **#130 Marco Leitzke** — German ICU consultant + nicotinic-receptor researcher. **Receptor-blockade hypothesis**: spike protein binds nAChR silently across the body; nicotine (~30× higher affinity) competes spike off; transdermal *low-dose-long-time* protocol; expect 7-day flare. Created [[marco-leitzke]], [[nicotine-patches]]; updated [[viral-persistence]] theme with adjacent receptor-blockade frame.
- **#131 Wes Ely** — Vanderbilt intensivist, PI of [[rvlc-trial]] (550-pt placebo-controlled, double-blind RCT of [[baricitinib]] in established LC, NIH-funded). Originally mistook LC for PICS; updated to `iAChC` (infection-associated chronic conditions) umbrella. Created [[wes-ely]], [[rvlc-trial]]; updated [[baricitinib]] (added evidence row), [[viral-persistence]] (added immunomodulation-arm note).
- **#132 Rosalba Courtney + Hadas Golan** — co-authors of 2024 LC IBT case series (5 consecutive patients, before/after a 6-week protocol). Created [[rosalba-courtney]], [[hadas-golan]], [[integrative-breathing-therapy]]; updated [[breathwork]] (added evidence row + new tag). **Three-axis frame** (biomechanics / biochemistry / psychophysiology) is the cleanest dysfunctional-breathing taxonomy on wiki. **LC hypocapnia may be mitochondrial under-production of CO₂, not over-breathing** — so reduced-volume work is too aggressive at start; cadence-first works better. ETCO₂ in 20s mmHg cohort.
- **#133 A K Davidson** — UK writer, mother of three, **3 × covid + 3 × LC**, recovered each time. **14th full recovery on the wiki**. Final round added **brain training** as the closing piece + felt resilience to reinfection. Other levers: York test → elimination diet; **osteopath → upper-chest breath revelation** (former flautist had been mistaking diaphragm-only for full breathing) → breathwork practice became load-bearing; POTS dx (Boon Lim materials); [[yoga-for-life-project]] peer-support; Radio 4 → Radio 3 news-detox. Created [[ak-davidson]], [[recovery-stories/ak-davidson-recovery]], [[yoga-for-life-project]]; updated [[breathwork]] (added evidence row + new tag).
- **#134 Vicky van der Togt + Jeremy Rossman** — co-authors of 2024 hypothesis paper proposing **acid-base disregulation** as a *central inter-mediator* across LC symptoms. Created [[vicky-van-der-togt]], [[jeremy-rossman]], [[research-aid-networks]], [[acid-base-disregulation]] theme. Wiki's first explicit acid-base / acidosis frame — links the breathing/CO₂ story (#12, #17, #29, #132) and the bioenergetic/mitochondrial story (#21, #44, #45, #128) under one inter-mediator. Testing plan: lactate measurement + biosensor wearable.
- **#135 + #136 Meg Anderson** — DPT, virtual LC autonomic-rehab; co-runs [[energy-expansion-project]] with Lily Spechler. **Two-part movement series**. Created [[meg-anderson]], [[reset-breathwork]], [[workwell-foundation]]; updated [[graded-exercise]] (added preconditioning frame + 2 evidence rows; mention_count 2→4). **RV CAMPING** preconditioning checklist (Respiratory, Vagus, Consistency, Activity-mod, Monitoring, Pacing/Positioning, Intake, Normalising MCAS, Grounding/Gratitude). **Resting HR + 15–20 bpm ceiling** (Workwell lineage); 10–20% progression rule. Won't use Levine/CHOPs as published — too aggressive, ~50–60% non-completion broadly applied. **Reset breathwork** as bridge for patients who can't tolerate any traditional exercise.
- **#137 Lorrie Rivers (return)** — deep-dive on **EFT Meridian Tapping**. Created [[eft-tapping]]; updated [[lorrie-rivers]] with episode + return-appearance note. Acknowledgement-first model distinguished from brain-retraining; live demo on episode (Jackie 8/9 → 5/6 in one round on concert anxiety). Self-administered, scalable, can be done by *imagining* the tapping for PEM-prone patients.
- **#138 Jules Rogers** — UK Mind-Body practitioner / life coach. **15th full LC recovery on the wiki**. Mind-Body therapy was ~80% of recovery (the inflection); life-coach training was the closing 20%; **HRT was a meaningful late lever for perimenopause-overlap brain fog** — wiki's first explicit positive HRT row from a recovered patient. Created [[jules-rogers]], [[recovery-stories/jules-rogers-recovery]]; updated [[hormonal-dysfunction]] theme.
- **#139 Patrick Ussher + Peter Deen** — anchor episode on **excessive thirst / hypovolemic dehydration**. Ussher hospitalised with sodium 116; mis-diagnosed as **primary polydipsia** (psychogenic framing for excessive water drinking); read the literature back to 1930s and concluded a subset of "primary polydipsia" cases are *thirst for low blood volume* with suppressed RAAS preventing the salt-craving signal. Self-protocol: **1.5 L/day [[oral-rehydration-solution]]** — sodium-glucose co-transport ≈ IV saline for blood-volume expansion (Meadow study cited). Created [[patrick-ussher]], [[peter-deen]], [[oral-rehydration-solution]], [[stress-for-health]].
- **#140 Jess Dove London** — founder of **[[turnto-app]]**, daily-health-breakthrough mobile aggregator launched April 2024 (LC + ME/CFS communities just brought online). Logged as `mentioned_only` — information infrastructure, not a treatment.

Batch-level signals:

- **The treatment-trial pipeline is now structurally readable on the wiki** with three parallel arms: (1) **antiviral suppression** ([[paxlovid-lc-trial]], [[gilead-antiviral-lc-uk]]) — viral-persistence story; (2) **immunomodulation** ([[rvlc-trial]] from #131) — persistent-immune-activation story; (3) **receptor blockade** ([[nicotine-patches]] hypothesis from #130 — pre-RCT, but hypothesised mechanism is clean and accessible). Multiple guests this batch note these are likely to converge into combination protocols downstream.
- **Mind-Body therapy → practitioner-training** is now a recognisable sub-pattern across recoveries (Jules #138 + Lorrie #70/#137 + arguably Esther #32). The training itself becomes therapy — coaches who completed their own recoveries treating other patients, with the training period providing a structured re-entry to cognitive load.
- **HRT in perimenopausal LC** is now a logged signal at the patient level. Eric is not the demographic but the wiki should track this as a sub-pattern given the perimenopause + LC overlap is large.
- **Movement-readiness vs movement-prescription** is now operationally clear: Anderson's **RV CAMPING** check is the missing piece that resolves the long-running Graded Exercise contradiction. Same intervention category, opposite outcomes — discriminator is whether upstream conditions (breathing, MCAS, metabolic intake, autonomic stability) are in place.
- **ORS / sodium-glucose co-transport vs salt-on-food** — Ussher #139 closes a question that has been latent since the early POTS episodes (#40 Boon Lim, #66 Stiles, #57 Sanjay Gupta). ORS is significantly more efficient than salt-on-food for blood-volume expansion. **Eric-actionable**: try Dioralyte experimentally on heat days or near-crashes.
- **Acid-base / acidosis frame (#134)** is the wiki's first unifying-mechanism theme that explicitly bridges breathing, mitochondria, microclots, hypoxia, ME/CFS lactate findings. Pre-test, but worth tracking — the testing plan is straightforward.
- **The "primary polydipsia → ME/CFS misdiagnosis" thread (#139)** is the wiki's strongest clean example of [[healthcare-gaslighting]] — a literally life-threatening misdiagnosis caused by a 1959 psychogenic frame that hadn't updated despite the discovery of the hypovolemic thirst centre in 1968. Worth knowing if Eric or anyone in his network ever encounters extreme thirst symptoms.

**Eric-relevant takeaways**:

- **#130 Leitzke** — transdermal nicotine is cheap, OTC, mechanism is clean (nAChR competition with spike). Logged as a low-cost candidate intervention worth tracking; not Eric's first move but worth knowing about.
- **#131 Wes Ely / RVLC** — strongest immunomodulation arm in the trial pipeline. Watch for results ~2027–2028. Eric not a candidate (his stack works); track for future.
- **#135/#136 Meg Anderson** — RV CAMPING + resting-HR-plus-15-20-bpm ceiling are the cleanest practical exercise framework on the wiki. Eric's pacing/movement plan should align with this.
- **#138 Jules Rogers** — HRT for perimenopausal LC is real signal; Eric not a candidate but useful knowledge for his network.
- **#139 Ussher / ORS** — Eric should experiment with **Dioralyte** as a more efficient sodium-delivery path during heat days / near-crashes vs salt-on-food.

## [2026-05-04] checkpoint | episodes 130-140 ingested (90 of 211; #31 missing transcript)

## [2026-05-04] ingest | batch #141–#150

Indexed 10 consecutive episodes covering Q3–Q4 2024 LC content. **Two more full recoveries** added (now 17 on wiki), the wiki's first comprehensive PEM-physiology episode, the first comprehensive sleep-medicine episode, the first clinician-side anchor of the neuroplastic-symptoms model, and the cleanest articulation of recovery-as-resilience we've logged.

Per-episode summary:

- **#141 Todd Davenport** — DPT, Workwell scientific advisor. **Anchor PEM episode.** ICC term *postexertional neuroimmune exhaustion*; **plug-in hybrid car analogy** (credits Chris Snell — aerobic = gas motor, glycolytic = battery, PEM = broken gas motor); **2-day CPET** with VAT drop on day 2 as **gold-standard PEM biomarker** (unfakeable); **energy envelope** (credits Leonard Jason); pacing as a discipline of balancing activity with rest; "beware the clinician who has you hop on the treadmill on a good day." [[bateman-horne-center]] crash care plan as canonical document. Created [[todd-davenport]], [[2-day-cpet]], [[bateman-horne-center]]; substantial rewrite of [[post-exertional-malaise]]; updated [[workwell-foundation]], [[pacing]] (with Jason credit), [[graded-exercise]] indirectly.
- **#142 Jackie host-solo** — 3-year anniversary; perfectionism in recovery; balance / self-care framing.
- **#143 David Joffe** — Australian respiratory + sleep specialist. **Anchor LC sleep episode.** SWS vs REM physiology; **dopaminergic injury** under-weighted in LC research (more restless legs in women, more PTSD/depression/narcolepsy); **REM sleep without atonia / REM behaviour disorder** showing up in young LC patients (historically a 60–65 yr old men's condition with 80% Parkinson's progression at 14 years); **slow-release melatonin 2 mg at 7 pm** protocol; vagal-axis breakdown ("LC absolutely monsters the vagus nerve"); CO₂-chemoreceptor disturbance; gut–sleep coupling; lab polygraphic study as irrefutable EEG biomarker. Created [[david-joffe]], [[sleep-disturbance]], [[slow-release-melatonin]].
- **#144 Dr Sarah** — UK GP/dermatologist. **16th full LC recovery on the wiki.** **Freeze response** (HR 40, low BP) — wiki's clearest articulation of LC-as-freeze (vs sympathetic-overdrive). **Six-pillar mental scaffold** (NS-regulation / nutrition / sleep / hormones / movement / mindset). **HRT slow-titrate over a year** for perimenopause overlap — second positive HRT row from a recovered patient. **Lightning Process at ~30%** as self-limiting-belief lever (helped_partial). **Cold water harmed her** — strongest harm signal on the cold-water page; freeze-state body may not benefit from cold shock. Snowdon climb as recovery marker. Created [[dr-sarah]], [[recovery-stories/dr-sarah-recovery]]; updated [[lightning-process]], [[suzy-bolt-recovery]], [[yoga-for-life-project]], [[hormonal-dysfunction]], [[cold-water-exposure]].
- **#145 Jenny Adams** — recovered ME/CFS coach (12 yr arc, glandular fever 2006 → ~2019 substantive recovery). **17th full recovery on the wiki.** Trauma stack + abusive-relationship pattern + ADHD-burnout (now diagnosed). Recovery via Pilates-in-chronic-illness-friendly-studio + vegan diet + talk therapy + boundary work. Now uses **Internal Family Systems / Dick Schwartz / *No Bad Parts*** post-recovery for everyday dysregulation. Trained in **compassionate inquiry** (Gabor Maté). Wiki's first **ADHD-burnout → ME/CFS** sub-pattern flag. Created [[jenny-adams]], [[recovery-stories/jenny-adams-recovery]], [[heal-good]], [[ifs-therapy]].
- **#146 Dr Becca Kennedy** — US family medicine, **ex-Kaiser Permanente long-COVID-clinic lead**, founder Resilience Healthcare. **Anchor neuroplastic-symptoms episode from the clinician side.** **30–50% of standard primary-care visits** = neuroplastic / medically-unexplained symptoms. **"Damage is the wrong word; changes are reversible."** Schubiner / Lumley **EAET** + Pennebaker **expressive writing** as primary tools. Pandemic-as-worldwide-trauma framing. Created [[becca-kennedy]], [[resilience-healthcare]], [[howard-schubiner]], [[eaet]], [[expressive-writing]].
- **#147–#148 Dan Neuffer** — return appearance ~12 months after #102. Two-parter. Pt 1: "looking too low on the tree"; cures-don't-exist; viral-onset reframe; cultural-critique tangent on modern fragility; responsibility-vs-blame distinction. Pt 2 anchors **recovery-as-resilience-not-Nirvana** and the **illness-as-solution-not-problem** reframe; militant self-prioritisation; **60–80% danger zone** observation; pain-then-pleasure motivation; recovery-moment markers (grocery shopping; Jackie's car-in-ditch). Per CLAUDE.md "same speaker, same intervention, same outcome → one row" rule, ANS Rewire evidence log not duplicated; episode list updated. Updated [[dan-neuffer]], [[ans-rewire]].
- **#149 Eleanor Stein** — Canadian psychiatrist, ME 35 yrs personally + 25-year clinical career. **Anchor self-management-as-biology episode.** Neuroplasticity = 100-year-old science; "damage is the wrong word, changes are reversible" (independent convergence with Kennedy #146). **Two-question filter "imminently dangerous? familiar?"** for symptom flares. Top tips: **sunlight + cave-person sun-cycle + eat-real-food + recovery-mindset**. Wearables nuanced (HR pacing yes; sleep-stage data unreliable for disrupted-sleep patients; obsessive personality should not get one). Introduces **quantum biology** + **Eric Gordon (cell-danger response)** as new threads worth tracking. Created [[eleanor-stein]], [[self-management]] theme.
- **#150 host-solo** — episode-150 milestone. Listener-question follow-up to #147 on identifying-pre-illness-patterns-without-blame. Buddhist **two-arrows** analogy (the insult + your reaction); seven-step breakdown of how Jackie worked through self-blame; Maya Angelou + Paulo Coelho closing quotes.

Batch-level signals:

- **The neuroplastic-symptoms model is now anchored from three independent angles**: Kennedy #146 (clinician), Adams #145 (post-recovery patient using IFS), Stein #149 (clinician with lived experience). All converge on "damage wrong, changes reversible." Different vocabularies (neuroplastic symptoms / IFS / self-management-as-biology) → same operative target: re-train the over-protective nervous system.
- **The recovery-as-resilience-not-Nirvana frame (#148)** is the wiki's strongest articulation of what "recovered" actually means — not symptom-free in cotton wool, but a body that handles normal life stressors without crashing. The **60–80% danger zone** is the most actionable framing on the wiki for plateaued patients.
- **HRT-in-perimenopausal-LC is now n=2 from recovered patients** (Jules #138 + Sarah #144). Sub-pattern firming up; not just one anecdote.
- **Cold-water-exposure now has its strongest harm signal** (Sarah #144) — and the discriminator may be **autonomic substate**: freeze-response patients may be harmed where sympathetic-overdrive patients benefit. New nuance worth tracking on subsequent cold-water rows.
- **PEM physiology now has its own canonical anchor** — #141 Davenport. The wiki's energy-envelope / plug-in-hybrid / pacing-as-discipline language now has named sources (Jason, Snell, Workwell).
- **Sleep is now properly anchored** — #143 Joffe. The dopaminergic-injury thread is wiki-new and clinically serious (REM behaviour disorder in young LC patients).
- **Recovery-story pattern**: of 17 full recoveries on the wiki, **at least 12 explicitly name multi-component approaches** (no monotherapy). Patterns repeating: nervous-system regulation + community + safe movement + dietary tweaks + mindset work. Sub-patterns: brain-retraining (LP / Curable / ANS Rewire) appearing in 8/17; Suzy Bolt program in 5/17; yoga / breathwork in most.

**Eric-relevant takeaways**:

- **#141 Davenport** — Eric's existing pacing should map cleanly onto the energy-envelope frame. The 2-day CPET is not Eric-relevant for use (he's stable) but the **VAT-as-objective-PEM-marker** matters if he ever has a PEM-relevant clinical question. **Bateman Horne crash care plan is worth downloading** as a kit-prep document.
- **#143 Joffe** — Eric does not have major LC-attributable insomnia, so **slow-release melatonin 2 mg at 7 pm** is below-threshold but worth knowing. The **REM-behaviour-disorder warning** is the single thing Eric should know — if ever he hears about himself acting out dreams, get a sleep study.
- **#144 Dr Sarah** — Sarah's **freeze response** is *not* Eric's pattern (he's POTS / sympathetic overdrive), but the **six-pillar mental scaffold** is a useful audit framework Eric can run against his own stack.
- **#145 Adams** — **Internal Family Systems** is now logged as a tool worth pointing at if Eric ever wants a vocabulary for everyday dysregulation different from brain-retraining. Vegan diet = N=1; not pushed.
- **#146 Kennedy** — **EAET / expressive writing** are contained-experiment tools Eric could try without changing medication or pacing protocol.
- **#147–#148 Neuffer** — **60–80% danger zone** is a real signal Eric should track. Easy to settle at "well enough" and stop pushing on the recovery work. **Pleasure-motivation** (what would 100% feel like?) is the engine he needs once pain has dropped below threshold.
- **#149 Stein** — **Sunlight, eyes open, no sunglasses, multiple times a day** is a free contained experiment. **"Imminently dangerous? Familiar?"** filter is operationally useful for daily symptom-noticing without becoming hypervigilant. **Rest = horizontal, eyes/ears closed, no Netflix** — Eric should consider whether his "rest" is actually cognitively load-bearing.
- **#150 host-solo** — **two-arrows** framing for self-blame moments. **"What would I say to a friend?"** test as a contained self-compassion exercise.

## [2026-05-04] checkpoint | episodes 141-150 ingested (149 of 211; #31 missing transcript)

## [2026-05-04] ingest | #151–#161 — batch (10 episodes; #157 missing transcript)

Episodes #151–#161 ingested in one batch. Per-episode highlights:

- **#151 Dr Lydia Knutson** — US chiropractor, Cambridge MA, 24+ years practice. **Anchor chiropractic-protocol-for-LC episode.** Created the **Axial Stability Method (ASM)** — low-force chiropractic + Eastern Energy Medicine adapted for LC summer 2020. **Open-label n=13 study tracking 40 symptoms: 90% reduction in severe-symptom severity in average 18 visits; ~70% reduction in phase 1 alone (8 visits, parasympathetic / upper-cervical work).** Three-phase sequence: parasympathetic → sympathetic (thoracic concordances mapping organ systems) → biomechanical. **Rain-barrel framing** for predisposition (echoes Perrin's iceberg). 150+ LC + post-vaccine patients treated. Created [[lydia-knutson]], [[axial-stability-method]].
- **#152 Jenny Adams** — return appearance after #145, recorded **deliberately unedited as a perfectionism exercise**. **Anchor perfectionism + ADHD episode.** **Perfectionism as a trauma response** (Gabor Maté lineage). Live compassionate-inquiry demo on Jackie traces the belief from teenage years (*if I do x, y, z perfectly, then I will be loved / accepted / safe*). Introduces the **90-second emotion-wave**. ADHD-burnout pipeline anchor; *"probably 80% of women with chronic illness in my client base have undiagnosed ADHD."* Adams's own ADHD assessment scheduled the week of recording. Per CLAUDE.md same-speaker rule, no recovery-row duplicates. Created [[perfectionism]] theme.
- **#153 Dr Amir Hadanny** — Israeli physician (neurosurgery + hyperbaric medicine since 2008; bioinformatics PhD). **Anchor RCT-evidence HBOT episode for LC** (pairs with [[096-dr-masha-makeeva-hbot]]). **Aviv LC RCT (n≈90, sham-controlled, double-blind)**: subjective + objective MRI/fMRI/SPECT + cognitive-battery improvements; **18-month sustained gains** (counter to "feels good then fades" critique). **"Covid horns" imaging signature** — orbital-frontal + temporal-pole + hippocampal metabolic deficits mapping to cribriform-plate viral entry. Established LC (>6mo) needs 60 sessions, not 40. Oxygen-fluctuation protocol mechanistic key (interval training for mitochondria). Created [[amir-hadanny]], [[hbot-lc-rct-aviv]] trial page; updated [[hbot]].
- **#154 Sean Moran** — Australian, recovered ME/CFS over **~10–12 year arc** (April 2012 → ~2022). **18th full recovery on the wiki.** Distinctive shape: **mould + heavy metals + MARCoNS sinus colonisation + dental cavitation** as the load-bearing stack — *not* nervous-system-primary recovery. **First MARCoNS recovery anchor on the wiki** (30-day protocol from a US recovered-practitioner; cleared chronic biofilm sinus colonisation; "my brain just started to switch on for the first time in 9–10 years"). **First explicit dental-extraction-as-step-change** (infected tooth removed, woke up the next morning with step-change in physical + cognitive energy). **Christopher Shade / Quicksilver Scientific lineage detox** (slow drainage-funnel-first; DIY without practitioner supervision was actively harmful). Mould remediation triggered the detective phase (covid-lockdown WFH AC unit was the chronic exposure). Pre-2020 "kitchen sink" phase logged as `mentioned_only` for the long list of modalities he tried without clear effect. Created [[sean-moran]], [[recovery-stories/sean-moran-recovery]], [[heavy-metal-detoxification]], [[marcons-protocol]].
- **#155 Nadyne McKie** — UK psychotherapist + yoga therapist + breathing coach; recovered LC + son had paediatric LC + co-authored book on convalescence with [[fiona-agombar]]. **Anchor convalescence-and-self-compassion practitioner episode.** First wiki-explicit naming of **screen apnoea** (shallow breath / breath-holding while scrolling). Movement-not-exercise reframe (exercise as distraction-from-emotion). Yoga therapy as Invitational not corrective ("the right way is the way that is right for you"). "I would never speak to a friend the way I speak to myself." Created [[nadyne-mckie]], [[recovery-stories/nadyne-mckie-recovery]].
- **#156 Nadyne McKie (return)** — **anchor paediatric-LC + caregiver-depletion episode**. First wiki articulation of **caregiver depletion as recovery-rate-limiter** via **NS-to-NS coupling**. Phased-school-return + PE-letter + advocacy patterns. **Believing-the-child as a long-term skill-teaching exercise** (not believing → child learns to ignore body signals → push-through pattern that recurs in adult recovery histories). "Just for now" framing matches Julie Black's "submit now ≠ accept forever." Son's recovery: long period off school, energy-management as central principle, supported by a believing NHS paediatric consultant (load-bearing). Created [[paediatric-long-covid]], [[caregiver-support]] themes.
- **#157** — missing transcript (no captions on YouTube). Skipped, per `_meta/failures.json`.
- **#158 Creativity 2024** — 4th annual creativity compilation (after #14, #65, #113). 8 contributors: Anna Bell (free-flow writing), Emma Major (digital painting + poetry; LC since 2020 + blind wheelchair user; book *Dora Vigilia*), **Olga's [[hibernation-sessions]]** (online-concert series for housebound community, founded autumn 2024 — wiki-new), Misty Brackett (process painter), Sally (retired nurse + LC art advocate; planning a May 2025 LC-artist exhibition), **Sarah** (moderate-to-severe ME, **housebound 90%**, watercolours from a day-bed; online shop + Zoom paint-with-me sessions — anchor for severe-cohort creative practice), Jade (LC since Dec 2023, learned crochet, runs *Living with Long Covid Jade* YouTube), and the **[[long-covid-choir]]** performing Brahms's *Wiegenlied*. Created [[creativity]] theme, [[hibernation-sessions]] program.
- **#159 Jackie's 2024 Reflections** — 11-min host-solo end-of-year wrap. Brief; journal-prompt response: "you are enough whether you do or don't"; "treasure yourself; respect yourself; you are worthy whatever you do or don't do." Plug for the new **virtual art-room** format in the LC creativity group (Zoom; ~40-min sit-and-create). Reaffirms perfectionism-as-recovery-blocker with no new evidence-log rows. Created [[long-covid-creativity-group]] program.
- **#160 Dr Raymond Perrin (pt 1)** — Manchester osteopath + neuroscientist. **Anchor lymphatic-drainage / Perrin Technique mechanism episode.** **35-year hypothesis-to-validation arc**: 1989 single-patient observation → 2005 PhD → 2012 mouse drainage proof → 2017 BMJ ~85% diagnostic accuracy from physical signs → September 2024 Oregon real-time gadolinium-dye human glymphatic visualisation (one month before recording — the proof Perrin had been waiting for). **Cribriform plate as covid entry route + main brain drainage exit** (matches Hadanny #153 from a different treatment angle). Hypothalamic + locus-coeruleus toxin accumulation + sympathetic dysfunction as the LC mechanism. Mid-thoracic spinal flatness + megalymphatics / varicose lymphatics as palpable physical signs. Heavy-metals magnet observation logged but flagged as preliminary / not externally replicated. Created [[raymond-perrin]], [[perrin-technique]], [[glymphatic-drainage]] theme.
- **#161 Dr Raymond Perrin (pt 2)** — Treatment side. **Concertina + siphon effects** of gentle hands-on cranial + thoracic + chest + face/neck massage + spinal mobilisation + breathing exercises. **2023–24 NHS feasibility study** of self-massage routines on 100 LC patients: **79% completion rate**. Self-massage protocols **free on perrintechnique.com** (no subscription) — Perrin emphasises this as democratised access. **Jigsaw-puzzle framing**: rest/relaxation/meditation/pacing as corner pieces; lymph-drainage as edges; supplements/nutrition/etc. as middle pieces; *start with the corners*. Created [[perrin-technique-nhs-feasibility]] trial page.

Batch-level signals:

- **The low-force-bodywork-for-LC family is now anchored from three angles**: Knutson's ASM (chiropractic, ANS rebalancing via spinal substrate), Perrin's technique (osteopathic, glymphatic drainage targeting), and existing cranial-sacral therapy (#48, gentle parasympathetic-supporting touch). All three converge on ANS rebalancing via gentle hands-on work; mechanism stories differ. None has RCT-level evidence equivalent to Hadanny's HBOT trial; all three should be tracked as a *family*.
- **Cribriform-plate convergence**: Hadanny (#153) and Perrin (#160) independently anchor the cribriform plate as the LC viral entry route. Hadanny treats the wounded brain tissue downstream (HBOT); Perrin treats the drainage that lets toxins clear out. Distinct interventions targeting the same neuroanatomical bottleneck — first time the wiki has a clean two-mechanism framing for the same anatomical site.
- **Perfectionism is now anchored from the trauma-response angle** (#152 Adams) on top of the existing "perfectionism as recovery-blocker" framing (#94, #142). Pairs with [[trauma-and-illness]] + [[self-compassion]] as a stack to address before / alongside / after specific interventions. The 90-second emotion-wave is the cleanest single tool the wiki has surfaced for working *through* (not around) discomfort.
- **The recovery-pattern landscape now has more shape variance**: of 18 full recoveries, **at least 12 explicitly name multi-component approaches** (still the dominant pattern). Sub-patterns now visible:
  - Brain-retraining + somatic + community (Suzy Bolt + Curable + ANS Rewire) — most common.
  - Mind-body / TMS / EAET — secondary.
  - **Mould + heavy metals + chronic infections + dental** (Sean Moran #154) — first wiki representation of this shape.
  - HRT-in-perimenopause (Jules #138 + Sarah #144) — second-tier.
  - Pre-existing ME/CFS framework adapted (Sarah Lotus Path + Sophie Reynolds + Pamela Rose) — second-tier.
- **Caregiver perspective is now anchored** (#156) — first wiki articulation of caregiver depletion as a recovery-rate-limiter. Builds on [[011-iain-partner-with-chronic-illness]] (the partner-as-carer founding episode).
- **Paediatric LC** is now a wiki-explicit theme. Three episodes anchor it (#61 Rosie + #65 LC Kids Choir + #156 Nadyne); recurring patterns: cognitive-load-dominant energy expenditure, advocacy load on parents, and the long-term consequence of teaching kids to ignore body signals.

**Eric-relevant takeaways**:

- **#151 Knutson** — ASM is currently US-only and Cambridge-MA-clinic-only for full practitioner-delivered protocol. **The hierarchy-of-systems sequence** (parasympathetic → sympathetic → biomechanical) is a useful framing for any low-force-bodywork Eric considers; it's not contingent on Knutson specifically. The "treatment vs practice" distinction (ASM is treatment; brain-retraining + breathwork are practices) matters — they're complementary, not substitutes.
- **#152 Adams** — **The 90-second emotion-wave** is a contained tool Eric can run as a daily practice without changing medication or pacing. When the discomfort arises (frustration, fear, sadness), name it, sit with it for ~90 seconds, breathe; the wave usually passes. Pairs with the "what would I say to a friend?" exercise from #150.
- **#153 Hadanny** — **HBOT remains a candidate** but Eric's autonomic / POTS-dominant phenotype isn't the orbital-frontal-cognitive-deficit phenotype the Aviv RCT enrolled. Imaging-first selection would inform whether it's worth the investment for him. **MS Charity UK at £15/session (from #96)** is still the cheapest UK access if it ever becomes a candidate.
- **#154 Sean Moran** — **MARCoNS + dental + mould** are worth a one-time check for Eric. He doesn't have a clear mould exposure history, but a baseline MARCoNS swab (if accessible) and a dental review would be cheap-and-low-harm checks. Heavy-metal panel could be considered if other paths plateau. Don't DIY any detox protocol.
- **#155–#156 Nadyne** — **Screen apnoea** is the single contained behavioural lever Eric can run for free starting today: notice your breath when you're scrolling / doing online work; insert micro-breaks; orient eyes off-screen for 30s. Compounds with the breathing tools Eric is already using.
- **#160–#161 Perrin** — **Free self-massage routines on perrintechnique.com** are a contained experiment for Eric — daily home practice, no cost, low harm. Pair with breathing exercises (already in his stack). The **jigsaw-puzzle framing** is operationally useful: rest/relaxation/meditation/pacing are non-negotiable corner pieces for Eric (mostly already in his stack); specific interventions like ivabradine + mestinon + florinef are middle pieces. Whether the Perrin Technique (or ASM, or HBOT) ever becomes a candidate, the corners stay the same.
- **#158–#159 Creativity** — Eric can engage the [[long-covid-creativity-group]] / virtual art room as a low-cost, low-energy practice without disrupting any current protocol. Useful pacing-friendly identity-substrate move beyond his current activities.

## [2026-05-04] checkpoint | episodes 151-161 ingested (159 of 211; #31, #157 missing transcripts)

## [2026-05-05] ingest | episodes 162-171 (10 episodes)

- **#162 Carrie Bailey (pt 1) — functional nutrition + interconnected body** — US functional nutritionist; root cause = **pathogens + toxins**; LC reactivates latent EBV/shingles/H.pylori/parasites/mould; insufficient stomach acid; liver fat-burdened (contrarian thesis: less protein, less fat, more fruit + veg); food-combining (no fat with sugar/starch); long carnivore/low-FODMAP diets short-term only; pathogen-die-off reframing for food reactivity. Created [[carrie-bailey]] person page.
- **#163 Carrie Bailey (pt 2) — supplements + elimination diets** — Foundational supplement stack: B12 (high-dose, 5,000 μg), magnesium glycinate, **buffered vitamin C** (NOT GMO ascorbic acid), zinc sulfate, lysine 2g BID, lemon balm + cat's claw alcohol-free tinctures. **Citric-acid avoidance** distinct from citrus (GMO-corn flavour enhancer hidden in jarred tomatoes / condiments / supplements). Vitamin-D scepticism (minority position). CBC-with-differential reading rules. Drop-by-drop titration for super-sensitive patients. Contributes harm-row to [[low-histamine-diet]] (avoid-by-category misapplication) + harm-row to [[low-fodmap-diet]] (long-term misuse).
- **#164 Clayton Powers — listening + validating** — US PT specialising in ME-CFS / POTS / LC; BHC affiliate; trained under [[todd-davenport]] / Workwell lineage. Listening + validating = treatment. PEM-screening-first. **Recharge-faster strategies** — cold packs / pneumatic compression / IV saline / supplemental O2 (PEM-crash recovery menu wiki-new). Telehealth advocacy + post-pandemic Medicare reimbursement rollback. **Disabled-parking sign-off** within Utah PT scope. Visible / Lumia Health / Apple Watch / Garmin as starter HR-pacing scaffolding. Education-as-treatment via BHC YouTube + family-share videos. Created [[clayton-powers]] person page; updated [[bateman-horne-center]] + [[visible]] + [[iv-saline]] + [[ice-packs-temperature]].
- **#165 Lizzie's Recovery** — UK ex-triathlete; July 2022 covid → ~2-year recovery. **19th full recovery** on the wiki. Inflection: **Jan Rothney's book** *Breaking Free from Long Covid and Chronic Fatigue* + **Curable**. Specific named techniques: language-shift ("I feel less energised than I would like"), **amygdala pep talk** mantra ("I am safe. Thank you body…"). **Step-counting harm story** — 1,000-step ceiling triggered fight-or-flight + new palpitations she didn't have before; her interpretation: threshold-anxiety as the iatrogenic mechanism. Therapy as post-recovery integration step. Created [[lizzie-recovery]] recovery story + [[jan-rothney]] author page; updated [[curable-app]] + [[mind-body]].
- **#166 Rebecca Tolin — "I'm Not Broken"** — US ex-broadcast-journalist; **13-year ME/CFS** recovery — **longest documented detour through biomedical model on the wiki**. Trauma-related onset (sexual assault → cluster of viruses → mecfs). 50+ doctors / IV antivirals / 3-year carnivore detour. Inflection: 3-hour conversation with recovered layperson "Kathy" who explained the Sarno/Schubiner framework. **Somatic tracking** as core daily practice (wiki-new as standalone term). Inner-emotional work + **TMS personality traits** (perfectionism, people-pleasing, holding-in-emotions, goodist) as targets. **Self-compassion** as antidote. Created [[rebecca-tolin]] person + [[rebecca-tolin-recovery]] recovery story + [[somatic-tracking]] intervention; updated [[howard-schubiner]].
- **#167 Dr Jacob Teitelbaum (return, ~2.5 yr after #55)** — Less time on SHINE walkthrough; more on symptom-targeted layers added since: **PEA (palmitoylethanolamide) 1,200-2,400 mg/day for brain pain + central sensitisation + MCAS sensitivities** (cites 350+ pain studies, recent disc/compression study ~70% pain reduction); **PEA 1,200 mg + Luteolin 70 mg × 3 months for smell/taste loss**. **HRG80 red ginseng** updated study (n=188; 60% improved; ~61% energy; half-chewable cuts cost 75%). **B2 riboflavin 400 mg × 6 weeks → ~70% migraine reduction**. Pain taxonomy (~7 named types). TBI/concussion → 44% hypothalamic-pituitary dysfunction parallel. ANS Rewire / Gupta / DNRS endorsed. Created [[pea-luteolin]] intervention; updated [[jacob-teitelbaum]] + [[shine-protocol]] + [[hrg80-red-ginseng]] + [[ans-rewire]] + [[gupta-program]] + [[dynamic-neural-retraining-system]].
- **#168 Rachael — Rebound Method (return, ~1 yr after #127)** — Membership grown to ~30 active. Codified the **Baseline Formula** (wiki-new program): three components = isolation-exercises movement modality + "could-I-repeat-daily" handbrake dosage + predictable progressions on flexible time. Mindset prerequisite: **consistency over progression**. **Cochrane re-review history** wiki-new (2020 review challenged on flawed control groups + ignored harm signals; subsequent re-analyses found GET harmful for >50% of ME/CFS participants; NICE pivoted). **Mitochondrial dysfunction → exercise intolerance** mechanism story now linked to a concrete prescription protocol. Training for Brighton Marathon. Created [[isolation-exercises]] + [[baseline-formula]]; updated [[rachael-rebound-athletic]] + [[rebound-athletic]] + [[graded-exercise]].
- **#169 Five Themes for Recovery (host-solo Q&A)** — Jackie's articulated meta-framework: **consistency / mindset / understanding / strategies / healing environment**, overarching theme = empowerment. Brain-retraining (Curable / Gupta / DNRS / ANS Rewire) named as common-but-not-universal piece of recovery stacks. Dr Sarah's "stress-bath vs healing-bath" framing reused. First wiki anchor for Jackie's own meta-framework — operational synthesis of the wiki's recurring patterns.
- **#170 Amy Mooney — Flipping the Iceberg** — US OT (~25 years, paediatric / sensory-integration); 10 years primary caregiver for 9-year-old daughter who developed ME/CFS. **First wiki anchor for OT-side LC perspective.** Iceberg metaphor — disease lives below the waterline (in PEM + recovery, not performance). **Aggressive rest** as the load-bearing intervention — **deliberate sensory + cognitive + somatic deactivation** (eye masks, weighted blanket, **Sensate** vibration tool, joint-compression-without-exertion, ear plugs). **Pre-emptive vs recuperative rest** with pre-arranged support kits. **Exertion buckets** (physical / cognitive / sensory / social-emotional). **3-day delayed-PEM window**. "Occupation = roles, not job." Created [[amy-mooney]]; updated [[radical-rest]] + [[ice-packs-temperature]] + [[bateman-horne-center]].
- **#171 Aaron West — Light Switch Recovery** — US IT manager + film enthusiast; Fall 2021 covid (Delta) → **light-switch recovery via Omicron reinfection + Paxlovid on Jan 5 2024**, after 2.5 years of LC. **20th full recovery on the wiki, first reinfection-as-healing anchor**. Pre-recovery stack: antihistamines (Zyrtec + Pepcid + Claritin) + beta-blockers + benzodiazepines (tapered post-recovery) + HR-ceiling-paced walking under 100 bpm. Severe insomnia (14h scattered over 24h), GI dysfunction (daily vomiting), altered taste (everything tasted *amazing* → poor eating habits). Cognitive rebound to *better than pre-illness* on creative tasks (writing book on A24 film label). His doctor confirmed light-switch recovery; said had seen this "a couple of other times" in 20-year practice. Aaron caveats explicitly — *"don't go out to get covid"*. Confounded data point — variant + Paxlovid + accumulated stack + immune reset. Created [[aaron-west-recovery]]; updated [[antihistamines]] + [[beta-blockers]] + [[famotidine-pepcid]] + [[paxlovid]] + [[walking]] + [[reinfection]].

Batch-level signals:

- **The mind-body / nervous-system route now has 4 new wiki anchors** (Lizzie #165, Tolin #166, plus reinforcement from #169's host synthesis): the dominant pattern across recovery stories on the wiki. The pattern looks identical from clinician-side ([[howard-schubiner]] / [[becca-kennedy]] #146), patient-side ([[032-esther-recovery-story]], [[109-julie-black-recovery]], [[127-rachael-recovery-story]], [[145-jenny-adams-recovery]], [[165-lizzie-recovery]]), and recovered-coach-side ([[166-rebecca-tolin-not-broken]]). The wiki is now well into "this is the dominant lineage" territory; the question of *how* to do the work has converged on **somatic tracking + inner-emotional work + self-compassion + brain-retraining-program-of-choice + mindset-shift-around-belief**.
- **The "movement-not-exercise" lineage gained its first codified protocol** — Rachael's Baseline Formula (#168). Until now the wiki had philosophy ([[047-darren-brown-long-covid-physio]], [[051-darren-brown-disability]], [[141-todd-davenport-pem]], [[155-nadyne-mckie-kindness]]) but no concrete prescription; now it has both. Pairs operationally with Mooney's OT-side aggressive rest (#170) — same family, different angle.
- **Cochrane re-review history is anchored** — #168 explicitly cites the 2020 Cochrane GET review being challenged + the subsequent re-analyses finding harm in >50% of ME/CFS participants + NICE pivoting. This is the answer to "but Cochrane said GET works for ME/CFS" that the wiki now has on file.
- **Reinfection theme is now bidirectional** — #171 introduces the rare third pattern (reinfection-as-healing) alongside the two existing ones (reinfection-as-relapse [[037-dr-asad-khan]], reinfection-as-fear-trap [[077-suzy-bolt-reinfection]]). Aaron West's recovery is rare, confounded, not engineerable — but now logged.
- **"Recharge-faster strategies" for PEM crashes** — Powers #164 contributes a tactical menu that the wiki had only fragments of: cold packs / pneumatic compression / IV saline / supplemental O2. Pairs with Mooney's aggressive rest as **proactive (pre-emptive) + reactive (recuperative)** crash management.
- **Functional-nutrition / pathogen-and-toxin frame** anchored from a new clinician (#162-163 Bailey) — adjacent to Lorrie Rivers (#70) but more clinically grounded; logged as a minority position with practical takeaways (food combining, lysine, B12, citric-acid avoidance) that don't require buying into the whole frame.
- **Recovery-story count: 20** — Aaron West (#171) the 20th. The pattern map continues to be dominantly multi-component; mind-body lineage strongly represented; reinfection-as-healing is the new outlier.

**Eric-relevant takeaways**:

- **#162-163 Bailey** — *low-cost contained experiments worth considering*: **lysine 2g BID** (first-amino-acid-depleted under viral load); **buffered vitamin C** (not GMO ascorbic acid) at the dose Eric currently uses or higher; **citric-acid label-reading** for any histamine-reactive day. Vitamin-D-scepticism is a minority position; not actionable. Bailey's whole frame ≠ peer-reviewed; treat as a practitioner perspective with some defensible tactical components.
- **#164 Powers** — **Pneumatic compression for PEM crash recovery** is wiki-new on Eric's menu; cold packs on neck (already in Eric's vocabulary from #60 Reema and #170 Mooney) reinforced. The "energy money / shower-cost ($100 standing vs $40 sitting vs $20 sponge-bath)" framing is a useful mental tool.
- **#165 Lizzie** — **Amygdala pep talk** + **language-shift** (Curable / Rothney) are zero-cost daily practices Eric can layer onto breathwork. *Step-counting harm story is a useful caution* — threshold-anxiety is itself a stressor; Eric is lower-risk here (not wearable-driven) but worth holding as a frame.
- **#166 Tolin** — **Somatic tracking** is a contained free practice Eric can layer on top of breathwork. The "I'm not broken" reframe is operationally significant — POTS + PEM are dysfunction, not damage. Pairs with [[149-eleanor-stein]] and [[146-dr-becca-kennedy]] independent convergence on the same line.
- **#167 Teitelbaum** — **PEA (palmitoylethanolamide)** is the most concretely-actionable wiki-new item: contained, cheap, low-harm, specific evidence base. Eric's pain load is light, but if neuropathic / mast-cell sensitivities emerge, this is the first item to try. **HRG80 half-chewable** is contained low-cost trial. **B2 riboflavin** if migraines emerge.
- **#168 Rachael** — The **Baseline Formula** is the cleanest concrete framework Eric has yet seen for *how* to reintroduce strength work without the GET trap. Specifically: isolation exercises (clams, glute bridges, scapular work — many can be done lying-flat = POTS-friendly); volume Eric could repeat daily *if he had to* but actually does less; stay at baseline 2-6 weeks before any micro-progression. Eric's perfectionist / push-through pattern is exactly what consistency-over-progression targets.
- **#169 Jackie's five themes** — All five apply to Eric. **Strategy 4 explicitly anchors medications-as-bridges** — Eric's stack (ivabradine + mestinon + florinef + Zyrtec/Pepcid + bufomix p.r.n.) is *good*, not failed-recovery; they're the bridges. *Consume less LC content with multi-year-pessimism narratives* is operationally useful — pairs with Lizzie's same caution.
- **#170 Mooney** — **Aggressive rest** is operationally distinct from Eric's current rest practice. Worth experimenting with: eye mask + earplugs + weighted blanket / vibration tool in a deliberate rest session. **Recuperative-rest support kit** as a one-time setup project — pre-warmed bed, electrolytes, vibration tool, eye mask, smoothie ingredients ready, *decisions pre-made*. **3-day window** before declaring an activity "safe" — Eric should resist the temptation to scale up after a "fine" first day.
- **#171 Aaron West** — *Caveat first*: Aaron's recovery is rare and not engineerable. But Aaron's pre-recovery stack (antihistamines + Pepcid + beta-blocker + benzo) is structurally similar to Eric's (Zyrtec + Pepcid + ivabradine + mestinon + florinef) — *some validation that this stack is a reasonable bridge while the deeper recovery factors play out*. **Spoon theory + HR-ceiling pacing** got Aaron through 2.5 years.

## [2026-05-05] checkpoint | episodes 162-171 ingested (169 of 211; #31, #157 missing transcripts)

## [2026-05-05] ingest | episodes 172-181 (10 episodes)

- **#172 Jo Thomas — "Recovery Perfection"** — UK fatigue coach + nurse + NLP-trained, recovered from postviral POTS / chronic fatigue (2017 onset). New sub-pattern named: **"recovery perfection"** — patients improve, then become rigidly afraid of slipping back; rigidity itself prolongs fragility. Reframe: "test the waters" — your responsibility is the attempt; the body's response is *not* your responsibility. Created [[jo-thomas]]; updated [[perfectionism]] + [[pacing]].
- **#173 Diana Driscoll — POTS Care + Driscoll Theory** — US optometrist, recovered postviral POTS, 12+ years disabled. Founded [[pots-care]] clinic + Genetic Disease Investigators. **Driscoll Theory of inflammatory POTS**: high intracranial pressure (often missed on MRI) + parasympathetic acetylcholine deficiency + oxidation from chronic inflammation. Built [[parasym-plus]] (acetylcholine support) and [[nac-max]] (glutathione recycling). Refutes the autoimmune-receptor-blockade theory using nicotine-patch receptor-probe testing. **Estrogen-as-inflammatory-driver** mechanistic story for the female skew. Created [[diana-driscoll]] + [[pots-care]] + [[parasym-plus]] + [[nac-max]]; updated [[nicotine-patches]] + [[hormonal-dysfunction]].
- **#174 Uroš Čimžar — From Crisis to Rebirth** — Slovenian entrepreneur (47), LC after 2nd COVID Dec 2023, bedbound to recovered in ~10 months. **First independent recovered-patient testimony for the Long Covid Breathing course** (Jackie + Vicky). Recovery framed as 5 phases: calm NS → remove stressors → gradual exposure → leave sick-person mindset → integration. Inflection moments: Kristin Neff self-compassion meditation (cried for first time in years on session 3); 3 days of expressive writing dissolved 20-year emotion backlog. **Cold showers tried too soon — didn't work.** Created [[uros-cimzar]] + [[uros-cimzar-recovery]]; updated [[long-covid-breathing]] (1st recovered-patient row) + [[breathwork]] + [[yoga-nidra]] + [[expressive-writing]] (now key_to_recovery row) + [[somatic-tracking]] + [[eft-tapping]] + [[meditation]] + [[cold-water-exposure]] (timing-and-readiness no_effect row) + [[intermittent-fasting]] (new) + [[perfectionism]] + [[self-compassion]] + [[trauma-and-illness]].
- **#175 Jackie host-solo — Cold Water Immersion Deep Dive** — Jackie's authoritative deep dive answering the show's second-most-asked question. Cites Susanna Søberg's research, Mark Harper's *Chill* (#87). Two failure modes named: **starting too soon** (no stress-down strategies in place — you stress up but can't come down, straight to crash) + **staying in too long** (max benefits at 90s–2 min). Self-tests + safety + routine. Updated [[cold-water-exposure]] notes on Jackie's existing #64 row — same speaker, same intervention, same outcome → no new row, expanded notes per CLAUDE.md rules.
- **#176 Carl Robot — When Your Body Becomes a Stranger** — UK English teacher (Leeds, ex-PE-teacher Bristol), LC from mild summer-2020 COVID, A&E presentation 2021, diagnosed Feb 2023, recovered to running marathons by mid-2024. **Inflection: Sheffield Hallam University SymProve probiotic clinical trial** — 3 months active arm. Cognitive baseline put him in bottom 7% nationally. Continued via homemade kefir. **First wiki anchor for a probiotic clinical-trial recovery.** Created [[carl-robot]] + [[carl-robot-recovery]] + [[simprove-probiotic]] + [[simprove-trial-sheffield]]; updated [[cold-water-exposure]] + [[yoga-nidra]] + [[breathwork]] + [[long-covid-breathing]] + [[intermittent-fasting]].
- **#177 Rachel Rock — The Stool with Four Legs** — Boston-based journalist, LC May 2022, recovered to 86-mile PMC bike ride summer 2024 + cleared a reinfection in 2-3 days. **Recovery framework: ANS as the seat of a stool, four supporting legs** = (1) ANS practitioner [[dr-lydia-knutson]] — see #151; (2) functional medicine — allergies + supplements; (3) diet (keto then off keto); (4) **trauma processing via EMDR**. Striking observation: the bodily sensation in EMDR was *identical* to chronic-fatigue feeling. Multiple "fake recoveries" until reactivated viruses (EBV, herpes zoster, Lyme) addressed. Created [[rachel-rock]] + [[rachel-rock-recovery]] + [[emdr]] (new); updated [[acupuncture]] + [[safe-and-sound-protocol]] + [[keto-diet]] + [[mount-sinai-lc-clinic]] + [[trauma-and-illness]] + [[viral-persistence]].
- **#178 Alisha — Rebuilding Safety: Couch to Mountains** — US mountain-region farm worker, LC 2020/2021, couchbound 1.5 years, recovered via TMS / mind-body lineage. Inflection: Dan Buglio + Sarno — believing she wasn't broken. **Daily Rebecca Tolin somatic-tracking meditation** + **2 hrs/day self-Reiki at peak** (engaged her mind in something other than her health) + **smiling on purpose** (Buglio's safety-creation list) + **boundaries / empath learning**. **One session with [[rob-ensor]] (TMS coach) cleared her last lingering "detox sensations".** Now mind-body coach. Created [[alisha]] + [[alisha-recovery]] + [[reiki]] (new); updated [[somatic-tracking]] (now 2 key_to_recovery rows) + [[meditation]] + [[expressive-writing]] + [[tms-mind-body-syndrome]] + [[perfectionism]] + [[self-compassion]] + [[neuroplasticity]].
- **#179 Dr David Clarke — Decoding Your Body's Secret Language** — US gastroenterologist + internal-medicine consultant, 40+ years, **7,000+ patients personally diagnosed and treated** for brain-to-body / neuroplastic symptoms. President of **ATNS — Association for the Treatment of Neuroplastic Symptoms** (symptomatic.me). Estimates: 20% of adults; 40% of GP visits; >90% probability of neuroplastic condition if all diagnostic tests are normal. **ACEs framework** broadly defined ("anything that, if it happened to a child you love, would make you sad or angry"). Adult patterns: stressful personality traits + high-need partner choices + no time for joy + triggers + unrecognised emotions. **"Letters not to mail"** + **"imagine your child going through what you went through"** + **strong/heroic-self reframe** as the Olympic-weightlifter analogy. *Story Behind the Symptoms* podcast. Created [[david-clarke]] + [[atns-symptomatic]]; updated [[expressive-writing]] + [[trauma-and-illness]] + [[neuroplasticity]].
- **#180 Jules Rogers — Boundaries** — return guest (~1 yr after #138 recovery story). Now runs 6-week "Start Your Chronic Fatigue Recovery" course. Boundary taxonomy: physical / emotional / material / mental / time. **No is a complete sentence**; over-explaining is the trap. Holding-yourself-back-when-better is the hardest boundary. Mantra-as-deciding-question: "is this going to help me heal?". Same speaker reaffirming her existing recovery — **no new evidence-log rows added per CLAUDE.md** ("same speaker, same intervention, same outcome, different episode = update notes"); content captured in episode page + theme cross-refs only. Updated [[perfectionism]] + [[self-compassion]].
- **#181 Dr David Putrino — Multifaceted Approach** — Mount Sinai professor of Rehabilitation + Director of Rehabilitation Innovation. 6 centres including Center for Infection-Associated Chronic Illness (LC + ME-CFS + fibromyalgia + hEDS + chronic Lyme + vector-borne illness under one roof on purpose). **LC reframed as partly accelerated cellular aging** — opens metformin / low-dose rapamycin / NAD+ / oxaloacetate / CoQ10 / HBOT carry-over from elite-athlete + longevity science. **POTS subtypes matter** — hypertensive supine vs hyperadrenergic POTS need different drug stacks; wrong stack confounds clinical trials. **Modafinil for slow-wave-sleep-disrupted fatigue** (cites David Joffe #143). **Pax-LC trial failed primary endpoint** — paxlovid does not penetrate tissue where SARS-CoV-2 hides; subgroup analysis ongoing. **Testosterone may be protective** — paper under review with Iwasaki on hormonal patterns in LC; female skew may be partly testosterone-deficiency mediated. Patients arrive **malnourished** because they've cut every triggering food. Visible/Guava apps for data-driven pacing (with caveats). Created [[david-putrino]] + [[modafinil]] (new) + [[rapamycin]] (new) + [[oxaloacetate]] (new); updated [[mount-sinai-lc-clinic]] + [[paxlovid-lc-trial]] (status: failed; subgroup analysis ongoing) + [[paxlovid]] (no_effect row at population level) + [[breathwork]] + [[ivabradine]] + [[mestinon]] + [[hbot]] + [[metformin]] + [[nad-niacin]] + [[mitochondrial-dysfunction]] + [[viral-persistence]] + [[hormonal-dysfunction]] + [[pacing]].

Batch-level signals:

- **The mind-body / neuroplastic-symptoms route now has its anchor clinician.** Clarke (#179) gives the wiki a clinically rigorous account with 40 years' practice and 7,000+ patients — alongside the patient-side wiki anchors (Tolin #166, Esther #32) and the multi-component recovery-story routes (Lizzie #165, Jenny Adams #145+#152, Alisha #178). The framing has matured from "alternative perspective" to "well-documented diagnostic + treatment lineage."
- **Probiotic / gut-microbiome route now has a recovery-trial-grade anchor** — Carl Robot's SymProve clinical trial (#176) is the wiki's first single-patient probiotic recovery row tied to a controlled trial. Watch for the published trial outcome.
- **Cold water exposure timing-and-readiness thesis is now load-bearing.** Three episodes in this batch touch it: #175 (Jackie's deep-dive naming the failure modes), #174 (Uroš tried too soon — no_effect), #176 (Carl tried later in stable conditions — helped_partial). The wiki's 11 cold-water rows now show a clean signal: *cold water is not a beginner intervention, but at the right time can be a powerful late-stage amplifier*.
- **The Mount Sinai clinical apparatus + Pax-LC failure** (#181) re-anchors viral persistence as still mechanistically real but **paxlovid-shaped failure** confirmed at population level. The wiki's paxlovid page now logs no_effect at population level, with the open hypothesis that a circulating-spike subset (small percentage) may have benefited. **The therapeutic search needs to move toward tissue-penetrating antivirals.**
- **Recovery-story count: 24** — Uroš #174, Carl #176, Rachel #177, Alisha #178 added. Mind-body / nervous-system regulation lineage continues to dominate; #176 Carl's probiotic-trial inflection is an important counter-data-point.
- **Estrogen-as-inflammatory-driver (Driscoll #173) and testosterone-as-protective (Putrino #181) are two complementary mechanistic stories** for the LC female skew that the wiki had previously held only as observational ("women have higher inflammation"). Both are pre-RCT but now logged.
- **First wiki rows for**: [[parasym-plus]], [[nac-max]], [[reiki]], [[emdr]], [[modafinil]], [[rapamycin]], [[oxaloacetate]], [[intermittent-fasting]], [[simprove-probiotic]], [[simprove-trial-sheffield]], [[atns-symptomatic]], [[pots-care]].

**Eric-relevant takeaways**:

- **#172 Jo Thomas** — *operational reframe Eric will need at recovery*: "test the waters" decouples symptom outcomes from self-blame. Eric's perfectionist pattern + recovery-perfection pattern are exactly the trap this targets.
- **#173 Diana Driscoll** — Eric's clinical picture (POTS + PEM + possible MCAS overlap) maps onto Driscoll's inflammatory-POTS framing. **Parasym Plus and NAC Max are direct-to-consumer single-source supplements with limited peer-reviewed evidence** — wiki position is *be cautious, but defensible mechanistic story + recovered-patient + clinician-built*. Driscoll's intracranial-pressure framing is worth raising with Eric's neurologist *if* head-pressure / position-dependent headache symptoms emerge — they don't currently feature.
- **#174 Uroš** — **Kristin Neff self-compassion guided meditation** is a 20-min free YouTube practice Eric can layer on top of breathwork. **Pennebaker-style expressive writing** (3-4 days, 15-20 min sessions) is similarly cheap; both Uroš (#174) and Clarke (#179) point at it as load-bearing.
- **#175 Jackie cold water** — Eric's stress-down strategies are not yet at the point that cold water would be safe to try; this should not be on the active menu. When his nervous-system regulation + breathwork stack are solid (probably months out), then it might be a candidate. Cold-face splash / end-of-shower cold seconds are reasonable bridges; full immersion is not.
- **#176 Carl Robot** — *Most concrete actionable item from this batch*: **SymProve** is a contained, low-harm, well-tolerated multi-strain probiotic. Worth considering as a contained 3-month experiment. **Homemade kefir** is a near-zero-cost alternative or maintenance approach.
- **#177 Rachel Rock** — **EMDR** (with a chronic-illness-aware therapist) is worth Eric considering if/when ready for trauma processing — particularly if he can identify any unprocessed material. Strong signal: **the bodily sensation in EMDR was identical to her chronic-fatigue feeling** — same alarm state.
- **#178 Alisha** — **Rob Ensor (TMS coach)** is wiki-named alongside Dan Buglio + Rebecca Tolin in the TMS lineage. Reiki is wiki-new but the mechanism Alisha names is generic (engaging mind in something else, structured calming, certification-as-curiosity-restoration) — Eric could substitute any practice that meets those criteria.
- **#179 David Clarke / ATNS** — **symptomatic.me 12-item questionnaire** is a contained free self-assessment. *Letters-not-to-mail* exercise is contained, free, and complementary to expressive writing. ACEs framework is broad enough that even an "I had a fine childhood" reading is worth re-examining ("imagine your own child going through what you went through").
- **#180 Jules Rogers / Boundaries** — Eric's perfectionist + helper pattern is exactly what boundary work targets. **"No is a complete sentence" — eliminate over-explaining.** Holding-back-when-better will be the hardest boundary to maintain through recovery.
- **#181 Putrino** — *Most important strategic update for Eric*: **POTS subtypes matter** — Eric should know whether his POTS pattern is hypertensive-supine + drop-on-standing or hyperadrenergic, because the drug stack is different. **Slow-wave sleep disruption** worth investigating (Joffe phenotype: vivid dreams + sleeps indefinitely + wakes unrefreshed) — modafinil / similar agents may help if it fits. **Mitochondrial-support cluster** (NAD+, CoQ10, oxaloacetate, low-dose rapamycin) worth holding as a *later* candidate stack if a mitochondrial-dysfunction subset describes him; Eric's current pattern is more autonomic than mitochondrial. **Testosterone level** worth checking — if low, that's a potential lever (Eric is male, so the relevant marker is testosterone directly + estradiol as a downstream conversion marker).

## [2026-05-05] checkpoint | episodes 172-181 ingested (179 of 211; #31, #157 missing transcripts)

## [2026-05-05] ingest | episodes 182-191 (10 episodes)

- **#182 Karen Wright** — recovery story. Scottish NHS physio who developed POTS-pattern LC autumn 2021. Recovery hinged on **low-histamine diet** as the first concrete intervention with felt benefit (within 24h, body's "revving" calmed), plus breathwork + meditation + yoga nidra (lying down). Thyroid-cancer surgery in 2024 may have removed some symptoms (migraine, tinnitus) previously attributed to LC. Now runs Sage Health and Wellness. New `key_to_recovery` for [[low-histamine-diet]] (first patient-recovery row), [[breathwork]], plus `helped_partial` rows on [[meditation]] and [[yoga-nidra]].
- **#183 Theresa Aristoark** — recovery story. Seattle SWE, severe localised quad-muscle pain post-second COVID. **Couldn't tolerate LDN** (first explicit `harmed` row on the LDN page). Functional medicine + IV nutritional therapy + physical therapy 3×/week were the early progress. **SSRI was the step-change** that unlocked the mental-health blocker — first `key_to_recovery` row for [[antidepressants]]. Husband's confrontation that "physical work has plateaued, mental health is the unaddressed blocker" is the pattern to remember.
- **#184 Mahncke + Uswatte / Brain HQ + CI Cognitive Therapy** — first **RCT-evidenced** cognitive-rehab intervention on this wiki. Three-component package: Brain HQ processing-speed training + in-clinic everyday-task training + transfer package. Pilot n=7+7: **80% return-to-work in CI Cognitive Therapy arm vs 0% in usual care**, plus large gains in fatigue and brain fog. Confirmatory study + vagus-nerve-stim arm in flight. New pages: [[brain-hq]], [[ci-cognitive-therapy-trial]], [[henry-mahncke]], [[gitendra-uswatte]]. Brain HQ is broadly accessible at brainhq.com.
- **#185 Kendal Stewart** — TX integrative MD with surgical (ENT) background. Genetics-driven approach. Microglial-activation framework: 3 inflammation off-switch systems + 4 levers to turn off (steroids / opiate via 3mg LDN / CB2 / **thymic peptides — thymosin α-1**). **Amantadine** (1972 Parkinson's drug from star anise) used to slow the glutamate-driven racing brain. **IL-5 mutation** in 95%+ of his LC patients explains herpes-family reactivations. New pages: [[kendal-stewart]], [[amantadine]], [[peptides-thymosin]], [[d-chiro-inositol]], [[ivermectin]], [[hydroxychloroquine]], [[vitamin-d]]. Clinical-experience claims, not RCT-grounded — use as hypothesis generator, not treatment menu.
- **#186 Jamie** — ⚠️ severe-bedbound recovery story with mental-health crisis (suicidal ideation, hospital admission). Detox protocol HARMED her. **Olanzapine** (an antipsychotic) stabilised the acute crisis (NOT recommended as treatment; she's still tapering). Recovery via **Primal Trust** brain retraining + **Healing Dudes** group + **Lightning Process** at 90%. New pages: [[jamie]], [[primal-trust]], [[healing-dudes]], [[antipsychotics-olanzapine]], [[zinc]]. Second `key_to_recovery` for [[lightning-process]].
- **#187 Robert Groysman (return)** — mechanism #2 of his six-mechanism model: **mitochondrial dysfunction**. SARS-CoV-2 damages mitochondria *and* impairs the recycling mechanism (mitophagy). Bursting mitochondria release mtDNA → cGAS-STING → inflammatory cell death. Treatment shape: **treat dysautonomia first**; step-1 daily antioxidant + matrix support; step-2 monthly *gentle* mitophagy. Months-long process. **Cautions against** aggressive fasting, HBOT, ozone, rapamycin in severe LC — pushes a broken system harder. Added `harmed` rows on [[intermittent-fasting]], [[hbot]], [[ozone-therapy]], [[rapamycin]]. Major theme update on [[mitochondrial-dysfunction]] and [[post-exertional-malaise]].
- **#188 Jackie (solo)** — late-stage-recovery essay. Three phases of her own recovery; **body works list**, celebrate small wins, mute support groups, [[fern-program]] (Suzy Bolt's fear-of-reinfection program — Jackie used it near end of her own recovery and now teaches some breath sessions inside it). Cites Dan Neuffer's "stuck at 80% — start gently challenging" rule and Kathleen King's "stop fixing, start re-engaging with life."
- **#189 Natalie Gold** — recovery story (CA CFO, small farm). 2-year recovery via **ANS Rewire** after hearing Joanna Rayl's #56. Long-standing **psoriatic arthritis, chronic migraine, chronic back/neck pain ALL resolved alongside LC**. Self-prescribed low-dose **aspirin** for burning-lung sensation gave a modest boost (placebo or real) which she reinvested into committing to ANS Rewire. **Small-t trauma framing**: you don't need big-T trauma to need nervous-system work. Character-reframing for stressful personality patterns. New pages: [[natalie-gold]], [[aspirin-low-dose]]. Second `key_to_recovery` for [[ans-rewire]].
- **#190 Jess (Turn2 founder, return after #140)** — practical AI-for-patient-research episode. Use big-four foundation models (ChatGPT/Claude/Gemini), always ask for citations, push back on people-pleasing, redact PII. New Turn2 product: AI personal-health-sidekick reads ~1M words/week and surfaces the 12 things relevant to *you*; ~$2/week.
- **#191 Leo Galland** — NY internist, 40+ years post-infectious illness, *Power Healing* 1996. **Web of Long COVID** with 10 strands centred on **ACE2 damage and mitochondrial damage**. ACE2-restoration triad: vitamin D + curcumin + resveratrol — claims near-zero LC progression in patients treated this way from acute COVID onward. **PEM-as-relative-ischaemia** mechanism story (capillary damage → low O₂ → KB cycle runs backwards under stress → more damage). **AB21 probiotic** (Lactobacillus plantarum, Spanish) has controlled-trial evidence in *acute* COVID. **Joint hypermobility** strikingly comorbid (post-Lyme + post-COVID). NAD high-dose IVs can backfire (creates dependency). Free 90-page document at drgalland.com. New pages: [[leo-galland]], [[ace2-restoration]], [[ab21-probiotic]], [[curcumin]], [[resveratrol]], [[hydrogen-water]].

### Eric-relevant signal from this batch

- **#182 Karen Wright** — Eric should consider a structured trial of **low-histamine diet** under nutritionist supervision (8 weeks, then reintroduce). Karen's POTS-pattern presentation is similar to yours, and her trajectory is the cleanest single-intervention inflection point in this batch. The yoga nidra "rest is not bad — body is the priority" reframe is also a useful idea to internalise.
- **#183 Theresa Aristoark** — *important pattern*: **late-stage recovery often plateaus on physical work alone — mental health is the unaddressed blocker**. If Eric reaches the late phase and progress stalls, the SSRI conversation belongs on the table without stigma. Pair with #48 (Mulder, severe-suicidality SSRI inflection).
- **#184 Brain HQ / CI Cognitive Therapy** — **Brain HQ is the strongest evidence-based cognitive-rehab tool on this wiki**. Free trial daily exercise; cheap subscription. Worth a real trial if cognitive symptoms persist into recovery. The CI Cognitive Therapy package needs UAB or future telehealth.
- **#185 Stewart** — interesting frame, but most of his stack (peptides, amantadine, ivermectin, hydroxychloroquine) is clinical-experience-only, US-centric, and not aligned with how UK private practice would dispense. Useful for understanding *why* LC stays inflammatory (microglial activation + IL-5 mutation + herpes reactivation framework) more than as a treatment menu.
- **#186 Jamie** — ⚠️ if Eric ever reaches the headspace Jamie did, hospitalisation is the right move and olanzapine is not a moral failure — it's a stabilisation tool. The detox-protocol-as-harm pattern is also worth holding against any future high-supplement protocol that reframes adverse reactions as "die-off."
- **#187 Groysman (mitochondrial)** — *important treatment-sequencing rule*: in severe LC with mitochondrial dysfunction, **HBOT, ozone, prolonged fasting, and rapamycin can backfire**. Don't chase the longevity-stack hype until dysautonomia is calmed and antioxidant stores are rebuilt. The "treat dysautonomia first" rule is consistent with #76, and consistent with where Eric's case sits.
- **#188 Jackie's liminal-space essay** — keep this one for the late phase of recovery. The "stuck at 80%, start gently challenging" Neuffer rule is the practical takeaway.
- **#189 Natalie Gold** — second strong recovery testimony for ANS Rewire. Worth considering as a serious candidate brain-retraining program for Eric — Dan Neuffer offers 4 free intro lessons; if the dysautonomia-rooted model resonates after watching, the program is in scope (~few hundred dollars, not thousands).
- **#190 Jess / AI** — practical: when Eric uses Claude/ChatGPT for medical research, ask for citations and push back on people-pleasing answers. This is a good habit anyway.
- **#191 Galland** — most mechanistically rich episode in this batch. Specific items worth surfacing for Eric: (1) **AB21 probiotic** (L. plantarum, controlled-trial evidence in acute COVID) is a candidate adjustment to gut work; (2) the **F. prausnitzii depletion → bifidobacteria collapse** pattern is the gut signature to look for in any microbiome test; (3) the **PEM-as-relative-ischaemia** model is the cleanest story for why blanket mitochondrial supplements fail and why oxidative therapies (HBOT, ozone) can harm; (4) **joint hypermobility** comorbidity worth checking your own pattern against (Beighton score). Galland's free document at drgalland.com is dense but tiered; worth a read when energy permits.

## [2026-05-05] checkpoint | episodes 182-191 ingested (189 of 211; #31, #157 missing transcripts)

## [2026-05-05] ingest | episodes 192-213 (22 episodes — completing the corpus)

- **#192 Kelly George** — recovery story. US ex-professor, mom of two; ~3-year recovery via **CFS Health (Toby Morrison)** + pacing + acupuncture-as-listening + meditation + pet snuggles. New `key_to_recovery` row for [[cfs-health-program]] (new program page). Pattern: husband's parallel loss bridges isolation when named bidirectionally.
- **#193 Jackie (solo)** — *Pilot, not passenger* essay. Four micro-strategies — micro-agency, sensory grounding (5-4-3-2-1), inner-script rewriting, boundaries-as-navigation. Light overlap with breathwork bandwagon (Jackie cautions to use breath practices with LC-aware guidance).
- **#194 Ivor Clark** — recovery story. Edinburgh, ex-GB American football. **HBOT at Compass charity (28 sessions in 3 months)** as catalyst + heart-rate-capped pacing at 55% max HR + **MOTS-c peptide weekly injection** as inflection. Wrote a book; 50% of profits to Compass. New pages: [[ivor-clark]], [[peptides-mots-c]].
- **#195 Katie Brennan + Andrea Heinberg** — recovery story + co-founder. American economist (March 2020 UK cohort, reinfected severely), met German Olympic biathlon trainer at outdoor exercise class. Recovered via vagus + eye + breath + cognitive-motor coordination drills. Co-founded **Thrive90**. New pages: [[katie-brennan]], [[andrea-heinberg]], [[thrive-90]].
- **#196 Drs Rudy Tanzi & Edmarie Guzman-Velez** — **first peer-reviewed RCT-grade evidence on this wiki for an oral supplement helping LC**. Niagen Biosciences-funded NR 2,000 mg/day trial, cross-over intra-individual design. NAD+ rose 3-fold in 5 weeks. Pooled-baseline analysis (n=43, 10 weeks NR vs own baseline) showed significant improvement in fatigue, sleep, depression, and Trail Making B (+8.4 sec). Tanzi COI disclosed (Niagen consultant + equity). New pages: [[rudy-tanzi]], [[edmarie-guzman-velez]], [[nicotinamide-riboside]], [[niagen-lc-trial]].
- **#197 + #198 Dan Neuffer (return, two-part)** — belief in healing. Acceptance-vs-resignation distinction; three layers of evidence (rational / social-proof / personal-proof); monthly symptom-+-activity journal blind to prior; identity framing; setbacks are *more* productive than steady-state for plasticity. Updates [[dan-neuffer]] and [[ans-rewire]] with a return-with-no-new-counts row (per wiki rule: same speaker, same intervention, same outcome → no new row, just update notes).
- **#199 Creativity 2025** — annual creativity tapestry. 9 contributors share songs, poems, books, choir performance, AI-generated music. Notable: Naomi Vandernoot's [[long-covid-kids-choir]] song *Roller Coaster*; Kirsten Melian's *I Don't Mind*; Jasmine's recovery-memoir won the Letter of Views prize. AI-music-as-low-energy-creativity (suno.com) is a useful reference for severely-ill patients.
- **#200 Jackie (solo, 200th milestone)** — *Power of intention.* Intentions as direction not destination; 5 reasons (cognitive priming, RAS, emotional regulation, identity-shifts, NS posture/breath). Daily / weekly / monthly / yearly intentions.
- **#201 Lily Spechler (return)** — *Fuel before you fix.* Weight changes in LC (gain *and* loss) are byproducts of metabolic dysfunction, not targets. **Cutting calories backfires** in LC — needs are BMR + 15%. **Erratic blood glucose — especially the lows — may be the biggest under-recognised LC driver** (CGM-eye-opening). Estrogen-MCAS-adipose loop. Stability before pursuing weight loss; gain via calorie-dense low-volume foods (olive-oil-rich, Himalayan butter tea).
- **#202 Michelle Irving (return after #100)** — Career and Chronic map: 5 stages (off-ramp / on-ramp / new / test-and-redesign — 80% of life / authentic leadership). Sovereignty over self-sacrifice; communicate from baseline not optimal capacity. New "Chronic Illness at Work" corporate arm + free Feb 2026 webinar series.
- **#203 Carissa Conrad** — DPT + recovered LC patient. **Vagus-nerve stimulation via tunable TENS** (auricular tVNS); preset TENS units don't work — need manual mode/pulse-rate/pulse-width. "Meds got me off the couch; VNS got me out of the house." Sells preconfigured kit + protocol via carissadpt.com. New pages: [[carissa-conrad]] + updates [[vagus-nerve-tens]].
- **#204 Simon Harrison** — UK ME/CFS recovery story (~10-year arc, recovered ~2.5y before interview). **Mindfulness body scans** as foundational + breathwork + GET (atypical case — sensory-hypersensitivity-dominant rather than PEM-dominant) + year in Portugal as geographic reset. Wrote *Leaving ME Behind*. New page: [[simon-harrison]]. **Note**: GET helped him; do not generalise — his case was atypical.
- **#205 Nadine McKie (return)** — carers and **co-regulation**. Carer load mirrors LC invisibility; carer's nervous system is part of the patient's treatment. Vicarious trauma in long-term carers. Now at Bonita Kane's LC clinic.
- **#206 Ashley** — recovery story. March 2020 cohort, severe bedbound; positive Lyme/mold/virus tests took her down alt-med path (got less severe, not better). **Somatic therapy with a coach** as inflection — "speaking the language of the body" — + brain retraining + EFT + visualisations. Danced 5 hours at her wedding. New pages: [[ashley]], [[somatic-therapy]], [[visualization]].
- **#207 Dr Nathan Keiser** — Doctor of Chiropractic Neurology. **Mechanism over syndrome.** Doppler-ultrasound-measured cerebral perfusion + tilt; structural neck-rotation compression of carotid arteries 40% (commonly missed); targeted vestibular/ocular-motor microdrills with self-assessment markers. **Strong caution against VNS done without mechanism check** — "we've had a ton of people wreck themselves." Hypocapnia from over-breathing also widespread. New pages: [[nathan-keiser]], [[vestibular-rehab]].
- **#208 Claire (mother)** — paediatric ME/CFS recovery via three-stage stack: **Bristol/Bath ME/CFS clinic (Esther Crawley)** referral → pacing 0–40% → **ANS Rewire** at 16-17 → 80% → **Mickel Therapy 3 sessions** at 21 → full recovery. Pivot moment: realising 10 minutes of negativity caused symptom cascade. New pages: [[claire-mother]], [[esther-crawley]], [[mickel-therapy]].
- **#209 Jackie (solo)** — *Beyond Lying Down.* Seven types of rest (physical, mental/cognitive, sensory, emotional, social, creative, nervous-system). Banking energy as healing-savings. Permission-slip practice (literal post-it).
- **#210 Roddy Schrock** — NYC classical homeopath. 250-year-old modality; 2-hour case-taking; deep-listening component plausibly accounts for much of the value. Logged as anecdote/expert-opinion (mainstream RCT evidence contested). New pages: [[roddy-schrock]], [[homeopathy]].
- **#211 Nora Rodden** — recovery story + Nirvana app founder. Three sequential conditions (chronic back pain post-car-accident, GI, severe insomnia) all resolved via neuroplastic recovery. **PSRT clinical trial** (66% pain-free vs ~10% placebo, beat mindfulness arm). **Outcome independence** for insomnia. *F It Diet* for GI. Expressive writing — write faster than you can think — to bypass analytical brain. New pages: [[nora-rodden]], [[nirvana-app]], [[psrt-back-pain-trial]], [[journaling]].
- **#212 Amy Davies** — UK embodiment + somatic coach (recovered chronic pain + fatigue 2018). **Internalised pressure** as second layer of NS stress in LC: perfectionism, achiever pattern, masking, inner drill sergeant. Compassionate awareness of patterns as protective mechanisms. New page: [[amy-davies]].
- **#213 Margaret Hampton + Pierre Brunschwig** — paired East-West LC clinical model at Helios Integrated Medical (Boulder CO; 12+ year collaboration). **Shao Yin (kidney + heart) deficiency** as dominant LC pattern. Adrenaline ↔ oxytocin teeter-totter. Latent virus reactivation + T-cell exhaustion subtype. Cordyceps mushrooms; strong anti-vegan / pro-animal-protein blood-building stance; cooked-food rule; H. pylori testing. Korean electroacupuncture-stem-cell protocol. New pages: [[margaret-hampton]], [[pierre-brunschwig]], [[cordyceps]].

### Eric-relevant signal from this batch

- **#196 NR/Niagen trial** — first peer-reviewed RCT-grade signal on this wiki. NR 2,000 mg/day for 10 weeks improved fatigue, sleep quality, depression, and executive function (Trail Making B +8.4 sec). Worth holding as an evidence-based add-on candidate. **Note dose**: trial was 2,000 mg/day under IRB approval; bottle-recommended is 1,000 mg/day. If self-experimenting, 1,000 mg is the safer default; 2,000 mg should be discussed with a doctor.
- **#201 Lily Spechler — blood glucose** — *the* high-signal new claim. Erratic blood glucose, especially lows, may be a major under-recognised LC driver. Worth Eric considering a 2-week CGM trial during a stable period to see if symptoms track glucose dips. Low cost, high information. Pair with electrolytes-before-getting-upright to blunt morning glucose spike.
- **#194 Ivor Clark — peptides** — MOTS-c was the inflection of his recovery. Peptide therapy is off-label, prescription-required, UK private route. Worth holding as a candidate intervention if/when ANS pacing has plateaued and mitochondrial fuel feels like the bottleneck. Pair with #185 (Stewart's thymosin α-1 immune-side peptides) for the broader peptide framework.
- **#203 Carissa Conrad / #207 Nathan Keiser — VNS via TENS** — *both can be true*. Carissa (DPT, recovered patient) treats VNS as the primary tool; Keiser (chiropractic neurologist) cautions strongly that VNS done without mechanism check has "wrecked" many of his patients. If considering VNS, structural assessment first (Doppler, neck rotation effects) is reasonable. Cheap TENS unit (~$38) with manual parameter control beats preset TENS unit.
- **#207 Keiser — neck-rotation-induced cerebral hypoperfusion** — Eric should consider raising this with his clinicians: do certain neck positions reproducibly worsen symptoms or HR? If so, structural cervical assessment may close a missed bottleneck. Doppler-cerebral-perfusion testing exists.
- **#207 Keiser — breathwork hypocapnia** — if Eric's breath practice ever produces tingling, anxiety, or worsening, that's a sign to *tighten* the breath window rather than push slower-deeper. Many LC patients are already hypocapnic.
- **#208 Claire / Mickel Therapy** — first Mickel-Therapy case on the wiki (3 sessions → full recovery). Worth holding as a UK-side late-stage option if other approaches plateau.
- **#211 Nora Rodden — outcome independence for insomnia** — if Eric's sleep ever becomes a tracked-and-anxious problem, the "stop caring about it" reframe (paired with safety mantras and analytical-data review of past nights) is the key technique, not more sleep hygiene rules.
- **#211 Nora Rodden — fast-handwriting expressive writing** — for someone who finds "feel into your body" prompts inaccessible (left-brain-dominant), writing faster than you can think bypasses the analytical filter. Very concrete tool.
- **#213 Hampton-Brunschwig** — the team-and-pivot model is exactly right for LC navigation. The Shao Yin (kidney + heart) frame maps well to Eric's POTS + dysautonomia + (latent emotional load). Cordyceps is a low-risk add-on. The anti-vegan / pro-animal-protein stance is sharp and should be weighted against Eric's actual diet preferences.

## [2026-05-05] checkpoint | episodes 192-213 ingested (211 of 211; full corpus indexed; #31, #157 transcripts unavailable)

## [2026-05-05] query | brain-retraining-programs-which-to-choose — ANS Rewire vs DNRS vs Gupta vs others for Eric's POTS+PEM+possible-MCAS profile. Filed at `wiki/queries/brain-retraining-programs-which-to-choose.md`. Headline: ANS Rewire has the strongest signal (2 key_to_recovery incl. Natalie Gold #189 with POTS); Curable app is the cheap-entry alternative (3 key_to_recovery); Gupta and DNRS lack recovered-patient credits on this podcast. Recommendation sequence: 4 free Neuffer intro lessons first → ATNS questionnaire → Curable as low-stakes trial → ANS Rewire as structured commitment if frame resonates. Wait until stable from April 2026 crash before committing. Copy also placed in `~/Projects/claude_home/` for TTS upload.

## [2026-05-05] query | episodes-to-listen-to — curated, tiered listening list for Eric's profile. Filed at `wiki/queries/episodes-to-listen-to.md`. Living document — append as conversations surface new episodes. Tier 1 (brain-retraining decision): #189 Natalie Gold, #56 Joanna Rayl, #102 Dan Neuffer. Tier 2 (HRV / tracking): #82 Jay Wiles, #86 Harry Leeming. Tier 3 (deeper Neuffer if model resonates): #147 / #148 / #197 / #198. Tier 4 (clinician pacing perspective): #164 Clayton Powers. Each entry: why, listen-for bullets, duration, videoId.

## [2026-05-08] update | corpus expanded to multi-source — Raelan Agle podcast added

- 44 Raelan Agle transcripts dropped in at `transcripts/raelan/` (4-digit numbering, range 0076–0998; preserves Raelan's own episode numbers).
- CLAUDE.md updated for multi-source corpus: source keys (`lcp`, `raelan-agle`), prefixed episode references (`LCP #87`, `RA #76`), `podcast:` frontmatter field, evidence-log Ep-cell prefix, scoped ingest globs.
- Wiki layout: existing LCP pages stay where they are (legacy default-to-LCP rule); new LCP ingests under `wiki/episodes/lcp/`; Raelan pages under `wiki/episodes/raelan/RA-NNNN-slug.md`.
- `overview.md` rewritten with two-source structure and explicit **Raelan selection-bias note**: Raelan curates recoveries, so aggregate `key_to_recovery` counts will tilt upward as Raelan rows arrive. Each row remains source-traceable; reporting must surface the LCP-vs-Raelan split when it changes the read.
- Combined-wiki rationale (vs. two separate wikis): synthesis layer (interventions, recovery stories, person pages) is the whole point. Splitting fragments arcs (Suzy Bolt is on both shows). Cost is attribution discipline, which is mechanical.

## [2026-05-08] ingest-start | Raelan Agle batch — beginning ingest of 44 transcripts

## [2026-05-08] ingest | RA #76 — Chimére's Story

First Raelan Agle ingest under the multi-source schema. Baltimore middle-school teacher, Black, first-wave US (March 22, 2020). Substantial recovery in progress at recording (December 2020, ~9 months in) — not full. Bedbound months, 5-month vision loss, occipital + trigeminal neuralgia residuals, suicidal ideation pre-pivot. Pivot **August–October 2020** via Raelan Agle's stretching videos (5-min sit-up timer → daily stretching) + Joe Dispenza's *Breaking the Habit of Being Yourself* (mindset shift). She did NOT take Dispenza's workshop — book only.

New pages:
- Episode: [[RA-0076-chimere]]
- Person: [[chimere]]
- Recovery story: [[recovery-stories/chimere]]
- Intervention: [[gentle-movement-restorative]] (sub-PEM-threshold movement-from-bed pattern; distinct from [[graded-exercise]])
- Program: [[joe-dispenza-method]] (mind-body / brain-retraining-adjacent; ⚠️ some Dispenza claims outside mainstream evidence — corpus indexes patient outcomes, not biological claims)

Aggregate-page updates:
- [[meditation]] — +1 helped_partial (RA #76); count 10 → 11
- [[healthcare-gaslighting]] — added RA #76 with **non-medical-political-channel advocacy** as a new gaslighting-unblock pattern (Google reviews + Baltimore city councilmen)
- [[raelan-agle]] (person) — added host-role section noting she is the host of all 44 Raelan ingests; her own stretching videos credited as recovery inflection by guests
- [[index]] — Raelan section now 1 of 44; new intervention/program/person/recovery-story entries linked

### Eric-relevant signal from this episode

- **Gentle-movement-restorative as a starter intervention** — the 5-minute timer pattern (sit up in bed → tiny stretches → scale slowly) is a generalisable technique for the post-crash "I literally cannot move" phase. Distinct from the graded-exercise framework that has crashed many ME/CFS patients on this corpus. Worth noting for any future Eric crash.
- **Mindset-shift via book-only Dispenza route** is a low-cost low-risk experiment for the brain-retraining axis if formal programs (ANS Rewire, Curable) don't resonate. Not a replacement; a different doorway.
- **Selection-bias check**: Chimére's `key_to_recovery` rows for gentle-movement and Joe-Dispenza-method should be read as RA-source rows. She is on the recovery path, not past it. The signal is real but earlier-stage than most LCP `key_to_recovery` credits.

## [2026-05-08] ingest-pause | Raelan Agle batch — 1 of 44 ingested

Schema validated end-to-end on the Chimére ingest:
- Episode lives at `wiki/episodes/raelan/RA-0076-chimere.md` — `RA-` filename prefix, `podcast: raelan-agle` frontmatter
- Evidence-log `Ep` cell uses `RA #76` — visually distinct from LCP rows on the same page (e.g., [[meditation]])
- Aggregate `episodes:` field migrated to prefixed strings (`"LCP-7"`, `"RA-76"`) on touched pages
- Cross-corpus link working: Chimére's gaslighting story sits in the same theme page as LCP #69 Fiona Lowenstein and LCP #60 Reema Ahmad — the racial-disparities thread now spans both shows on a single page

Remaining: 43 Raelan transcripts. Ingest will continue in subsequent sessions or via fork-batched runs; each follows the same pattern.

## [2026-05-08] ingest | RA #118 — Lorrie Rivers (cross-corpus reaffirmation)

Cross-corpus appearance: Lorrie Rivers already on the wiki as guest of LCP #70 and LCP #137. **Earlier date-stamp than LCP** — June 2021 recording. Useful finding: in 2021 her recovery framework leads with **energy medicine** ([[eft-tapping]] → [[healing-codes-trilogy]]) on a foundation of pacing + diet + mindset; the parasite / hidden-infection theory that dominates her LCP appearances is **absent**. Read this as evidence that the holistic / energy-medicine layer was load-bearing *before* the parasite framing crystallised.

Aggregate handling: per CLAUDE.md cross-podcast same-speaker-same-outcome rule, the existing `key_to_recovery` row for [[lorrie-rivers-relief-and-transformation]] (originally LCP #70) is **not double-counted** — added a "Reaffirmed RA #118" note and noted the framing difference. Same treatment for [[eft-tapping]].

New page: [[healing-codes-trilogy]] (Alex Lloyd's energy-medicine method) — first instance.

## [2026-05-08] ingest | RA #147 — Kristyna (post-viral CFS, ~1 year)

Czech-born Vienna-based. Recovery via brain-retraining (unnamed coach "Jason" found on Raelan's channel) + leaving her stressful job + late-stage Kambo ×2 for emotional release at ~95%.

**Healthcare-gaslighting in non-English-speaking systems** — explicit anchor row: in Austria/Czechia she found *zero* CFS information in her own languages; recovery was gated on enough English to consume Raelan's channel. Added to [[healthcare-gaslighting]] would've been valuable but I deferred — opportunistic backfill candidate.

**LDN never-started row** — Austrian neurologist prescribed it but never responded to follow-up calls when she got worse. Logged as `mentioned_only` on [[low-dose-naltrexone]]; second never-started LDN row on the corpus (after LCP #186 Jamie). Useful when computing prescribed-but-never-reached-the-patient rate.

New page: [[kambo]] (frog-poison ceremony) — first instance. Caution flag: late-stage / post-recovery only; not for unstable nervous systems.

Brain-retraining "Jason" coach: identity not on transcript. Logged at the generic [[mind-body]] level rather than against a named program. If a future Raelan ingest disambiguates, link can be added.

## [2026-05-08] ingest | RA #150 — Erik Hajj (substantial recovery, 11 months in)

27 yo St. Louis MO videographer. Two named inflection points: **Moderna vaccine (March/April 2021)** and **[[ans-rewire]]** (Dan Neuffer's program). *"I didn't start recovering until I got my vaccine."*

New page: [[covid-vaccine-post-acquisition]] — first instance of **patient-self-credit for vaccine as a recovery inflection** on the corpus. Caroline Pover (LCP #84) anchors the opposite direction (vaccine-injury); both can be true across different patients. Wiki position: log anecdotal patient outcomes; don't speculate on mechanism.

[[ans-rewire]] now at **3 key_to_recovery** (2 LCP + 1 RA). Source-bias note: the new RA row should be read as Raelan-curated.

Erik runs his own LC YouTube channel — meta-content creator within Raelan's ecosystem. Cites [[miguel-bautista]]'s pain-receptor visualization (Miguel ingest pending — RA #623).

## [2026-05-08] ingest | RA #170 — Matt Butler (full recovery, ~1 year, multi-component)

31 yo Londoner; full recovery from probably-LC / probably-post-viral-CFS via an explicitly multi-component stack with no single key. Aggregate rows logged as `helped_partial` for each component (Pamela Rose pacing, yoga + meditation + breathing daily 2 hrs, CBT, Lightning Process intro audio, DNRS full program).

Notable anchors:
- **Lightning Process intro-audio-only variant** as a low-cost first-step lever — the *"I am safe"* self-talk technique. *"First time I tried it I walked 15 minutes."* Logged as a distinct sub-pattern on [[lightning-process]].
- **DNRS full-program `helped_partial` from a recovered patient** — first such row on the corpus. Hard work; not magic; but meaningful contribution within a stack.
- **CBT-as-recovery-stage tool** (graded behavioural experiments around feared activities), distinct from CBT-as-coping-tool. Worth flagging for future ingests — CBT may have a more nuanced role on the wiki than its current minimal coverage suggests.
- **"Belief is a precondition"** — *"For half the period I was ill, deep down I didn't believe I'd recover. Only when I started believing did progress start."* Pairs with [[raelan-agle]]'s "hope as a recovery input."

Deferred: aggregate updates to [[meditation]], [[pamela-rose]] coaching — non-directional incremental rows. Will batch on a future ingest pass through the same speakers/programs.

## [2026-05-08] ingest | RA #221 — Roberto Escobar (1.5y severe LC + PTSD → full recovery)

Queens NY registered nurse. **Healthcare-worker-trauma sub-pattern**: front-line COVID-unit work in March 2020 (~9 months pre-illness) named as the load-bearing predisposing factor, *not* the infection itself. Hospitalized 2 weeks for severe acute Covid (almost ventilated). 1.5 years of severe LC + severe PTSD before the pivot.

The pivot was **two threads converging**:
- **Self-compassion / self-love mindset shift** at the ~year mark — chose acceptance of where he was over comparison to who he was.
- **Polyvagal-theory framing** discovered via a YouTube psychologist's video (type-A + past trauma → LC).

Once he had both, his existing breathing + yoga + laughing yoga practice gained traction it hadn't had before. **2.5–3 month recovery** from there.

Aggregate updates:
- [[yoga]] — **2nd `key_to_recovery` on the corpus, first from RA source.**
- [[breathwork]] — 4th `key_to_recovery`.
- [[emdr]] — added `helped_partial` row (PTSD only — explicitly **not** physical LC); first **healthcare-worker occupational-trauma** row.
- [[gupta-program]] — **first `no_effect` row on the corpus**. Roberto's framing: not a knock on Gupta — a *frame-fit* claim. Same nervous-system work, different mental-model fit per patient.
- [[polyvagal-theory]] — added Roberto as the corpus's first instance of **polyvagal-theory framing as the load-bearing factor for a severe-LC recovery**. Counter-evidence to "polyvagal is just a belief story" — frame fit gates whether the patient sustains the techniques.

Deferred: aggregate row on [[self-compassion]] theme. Opportunistic backfill candidate.

### Eric-relevant signal from this batch (RA #76, #118, #147, #150, #170, #221)

- **Type-A personality + past trauma + perfectionism** as the recurring predisposing pattern across 5 of 5 Raelan recoveries (Chimére, Lorrie, Kristyna, Erik, Matt, Roberto). Eric-relevance: known. Worth holding if Eric finds himself on the post-crash recovery curve — the identity / pacing-with-self-compassion frame is consistently named, not just by one show.
- **Frame-fit matters as much as technique** — Roberto could not get yoga + breathing to work without the polyvagal frame; Kristyna could not get supplements + acupuncture to work without believing in them. The same nervous-system work fails or succeeds based on whether the *patient's* frame can sustain the practice. Implication: when picking a brain-retraining program, the *mental model fit* (polyvagal vs. limbic-system vs. ANS-rewire) matters more than the specific program. ANS Rewire is still the corpus's strongest signal (now 3 `key_to_recovery`) for Eric, but if it doesn't click within a few weeks, polyvagal-theory routes via Sally Riggs (LCP #23, #101) or Joe Dispenza self-study are reasonable alternates rather than persisting with a frame that doesn't fit.
- **"I am safe" self-talk** (Matt's Lightning Process intro audio takeaway) is a single concrete in-the-moment technique Eric could try cheap and small, separate from the brain-retraining-program decision tree.
- **Vaccine-helped-LC** (Erik) is a single anecdotal data point; in 2026 we've been past the wave of such anecdotes for a while. Mostly archival interest unless Eric is specifically trying to weigh booster-related decisions.
- **Gentle-movement-restorative** (Chimére's 5-min sit-up timer pattern) is a strong post-crash micro-dosing technique — distinct from graded exercise — worth holding for any future Eric crash.

## [2026-05-08] ingest-pause | Raelan Agle batch — 5 of 44 ingested

Schema continues to hold up at 5 episodes. New aggregate pages created in this batch: [[gentle-movement-restorative]], [[joe-dispenza-method]], [[healing-codes-trilogy]], [[kambo]], [[covid-vaccine-post-acquisition]]. New person/recovery pages: [[chimere]], [[kristyna]], [[erik-hajj]], [[matt-butler]], [[roberto-escobar]] + their recovery stories. [[lorrie-rivers]]'s existing pages updated for the cross-corpus reaffirmation.

**Deferred opportunistic-backfill candidates** (won't break anything; clean up on a future pass):
- [[meditation]], [[pamela-rose]], [[cbt]] — Matt #170 helped_partial rows
- [[self-compassion]] theme — Roberto #221 anchor row
- [[healthcare-gaslighting]] — Kristyna's non-English-speaking-system pattern row

Remaining: 39 Raelan transcripts (next: 0226, 0228, 0232, 0235, 0261, …).

## [2026-05-08] ingest | RA #226 — Kristine (post-viral CFS, ~3 months)

Latvian, Denmark-based. Post-vaccine + virus stack → severe ME/CFS with severe insomnia + sleep paralysis. Failed: supplements, sleep pills, alternative therapies, Headspace meditation, psychologist body-scan / relaxation work. Recovered via the **same unnamed Jason brain-retraining coach** as Kristyna RA #147.

**Striking timeline anchor for Jason's program**: week-1 sleep restoration after months of severe insomnia; week-4-5 skiing 8 am to 4 pm. Now uses the techniques for non-health goals.

New page: [[jason-brain-retraining-coach]] — placeholder consolidating credit for the same coach across RA #147 + RA #226. Identity pending; awaits a future ingest that names him fully.

Notable: also a clean **`no_effect` row for Headspace-style app-meditation** in a fear-state nervous system — useful counter-row to the meditation-as-helped pattern across the corpus.

## [2026-05-08] ingest | RA #228 — Donna Shaw (full recovery, ~2 years, multi-component)

Surrey UK first-wave (April 2020). Severe acute (throat-closing symptom no clinician understood; two ER visits, scans clean). Post-birthday-cake crash October 2020 → near-bedbound for months → multi-component recovery via Pamela Rose pacing + Optimum Health Clinic / Alex Howard mindset + Sopfit graduated walking + Hill with Liz affirmations + heal-the-gut nutrition. Now a qualified life coach for anxiety.

Anchor framing she names: **"healing state vs. stress state"** — the body cannot heal while the autonomic nervous system is locked sympathetic. Pairs with [[polyvagal-theory]] and Roberto Escobar's polyvagal anchor (RA #221).

Aggregate updates:
- [[optimal-health-clinic]] — added `helped_partial` row; first Raelan-source row for OHC.
- Pamela Rose coaching `helped_partial` row — deferred (opportunistic backfill candidate, no Pamela-Rose-program page exists yet).
- Sopfit / Hill with Liz — referenced; no wiki pages yet (future ingest candidates).

Useful counter-row: a clinician early on told Donna *"don't walk while legs hurt"* (3 months no walking). Sopfit's contrary advice (sub-30-second graduated movement) was what unlocked her. The "don't move while symptomatic" advice was wrong for her — graduated micro-doses worked.

## [2026-05-08] ingest | RA #232 — Kyle (full recovery, ~2 years, meditation-load-bearing)

South African; got Covid October 2020. ~2 years severely ill. Full recovery via Buddhist-adjacent meditation + identity letting-go.

**Two `no_effect` rows added — both notable counter-evidence on otherwise-helpful interventions:**
- [[low-histamine-diet]] — `no_effect` (food-fear loop). Diet failed because the framing made foods threats and the body learned to react to them. Distinct mechanism from Bailey LCP #163's citric-acid harm case.
- [[pacing]] — `no_effect` (perfectionism / fear-amplifier loop). First recovered-patient `no_effect` for pacing on the corpus. Added a *"failure mode — pacing as fear-amplifier"* section to [[pacing]] consolidating Kyle + Donna + Matt's nuances on this.

Load-bearing intervention: **[[meditation]] — second `key_to_recovery` on the corpus.** Operative techniques: *"What am I resisting?"* welcoming-discomfort + flare-up reframe (vs "crash"). The Kyle / Alisha LCP #178 pair is the corpus's clearest articulation of meditation-as-primary-vector.

**Strong cross-corpus thread**: Kyle's frame-fit failure (low-histamine, pacing) + Roberto's frame-fit failure (Gupta) + Kristyna's belief-state framing (acupuncture only worked when believed) all converge on the same lesson: **the patient's nervous-system state at the time of applying an intervention determines whether the intervention can land**. The same intervention is `key_to_recovery` for one patient and `no_effect` for another based on this. This is now strong enough to add as a stand-alone framework on [[mind-body]] in a future pass.

## [2026-05-08] ingest | RA #235 — Raelan host-solo synthesis (3-component framework)

Host-solo synthesis episode. Raelan distils her 3-component recovery framework after ~100 interviews:

1. Nervous-system work — virtually everyone needs it
2. Brain retraining — most need it
3. Underlying infections / gut / mould / metals / nutrition — some need it

Pairs with LCP #107 (longer version of the same synthesis). This is the cleanest standalone articulation on the corpus.

Useful for future Eric conversations: when explaining "why does the wiki keep coming back to nervous-system + brain-retraining as the load-bearing axes," cite RA #235 as the anchor synthesis.

No new aggregate pages or person/recovery-story pages — host-solo, no patient interview content beyond the framework itself.

## [2026-05-08] ingest | RA #261 — Raelan meal-planning course promo (low-content stub)

Host-solo promo for Raelan's Udemy course on meal planning. Almost zero LC-specific content — energy-conservation framing implicit. Stub episode page only; no aggregate updates.

Only corpus-relevant tidbit: Raelan names the cookbook *Healthy Living James* (James recovered from the same chronic-fatigue condition as Raelan).

### Eric-relevant signal from this batch (RA #226–#261)

- **Frame-fit framework strengthens**: Kyle's pacing-no-effect + low-histamine-no-effect + Roberto's Gupta-no-effect + Kristyna's belief-required-for-efficacy form a now-robust pattern on the corpus. **Implication for Eric**: if a brain-retraining program (e.g., ANS Rewire) doesn't click within a few weeks, the right next move is *not* to push harder on the same frame — it's to switch to a different frame (polyvagal-theory route, contemplative meditation route, mindfulness-as-welcoming-discomfort route). Persistence in a non-fitting frame can itself be the trap.
- **Meditation as primary vector** is now a more credible recovery axis on the corpus (Kyle RA #232 + Alisha LCP #178 = 2 `key_to_recovery`). The operative technique isn't generic mindfulness — it's specifically **welcoming discomfort** ("What am I resisting?"). Worth holding for Eric as a low-cost low-risk first-line technique alongside any structured program.
- **Crash → flare-up reframe** is a genuinely useful semantic shift Eric could try. Same physical experience, different label, different nervous-system response. Pairs with the existing wiki framing of pacing as PEM-threshold-respecting.
- **Multi-component recoveries dominate the Raelan-source data** (Donna Shaw, Matt Butler). Single-vector recoveries (Kristine via Jason; Kyle via meditation) are the exception. The default expectation should be a stack, not a single magic intervention.
- **Healthcare-worker occupational trauma** (Roberto RA #221) is its own predisposing-factor sub-pattern that may be relevant if Eric encounters frontline-clinician LC patients. Probably not directly relevant to Eric's own profile.
- **The "5% recover" prognosis stat** — both Donna and Raelan call it baseless. Worth holding if Eric ever encounters this stat from a clinician or read it online; the corpus's tally already exceeds dozens of full recoveries.

## [2026-05-08] ingest-pause | Raelan Agle batch — 10 of 44 ingested

New aggregate pages this batch: [[jason-brain-retraining-coach]] (placeholder, identity pending). New person/recovery-story pages: [[kristine]], [[donna-shaw]], [[kyle]] + recovery stories.

Aggregate updates touched: [[low-histamine-diet]] +1 `no_effect`; [[pacing]] failure-mode section added with 3 cross-references; [[meditation]] +1 `key_to_recovery` (Kyle), +1 `no_effect` (Kristine); [[optimal-health-clinic]] +1 `helped_partial` (Donna).

Cross-cutting frame-fit framework now strong enough across the corpus (Kyle/Roberto/Kristyna all converge) to merit a dedicated section on [[mind-body]] in a future pass.

**Deferred opportunistic-backfill candidates** (now larger backlog):
- [[meditation]], [[pamela-rose]], [[cbt]], [[breathwork]], [[yoga]] — incremental Matt #170 helped_partial rows
- [[self-compassion]] theme — Roberto #221 anchor row
- [[healthcare-gaslighting]] — Kristyna's non-English-speaking-system pattern row
- Pamela Rose program page — does not yet exist; could create when patterns warrant
- Sopfit and Hill with Liz pages — multiple references; could create when 3rd reference appears
- Frame-fit framework section on [[mind-body]] — strong enough now

Remaining: 34 Raelan transcripts (next: 0276, 0279, 0280, 0300, 0309, …).

## [2026-05-08] ingest-batch | Raelan Agle batch 3 — 10 episodes (RA #276–#465)

Batched 10 episodes; tighter ingest discipline given volume. Highlights:

**Host-solo episodes (4 of 10)**:
- [[RA-0276-three-strategies-healing-state]] — slip-vs-slide, dial-down-importance, make-your-head-a-good-place-to-be (3 strategies for healing state)
- [[RA-0279-overcome-setbacks-five-steps]] — 5-step setback framework (acknowledge → perspective → learn → forgive → let go)
- [[RA-0317-five-ways-calm-nervous-system]] — smiling, word-swap, breathing/physiological-sigh, meditation, nature
- [[RA-0261-meal-planning-course-promo]] — done in batch 2 (low-content stub)

**Patient interviews (6 of 10)**:
- [[RA-0280-amy-engkjer]] — **cross-corpus reaffirmation = Amy Anker LCP #20** (name change). Tightest corpus articulation of *meditation as a 3-layer tool* (calm first → respond not react → loosen identity grip). Coined "joy shocking."
- [[RA-0300-adam-langdon]] — Ontario Canada; **neurological long covid subtype**; ~95% recovered; **fasting (Tom Bunker protocol)** as load-bearing intervention; brain inflammation confirmed via PET scan. Runs *Beating Long Covid* YouTube.
- [[RA-0309-becky-sharpe]] — London UK; full recovery; **TMS / Sarno book = 30%→80% in 3 days**; **harsh-naturopath-protocol harm row** with herxheimer-as-progress warning; PEMF-mat retrospectively re-attributed to the meditation that ran alongside it.
- [[RA-0335-jackie-baxter]] — **= Jackie Baxter (LCP host)**, cross-corpus reaffirmation; her Big Three (breathing → yoga nidra → cold water) consolidated; now a breathing instructor with Vicki Jones via [[long-covid-breathing]].
- [[RA-0354-karen-knutson]] — Watertown MN single mom; in-progress halfway recovery. Counter-evidence rows: **SGB `no_effect` (first patient row on the wiki)**, Sarno book `no_effect` (counter to Becky #309), supplements `no_effect`, detoxes `no_effect`. Helped: sleep meds, anxiety meds, cold showers, affirmations, ayurvedic.
- [[RA-0448-katrine]] — Belgium, full recovery, ~1 year. **Disambiguates the unnamed Jason coach as Jason McAuliffe and the program as "I Can Thrive."** Three Raelan-source `key_to_recovery` rows now stand on the [[i-can-thrive]] page (placeholder retitled).
- [[RA-0465-glenn-chan]] — vaccine-injured cohort, ~95% recovered. Built **sickandabandoned.org** patient-led-survey + Python data analysis. **Personal recovery: ivermectin + black seed oil.** Survey findings: HBOT + fasting + antimicrobial supplements rank promising; SSRIs + gabapentin + antibiotics rank bottom. Critical warning: even working interventions (HBOT) can permanently set patients back.

### Major schema events from this batch

- **Jason McAuliffe / I Can Thrive identity confirmed** at RA #448. Updated [[i-can-thrive]] (formerly placeholder) with full identity + 3 `key_to_recovery` rows.
- **Amy Engkjer = Amy Anker** identified in RA #280. Updated [[amy-anker]] person page with the name change + appearances field.
- **Jackie Baxter cross-corpus** in RA #335. Updated [[jackie-baxter]] person page with appearances field.

### New aggregate page

- [[i-can-thrive]] (formerly [[jason-brain-retraining-coach]] placeholder; now identified). 3× `key_to_recovery` from Raelan source.

### Aggregate-page implications (deferred to opportunistic backfill)

- [[stellate-ganglion-block]] needs `no_effect` row from Karen RA #354 — first patient `no_effect` for SGB on corpus. Currently 3 `recommended` rows from clinicians. Worth a directional update.
- [[tms-mind-body-syndrome]] needs `key_to_recovery` row from Becky RA #309 (30%→80% in 3 days from Sarno book, very strong) AND `no_effect` row from Karen RA #354 (couldn't get through the book). Two opposite outcomes from the same book — frame-fit data points.
- [[meditation]] needs Amy Engkjer reaffirmation (no double-count; existing LCP row stands).
- [[fasting]] page does not exist; warrants creation given Adam #300 + Glenn #465 + Tom Bunker patient-led-research clinical trials. **Strongest deferred backfill candidate** in this batch.
- [[ivermectin]] page does not exist; Glenn #465 single anecdotal but vaccine-injury cohort. Lower-priority creation candidate.
- [[hbot]] / hyperbaric oxygen has rows from earlier ingests; Glenn #465 affirms it as RCT-supported with set-back warning. Worth updating.

### Key cross-cutting signal from this batch

- **Identity disambiguation**: 3 placeholder / unnamed references collapsed into named real entities — Jason McAuliffe (I Can Thrive), Amy Anker = Amy Engkjer, Jackie cross-corpus. The wiki's same-person-across-shows handling (per CLAUDE.md) is working — multiple patients hadn't been confused into separate pages.
- **Herxheimer-as-progress warning** is now a 3-source pattern: Becky #309 (worst case — 1.5–2 years stuck on harsh protocol), Glenn #465 (data-driven warning that even good interventions can set patients back), Karen #354 (detoxes crashed her for 4 weeks each). Strong enough that a dedicated [[mind-body]] section could be warranted.
- **Frame-fit framework strengthens further**: Becky's TMS book = 30%→80% in 3 days vs Karen's TMS book = couldn't get through it. Same intervention, opposite outcomes, same family of patients (LC + ME-CFS). Pairs with batch 2's Kyle / Roberto / Kristyna data. The pattern is now robust enough that the corpus's recommendation tree should explicitly include "if X frame doesn't click, try Y frame."
- **Patient-led research as the actual LC frontier**: Tom Bunker (fasting protocol → clinical trials), Glenn Chan (sickandabandoned.org), Lily Spechler (LCP #129/#201 — Energy Expansion Project). Three distinct patient-led research efforts now on the corpus.
- **Eric-relevant signal**: HBOT keeps showing up across the corpus. The Glenn #465 framing — *"only LC treatment supported by an RCT"* + *"can permanently set patients back"* — is the cleanest summary of the dual-edged nature. Worth holding as a candidate intervention but with explicit dose-titration discipline if Eric ever pursues it.

## [2026-05-08] ingest-pause | Raelan Agle batch — 20 of 44 ingested

20 of 44 transcripts now ingested (≈45% of the Raelan corpus). New aggregate pages this batch: [[i-can-thrive]] (formerly placeholder; now identified). New person/recovery-story pages: [[adam-langdon]], [[becky-sharpe]], [[karen-knutson]], [[katrine]], [[glenn-chan]] + their recovery stories. Cross-corpus updates: [[amy-anker]] + [[jackie-baxter]] person pages.

**Deferred opportunistic-backfill candidates** (now larger backlog):
- [[stellate-ganglion-block]] — Karen #354 `no_effect` row
- [[tms-mind-body-syndrome]] — Becky #309 `key_to_recovery` + Karen #354 `no_effect` (opposite outcomes from same book)
- [[meditation]], [[breathwork]], [[cold-water]] — multiple incremental rows
- [[fasting]] — page creation warranted (Adam #300 + Glenn #465 + Tom Bunker clinical trials)
- Frame-fit framework section on [[mind-body]] — strong enough now across batches 2 + 3
- Herxheimer-as-progress warning section — strong enough now across Becky + Glenn + Karen

Remaining: 24 Raelan transcripts (next: 0491, 0502, 0513, 0516, 0524, …).

## [2026-05-08] ingest-batch | Raelan Agle batch 4 — 10 episodes (RA #491–#581)

Batched 10 episodes. Major schema events + cross-corpus identifications:

**New patient interviews + new aggregate pages:**
- [[RA-0491-neal-cotter]] (LA, ~4y POTS LC) — **first [[epipharyngeal-abrasive-therapy]] on corpus** (Japanese vagus-nerve treatment, EAT/B-Spot, self-taught from a Japanese patient's home-practice video). Multi-component with Primal Trust + cranial-sacral.
- [[RA-0502-julien]] (Berlin, in-progress) — **first ketamine-infusion + body-therapy-felt-safety rows on corpus**. Drug-induced glimpses of recovery (smell/taste back transiently after SGB and ketamine) as proof-of-mechanism.
- [[RA-0513-melissa-mansfield]] (Brooklyn) — **first patient `key_to_recovery` for [[low-dose-naltrexone|LDN]] on the corpus.** Two NYC long-covid clinics failed her; patient-recommended doctor + careful LDN titration + 9 months radical rest + community.
- [[RA-0516-linley]] (NZ) — **first [[the-switch-mel-abbott]] anchor on corpus** (Mel Abbott's 4-day online program). Striking 2-week recovery timeline.
- [[RA-0534-troy-roach]] (Madrid) — **first HSP-as-predisposing-factor framing on corpus**. Citizen-scientist + nicotine-patch advocate. 80/20 pacing rule.

**Cross-corpus reaffirmations + identity disambiguations:**
- [[RA-0524-rachael-rebound]] = LCP #127, #168 (Rachael, Rebound Athletic). Coach-side perspective; Baseline Club launch.
- [[RA-0527-ellen-alden]] = **LCP #157 (the transcript-unavailable episode)**. Her substantive wiki content now lives at this Raelan ingest. **Bridges the LCP transcript gap.**
- [[RA-0546-jamie-waterhouse]] = LCP #186. Three-program-sequenced-stack articulation.
- [[RA-0579-alisha-braswell]] = LCP #178. Surname disambiguation; same TMS-lineage recovery.

**Major aggregate-page updates this batch:**
- [[low-dose-naltrexone]] +2 directional rows: **first patient `key_to_recovery`** (Melissa) + **strong harm-as-trigger row** (Susanna RA #581 — 3 weeks of LDN at age 20 triggered her 8-year ME/CFS arc). LDN counts now: 1 key_to_recovery / 2 helped_partial / 0 no_effect / 2 harmed / 4 recommended / 2 mentioned_only. **Sentiment moved from `helped-some` to `mixed`** — directional change.
- [[stellate-ganglion-block]] — Julien #502 `helped_partial` row pending (deferred backfill); now has `recommended` (3 LCP), `helped_partial` (Julien transient), `no_effect` (Karen #354). Variable-response pattern strong now.
- [[i-can-thrive]] (formerly Jason placeholder) — already updated in batch 3.

**New aggregate pages:**
- [[epipharyngeal-abrasive-therapy]] (EAT / B-Spot, Japanese)
- [[the-switch-mel-abbott]] (4-day online brain-retraining program)

### Patterns strengthening across batches

- **Cross-corpus identifications** — 4 in this batch alone (Rachael, Ellen, Jamie, Alisha). The corpus's same-person-across-shows handling is now well-validated. Wiki gap bridged for LCP #157 specifically.
- **Three-programs-sequenced** stacks (Jamie #186 / #546) are emerging as a distinct recovery template — Primal Trust foundation → Healing Dudes facing-fears → Lightning Process final-stretch. Worth tracking if other patients sequence similarly.
- **Post-recovery anxiety / lingering-fear-loop** — now a 5+ source pattern (Erik #150, Kristyna #147, Melissa #513, Jamie #546, Susanna #581). Strong enough for a dedicated section in [[mind-body]] alongside the frame-fit framework.
- **Patient-led research as the LC frontier** — fourth example added (Troy Roach + Tess Falor's Remission Biome). Pattern is now robust.
- **HBOT dual-edged** — Glenn #465's "RCT-supported but can permanently set you back" pairs with Rachael #524's "made me feel worse before better." Worth opportunistic update on the HBOT page.

### Eric-relevant signal from this batch

- **LDN now has a patient-credit `key_to_recovery` (Melissa)** but ALSO a strong harm-as-trigger row (Susanna). The wiki's earlier framing ("LDN is generally helped-some, dose carefully") now needs **stronger split-signal framing**: in established LC patients with careful titration LDN can be load-bearing; in pre-stress-loaded patients (especially being prescribed LDN for non-LC reasons like hormonal balance) it can push them over the edge. Eric's profile sits closer to Melissa's (established LC, considered as a treatment) than Susanna's (pre-LC, hormonal-balance trigger), so the directional update is actually positive for him — but Groysman's careful-titration protocol (LCP #91) becomes even more important.
- **HBOT: hold the candidate-with-discipline framing.** Glenn #465 + Rachael #524 + Hadanny LCP #153 all converge on "yes it works, careful with dose."
- **Epipharyngeal Abrasive Therapy (EAT)** is a new candidate worth holding for the *viral-persistence* axis if Eric ever wants to push that direction — nasopharyngeal viral reservoir thesis fits with the broader [[viral-persistence]] framing on the wiki. No US clinicians; home-practice variant exists; deep nasal swabbing technique.
- **Mel Abbott's *The Switch*** is now another brain-retraining option in the corpus's tree (joining ANS Rewire, Primal Trust, Gupta, DNRS, I Can Thrive, Joe Dispenza, Jason McAuliffe). 4-day intensive — good fit for someone who wants compression rather than month-long programs.
- **HSP framing (Troy)** is worth Eric checking — if HSP correlates with the LC/ME-CFS cohort at the rate Troy's polls suggest, knowing that about himself could inform brain-retraining-program-fit.

## [2026-05-08] ingest-pause | Raelan Agle batch — 31 of 44 ingested

20 of 31 are patient interviews; 5 are host-solo synthesis episodes; 1 is a course promo stub; 5 are cross-corpus reaffirmations of existing LCP guests (Lorrie #118, Amy Anker #280, Jackie #335, Rachael #524, Ellen #527 — and now Jamie #546 + Alisha #579).

New aggregate pages this batch: [[epipharyngeal-abrasive-therapy]], [[the-switch-mel-abbott]]. Aggregate updates touched: [[low-dose-naltrexone]] (directional — sentiment moved from helped-some to mixed).

**Deferred opportunistic-backfill candidates** (now substantial backlog):
- [[stellate-ganglion-block]] — Julien #502 helped_partial row
- [[meditation]], [[breathwork]], [[cold-water]] — multiple incremental rows across batches
- [[fasting]] page creation — now 3 sources (Adam #300, Glenn #465, Troy #534)
- [[primal-trust]] — Neal #491, Jamie #546 reaffirmation
- [[curable-app]] — Rachael #524 reaffirmation
- [[tms-mind-body-syndrome]] — Becky #309, Karen #354, Ellen #527, Alisha #579 — multiple rows pending
- Frame-fit framework section on [[mind-body]] — still deferred; pattern still strengthening
- Herxheimer-as-progress warning section on [[mind-body]] — strong enough; now Becky + Glenn + Karen + Susanna anchor it
- Post-recovery-anxiety pattern — could be its own theme page

Remaining: 13 Raelan transcripts (next: 0623, 0753, 0761, 0767, 0784, …).

## [2026-05-08] ingest-batch | Raelan Agle batch 5 (final) — 13 episodes (RA #623–#998)

Final batch. **44 of 44 transcripts now ingested.**

**Patient interviews:**
- [[RA-0623-miguel-bautista-qa]] — Miguel Bautista (founder of CFS Recovery). Hypersensitive nervous system + stress threshold + Golden Rule (respond well to symptoms). Created [[miguel-bautista]] + [[cfs-recovery-miguel-bautista]].
- [[RA-0767-dusty-dustin]] — **age 73-74, oldest recovered patient on the corpus.** California cyclist. 140 miles/week now.
- [[RA-0845-nate-singer]] — coach (Sayulita Mexico). Anti-checklist NS regulation. "Trauma + emotions aren't always the root cause."
- [[RA-0862-faith-canter]] — coach (Portugal). Multi-condition recovery (ME/CFS + autoimmune + heart + thyroid). "Hidden fuels" framing.
- [[RA-0864-devon-carter-tips]] + [[RA-0984-devon-carter-recovery]] — Devon Carter (Victoria BC), lead coach in Raelan's Brain Retraining 101. **"Life looked fine on paper" anchor articulation** for patients whose pre-illness stress wasn't externally visible.
- [[RA-0931-chelsea-verbeek]] — Edmonton AB, vaccine-injured 2021, wheelchair-bound ~1 year, recovered via Primal Trust + The Switch stack. **First doctor-recommended-brain-retraining anchor on the corpus.**

**Cross-corpus reaffirmations:**
- [[RA-0821-suzy-bolt]] = LCP #007/#064/#094 (Brighton UK). "Being seen" as recovery input.
- [[RA-0961-karen-wright]] = LCP #182 (NHS physiotherapist who ran an LC service then got LC).

**Host-solo synthesis:**
- [[RA-0753-emotional-reservoir]] — emotional reservoir / Nicole Sachs's beaker as the often-missed second step.
- [[RA-0761-how-to-know-fully-recovered]], [[RA-0784-why-still-stuck]], [[RA-0998-what-worked-for-thousands]].

### Final-state patterns across all 44 Raelan ingests

- **Cross-corpus identifications: 9 total** (Lorrie #118, Amy Anker #280, Jackie #335, Rachael #524, Ellen #527 = LCP #157, Jamie #546, Alisha #579, Suzy Bolt #821, Karen Wright #961). The wiki bridges the LCP #157 transcript-unavailable gap. Same-person-across-shows handling fully validated.
- **Brain-retraining-program-stacking** is the dominant Raelan-recovery pattern. Jamie sequenced 3 programs; Chelsea stacked 2; Matt stacked 4 components; Devon Carter combined PRT + Brain Retraining 101. **Recommendation tree should reflect this**: brain-retraining is rarely one program — typically 2–3 stacked or sequenced.
- **Frame-fit framework** confirmed across all 5 batches.
- **Post-recovery anxiety / lingering-fear-loop** is universal (6+ explicit data points in Raelan corpus alone).
- **Coach-side insider perspective** now well-represented (Miguel, Mel Abbott, Jason McAuliffe, Cat King, Suzy Bolt, Faith Canter, Nate Singer, Devon Carter, Lorrie Rivers, Pamela Rose).
- **First on corpus this final batch**: doctor-recommended-brain-retraining (Chelsea); oldest recovered patient (Dusty 73-74).

### Eric-relevant final signal

1. **Brain-retraining-program-stacking matters for Eric**: if ANS Rewire is the wiki's strongest single-program signal, the Raelan corpus suggests it's likely *not the only program* he'll benefit from. Expect to layer in TMS reading (Sachs/Buglio/Sarno), Curable, or a cohort-style program like Brain Retraining 101.
2. **Frame-fit determines whether techniques land** — if ANS Rewire doesn't click within a few weeks, switch frames rather than push harder.
3. **LDN signal moved to `mixed`** — Eric's profile fits Melissa's (positive) more than Susanna's (harm-trigger), but Groysman's careful titration protocol (LCP #91) becomes even more important.
4. **HBOT dual-edged signal hardens** — hold as candidate with discipline.
5. **EAT (epipharyngeal abrasive therapy)** — new candidate for the viral-persistence axis.
6. **Patient-led research** is the actual LC frontier (Tom Bunker, Glenn Chan, Tess Falor).
7. **HSP framing (Troy)** is worth checking — could inform brain-retraining-program-fit.
8. **"Life looked fine on paper" pattern (Devon Carter RA #984)** — fits Eric's high-functioning Grasp founder profile; pre-illness stress wasn't externally visible.
9. **Post-recovery anxiety is universal** — expect it as part of any future recovery transition.
10. **Age is not a barrier** (Dusty 73-74) — useful for any future "too late" self-talk.
11. **Doctor-recommended-brain-retraining (Chelsea, Edmonton)** — useful citation for any clinician conversation if Eric's Swedish team is sceptical.

## [2026-05-08] checkpoint | Raelan Agle batch — 44 of 44 ingested ✓ (full Raelan corpus indexed)

**Total Raelan corpus state:**
- 44 episodes ingested across 5 batches in this session
- ~33 patient interviews + 9 host-solo + 2 hybrid (return-coach Q&A)
- 9 cross-corpus reaffirmations (LCP guests appearing on Raelan's channel)
- ~25 new person pages + ~22 new recovery-story pages
- 9 new aggregate pages: [[gentle-movement-restorative]], [[joe-dispenza-method]], [[healing-codes-trilogy]], [[kambo]], [[covid-vaccine-post-acquisition]], [[i-can-thrive]] (formerly placeholder), [[epipharyngeal-abrasive-therapy]], [[the-switch-mel-abbott]], [[cfs-recovery-miguel-bautista]]

**Aggregate updates with directional changes:**
- [[low-dose-naltrexone]] sentiment: `helped-some` → `mixed`
- [[gupta-program]] +1 `no_effect` (Roberto)
- [[meditation]] +1 `key_to_recovery` (Kyle)
- [[breathwork]] +1 `key_to_recovery` (Roberto)
- [[yoga]] +1 `key_to_recovery` (Roberto)
- [[ans-rewire]] +1 `key_to_recovery` (Erik) — 3rd on corpus
- [[low-histamine-diet]] +1 `no_effect` (Kyle)
- [[pacing]] theme: added pacing-as-fear-amplifier failure-mode section
- [[emdr]] +1 `helped_partial` (Roberto, healthcare-worker-trauma anchor)
- [[lightning-process]] +1 `helped_partial` (Matt, intro-audio-only variant)
- [[dynamic-neural-retraining-system]] +1 `helped_partial` (Matt)
- [[optimal-health-clinic]] +1 `helped_partial` (Donna)

**Status: Raelan 44/44 ✓. Combined corpus: LCP 211/211 + Raelan 44/44 = 255 episodes indexed.**

## [2026-05-19] ingest | LCP #214 — Out of the Long Covid Maze: How Lalita Found Her Way Back to Health

- New episode page: [[214-lalita-neuroplasticity-recovery]] (under `wiki/episodes/lcp/` — first ingest in the new subfolder location)
- New person page: [[lalita]] (neuroplasticity coach, Tasmania; Schubiner-trained)
- New recovery-story page: [[lalita]] — full recovery in 12-14 months, second NS-led rebuild
- New intervention pages: [[bowen-therapy]], [[bio-resonance-therapy]], [[nattokinase]] — all first-mentions on the wiki
- [[breathwork]] +1 `key_to_recovery` (Lalita; 5th `key_to_recovery` row — strongest articulation yet of breath-as-active-NS-tool combined with self-talk inside the breath cycle)
- [[eaet]] +1 `helped_partial` (Lalita; first patient-application row alongside Kennedy's clinical row — distinct use-case: dig-deeper for repeating symptom patterns)
- [[eft-tapping]] +1 `helped_partial` (Lalita; stacked with breath + self-talk)
- [[somatic-tracking]] +1 `helped_partial` (Lalita; supportive rather than load-bearing)
- [[yoga-nidra]] +1 `helped_partial` (Lalita; nightly anchor)
- [[antihistamines]] +1 `helped_partial` (Lalita; **specifically credited for resolving tinnitus** — novel claim for the tinnitus page)
- [[cranial-sacral-therapy]] +1 `helped_partial` (Lalita; parasympathetic-bodywork framing)
- [[quercetin]] +1 `mentioned_only`; [[curcumin]] +1 `mentioned_only` (Lalita's naturopath stack)
- [[pots]] +1 row (Lalita; POTS resolved early in her NS-led recovery, no pharmacology)
- [[tinnitus]] symptom page: **added antihistamines + NS-protocol approaches** (previous version only had hearing aids / CBT / sound therapy / SGB)
- [[dysautonomia]] +1 anchor row (Lalita)
- [[neuroplasticity]] theme: added #214 as second wiki recovery directly trained in Schubiner's method
- [[self-compassion]] theme: added the "self-compassion inside the breath cycle" framing (vs separate practice)
- [[mind-body]] theme: added #214 — breath-led variant of the Sarno/Schubiner/Gordon lineage
- [[howard-schubiner]] person page: added Lalita as wiki appearance; added 5/7 Fs framework to notable claims

**Status: LCP 212/212 ✓ (#1–#214 minus #31 & #157). Raelan 44/44 ✓. Combined corpus: 256 episodes indexed.**

## [2026-05-21] ingest | LCP #215 — Jackie host-solo: Overwhelm 101: Why Your System Says "Too Much"

- New episode page: [[215-jackie-overwhelm-101]] (host-solo educational, 20:21)
- [[self-compassion]] theme: added LCP-215 as anchor — "capacity-not-character" reframe + the 7-tool list as a concrete operationalisation of self-compassion
- [[somatic-tracking]] +1 `recommended` (Jackie host-solo, longer-term tool for meeting sensations with curiosity); mention_count 4 → 5
- [[breathwork]] — added reaffirmation note to existing Jackie row (NOT a new row, per "same speaker, same intervention, same outcome rule"). Added LCP-215 to episodes array. Key novel framing captured: *"micro pause = one soft breath out, NOT a deep breath"* — explicit correction to the common "take a deep breath" advice that worsens overbreathing
- Index updated; status moved to LCP 213/213

**Cross-source note**: Jackie's three-state framing in this episode is the same teaching as her Advent Calendar #16 on the breathing channel (`long-covid-breathing/wiki/concepts/vagus-nerve.md`). The podcast version is more polished and condensed; both anchor the same polyvagal-applied framework.

**Status: LCP 213/213 ✓ (#1–#215 minus #31 & #157). Raelan 44/44 ✓. Combined corpus: 257 episodes indexed.**

## [2026-05-25] query | severe headaches/migraine — what helped for Eric's friend

Filed `wiki/queries/headaches-and-migraine-what-helped.md`. Synthesised 17 episodes (15 LCP + 2 Raelan). Strongest specific protocol: B2 400 mg + magnesium daily (Teitelbaum LCP #167, cites 67–70% migraine-frequency reduction). Strongest device evidence: non-invasive vagus stimulation (Bagnell LCP #63). Strongest patient-recovery pathway: nervous-system / brain-retraining work — Natalie Gold (LCP #189), Rebecca Tolin (LCP #166), Esther (LCP #32) all resolved chronic migraine alongside LC. MCAS overlap → H1+H2 antihistamines (Peers LCP #38, Saperstein LCP #68). Negative signals: triptans when not really migraine (Chiara LCP #3), OTC painkillers (Rosie LCP #61), repeated antibiotics for assumed sinus infection (Devon Carter RA #984).

## [2026-05-26] update | headache/migraine backfill — new symptom page + 3 intervention pages + pain.md expanded

Diagnosed an indexing-synthesis gap raised by Eric: per-episode pages had headache/migraine content extracted, but the aggregator layer was missing — no symptom page, no specific-protocol pages, and `pain.md` had only one row.

**Created**:
- `wiki/symptoms/headache-migraine.md` — 16-row evidence log spanning 17 episodes (15 LCP + 2 Raelan). Anchored on Teitelbaum #167 (B2/magnesium/triptans), Ravindran #53 (nociplastic), Bagnell #63 (gammaCore/brain-stem), Natalie Gold #189 (key_to_recovery alongside LC recovery), Tolin #166 (key_to_recovery), Esther #32 (key_to_recovery, mind-body).
- `wiki/interventions/vitamin-b2-riboflavin.md` — Teitelbaum 400 mg/day × 6 weeks protocol; 67–70% migraine-frequency reduction.
- `wiki/interventions/magnesium.md` — 5-row evidence log; uses across migraine, POTS, mitochondrial, sleep.
- `wiki/interventions/triptans-imitrex.md` — Teitelbaum's early-dose protocol + two cautionary no_effect rows (Chiara #3 misdiagnosis, Devon Carter RA #984 ER misapplication).

**Expanded**:
- `wiki/symptoms/pain.md` — evidence log went from 1 row to 12; added Teitelbaum's 7-subtype framing alongside Ravindran's nociplastic-only; counts: 3 key_to_recovery / 2 helped_partial / 6 recommended / 1 mentioned_only.
- `wiki/interventions/ice-packs-temperature.md` — added Rosie #61 row for migraine symptom relief.
- `wiki/interventions/vagus-nerve-tens.md` — updated Bagnell #63 row indication to include migraine + cluster-headache explicitly.
- `wiki/interventions/homeopathy.md` — expanded Schrock #210 row with the specific migraine-patient case.
- `wiki/interventions/acupuncture.md` — Elizabeth So #124 row updated with her pre-LC migraine self-treatment.
- `wiki/index.md` — symptoms section + interventions section + filed-queries section updated.

**Root cause of the gap**: per-episode extraction picked up headache mentions (they made it into `symptoms_discussed:` arrays), but no aggregator pages existed for headache/migraine, so the synthesis layer had nowhere to land them. Profile-bias (Eric: POTS+PEM+MCAS, not migraine) contributed but wasn't the primary cause.

## [2026-05-28] update | supplement coverage gap-fill — 10 new pages + 4 rebuilds

Triggered by Eric's request to look for supplements potentially missed by the initial ingest (he's considering adding supplements to his regimen and wanted a complete picture). Sweep grepped ~130 supplement-related keywords across all 255 transcripts; report identified Tier A gaps (electrolytes, CoQ10, B12, glutathione) and materially under-counted existing pages (vitamin D 2→16, zinc 1→6, magnesium 5→11, melatonin 1→3).

**New intervention pages (10)**:
- `electrolytes.md` — 14 mentions; 2 helped_partial / 7 recommended / 5 mentioned_only. Most consistently *recommended* non-drug POTS intervention in the corpus. **Eric-relevant — actively titrating per memory.** Distinct from [[salt-loading]] and [[oral-rehydration-solution]].
- `coq10.md` — 4 recommended. Clinician-stack anchor (Myhill, Teitelbaum, Putrino, Galland). Floor, not lever.
- `glutathione.md` — 1 harmed (RA #546 Jamie) + 6 recommended. Cross-ref [[nac-max]] (Driscoll's product *recycles* glutathione).
- `alpha-lipoic-acid.md` — 1 recommended (Teitelbaum #167 nerve-pain pairing with ALCAR). Thin. Filtered out LCP #33 false positive (auto-caption mangling of "lipoteichoic acid" not "lipoic acid").
- `acetyl-l-carnitine.md` — 3 recommended. ALCAR + L-carnitine in one page; vegetarian heads-up.
- `vitamin-b12.md` — 2 helped_partial (Sarah #114 high-dose injections + Rachel #8 4-item-cull retainer) / 2 recommended. **Strongest of the new micronutrient pages.**
- `folate-methylfolate.md` — 1 mentioned_only (Spechler #129). Thin.
- `thiamine-b1.md` — 2 (Myhill mito-stack + Rivers RA #118). The broader Lonsdale/Overton TTFD community signal is absent from corpus — that absence is data.
- `iodine.md` — 2 (Myhill #118 + Littlewood #45). Outlier framing; not echoed.
- `selenium.md` — 1 recommended / 1 no_effect (Groysman #91 for LC hair loss) / 1 mentioned_only. Thin with one explicit negative row.

**Rebuilt existing pages (4)**:
- `vitamin-d.md` — 2 → 16. All clinician-recommended (Stewart, Galland, Dempsey, Myhill, Bailey, Groysman, Krick, Taylor, Joffe, Littlewood, Gerlach). No patient `key_to_recovery`. Bailey #163 anti-megadose voice now captured. Includes Dempsey #88 MCAS excipient-not-vitamin caveat.
- `zinc.md` — 1 → 6. Bailey #162/163 anchor (zinc sulfate 7 mg 2×/day + vit C + lysine immune trio); Jamie #186 placebo-frame helped_partial (reaffirmed RA #546); copper-balance + check-serum cautions.
- `magnesium.md` — 5 → 11. Preserved existing 5 rows; added Joffe #143 (restless-legs/dopamine), Bailey #163 (foundational glycinate), Donna Shaw RA #228 (Epsom-salt baths, helped_partial), Kelly Mitchell #12 (electrolyte mechanism), Spechler #129 (dietary), Kristine RA #226 (mentioned_only).
- `slow-release-melatonin.md` — 1 → 3. **Rescoped to broader "Melatonin"** (filename kept to preserve inbound links; `title:` changed). Added Teitelbaum #167 (EP120 sustained-release) and Spechler #129 (serotonin-melatonin tryptophan-pathway mechanism). Kept Joffe #143 low-dose slow-release as named subsection.

**Cross-source observations**:
- Raelan corpus is supplement-light — only 3 RA rows across all 14 pages this batch (Donna Shaw magnesium Epsom; Jamie glutathione harmed + RA #546 zinc reaffirmation; Kristine RA #226 magnesium mentioned). Reinforces the Raelan source-bias documented in CLAUDE.md: recovery narratives there are dominated by brain-retraining / nervous-system work, not supplement stacks.
- Zero patient `key_to_recovery` rows across the entire 14-page batch. Supplements in this corpus are clinician floor, not patient lever. **The strongest patient signal in this batch is `helped_partial`** (B12 ×2, electrolytes ×2, magnesium ×2).
- Only explicit `harmed` row: Jamie/glutathione (RA #546) — IV glutathione + vit C "didn't do anything, in fact I think made me worse" pre-Clinic-19.
- Only explicit `no_effect` row: Groysman/selenium for LC hair loss (#91).
- Recurring "mitochondrial stack" clinician pattern (Teitelbaum/Myhill/Galland/Putrino): Mg + CoQ10 + ALCAR + B-vitamins + D-ribose. Now properly cross-linked across pages.

**Process notes**: First parallel run (4 sub-agents) crashed mid-session — only electrolytes + vitamin-d + zinc survived. Second pass ran the remaining 3 cluster-agents sequentially, which worked. All 14 pages verified for counts integrity (frontmatter `counts:` block sums to evidence-log row count).
