# LLM Response Evaluation Benchmark

A structured benchmark for evaluating and comparing responses from **ChatGPT, Claude, and DeepSeek** across 50 prompts and multiple task categories.

The project uses a consistent evaluation rubric to assess response quality across six core dimensions: **correctness, relevance, instruction following, completeness, clarity, and reasoning quality**.

It also records additional evaluation information such as hallucination indicators, error types, and error severity.

---

## Project Overview

Large Language Models can produce different responses to the same prompt. This project evaluates three widely used LLMs using the same benchmark prompts and a consistent evaluation framework.

The goal is to replace purely subjective model comparisons with a structured, documented evaluation process.

### Models Evaluated

* ChatGPT
* Claude
* DeepSeek

### Benchmark Size

| Metric                     |  Value |
| -------------------------- | -----: |
| Models                     |      3 |
| Prompts                    |     50 |
| Total Responses            |    150 |
| Core Evaluation Dimensions |      6 |
| Score per Dimension        | 1 to 5 |
| Maximum Score per Response |     30 |

Each model was evaluated against the same set of benchmark prompts.

---

## Objectives

The primary objective is to develop a reproducible framework for evaluating LLM response quality.

The benchmark focuses on:

* Response correctness
* Relevance to the prompt
* Instruction following
* Completeness
* Clarity
* Reasoning quality
* Hallucination indicators
* Error classification
* Error severity
* Cross-model performance comparison

The project also demonstrates a practical workflow for collecting, evaluating, analyzing, and documenting LLM-generated data.

---

## Evaluation Framework

Each response is scored across six core quality dimensions.

Each dimension receives a score from **1 to 5**.

| Dimension             | Description                                                                                |
| --------------------- | ------------------------------------------------------------------------------------------ |
| Correctness           | Measures whether the response provides accurate information or reaches a correct solution. |
| Relevance             | Measures whether the response directly addresses the requested task.                       |
| Instruction Following | Measures whether the response follows the user's explicit requirements and constraints.    |
| Completeness          | Measures whether the response covers the important aspects of the task.                    |
| Clarity               | Measures whether the response is understandable, well organized, and easy to follow.       |
| Reasoning Quality     | Measures whether the reasoning is logically structured and appropriately supported.        |

### Scoring System

Each response receives a total score between:

* **Minimum:** 6/30
* **Maximum:** 30/30

The total score is calculated by adding the six dimension scores.

Detailed scoring criteria are documented in:

[`rubric/evaluation-rubric.md`](rubric/evaluation-rubric.md)

### Supplementary Evaluation Fields

In addition to the six scored dimensions, the dataset records qualitative evaluation information where applicable:

* Hallucination indicators
* Error type
* Error severity
* Evaluation comments

These fields provide additional context for understanding why a response received a particular score.

---

## Benchmark Methodology

The benchmark follows a structured evaluation workflow:

```text
Benchmark Prompts
       ↓
Generate Model Responses
       ↓
Collect Raw Responses
       ↓
Evaluate Responses
       ↓
Apply Consistent Rubric
       ↓
Calculate Scores
       ↓
Compare Models
       ↓
Analyze Results
       ↓
Document Findings
```

The same benchmark prompts are evaluated across all three models to provide a consistent basis for comparison within the scope of this dataset.

The benchmark results should be interpreted as an evaluation of the selected prompts, model configurations, and evaluation methodology. They should not be treated as a universal ranking of LLMs.

---

## Task Categories

The benchmark covers multiple task categories, including:

* General knowledge
* Programming
* C programming
* C++ programming
* Python programming
* Reasoning
* Instruction following

The categories are intended to evaluate different aspects of response quality rather than a single model capability.

---

## Results

Based on the current benchmark dataset:

| Rank | Model    | Average Score | Average Percentage |
| ---: | -------- | ------------: | -----------------: |
|    1 | Claude   |    29.96 / 30 |             99.87% |
|    2 | ChatGPT  |    28.30 / 30 |             94.33% |
|    3 | DeepSeek |    27.02 / 30 |             90.07% |

### Score Differences

| Comparison          |  Difference |
| ------------------- | ----------: |
| Claude vs ChatGPT   | 1.66 points |
| Claude vs DeepSeek  | 2.94 points |
| ChatGPT vs DeepSeek | 1.28 points |

### Result Interpretation

Claude achieved the highest average score in the current benchmark, followed by ChatGPT and DeepSeek.

The differences are relatively small compared with the maximum possible score of 30. The results therefore provide useful evidence about performance within this dataset, but they should not be interpreted as evidence that one model is universally better than another.

Model performance can change with different:

* Prompts
* Task categories
* Model versions
* System instructions
* Generation settings
* Evaluation criteria
* Evaluators

Detailed findings are available in:

[`analysis/findings.md`](analysis/findings.md)

---

## Data

The project separates raw responses, evaluated responses, and processed analysis.

### Raw Responses

[`data/benchmark_responses.xlsx`](data/benchmark_responses.xlsx)

Contains the collected model responses before evaluation.

### Evaluations

[`data/benchmark_evaluations.xlsx`](data/benchmark_evaluations.xlsx)

Contains evaluation scores and additional evaluation fields.

### Analysis

[`results/LLM_Benchmark_Analysis_Professional.xlsx`](results/LLM_Benchmark_Analysis_Professional.xlsx)

Contains processed benchmark results, comparisons, and visual analysis.

---

## Repository Structure

