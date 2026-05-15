---
title: Run Discovery
description: Orchestrates the entire PM discovery process from context setting to hypothesis generation.
---

# Workflow: Run Discovery

This workflow orchestrates the PM discovery process by chaining together the specialized agents defined in `agents.md`.

## Step 1: Establish Context
Call the `@context-analyst` to execute the `analyze_context` skill.
- **Input**: `inputs/company_details/`
- **Output**: `outputs/Company_Context.md`
- **Action**: Wait for the `@context-analyst` to confirm completion before proceeding.

## Step 2: Parallel Data Analysis
Once Step 1 is complete, trigger the following agents to run concurrently (in parallel):

- **Task A**: Call the `@qual-researcher` to execute the `analyze_qual_data` skill.
    - **Input**: `inputs/qual_data/`
    - **Output**: `outputs/Qual_Report.md`

- **Task B**: Call the `@behavior-analyst` to execute the `analyze_beh_data` skill.
    - **Input**: `inputs/beh_data/`
    - **Output**: `outputs/Beh_Report.md`

- **Task C**: Call the `@data-scientist` to execute the `analyze_quan_data` skill.
    - **Input**: `inputs/quan_data/`
    - **Output**: `outputs/Quan_Report.md`

- **Action**: Wait for all three tasks (A, B, and C) to confirm completion before proceeding to Step 3.

## Step 3: Synthesis and Hypothesis Generation
Once Step 2 is complete, call the `@orchestrator` to execute the `synthesize_and_score` skill.
- **Input**: `outputs/Company_Context.md`, `outputs/Qual_Report.md`, `outputs/Beh_Report.md`, `outputs/Quan_Report.md`
- **Output**: `outputs/Problem_Statements.md`, `outputs/Hypotheses.md`
- **Action**: Wait for the `@orchestrator` to confirm completion.

## Step 4: Final Review
Notify the user: "The discovery process is complete. Please review the generated `Problem_Statements.md` and `Hypotheses.md` files in the `outputs/` directory."
