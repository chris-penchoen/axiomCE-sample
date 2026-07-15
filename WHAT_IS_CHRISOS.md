# What ChrisOS Is

ChrisOS is a **model-agnostic operating environment for durable human–AI collaboration**.

It is not an AI model, a chatbot, a vector database, or an agent framework. It is the persistent layer that sits around those systems so accumulated context and collaboration practices are not trapped inside any one vendor's hidden state.

ChrisOS asks two separate questions:

1. **What is true about the human and their world?**
2. **How should an AI collaborate effectively with that human?**

Those questions have different evidence models and therefore different architectures.

## Knowledge pillar

The knowledge pillar manages factual and temporal state:

- immutable source material;
- atomic claims;
- stable entity identifiers;
- provenance;
- contradiction preservation;
- valid time versus learned time;
- confidence labels;
- reconciliation;
- generated human-readable views.

Old facts are not silently overwritten. Conflicting claims can coexist until evidence supports resolution.

## Cognitive-model pillar

The cognitive-model pillar describes collaboration policy:

- delivery expectations;
- decision heuristics;
- recurring friction;
- optimization priorities;
- interaction rules;
- model-specific presentation adapters;
- calibration cases showing poor versus preferred output.

Each policy rule has one authoritative owner and a stable identifier so examples and evaluations can reference it without duplicating it.

## Evaluation status

The architecture includes a human-governed evaluation design. Model outputs may be compared against policy and calibration cases, but model-generated scores remain estimates until human-ratified.

The evaluation loop is designed, not yet an autonomous operating subsystem.
