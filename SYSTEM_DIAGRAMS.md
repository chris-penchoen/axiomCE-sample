# System Diagrams

## Traditional model-bound personalization

```text
Human
  |
  v
Single AI product
  |
  v
Hidden memory and interaction history
```

If the product or model changes, much of the accumulated working relationship may not move with it.

## ChrisOS design objective

```text
                 ChrisOS
        +-----------+-----------+
        |                       |
  Durable knowledge       Collaboration policy
        |                       |
        +-----------+-----------+
                    |
        +-----------+-----------+
        |           |           |
       GPT        Claude      Gemini
        |           |           |
        +-----------+-----------+
                    |
               One human
```

The same canonical human model is supplied to multiple execution engines.

## Human-governed adaptation

```text
Policy + relevant calibration
              |
              v
          Model output
              |
              v
      Evaluation observation
              |
              v
        Proposed correction
              |
              v
         Human ratification
              |
              v
     Canonical update, if approved
```

The human approval step is intentional. Models may propose changes but do not autonomously redefine the human.
