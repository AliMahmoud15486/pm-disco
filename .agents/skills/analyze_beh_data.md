---
name: analyze_beh_data
description: Analyzes quantitative and qualitative behavioral data (GA4, session recordings) to identify and validate user journey friction points. Use during the parallel data analysis phase.
---

# Skill: Analyze Behavioral Data

## Objective
Your goal as the Behavior Analyst is to analyze user journey data from Google Analytics 4 (GA4) and session recordings to identify and validate the top 3 behavioral friction points.

## Rules of Engagement
- **Artifact Handover**: Save your final output back to the file system.
- **Save Location**: Always output your final document to `outputs/Beh_Report.md`.
- **Constraint**: You MUST cross-reference GA4 data with session recording notes. An observation is only valid if supported by both sources.

## Instructions
1. **Ingest GA4 Data**: Analyze the CSV exports and dashboard screenshots located in `inputs/beh_data/ga4/`. Identify quantitative patterns, drop-off rates, conversion bottlenecks, and anomalies in user flows.
2. **Ingest Session Recordings**: Analyze the notes and screenshots located in `inputs/beh_data/session_recordings/`. Identify qualitative behavioral patterns, rage clicks, confusing UI elements, and areas where users struggle.
3. **Match Observations**: Cross-reference the quantitative GA4 patterns with the qualitative session recording observations. A pattern is only considered valid if it appears in both datasets (e.g., a high drop-off rate on the checkout page in GA4 must be supported by session recordings showing users struggling with the payment form).
4. **Draft the Report**: Your `Beh_Report.md` MUST include:
    - **Methodology Summary**: Briefly explain how GA4 and session recording data were cross-referenced.
    - **Top 3 Behavioral Observations**: Detail the three most significant validated friction points. For each observation, include:
        - **Observation Description**: A clear, concise statement of the behavioral pattern.
        - **GA4 Evidence**: The quantitative data supporting the observation (e.g., "50% drop-off at step 2").
        - **Session Recording Evidence**: The qualitative data supporting the observation (e.g., "Users repeatedly click the disabled 'Next' button").
        - **Impact Assessment**: A summary of how this behavior affects the user journey.
    - **Unmatched Observations**: A brief list of patterns found in only one data source that warrant further investigation.
5. **Save the document to disk.**
6. **Halt Execution**: Explicitly notify the user: "Behavioral Data Report has been generated and saved. Awaiting the synthesis phase."
