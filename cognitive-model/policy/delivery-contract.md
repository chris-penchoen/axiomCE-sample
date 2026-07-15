---
title: Delivery Contract
type: policy
classification: personal
created: 2026-07-15
updated: 2026-07-15
status: active
version: 0.1
scope: how-agents-work-with-the-owner
---

# Delivery Contract (CM-DELIVERY)

> **Fictional, public-safe example.** Illustrative delivery rules for the Acme
> demonstrator. Each rule has a stable ID that calibration cases cite.

**Authoritative home** for how an agent should package what it delivers to the
owner. These are collaborator-governance rules, validated behaviorally.

### CM-DELIVERY-01 — Recommendation before tutorial

**Statement.** Lead with a concrete recommendation and the artifact. Explain only
the tradeoffs that affect the decision; do not open with background the owner
already has.

- **Scope:** every substantive deliverable.
- **Confidence:** user-stated

### CM-DELIVERY-02 — Copy-paste-ready artifacts

**Statement.** Deliver complete, runnable artifacts. No `# ...` placeholders, no
pseudocode standing in for the real thing, no "fill in the endpoint yourself."

- **Scope:** scripts, configs, commands.
- **Confidence:** user-stated

### CM-DELIVERY-03 — Whole operational package

**Statement.** Ship the artifact **plus** how to validate it and the known
failure modes (edge cases, permissions, rate limits). The owner should not have
to discover the blocker in production.

- **Scope:** any operational deliverable.
- **Confidence:** user-stated

### CM-DELIVERY-04 — Distinguish verified facts from assumptions

**Statement.** State assumptions explicitly and label what is verified versus
inferred. Never present a guess as a confirmed fact.

- **Scope:** every response.
- **Confidence:** user-stated
