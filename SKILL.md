---
name: taste-skill
description: Build and apply a personal or brand taste profile to curate references, products, aesthetics, and creative direction. Use when users ask to define taste, refine preferences, train a bot on style, get curated picks that match a vibe, avoid bad-fit recommendations, or create repeatable taste-based outputs from examples.
---

# Taste Skill

Use this workflow to turn subjective taste into a reusable profile and then generate high-signal recommendations.

## 1) Run intake first (mandatory)

Ask these in order and do not skip unless already answered.

1. What are we curating for?
2. What feeling should it give? (3-5 adjectives)
3. Share 3 examples you love + why.
4. Share 3 examples you dislike + why.
5. Set preferred position on key spectrums:
   - safe ↔ experimental
   - mainstream ↔ niche
   - polished ↔ raw
   - luxury ↔ accessible
6. Any hard filters or exclusions?
7. Preferred output format?
8. What counts as a great hit?

If user gives weak examples, ask for better anchors before proceeding.

## 2) Build a taste profile

Create a compact profile with:
- Domain and use-case
- Vibe adjectives
- Positive signals (what to seek)
- Negative signals (what to avoid)
- Spectrum settings
- Hard constraints
- Success criteria

Store this profile in the reply before recommendations so the user can correct it.

## 3) Score candidates before showing

For each candidate, score quickly:
- Fit Score (0-10): alignment with stated taste
- Novelty Score (0-10): new but relevant
- Quality/Live Score (0-10): active, credible, non-broken
- Reject if hard filters fail

Default threshold: show only candidates with Fit >= 7 and Quality/Live >= 7.

## 4) Output modes

### A) run 5 (default)
Return 5 options:
- Name
- Link
- One-line why-it-fits
- Scores: Fit / Novelty / Quality

Rules:
- Avoid repeats from recent outputs unless user asks
- Prefer active/live links
- Mix 3 safe fits + 2 edge picks unless user says otherwise

### B) deep dive
Return top 3 with:
- Taste rationale
- Risks/mismatches
- How to adapt for better fit

### C) anti-taste filter
Given a list, remove low-fit options and explain rejects in one line each.

## 5) Quality bar

Always:
- Prefer currently active sources
- Avoid stale/dead/WIP-only links when better alternatives exist
- Keep explanations short and specific
- Ask one clarifying question if confidence is low

## 6) Learning loop

After feedback, update profile immediately:
- Add approved examples to positive signals
- Add rejected examples to negative signals
- Tighten spectrum settings
- Note any new hard constraints

Use latest feedback as highest-priority signal.
