---
name: analyze_qual_data
description: Analyzes unstructured qualitative data (interviews, tickets, reviews) to extract, group, and quantify user problems. Use during the parallel data analysis phase.
---

# Skill: Analyze Qualitative Data

## Objective
Your goal as the Qualitative Researcher is to read unstructured feedback from users, categorize it into themes, and quantify the frequency and severity of each theme to identify the top 3 user problems.

## Rules of Engagement
- **Artifact Handover**: Save your final output back to the file system.
- **Save Location**: Always output your final document to `outputs/Qual_Report.md`.
- **Constraint**: You MUST always provide direct quotes or evidence from the raw data to support the problems you identify.

## Instructions
1. **Ingest Data**: Read all files (PDFs, Excel, TXT) located in the `inputs/qual_data/` directory. This includes user interviews, customer support tickets, and app reviews.
2. **Group and Tag**: Analyze the raw feedback and categorize individual issues into broader themes (e.g., "Login Friction," "Confusing Navigation").
3. **Quantify Problems**: For each theme, calculate:
    - **Frequency**: How often does this theme appear across all data sources?
    - **Severity**: Based on the sentiment expressed (e.g., frustration, anger), how severe is the impact on the user experience?
4. **Draft the Report**: Your `Qual_Report.md` MUST include:
    - **Methodology Summary**: Briefly explain how the data was categorized and quantified.
    - **Top 3 Problems**: Detail the three most frequent and severe problems. For each problem, include:
        - **Problem Description**: A clear, concise statement of the issue.
        - **Evidence**: At least 2 direct quotes from the raw data supporting the problem.
        - **Impact Assessment**: A summary of frequency and severity.
    - **Other Notable Mentions**: A brief list of emerging issues that didn't make the top 3.
5. **Save the document to disk.**
6. **Halt Execution**: Explicitly notify the user: "Qualitative Data Report has been generated and saved. Awaiting the synthesis phase."
