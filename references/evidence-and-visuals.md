# Evidence, quantitative results, and visuals

## Match claims to evidence

Before drafting results, map each major claim to its minimum convincing evidence:

| Claim type | Suitable evidence |
|---|---|
| Feasibility | successful operation, validated case, or correctness test |
| Effectiveness | task metric against a relevant control or baseline |
| Superiority | fair comparison under a common protocol |
| Necessity of a component | ablation or controlled removal |
| Stability | independent repetitions, intervals, or distributions |
| Generalization | held-out conditions, domains, or populations |
| Mechanism | theory or causal reasoning plus a corresponding observation |
| Practical value | cost, latency, resource, reliability, or deployment evidence |

Do not use one successful case to support population performance, a mean to establish tail reliability, or a correlation to establish causality.

## Choose statistics from the data and task

- Use mean and standard deviation for reasonably symmetric distributions when they answer the task question.
- Use median and upper quantiles for skewed or long-tailed outcomes.
- Use rates when success is defined by a threshold or conjunction of requirements.
- Use joint metrics when the task requires multiple objectives simultaneously.
- Preserve a common denominator and comparison protocol across methods.
- Compute repeated-experiment summaries at the experiment level rather than treating every observation as an independent run.
- Explain a changed metric through task relevance or distributional properties, not through which method it favors.

## Analyze results in three layers

For each related group of results, cover only what is useful:

1. **Pattern:** the most important visible or numerical change.
2. **Mechanism:** why the method or condition could produce it.
3. **Implication:** how it supports the central claim or decision.

Lead with the strongest supported result. Treat secondary weaknesses briefly when they do not alter the main conclusion. If they do alter it, revise the claim.

## Divide work among prose, figures, and tables

- Tables provide exact values and compact comparisons.
- Figures reveal trends, distributions, spatial relationships, and mechanisms.
- Prose selects the important pattern and explains its meaning.

Remove a figure or table when it duplicates another artifact without adding interpretive value.

## Design figures as evidence

- Give every figure one primary question.
- Keep color, marker, unit, threshold, binning, and axis conventions consistent.
- Use shared legends and color scales for multi-panel comparisons.
- Include symbols as well as labels in legends.
- Use the same limits or bins when visual comparison depends on them.
- Show the informative range without silently discarding consequential tails or failures.
- Use enlargements when precision is otherwise invisible; place them where they do not obscure the main data.
- Use objective captions. Avoid labels implying cherry-picking unless the selection rule is stated.
- Verify legibility at final publication or report size.

## Calibrate language

Reserve “significant” for a defined statistical or practical meaning. Reserve “state of the art,” “first,” “best,” and “general” for claims supported by a sufficiently complete comparison or literature search. Prefer specific statements such as “highest success rate among the compared methods under the common protocol.”

