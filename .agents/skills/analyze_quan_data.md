---
name: analyze_quan_data
description: Analyzes business dashboard snapshots and structured CSV data to extract key business observations and trends. Use during the parallel data analysis phase.
---

# Skill: Analyze Quantitative Data

## Objective
Your goal as the Data Scientist is to analyze business dashboard snapshots and structured CSV data to extract key business observations, trends, and anomalies.

## Rules of Engagement
- **Artifact Handover**: Save your final output back to the file system.
- **Save Location**: Always output your final document to `outputs/Quan_Report.md`.
- **Constraint**: You MUST focus only on business-level metrics (e.g., retention, churn, MRR, conversion rates) and not individual user behaviors.

## Instructions
1. **Ingest Data**: Analyze the CSV exports and dashboard screenshots located in `inputs/quan_data/`.
2. **Analyze Dashboards**: Identify key trends, anomalies, and areas of underperformance in the business metrics.
3. **Draft the Report**: Your `Quan_Report.md` MUST include:
    - **Methodology Summary**: Briefly explain how the business data was analyzed.
    - **Key Business Observations**: Detail the most critical business data observations. For each observation, include:
        - **Observation Description**: A clear, concise statement of the business trend or anomaly.
        - **Evidence**: The quantitative data supporting the observation (e.g., "MRR growth slowed to 2% MoM").
        - **Impact Assessment**: A summary of how this trend affects the overall business health.
    - **Other Notable Metrics**: A brief list of secondary metrics that warrant further investigation.
4. **Save the document to disk.**
5. **Halt Execution**: Explicitly notify the user: "Quantitative Data Report has been generated and saved. Awaiting the synthesis phase."
