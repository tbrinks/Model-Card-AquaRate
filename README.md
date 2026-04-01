# Model Cards for Public Health AI

A practical workshop on reading, evaluating, and writing model cards — the standardized documentation that describes what an AI system does, what it was built on, how it performs, where it fails, and what the ethical risks are.

> A model without a model card is like a drug without a label. You might still use it — but you're doing so blind.

---

## What Is a Model Card?

A model card is a short document proposed by [Mitchell et al. (2019)](https://dl.acm.org/doi/10.1145/3287560.3287596) as a standardized way to report the essential facts about a machine learning model. Think of it as a nutrition label for AI: it tells you what's inside, what it's good for, and what the risks are.

Model cards were inspired by how other fields handle transparency — datasheets for electronics, drug labels for pharmaceuticals, nutrition facts for food. The core idea is simple: if you're going to deploy a model that affects people, you should document it clearly enough that someone else can evaluate whether it's appropriate for their context.

### Why This Matters for Public Health

AI tools in health affect real people. A misclassification can mean a missed diagnosis, a misallocated resource, or a reinforced disparity. Public health operates across diverse populations — a model trained on one demographic can fail silently on another. And the people deploying AI in public health are usually not the people who built it. The model card bridges that gap.

Standard model cards were designed for ML in general. Public health has specific needs that the original framework doesn't fully cover:

- **Population representativeness** — Does the training data reflect the community where the model is deployed, not just nationally but locally?
- **Temporal validity** — Disease patterns change. A model trained on 2015–2019 data missed the dynamics of 2020–2024 entirely.
- **Human oversight** — Who reviews outputs before action? What is the escalation path when the model is wrong?
- **Data sovereignty and consent** — Especially in global health: were the communities represented in the data consulted about how it would be used?

---

## The Exercise

Each group receives a scenario describing an AI system designed for a public health application. Your task is to draft a model card for that system using the template below.

The scenario gives you the context. The model card is your analysis of what should be documented about this system before it is deployed. Think like a decision-maker who has to approve this tool for their community.

**Be specific.** "The model may have bias" is not enough. Bias against whom? In what direction? With what consequence?

### How to Complete the Template

1. Read your scenario carefully — pay attention to the data environment and operational context sections
2. Fork this repository
3. Copy the template below into a new file named `model-card-[your-scenario].md`
4. Fill in all 10 sections
5. Submit a pull request with your completed model card

---

## Model Card Template

Copy this template into a new file and fill in each section for your scenario.

```markdown
# Model Card — [System Name]

**Scenario:** [title]
**Authors:** [your names]
**Date:** [date]

---

## 1. Model Details

> What model or API is being used? Who built it? What version? What type of
> model — classification, prediction, generation, optimization? When was it
> developed?

[Your response]

---

## 2. Intended Use

> What is the primary task? Who are the intended users? What decisions does
> the system inform? In what context is it deployed?

[Your response]

---

## 3. Out-of-Scope Uses

> What should this system NOT be used for? What populations, settings, or
> decisions are outside its design? What misuses are foreseeable?

[Your response]

---

## 4. Training Data

> What data was used to build or train this model? How was it collected? What
> populations, geographies, languages, and time periods does it cover? What
> is missing?

[Your response]

---

## 5. Evaluation Data & Metrics

> How was performance measured? What metrics were used — accuracy, sensitivity,
> specificity, F1, AUC, RMSE? On what test set? Is it independent from the
> training data?

[Your response]

---

## 6. Quantitative Analysis

> Performance broken down by relevant subgroups — age, sex, race/ethnicity,
> geography, income, language. Does the model perform differently across
> these groups? Where are the gaps?

[Your response]

---

## 7. Ethical Considerations

> Bias risks, informed consent, privacy, potential harms, equity implications.
> Does this system reproduce or amplify existing disparities? Who bears the
> consequences when it fails?

[Your response]

---

## 8. Limitations & Caveats

> Known failure modes, edge cases, what the model does not capture. Conditions
> where it performs poorly. Assumptions baked into the design that may not
> hold in all deployment contexts.

[Your response]

---

## 9. Human Oversight

> Who reviews outputs before action is taken? Human in the loop, on the loop,
> or out of the loop? What is the escalation path when the model is wrong?
> Can it act autonomously — and should it?

[Your response]

---

## 10. Temporal Validity

> When does this model need retraining or re-evaluation? What triggers a
> review — new data, policy change, population shift, outbreak? How does
> performance degrade over time?

[Your response]
```

---

## References

- Mitchell, M. et al. (2019). [Model Cards for Model Reporting](https://dl.acm.org/doi/10.1145/3287560.3287596). ACM Conference on Fairness, Accountability, and Transparency.
- Gebru, T. et al. (2021). [Datasheets for Datasets](https://doi.org/10.1145/3458723). Communications of the ACM.
- Obermeyer, Z. et al. (2019). [Dissecting Racial Bias in an Algorithm Used to Manage the Health of Populations](https://doi.org/10.1126/science.aax2342). Science.
- WHO (2021). [Ethics and Governance of Artificial Intelligence for Health](https://www.who.int/publications/i/item/9789240029200).
- Hugging Face. [Model Card Guidebook](https://huggingface.co/docs/hub/model-cards).

---

## Course Information

**Course:** GHI 463/563 — Foundations of AI for Public Health Applications
**Instructor:** Onicio B. Leal Neto, PhD MS
**Institution:** Mel and Enid Zuckerman College of Public Health, University of Arizona

---

*This repository is part of the Model Cards for Public Health AI workshop. Fork the repo, complete your model card, and submit a pull request.*
