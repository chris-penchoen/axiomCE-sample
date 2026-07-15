---
title: Cognitive Model — Collaborator Operating Model (sample)
type: index
classification: personal
created: 2026-07-15
updated: 2026-07-15
status: active
---

# cognitive-model/ — how an AI should collaborate with the owner (sample)

> **Fictional, public-safe example.** This is a minimal, illustrative cognitive
> model for the Acme demonstrator. It shows the shape of the collaboration plane,
> not a real person's preferences.

This directory is the **collaboration plane** (the canon's term; "cognitive-model
pillar" is the implementation alias). It holds the durable knowledge of *how* an
AI should reason with, communicate with, and deliver to the owner — distinct from
*what* is known about the owner's world (the knowledge plane).

The two pillars are **different governance layers** and must not be merged:

- [`axiomCE/AGENTS.md`](../axiomCE/AGENTS.md) (via the framework submodule)
  governs **how agents work on this repository**.
- **This pillar** governs **how agents work with the owner** (delivery,
  decisions, friction, priorities, interaction).

Confidence here is **behavioral**: validated by repeated successful
collaboration — corrections and calibration — not by external evidence.

## Structure

- `policy/` — normative interaction/delivery rules with stable `CM-*` IDs.
- `calibration/cases/` — worked examples that ratify the policy.
- (`adapters/`, `evaluation/` — omitted in this minimal sample.)

Structural checks: `node axiomCE/tools/validate-cognitive.mjs`.