```text
llm-response-evaluation-benchmark/
│
├── README.md
│
├── rubric/
│   └── evaluation-rubric.md
│
├── analysis/
│   └── findings.md
│
├── data/
│   ├── README.md
│   ├── benchmark_responses.xlsx
│   └── benchmark_evaluations.xlsx
│
└── results/
    └── LLM_Benchmark_Analysis_Professional.xlsx
```

---

## Key Findings

The current benchmark produced three primary observations.

### 1. Claude achieved the highest average score

Claude recorded an average score of **29.96/30**, the highest among the three evaluated models.

### 2. ChatGPT ranked second

ChatGPT recorded an average score of **28.30/30** and ranked second in the benchmark.

### 3. DeepSeek ranked third

DeepSeek recorded an average score of **27.02/30** and ranked third in the current dataset.

These findings apply specifically to the benchmark prompts, evaluation framework, model versions, and dataset used in this project.

---

## Limitations

### Dataset Size

The benchmark contains 50 prompts and 150 total responses.

A larger dataset would provide broader coverage of model behavior.

### Prompt Selection

Benchmark results depend heavily on prompt selection and task distribution.

Different prompts can produce different rankings.

### Evaluation Subjectivity

Human evaluation can introduce subjectivity, even when a structured rubric is used.

Using multiple independent evaluators would reduce this limitation.

### Model Versions and Configurations

LLM behavior can change between model versions and generation configurations.

Results from this benchmark should therefore be associated with the specific model versions and settings used during data collection, where available.

### High Average Scores

All three models achieved relatively high average scores.

This may indicate strong performance on the selected tasks. It may also indicate that some benchmark prompts were relatively easy or that the scoring criteria were not sufficiently strict.

Future versions should include more challenging, adversarial, ambiguous, and edge-case prompts.

### Benchmark Scope

The benchmark contains a limited number of task categories and does not represent every type of LLM workload.

The results should therefore be interpreted within the defined benchmark scope.

---

## Future Improvements

The benchmark can be extended in several directions.

### Larger Dataset

Increase the benchmark from 50 prompts to several hundred or thousands of prompts.

### More Models

Add additional models and model versions to improve comparative coverage.

### More Difficult Prompts

Add:

* Edge cases
* Adversarial prompts
* Ambiguous instructions
* Multi-step reasoning tasks
* Factual verification tasks
* Code debugging tasks
* Long-context tasks
* Structured output tasks

### Multiple Evaluators

Use multiple independent evaluators and calculate inter-rater agreement.

Potential metrics include:

* Cohen's Kappa
* Fleiss' Kappa
* Krippendorff's Alpha
* Inter-rater agreement percentage

### Automated Evaluation

Introduce automated checks where objective verification is possible, including:

* Code execution and correctness
* Exact-answer matching
* Mathematical verification
* Structured output validation
* Factual consistency checks

### Statistical Analysis

Future versions can include:

* Mean and median scores
* Standard deviation
* Score distributions
* Confidence intervals
* Per-category performance
* Per-difficulty performance
* Error rates
* Hallucination rates
* Statistical significance testing
* Effect size analysis

### Reproducible Evaluation Pipeline

Future versions can include Python scripts for:

* Data validation
* Score calculation
* Statistical analysis
* Visualization
* Automated report generation

---

## Skills Demonstrated

This project demonstrates practical skills in:

* LLM evaluation
* AI response quality assessment
* Evaluation rubric design
* Data collection
* Data annotation
* Spreadsheet-based analysis
* Comparative analysis
* Data organization
* Technical documentation
* GitHub project organization

The programming-related benchmark tasks also provide practical connections to:

* C
* C++
* Python

Future automation can further extend the project into Python-based data analysis and evaluation tooling.

---

## Reproducibility

The repository is organized so that another evaluator can understand and review the evaluation process.

A reviewer can:

1. Review the benchmark prompts.
2. Review the collected model responses.
3. Review the evaluation rubric.
4. Review the evaluation dataset.
5. Verify the score calculations.
6. Review the analysis workbook.
7. Compare the documented findings with the underlying data.

The evaluation methodology is documented in:

[`rubric/evaluation-rubric.md`](rubric/evaluation-rubric.md)

Exact reproduction of model outputs may not be possible because LLM responses can vary across model versions, configurations, system instructions, and generation settings.

---

## Project Status

**Status: Completed initial benchmark and analysis**

### Completed

* [x] Benchmark prompt collection
* [x] Model response collection
* [x] Evaluation rubric
* [x] Response evaluation
* [x] Model comparison
* [x] Data analysis
* [x] Findings documentation
* [x] GitHub repository organization

### Planned

* [ ] Expand the benchmark dataset
* [ ] Add more difficult evaluation cases
* [ ] Add automated evaluation scripts
* [ ] Add Python-based analysis
* [ ] Add additional LLMs
* [ ] Add multiple independent evaluators
* [ ] Add statistical significance testing
* [ ] Add automated validation for programming tasks

---

## Author

**Saurabh Pawar**

2nd Year Computer Engineering Student

GitHub: [@saurabhpawar-ai](https://github.com/saurabhpawar-ai)

---

## Purpose

This project was created as a practical portfolio project focused on **LLM evaluation, AI data annotation, data analysis, and technical documentation**.

The project aims to develop practical experience relevant to:

* AI evaluation
* AI training data
* Data annotation
* LLM benchmarking
* Data analysis
* AI quality assessment
* Evaluation-focused freelance work

The long-term goal is to expand the benchmark into a more rigorous and automated LLM evaluation framework.
