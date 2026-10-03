---
title: Run LinkedIn Analysis
description: Analyzes the latest LinkedIn connections export, scores it against the ICP, and builds an outreach plan.
---

# Workflow: Run LinkedIn Analysis

This workflow chains together the agents defined in `agents.md`.

## Step 0: Pre-flight Checks
- Confirm at least one `Connections_YYYY-MM-DD.csv` exists in `inputs/connections/`. If not, tell the user how to get one:
  LinkedIn → **Settings & Privacy** → **Data privacy** → **Get a copy of your data** → select **Connections** → **Request archive**. Then rename the file to `Connections_YYYY-MM-DD.csv` and add it to `inputs/connections/`.
- Confirm `inputs/business/icp.md` is filled in. If not, ask the user to complete it.

## Step 1: Segment the Network
Call the `@network-analyst` to execute the `analyze_connections` skill.
- **Input**: `inputs/connections/`
- **Output**: `outputs/Network_Segments.md`, `outputs/connections_clean.csv`

## Step 2: Score and Compare (parallel)
Once Step 1 is complete, run concurrently:
- **Task A**: Call the `@prospect-strategist` to execute the `score_and_prioritize` skill.
    - **Output**: `outputs/Prioritized_Contacts.csv`, `outputs/Outreach_Plan.md`
- **Task B** (only if 2+ exports exist): Call the `@network-analyst` to execute the `compare_snapshots` skill.
    - **Output**: `outputs/Network_Changes.md`

## Step 3: Final Review
Notify the user: "LinkedIn analysis is complete. Start with `outputs/Outreach_Plan.md`."
