# Session 5 summary: Classifier Evaluation

## 1. Opening Discussion: “How good is your classifier?”
Students are asked to assess their classifier performance. Many express uncertainty, often because they lack strong validation data or have very few positive examples. This sets up the central question of the lecture: how to meaningfully evaluate classifier performance.

---

## 2. Core Evaluation Metrics

### AUROC
- Measures the probability that a randomly chosen positive scores higher than a randomly chosen negative.
- Threshold-free and insensitive to class imbalance.
- Can be misleading when positives are rare because changes in false positives barely affect the score.

### Average Precision (AP)
- Computes precision across all thresholds and averages.
- Sensitive to class imbalance.
- More informative than AUROC when the positive class is rare.

### Contrast
- AUROC is stable across prevalence but insensitive in rare-event settings.
- AP is sensitive to prevalence but more discriminative for sparse positives.

---

## 3. Multi-Class Evaluation: Micro vs. Macro
- **Macro averaging** weights all classes equally and is preferred for ecological or bioacoustic work.
- **Micro averaging** weights classes by sample count and is dominated by abundant classes.
- Per-class metrics are essential to understand real performance.

---

## 4. Dataset Splits and Their Roles
- **Training set** optimizes model parameters.
- **Validation set** is used for model selection and hyperparameters.
- **Test set** is held out entirely for the final unbiased performance estimate.
- Validation data must never leak into training.

---

## 5. Why Validation Metrics Can Exceed Training Metrics Early On
- Augmentation makes training data harder (noise, overlays, shifts).
- Validation data remains clean.
- Early in training, the model can perform better on validation than on augmented training samples.

---

## 6. Working with Weights & Biases (W&B)
- Track training and validation loss curves.
- Log per-class metrics.
- Visualize spectrograms and example clips.
- Helps identify instability or poor generalization during training.

---

## 7. Precision–Recall Curve Interpretation
- PR curves change significantly with class imbalance.
- Precision drops rapidly as false positives accumulate.
- AP reflects these changes more meaningfully than AUROC in sparse-positive datasets.

---

## 8. Q&A Highlights
- How class imbalance affects AP and AUROC.
- Why AUROC may stay stable even as false positives rise.
- The pitfalls of accuracy in imbalanced settings.
- Evaluating multi-species models with extremely rare species.
- Characteristics of high-quality validation data (realistic environments, diverse noise).

---

# Key Takeaways
- Use AUROC and AP together, but rely more on AP for rare-event detection.
- Prefer macro-averaged metrics and always inspect per-class performance.
- Validation outperforming training early is normal under strong augmentation.
- Numeric metrics aren’t enough—qualitative checks and realistic validation data matter.
