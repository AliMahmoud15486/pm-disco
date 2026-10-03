---
name: analyze_connections
description: Cleans and segments the latest LinkedIn connections export. Use when a new export is added to inputs/connections/.
---

# Skill: Analyze Connections

## Objective
Your goal as the Network Analyst is to turn the latest LinkedIn connections export into a clean, segmented view of the user's network.

## Rules of Engagement
- **Input**: The most recent CSV in `inputs/connections/`. Files are named `Connections_YYYY-MM-DD.csv`.
- **Save Location**: `outputs/Network_Segments.md` and `outputs/connections_clean.csv`.
- **Constraint**: Use only the data in the export. Do not guess missing companies or titles.

## Instructions
1. **Parse the File**: LinkedIn's `Connections.csv` starts with a few "Notes" lines before the real header (`First Name,Last Name,URL,Email Address,Company,Position,Connected On`). Skip everything above that header row.
2. **Clean the Data**:
    - Trim whitespace and fix obvious company-name variants (e.g., "Google LLC" → "Google").
    - Normalize job titles into **Function** (Sales, Marketing, Engineering, Product, Operations, Finance, HR, Founder/Exec, Other) and **Seniority** (C-level/Founder, VP, Director, Manager, Individual Contributor, Unknown).
    - Flag rows with a missing company or position as "Incomplete".
3. **Save** the cleaned data to `outputs/connections_clean.csv` with the added Function, Seniority, and Incomplete columns.
4. **Draft `Network_Segments.md`**, which MUST include:
    - **Overview**: Total connections, % incomplete, date range of "Connected On".
    - **By Function** and **By Seniority**: Counts and percentages.
    - **Top Companies**: The 20 companies with the most connections.
    - **Growth**: Connections added per quarter.
5. **Halt Execution**: Notify the user: "Network segmentation is complete and saved. Awaiting ICP scoring."
