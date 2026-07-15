---
title: axiomCE-sample
type: index
classification: public
created: 2026-07-15
updated: 2026-07-15
status: sample
---

# axiomCE-sample

**A public, data-free sample reference implementation of [AxiomCE](https://github.com/chris-penchoen/axiomCE) — the Axiom Continuity Engine.**

This repository demonstrates the AxiomCE knowledge loop end to end using a
small, **fictional** organization ("Acme"). It contains no private data. Its
purpose is to show *how the engine behaves once populated* — not to be a useful
personal instance.

## Where this sits: the three layers

- **[axiom](https://github.com/chris-penchoen/axiom)** — the invariant theory
  (the Canon). Included here as the `axiom/` submodule.
- **[axiomCE](https://github.com/chris-penchoen/axiomCE)** — the Continuity
  Engine that operationalizes Axiom: schema, tools, governance templates.
  Included here as the `axiomCE/` submodule.
- **axiomCE-sample** (this repo) — a reference implementation that *consumes*
  both as dependencies and adds fictional data.

## Getting the dependencies

This repo uses git submodules. Clone with:

```sh
git clone --recurse-submodules https://github.com/chris-penchoen/axiomCE-sample.git
# or, after a plain clone:
git submodule update --init --recursive
```

## What's here

```
axiom/                     # submodule — the Canon (theory)
axiomCE/                   # submodule — the engine (schema, tools, governance)
acme/overview.md           # canonical narrative for the demo organization
sources/                   # immutable provenance records (a conversation + an inventory)
claims/                    # append-only atomic facts (JSONL)
entities/                  # stable identity anchors
reconcile/manifest.jsonl   # declares which canonical fields are claim-backed
cognitive-model/           # collaboration plane: policy + one calibration case
views/                     # generated (git-ignored; run the tool to build them)
```

The engine's tools live in the `axiomCE/` submodule and operate on this repo's
data (they scan the current working directory).

## Run the loop

From the repository root:

```sh
# 1. Build the generated views from the claim log:
node axiomCE/tools/generate-views.mjs

# 2. Validate everything:
node axiomCE/tools/validate.mjs            # Markdown front matter + links
node axiomCE/tools/validate-claims.mjs     # claim schema + entity/supersedes refs
node axiomCE/tools/privacy-check.mjs       # leak scan
node axiomCE/tools/validate-cognitive.mjs  # policy rule IDs + calibration refs
node axiomCE/tools/reconcile.mjs           # canonical prose vs. active claims

# Run the engine's own test suite:
node --test axiomCE/tools/*.test.mjs
```

## What the sample demonstrates

- **Provenance:** every claim links back to a source record.
- **Contradiction without adjudication:** a `$400` standard price and a `$350`
  early-bird coexist as distinct predicates.
- **Supersession + confidence upgrade:** a `user-stated` price is superseded by a
  `confirmed` one after a firsthand observation.
- **Retraction as history:** a "Webflow selected" claim is retracted (the pilot
  was never a decision) and preserved in the view's history section.
- **Reconciliation:** `reconcile/manifest.jsonl` ties canonical prose to the
  active claims so drift is reported, never silently rewritten.
- **The collaboration plane:** a delivery-contract policy with stable `CM-*` IDs
  and a calibration case that cites them.

## License

See [LICENSE.md](LICENSE.md).
