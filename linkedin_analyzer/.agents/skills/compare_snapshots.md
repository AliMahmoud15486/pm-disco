---
name: compare_snapshots
description: Compares the two most recent LinkedIn exports to find network changes. Use when at least two exports exist in inputs/connections/.
---

# Skill: Compare Snapshots

## Objective
Your goal as the Network Analyst is to show what changed in the user's network between two exports and highlight changes that create outreach opportunities.

## Rules of Engagement
- **Input**: The two most recent CSVs in `inputs/connections/` (by date in the filename).
- **Save Location**: `outputs/Network_Changes.md`.
- **Constraint**: Match people by profile URL. Only report changes that are visible in the data.

## Instructions
1. **Compare** the older and newer snapshots by `URL`.
2. **Draft `Network_Changes.md`**, which MUST include:
    - **New Connections**: Everyone added since the last export, with their ICP score if available.
    - **Job Changes**: People whose Company changed — a strong reason to reconnect.
    - **Promotions**: People whose title moved up in seniority at the same company.
    - **Removed**: Connections present before but missing now.
    - **Trend**: Is the network moving toward or away from the ICP? Compare the share of A/B-tier contacts.
3. **Halt Execution**: Notify the user: "Network comparison is complete. Please review `Network_Changes.md`."
