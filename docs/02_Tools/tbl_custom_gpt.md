# 🧭 Triple Bottom Line Project Advisor — Usage Guide

## Overview
The **Triple Bottom Line (TBL) Project Advisor** is a custom ChatGPT-5 agent that helps Project Managers assess and improve projects across the **People**, **Planet**, and **Profit** dimensions.  
It reads project inputs (charter, risks, constraints, stakeholders, etc.) and returns:
- A quantitative **TBL scorecard**
- Risks and opportunities per dimension
- **Actionable recommendations** with estimated impact
- **Executive summaries** suitable for reporting

Use this tool to make your project reviews more sustainable, balanced, and transparent.

---

## Getting Started

### 1️⃣  Open the Custom GPT
1. In ChatGPT, select **Explore GPTs → My GPTs → Triple Bottom Line Project Advisor** (or click [here](https://chatgpt.com/g/g-68e01c7d6ab08191bdf647d9e903560d-triple-bottom-line-project-advisor))  
2. Click **Use GPT** to start a new conversation.

### 2️⃣  Prepare Your Project Data
Collect or summarize:
- **Project title and summary**
- **Scope, stakeholders, constraints**
- **Known risks**
- **Sustainability or ESG posture**

Tip: keep your input to **2–4 short paragraphs**. You can paste from a charter, RFP, or project brief.

---

## Running an Assessment

### 🧩 Basic Prompt
Copy and modify this template:
```text
Project title: [[Your Project Name]]
Project summary: [[Short description of purpose and goals]]

Key details:
- Scope: [[Key activities]]
- Stakeholders: [[Who’s involved]]
- Constraints: [[Timeline, budget, regulations]]
- Risks (known): [[List key risks]]
- Sustainability posture: [[Company policies or targets]]

Request:
1. Provide a TBL scorecard + confidence.
2. List top 5 risks/opportunities per dimension.
3. Recommend 5 interventions with impact deltas, effort, and rationale.
4. End with a short executive narrative and 3 next steps.

The GPT will return:
- A JSON block (machine-readable structure for dashboards)
- Tables and narrative for human review
```

---

## Reading the Results

### Recommendations

Each recommendation includes:
- **Impact deltas:** how each dimension changes
- **Effort:** low / medium / high
- **Framework reference:** PMI, GRI, SASB, or UN SDG mapping
- **Rationale:** Why it matters

### Executive Narrative

A short, plain-language summary explaining trade-offs and next steps.

---

## Best Practices for PMs
1. Use early and often - run a TBL assessment during initiation, major phase gates, and post-project review.
2. Be transparent - include assumptions and data sources in your input.
3. Act on insights - treat  recommendations as discussion starters, not directives.
4. Track changes - re-run with updated data to measure improvement over time.
5. Share responsibly - outputs may include estimates; confirm data before publishing externally.

---

## Example Workflow
1. Paste the [Cloud Data Migration](prompts/cloud_data_migration.txt) case → get baseline scores.
2. Ask:
```text 
What if we extend the schedule by 2 weeks to reduce overtime and avoid air freight?
```
3. Observe People ↑, Planet ↑, Profit ↓ slightly → balanced TBL
4. Ask for a risk register
```text
Convert the top 5 risks into a risk register with columns:
ID | Risk | TBL Dimension | Likelihood (L/M/H) | Impact (1–5) | Exposure (auto) | Trigger | Owner | Mitigation | Contingency.
```
5.  Ask for a slide-ready summary.
```text
Summarize this project in a slide-ready executive brief:
- Title + 2-sentence context
- Radar values (P,Pl,Pr) with one insight
- 3 must-do moves (verbs first, each with TBL deltas)
- 1 risk to watch, 1 weekly metric, 1 stakeholder to brief
Limit to 120 words.
```
---

## Deeper Analysis Prompts

| Goal | Prompt |
|-----------|-----------|
| Compare schedule & supplier trade-offs | Run a 3-scenario comparison: baseline vs. extended schedule vs. local suppliers. Show updated TBL scores and trade-offs. |
| Improve weakest dimension | Create a 90-day improvement plan for the weakest dimension with levers, owners, and weekly checkpoints. |
| Convert to risk register | Convert the top 5 risks into a risk register with columns: ID, Risk, Dimension, Likelihood, Impact, Owner, Mitigation, Contingency. |
| Generate executive summary | Summarize this project in a slide-ready executive brief (≤120 words) with radar values and top 3 actions. |
| Red-team your assumptions | List 5 optimistic assumptions that could bias the TBL results and how the outcomes would change if they were false. |

---

## Notes
- Outputs are **decision-support**, not compliance documents.
- TBL advisor relies on your input quality - clearer data = stronger recommendations.
- You can export JSON results to Excel or Power BI (or your tool of choice) for tracking over time.

