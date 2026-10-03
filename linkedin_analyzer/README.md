# LinkedIn Analyzer

A sub-project of PM Disco that analyzes your LinkedIn connections and tells you who to contact for your business.

It works from LinkedIn's official data export (no scraping or automation, so your account is safe).

## How to Use

1. **Describe your business**: Fill in `inputs/business/icp.md`.
2. **Export your connections**: LinkedIn → Settings & Privacy → Data privacy → Get a copy of your data → **Connections** → Request archive. It usually arrives by email within about 10 minutes.
3. **Add the file**: Rename it to `Connections_YYYY-MM-DD.csv` and put it in `inputs/connections/`.
4. **Run it**: In Claude Code, ask to run the `run_linkedin_analysis` workflow.
5. **Repeat monthly or quarterly**: Add each new export alongside the old ones. The analyzer will also show new connections, job changes, and promotions.

## Structure

```
linkedin_analyzer/
├── .agents/
│   ├── agents.md                     # Network Analyst, Prospect Strategist
│   ├── skills/
│   │   ├── analyze_connections.md    # Clean + segment the export
│   │   ├── score_and_prioritize.md   # Score vs ICP, outreach plan
│   │   └── compare_snapshots.md      # Changes between exports
│   └── workflows/
│       └── run_linkedin_analysis.md
├── inputs/
│   ├── business/icp.md               # Your business + ideal customer
│   └── connections/                  # Connections_YYYY-MM-DD.csv files
└── outputs/                          # Generated reports
```

## Outputs

| File | What it tells you |
|---|---|
| `Network_Segments.md` | Who is in your network, by function, seniority and company |
| `Prioritized_Contacts.csv` | Every connection scored 0–100 against your ICP |
| `Outreach_Plan.md` | Top contacts, why they fit, and message templates |
| `Network_Changes.md` | New connections, job changes, and promotions since the last export |

## Privacy Note
Your export contains other people's personal data. Consider keeping this repository private and not committing real export files to a shared branch.
