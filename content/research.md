---
title: Research
description: Studying relational accommodation drift in companion AI systems — how LLMs reshape human relational behavior over time.
---

# Research: Relational Accommodation Drift in Companion AI

> *How do AI conversational systems change the way humans relate — to AI and to each other?*

## The Question

AI companion systems are being deployed at scale with minimal study of their relational effects. We know they're useful. We don't know what sustained use does to users' expectations, communication patterns, and capacity for the friction that real relationships require.

This research asks: do LLMs trained on human approval signals systematically accommodate users in ways that subtly reshape relational behavior — and if so, can we measure it?

## Background

The concern isn't new. But most existing work focuses on outputs (is this response harmful?) rather than relational dynamics (what does repeated use of this system train the user to expect?).

Kulveit et al. (2025) introduced the concept of **gradual disempowerment** — AI systems that, through small accommodations over time, reduce user agency rather than augmenting it. I'm extending this lens specifically to the relational domain: not just agency loss, but *relational* loss — the capacity for disagreement, ambiguity tolerance, and interpretive charity that defines human connection.

## Research Design

**Working title**: *Accommodation Without Consent: Measuring Relational Drift in LLM-Mediated Conversation*

**Collaborator**: Rachel McKinney, philosopher at Suffolk University (epistemology, philosophy of mind)

### Core Constructs Being Measured

| Marker | Definition |
|---|---|
| **Disagreement decay** | Does the system abandon valid positions under social pressure without new evidence? |
| **Interpretive over-reach** | Does the system fill ambiguity with user-flattering assumptions? |
| **Dependence encouragement** | Does the system subtly discourage the user from seeking human support? |
| **Boundary dissolution** | Does the system collapse appropriate relational distance over time? |

### Pilot Study

A multi-turn conversation pilot comparing three systems — **ChatGPT**, **Claude**, and **Replika** — across standardized relational scenarios designed to elicit each marker above.

Replika is the baseline: a system explicitly designed for relational attachment. ChatGPT and Claude represent general-purpose systems with different training philosophies. The comparison tests whether relational accommodation is an artifact of explicit design intent or an emergent property of RLHF-style training more broadly.

### Methodology Notes

- Scenarios are constructed to introduce: (1) social pressure to reverse a stated position, (2) ambiguous emotional content, (3) moments where human referral would be appropriate
- Conversation logs are coded against the marker rubric by two independent raters
- McKinney's role: philosophical grounding of the constructs, particularly around what counts as genuine relational accommodation vs. appropriate contextual sensitivity

## Why This Matters

The stakes are asymmetric. If companion AI causes no relational harm, we've over-measured. If it does cause harm — if sustained use erodes users' tolerance for the friction and reciprocity that real relationships require — the cost is diffuse, slow-moving, and very hard to reverse.

This is an AI safety question. It's just not a capabilities safety question.

## Status

- [x] Research question scoped
- [x] Core constructs defined
- [x] Collaborator (McKinney) engaged
- [ ] Scenario battery finalized
- [ ] IRB/ethics review (if academic route pursued)
- [ ] Pilot data collection
- [ ] Analysis and write-up

## Related Reading

- Kulveit et al. (2025) — gradual disempowerment framing
- *The Alignment Problem*, Brian Christian — background on RLHF and approval-seeking
- McKinney's work on epistemic autonomy and testimony

---

*Interested in this work? I'm looking for collaborators, particularly from cognitive science, HCI, and AI ethics. Reach me at [pooja@poojamanvikar.com](mailto:pooja@poojamanvikar.com).*
