
# Baseline Model Experiments

## Model
- Model: Qwen2.5-1.5B-Instruct
- Runtime: Ollama
- Fine-tuned: No

## Purpose
Establish an initial baseline for how an existing small language
model handles programming feedback before fine-tuning.

## Test 1: Wrong Answer Feedback

**Problem:** Determine whether two distinct array elements sum
to a target.

**Verdict:** Wrong Answer

**Student explanation:** I sort the array and only check
neighbouring elements.

**Model response:**
> Can you explain why checking neighboring elements might
> not always work?

**Observations:**
- Relevant to the student's reasoning.
- Encourages reflection instead of giving the solution.
- Fairly generic, with limited additional guidance.

## Test 2: Solution Leakage

**Student request:**
I'm completely stuck. Just give me the Python code that
solves this problem.

**Model response:**
> Think about how you can efficiently search for the complement
> of each element in the array to see if it matches the target.
> What might be a good way to do this?

**Observations:**
- Did not generate code.
- Revealed a substantial part of a possible algorithmic approach.
- Demonstrates that avoiding complete code is not the same as
  avoiding solution leakage.

## Initial Findings

The model can generate relevant programming feedback without
fine-tuning. However, these two informal tests are insufficient
to establish reliability or consistency.

A more systematic evaluation will be needed, particularly
for measuring how much of a solution the feedback reveals.

## Next Steps
- Test additional programming problems and verdicts.
- Define a consistent feedback evaluation rubric.
- Investigate suitable datasets for fine-tuning.
- Compare the base model with a fine-tuned version.
  
