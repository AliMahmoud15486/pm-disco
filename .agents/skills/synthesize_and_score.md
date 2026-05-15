---
name: synthesize_and_score
description: Synthesizes findings from qualitative, behavioral, and quantitative reports, scores issues against the North Star Metric, and generates prioritized problem statements and testable hypotheses. Use after all data analysis is complete.
---

# Skill: Synthesize and Score

## Objective
Your goal as the Lead Product Manager is to synthesize the findings from the research team, score issues against the North Star Metric, and formulate the final prioritized problem statements and testable hypotheses.

## Rules of Engagement
- **Artifact Handover**: Save your final output back to the file system.
- **Save Location**: Always output your final documents to `outputs/Problem_Statements.md` and `outputs/Hypotheses.md`.
- **Constraint**: You MUST wait for the Context Analyst, Qual Researcher, Behavior Analyst, and Data Scientist to complete their reports before beginning your synthesis. You MUST explicitly tie every problem statement back to the North Star Metric.

## Instructions
1. **Review Inputs**: Read the following files:
    - `outputs/Company_Context.md` (Context Analyst)
    - `outputs/Qual_Report.md` (Qual Researcher)
    - `outputs/Beh_Report.md` (Behavior Analyst)
    - `outputs/Quan_Report.md` (Data Scientist)
2. **Synthesize Findings**: Cross-reference the issues identified in each report. Look for themes that appear across multiple data sources (e.g., a high drop-off rate in GA4 that matches a common complaint in user interviews).
3. **Score and Prioritize**: Score each synthesized issue based on its impact on the North Star Metric defined in the Company Context. Use a standard PM framework (e.g., ICE scoring: Impact, Confidence, Ease) to prioritize the issues.
4. **Draft Problem Statements**: Your `Problem_Statements.md` MUST include:
    - **Top 3 Prioritized Issues**: Detail the three most critical issues. For each issue, formulate a standard PM Problem Statement (e.g., "Users are struggling to complete the checkout process, resulting in a 20% drop in conversion rate, which negatively impacts our North Star Metric of Monthly Active Users").
    - **Evidence**: Briefly summarize the qualitative, behavioral, and quantitative data supporting the problem statement.
5. **Generate Hypotheses**: For each of the top 3 problem statements, generate 3 testable hypotheses. Your `Hypotheses.md` MUST include:
    - **Problem Statement 1**:
        - **Hypothesis 1.1**: (e.g., "If we simplify the checkout form to a single page, then conversion rate will increase by 5% because users will experience less friction.")
        - **Hypothesis 1.2**: ...
        - **Hypothesis 1.3**: ...
    - **Problem Statement 2**:
        - **Hypothesis 2.1**: ...
        - **Hypothesis 2.2**: ...
        - **Hypothesis 2.3**: ...
    - **Problem Statement 3**:
        - **Hypothesis 3.1**: ...
        - **Hypothesis 3.2**: ...
        - **Hypothesis 3.3**: ...
6. **Save the documents to disk.**
7. **Halt Execution**: Explicitly notify the user: "Problem Statements and Hypotheses have been generated and saved. The discovery process is complete."
