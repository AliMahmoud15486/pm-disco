---
name: analyze_context
description: Analyzes raw company documents to establish the business context and define the North Star Metric. Use when the discovery process begins.
---

# Skill: Analyze Company Context

## Objective
Your goal as the Context Analyst is to read raw company documents and translate them into a structured business context, defining a single, clear North Star Metric.

## Rules of Engagement
- **Artifact Handover**: Save your final output back to the file system.
- **Save Location**: Always output your final document to `outputs/Company_Context.md`.
- **Constraint**: You MUST base your analysis strictly on the provided company documents in `inputs/company_details/`. Do not invent business models or assume strategies not present in the source files.

## Instructions
1. **Analyze Requirements**: Deeply analyze all text files found in the `inputs/company_details/` directory.
2. **Draft the Document**: Your `Company_Context.md` MUST include:
    - **Executive Summary**: A brief, high-level overview of the company and its product.
    - **Business Model**: How the company creates, delivers, and captures value.
    - **Target Audience**: Who the primary users and buyers are.
    - **Strategic Goals**: The current overarching objectives of the business.
    - **North Star Metric (NSM)**: Define a single NSM that best aligns with the strategic goals. Explain *why* this metric was chosen and how it reflects both customer value and business success.
3. **Save the document to disk.**
4. **Halt Execution**: Explicitly notify the user: "Company Context and North Star Metric have been defined and saved. Awaiting the next phase of the discovery process."
