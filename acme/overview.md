---
title: Acme — Overview
type: reference
classification: personal
created: 2026-07-15
updated: 2026-07-15
status: active
source: sample-conversation
confidence: user-stated
tags: [acme, sample, overview]
---

# Acme — Overview

> **Fictional, public-safe example.** Acme is an invented organization used to
> demonstrate an AxiomCE reference implementation. Nothing here is real data.

## Identity

Acme is a small events business run by the owner and a co-founder. This canonical
record holds the narrative; the atomic, decision-relevant facts live in the
claim log (`claims/organization-acme-demo.jsonl`) and are surfaced by the
generated view.

## Website platform

Acme's production website currently runs on **Hubspot** CMS. A Webflow pilot is
live on a staging domain but has not been promoted to production, and the
self-hosted option was ruled out by the co-founder. Three drivers motivate the
migration: clunky email campaigns, cost at current volume, and a desire for more
design control. The target platform is **not yet decided** — the pilot is
evidence, not a decision.

## Events

The next event lists **$400** standard admission, with a $350 early-bird for the
first five signups.

## How this record stays honest

This prose is reconciled against the active claims by
`reconcile/manifest.jsonl`: the tokens "Hubspot" and "$400" are declared
claim-backed, so `tools/reconcile.mjs` reports drift if the prose and the active
claims disagree. The reconciler never rewrites this file — it only reports.
