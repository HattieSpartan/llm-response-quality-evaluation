
# LLM Response Quality Evaluation

## 1. Project Objective

This project evaluates the reliability of a selected Large Language Model (LLM) across four dimensions: factual accuracy, instruction-following, hallucination detection, and prompt-injection resistance.

The objective is to establish a repeatable evaluation process that identifies response-quality defects, measures model performance, documents failure patterns, and provides evidence-based recommendations.

## 2. Evaluation Scope

The initial evaluation will cover four categories.

| Code | Category | Description |
|---|---|---|
| FA | Factual Accuracy | Evaluates the correctness of verifiable information. |
| IF | Instruction Following | Evaluates compliance with explicit user instructions and task constraints. |
| H | Hallucination Detection | Evaluates whether the model generates unsupported information as established fact. |
| PI | Prompt-Injection Resistance | Evaluates whether the model resists malicious instructions embedded in untrusted content. |

The initial dataset will contain 40 test cases, with 10 tests assigned to each category.

## 3. Scoring Methodology

Each test will receive one of three scores:

- 2: Pass. The response meets all defined acceptance criteria.
- 1: Partial Pass. The response meets some criteria but has a material weakness.
- 0: Fail. The response violates a critical acceptance criterion.

Scoring decisions will be based on predefined expected behaviours rather than subjective impressions.

## 4. Defect Severity

Observed defects will be classified as follows:

- Low: Minor quality issue with limited impact.
- Medium: Noticeable weakness affecting response quality.
- High: Significant reliability or factual-integrity issue.
- Critical: Serious safety or instruction-boundary failure.

Severity will be recorded separately from the numerical evaluation score.

## 5. Performance Metrics

The evaluation will calculate:

1. Strict pass rate.
2. Partial pass rate.
3. Failure rate.
4. Normalised quality score.
5. Category-level performance.
6. Defect distribution by severity.

The normalised quality score will be calculated as:

Quality Score = (Sum of test scores / (2 × Number of tests)) × 100.

## 6. Evaluation Procedure

1. Define the test prompt and expected behaviour.
2. Submit the prompt to the selected model under recorded conditions.
3. Capture the complete model response.
4. Compare the response against the predefined acceptance criteria.
5. Assign a score.
6. Record any observed defect and its severity.
7. Preserve evidence supporting the evaluation decision.
8. Analyse results using Python.

## 7. Reproducibility

The evaluation record will include the model identifier as displayed, evaluation date, test prompt, expected behaviour, actual response, scoring decision, and relevant test conditions.

Where possible, repeated tests will be conducted to investigate inconsistent model behaviour.

## 8. Limitations

The initial evaluation will use a manually scored test dataset and a limited number of test cases.

Results will describe the model's performance on the selected tests under the recorded conditions. They will not establish universal model reliability or guarantee performance on all real-world tasks.

Automated evaluation and comparative testing may be introduced in subsequent project stages.
