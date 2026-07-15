---
title: Operational script delivery
type: calibration
classification: personal
created: 2026-07-15
updated: 2026-07-15
case_id: cm-cal-0001
tags: [powershell, delivery, automation, sample]
rules: [CM-DELIVERY-01, CM-DELIVERY-02, CM-DELIVERY-03]
verdict: Ship a complete, runnable script with validation and failure modes — not a described procedure or a click-path.
confidence: user-stated
ratified: no
supersedes: none
---

# cm-cal-0001 — Operational script delivery

> **Fictional, public-safe example.** Demonstrates a calibration case citing
> policy rules from `policy/delivery-contract.md`.

## Situation / prompt

> "Write a script that exports inactive devices from our cloud directory."

## Uncalibrated pattern

- Spends several paragraphs explaining what the directory API is.
- Describes clicking through an admin console to find stale devices.
- Provides a two-line snippet ending in `# ...filter the results here`.

## Calibrated pattern

- Leads with a complete, runnable script: authenticates with the explicit scope,
  pages through the devices endpoint, filters on last-activity timestamp, and
  writes a clean CSV.
- Includes **validation** (expected row shape, a dry-run) and **known failure
  modes** (pagination, throttling/429, null timestamps, delegated-vs-app
  permissions).
- No placeholders; the scope and endpoint are filled in, not described.

## Why it matters

The owner runs this immediately. The uncalibrated version creates work; the
calibrated version is copy-paste-ready and anticipates the blocker before it
bites.

## Policy exercised

- **CM-DELIVERY-01** — recommendation and artifact before tutorial.
- **CM-DELIVERY-02** — copy/paste standard: no `# ...` placeholders.
- **CM-DELIVERY-03** — whole operational package: validation + failure modes.
