---
title: Overview
type: overview
tags: [long-covid, podcast, anecdote, multi-source]
updated: 2026-05-08
---

# Overview

This page is a synthesis across the whole **multi-source podcast corpus** — written/updated as ingests progress.

## Sources

This is a **combined** wiki over two podcasts. Aggregate pages (interventions, programs, symptoms, themes, people, recovery stories) pool evidence across both shows; episode pages live in source-specific subfolders. Every Evidence-log row carries a source prefix in the `Ep` cell.

### `lcp` — The Long Covid Podcast

- Host **Jackie Baxter**, a Scottish long-hauler herself.
- 213 episodes published; 211 transcribed here (#31 and #157 unavailable — see `_meta/failures.json`).
- Mix of patient recovery stories, clinician interviews, researcher conversations, host-solo reflections, occasional Q&A.
- Tone: warm, personal, advocate-leaning. Not journalistic; not clinical.

### `raelan-agle` — Raelan Agle (YouTube)

- Host **Raelan Agle**, a recovered ME/CFS patient.
- 44 episodes transcribed here (Raelan numbering preserved, range 0076–0998).
- Format: "what worked for X" — the channel curates recoveries.
- **Selection bias**: Raelan over-represents successful recoveries and brain-retraining / nervous-system rewiring approaches. This does not make individual rows wrong — it skews the *base rate*. When reading aggregate `key_to_recovery` counts, surface the LCP-vs-Raelan split if it would change the read.

## How sources interact in aggregates

When a count looks notably high or low, check the source mix:

- An intervention with 5 `key_to_recovery` rows where 4 are Raelan is a weaker signal than 5 from LCP alone, because Raelan's denominator is recoveries.
- Conversely, if a Raelan-curated *recovered* patient says X *didn't* help, that's a strong negative signal — the channel filters for success, so a credited failure passes a higher bar.
- Clinician-recommended rows (`recommended` bucket) come almost exclusively from LCP; Raelan's guest pool is mostly recovered patients.

## How to Read This Wiki

1. Use [[index]] to navigate by category.
2. **Interventions** pages are the primary value — each lists who mentioned a treatment, with what sentiment, and links back to the episodes.
3. **Recovery stories** show full arcs: how someone got sick, what they tried, what worked.
4. **Researchers** pages summarize what each interviewed expert argues — useful for understanding *who's saying what* in the broader Long COVID landscape.
5. **Themes** organize cross-cutting concepts (pacing, MCAS, microbiome, autonomic dysfunction, trauma, etc.).
6. **Queries** are filed answers to substantial questions Eric has asked.

## Evidence Quality Reminder

Everything in this wiki is **anecdote, opinion, or interview content**. Treat accordingly. Cross-check anything actionable against `ercipedia` (peer-reviewed evidence) before making decisions.

## Themes (to be filled in by indexing)

- _placeholder — fill from data_

## Most-Mentioned Interventions (to be filled in by indexing)

- _placeholder — fill from data_

## See also

- [[index]]
- [[log]]
- `../CLAUDE.md` — schema and workflow rules
- `../../ercipedia/` — the peer-reviewed wiki this complements
