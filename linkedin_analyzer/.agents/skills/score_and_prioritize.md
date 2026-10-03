---
name: score_and_prioritize
description: Scores segmented connections against the ICP and produces a prioritized outreach plan. Use after analyze_connections.
---

# Skill: Score and Prioritize

## Objective
Your goal as the Prospect Strategist is to find the connections that matter most for the user's business and tell them who to contact first and how.

## Rules of Engagement
- **Input**: `outputs/connections_clean.csv`, `outputs/Network_Segments.md`, `inputs/business/icp.md`.
- **Save Location**: `outputs/Prioritized_Contacts.csv` and `outputs/Outreach_Plan.md`.
- **Constraint**: If `inputs/business/icp.md` is empty or mostly blank, STOP and ask the user to complete it. Do not invent an ICP.
- **Optional Enrichment**: If the user has asked for it, Apollo may be used to fill in company industry and size for top-scoring contacts only. Always state the expected credit cost and get the user's approval before any credit-consuming call.

## Instructions
1. **Score Each Connection (0–100)**:
    - **Title fit (40)**: Decision-maker title = 40, champion/influencer = 25, other relevant function = 10.
    - **Seniority fit (20)**: Matches the ICP seniority levels.
    - **Company fit (30)**: Matches ICP industries / company size (only where known).
    - **Relationship (10)**: Connected within the last 2 years = 10, older = 5.
    - Set the score to 0 for anyone at a listed competitor or matching an exclusion.
2. **Assign a Tier**: A (75+), B (50–74), C (25–49), Not a fit (<25). Separately tag Partners/Referrers and Investors/Advisors per the ICP.
3. **Save** `outputs/Prioritized_Contacts.csv` sorted by score, with Score, Tier, Tag, and a one-line "Why" column.
4. **Draft `Outreach_Plan.md`**, which MUST include:
    - **Summary**: How many A/B/C contacts and partners were found.
    - **Top 25 Contacts**: Name, title, company, score, and why they fit.
    - **Segment Playbooks**: For each major segment, a suggested angle and a short, personalized message template for manual sending.
    - **Gaps**: ICP segments where the network is thin, and suggestions for growing it.
5. **Halt Execution**: Notify the user: "Scoring and outreach plan are complete. Please review `Outreach_Plan.md`."
