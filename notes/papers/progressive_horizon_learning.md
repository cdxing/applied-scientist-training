## Problem
Long-term customer outcomes matter, but their labels mature slowly.

## Why it is hard
- Long-horizon feedback is delayed.
- Customer preferences may change over time.
- Waiting for mature labels delays deployment.
- Short-horizon optimization may not align with long-term value.

## Core mechanisms

### 1. Multi-Horizon Augmentation
Predict multiple horizons such as 1D, 7D, 14D, 30D, and 60D.

### 2. Horizon Masking
Only include a sample-horizon target in the loss after that target has matured.

### 3. Dynamic Horizon Selection
Use the longest horizon that has enough mature data and satisfies a performance guardrail.

## Questions still open
- How exactly is linkage implemented?
- Why does the pretrained encoder help?
- How does Boltzmann exploration affect the policy?
- What are the tradeoffs of extending to very long horizons?
