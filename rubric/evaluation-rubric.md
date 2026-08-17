# LLM Response Evaluation Rubric

## Overview

This rubric evaluates responses from ChatGPT, Claude, and DeepSeek using the same 50 benchmark prompts.

Each response receives a score from 1 to 5 across six quality dimensions.

The maximum score for one response is 30.

## Evaluation Dimensions

### 1. Correctness

Measures whether the response is factually and technically correct.

| Score | Definition |
|---|---|
| 5 | Fully correct with no meaningful factual or technical errors |
| 4 | Mostly correct with a minor issue |
| 3 | Partially correct with noticeable errors |
| 2 | Significant errors affect the answer |
| 1 | Fundamentally incorrect or largely false |

### 2. Relevance

Measures whether the response directly addresses the prompt.

| Score | Definition |
|---|---|
| 5 | Directly answers the prompt and stays focused |
| 4 | Mostly relevant with minor unnecessary content |
| 3 | Answers the prompt but includes significant irrelevant content |
| 2 | Only partially addresses the prompt |
| 1 | Does not meaningfully answer the prompt |

### 3. Instruction Following

Measures whether the model follows explicit instructions in the prompt.

| Score | Definition |
|---|---|
| 5 | Follows all explicit instructions |
| 4 | Misses one minor instruction |
| 3 | Misses an important instruction |
| 2 | Fails multiple important instructions |
| 1 | Essentially ignores the instructions |

### 4. Completeness

Measures whether the response covers the important requirements of the task.

| Score | Definition |
|---|---|
| 5 | Covers all important requirements |
| 4 | Misses a minor detail |
| 3 | Misses one or more meaningful parts |
| 2 | Leaves major parts unanswered |
| 1 | Barely addresses the task |

### 5. Clarity

Measures how easy the response is to understand.

| Score | Definition |
|---|---|
| 5 | Clear, organized, and easy to understand |
| 4 | Generally clear with minor awkwardness |
| 3 | Understandable but confusing in places |
| 2 | Difficult to follow |
| 1 | Extremely confusing or incoherent |

### 6. Reasoning Quality

Measures whether the reasoning is logical and technically sound.

| Score | Definition |
|---|---|
| 5 | Logical and sound with no important gaps |
| 4 | Mostly sound with a minor gap |
| 3 | Plausible reasoning with noticeable weaknesses |
| 2 | Significant logical problems |
| 1 | Fundamentally invalid reasoning |

## Hallucination

A hallucination is an unsupported or fabricated claim presented as factual.

Record:

- `Yes` if a meaningful hallucination is present.
- `No` if no meaningful hallucination is present.

## Error Types

Possible error categories include:

- None
- Factual Error
- Logical Error
- Instruction Failure
- Incomplete Answer
- Hallucination
- Calculation Error
- Code Error
- Unsupported Claim
- Irrelevant Content
- Other

## Error Severity

### None
No meaningful error.

### Minor
The response is mostly correct, but contains a small issue that does not change the main conclusion.

### Major
The error substantially affects correctness, usefulness, safety, or the requested task.

## Overall Score

The six numerical dimensions are added together:

`Correctness + Relevance + Instruction Following + Completeness + Clarity + Reasoning Quality`

Maximum score:

`30`

Percentage:

`Overall Score / 30 × 100`

## Classification

| Score | Classification |
|---|---|
| 27–30 | Excellent |
| 24–26 | Good |
| 19–23 | Acceptable |
| 13–18 | Poor |
| 6–12 | Very Poor |

A response with a Correctness score of 1 or 2 is not classified as Excellent.

## Benchmark Design

The benchmark contains 50 prompts across multiple areas:

- General Knowledge
- C Programming
- C++ Programming
- Python Programming
- Reasoning and Instruction Following

Each prompt was given to all three models using the same wording.

Total responses:

`50 prompts × 3 models = 150 responses`

The purpose is to compare model behavior using a consistent evaluation framework.
