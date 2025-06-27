# promptlearn

**promptlearn** is a drop-in extension for `scikit-learn` that brings the power of LLMs to existing machine learning pipelines.
It provides `scikit-learn`-compatible estimators powered by LLMs, such as:

- `PromptClassifier` – classifies data with LLM prompts
- `PromptRegressor` – regresses data with LLM prompts

The estimators support standard `fit()` and `predict()` methods, and can be used in the same way as any other `scikit-learn` estimator.

The noteworthy difference from traditional estimators is that the LLM is able to *automatically detect and exploit higher-level patterns* in the data,
for example

> the target is an XOR of x1 and x2

> the equation y=2x*3 is a good linear fit for this noisy data

> here is a simple human-readable decision tree that classifies this data well (followed by the actual tree)

The estimators detect these patterns during the `fit()` step, and then use this knowledge to output exact predictions in the `predict()` step.

---

## 📁 License

MIT © 2025 Erland Kirkfire
