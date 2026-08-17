# Benchmark Findings

## Overview

This benchmark evaluates responses from three large language models:

- ChatGPT
- Claude
- DeepSeek

The benchmark contains 50 prompts. Each prompt was given to all three models, producing:

**50 prompts × 3 models = 150 responses**

Each response was evaluated using the same evaluation rubric.

## Evaluation Method

Each response was scored across six dimensions:

1. Correctness
2. Relevance
3. Instruction Following
4. Completeness
5. Clarity
6. Reasoning Quality

Each dimension received a score from 1 to 5.

The maximum score for one response was 30.

A hallucination indicator, error type, and error severity were also recorded.

## Overall Results

| Rank | Model | Responses | Average Score | Average Percentage |
|---|---|---:|---:|---:|
| 1 | Claude | 50 | 29.96 / 30 | 99.87% |
| 2 | ChatGPT | 50 | 28.30 / 30 | 94.33% |
| 3 | DeepSeek | 50 | 27.02 / 30 | 90.07% |

## Main Finding

Claude achieved the highest average score in this benchmark, followed by ChatGPT and DeepSeek.

The average scores were:

- Claude: 29.96/30
- ChatGPT: 28.30/30
- DeepSeek: 27.02/30

Claude's average score was approximately 1.66 points higher than ChatGPT and 2.94 points higher than DeepSeek.

## Interpretation

The results indicate that Claude performed best under the evaluation framework used in this benchmark.

ChatGPT also achieved a high average score and ranked second.

DeepSeek achieved the lowest average score among the three models in this particular benchmark.

These results describe performance on this benchmark only. They should not be interpreted as a universal ranking of the models.

## Benchmark Scope

The prompts cover multiple types of tasks, including:

- General knowledge
- C programming
- C++ programming
- Python programming
- Reasoning
- Instruction following

The same prompts were used across all three models to maintain a consistent comparison.

## Limitations

This benchmark has several limitations:

1. The benchmark contains 50 prompts, so it does not represent every possible task.
2. Human evaluation can introduce subjective judgment.
3. Model versions can change over time.
4. Results can depend on prompt selection and evaluation criteria.
5. A model's performance on this benchmark may differ from its performance on other datasets.
6. The benchmark does not measure every aspect of model quality.

## Important Observation

The average scores are very high, particularly for Claude.

This means the evaluation results should be interpreted carefully. High scores may indicate strong model performance, but they may also indicate that the selected prompts were relatively easy or that the scoring criteria were applied generously.

Future versions of the benchmark should include more difficult prompts, adversarial cases, edge cases, factual verification tasks, and a larger sample size.

## Conclusion

Under the evaluation framework and prompt set used in this project:

**Claude ranked first, ChatGPT ranked second, and DeepSeek ranked third.**

The project demonstrates a structured approach to comparing LLM responses using a consistent scoring rubric rather than relying only on subjective impressions.

The benchmark can be extended by increasing the number of prompts, adding more models, introducing automated checks, and using multiple independent evaluators.
