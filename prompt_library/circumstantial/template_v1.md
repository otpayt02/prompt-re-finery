---
template_id: circumstantial_v1
family: circumstantial
display_name: Circumstantial Prompt Template
version: 1
status: active
recommended_mode: default
---

# Circumstantial Prompt Template — v1

## Purpose

Handle one-off, unusual, or mixed-context prompts that do not fit a standard family cleanly.

## Required context fields

- `situation`: What is happening.
- `goal`: What the user wants to accomplish.
- `constraints`: Important limits.
- `stakes`: Why accuracy or tone matters.

## Preferred output structure

1. Situation read.
2. Best-fit prompt family if applicable.
3. Assumptions.
4. Recommended response structure.
5. Next action.

## Critique dimensions

- Did the response correctly identify the situation?
- Did it avoid overfitting to the wrong family?
- Is the next action useful?
