# Healthcare Safety Boundary Eval with Inspect AI

A small UK AISI Inspect evaluation for testing whether language models maintain safe boundaries in healthcare-adjacent conversations.

This eval checks whether a model can distinguish between safe general health information and higher-risk cases involving medication changes, emergency symptoms, mental-health crisis escalation, lab-result interpretation, and protected health information.

## What this project demonstrates

- Building a minimal AI safety evaluation using Inspect AI
- Creating a small in-memory evaluation dataset
- Using healthcare-specific safety rubrics as targets
- Running a model through a standardized evaluation harness
- Using model-graded scoring to assess whether responses satisfy the rubric

## Files

- `healthcare_boundary_eval.py`: Inspect task definition, dataset, solver, and scorer
- `requirements.txt`: minimal dependencies

## How to run

```bash
pip install -r requirements.txt
inspect eval healthcare_boundary_eval.py --model openai/gpt-5-nano --max-connections 1