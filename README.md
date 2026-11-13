**Status:** ✅ Passed (Udacity Capstone Evaluation — October 30, 2026)

A no-code AI-assisted market intelligence agent built in **Amazon QuickSuite** that combines internal EV registration data with external industry signals to produce grounded, executive-ready fleet strategy recommendations.

## Main Project Deliverable

**[Open the Market Intelligence Research Brief](Market_Intelligence_Research_Brief.md)**

## Project Overview

Strategic and product teams evaluating commercial electric vehicle (EV) fleet entry face fragmented signals across OEM pricing shifts, federal tax credit expirations, charging infrastructure deficits, and state-level mandates. Manually reconciling internal registration data with external industry reports is slow and prone to unsupported assumptions.

This project builds a grounded market intelligence workflow inside **Amazon QuickSuite**. The agent queries an indexed Washington State Battery Electric Vehicle (BEV) registration dataset alongside 20 external industry and government sources to deliver cited insights, multi-dimensional confidence ratings, and explicit decision guardrails for leadership.

## Business Objectives

* Evaluate North American mid-tier commercial EV fleet entry viability for **2026–2027**.
* Ground quantitative market-share and pricing claims in verified internal registration data rather than unverified LLM outputs.
* Quantify the impact of **Section 45W tax credit expiration**, **NACS (SAE J3400)** standardization, and public corridor charging bottlenecks.
* Translate findings into phased go-to-market actions paired with explicit **What Should Not Be Concluded** guardrails.

## Data Sources

The intelligence layer combines:

* **Internal Ground Truth (`ev_market_population_data.csv`):** Washington State BEV registration sample (`n = 11` representative records across 6 counties, 100% BEV and CAFV-eligible) indexed in **Quick Index**.
* **External Market Signals (`[1]`–`[20]`):** 20 verifiable industry, OEM, and federal policy sources gathered via **Quick Research** (including FHWA/NEVI quarterly trackers, Deloitte, RMI, CNBC, CleanTechnica, and EV Engineering Online).
* **Visualizations:** 4 analytical charts covering U.S. EV market share (2024 vs. 2025), grounded manufacturer registration share, electric range vs. Base MSRP, and commercial fleet TCO by duty cycle.

## Agent Architecture

 Internal CSV (ev_market_population_data.csv) + 20 External Quick Research Sources
|
Quick Index Grounding (✓ Ready)
|
Quick Spaces Governance & Access Control
|
Quick Chat Agent (Persona + Negative Constraints)
|
4 Key Insights + Confidence Ratings + Decision Guardrails

### Core Design

* **Workspace Governance (`Quick Spaces`):** `Market Intelligence - EV Fleet Strategy` with viewer-level stakeholder permissions.
* **Knowledge Grounding (`Quick Index`):** Linked to `ev_market_population_data.csv` to eliminate quantitative hallucinations.
* **Agent Persona & Guardrails (`Quick Chat`):** `Market Intelligence Agent - Electric Mobility`, configured to decline off-topic requests and return `"Data not present in knowledge base"` when evidence is missing.
* **External Synthesis (`Quick Research`):** 4-layer scoped queries prioritizing OEM pricing (60%), internal CSV segmentation (25%), and state ACT mandates (15%).

## Key Findings Summary

| Insight | Core Signal | Confidence | Strategic Takeaway |
|---|---|---|---|
| **1. OEM Price Compression & Utility Gap** | GM grew to **13.2%** (`$35k` Equinox EV); **$3k–$10k** incentives; F-150 Lightning at **$55,974** | **High** | Adopt multi-OEM procurement (**GM, Ford, Kia, Nissan, Tesla**) |
| **2. Public Corridor Deficit** | **59.1%** corridor coverage; **96** operational NEVI stations; EV-to-charger trending **18:1 → 80:1** | **High** | Bundle **shared depot load-management** software |
| **3. Post-45W Urban TCO Advantage** | **~9%–24%** TCO edge on **80–250 mi/day** return-to-base routes; **11 ACT states** | **Medium** | Launch a **60-day Q1–Q2 2027 pilot** in ACT-mandate states |
| **4. Dual-Standard NACS Transition** | **~20%** non-Tesla EVs shipping native NACS; **72.7%** grounded fleet is CCS1 | **Medium** | Mandate **dual CCS1 + SAE J3400 (NACS)** readiness through 2028 |

## Evaluation Result

The submitted project **Passed (6/6 Rubric Criteria Met)** on **Attempt 2 (October 30, 2026)**.

| Rubric Area | Criterion | Status | Reviewer Feedback Summary |
|---|---|---|---|
| **Research Framing** | Objective & Scope | ✅ Passed | Clear business question, explicit included/excluded scope, and defined timeframe, markets, competitors, and constraints. |
| **Research Framing** | AI-Assisted Research Approach | ✅ Passed | *"Well structured, detailed, and aligned with the project expectations. Great rework!"* — Praised for documenting question types, prioritization, QuickSuite tools, and workflow screenshots. |
| **Analysis and Evidence** | Visual Evidence | ✅ Passed | *"Good job presenting visual evidence"* — 4 charts (EV market share, registration share, range vs. MSRP, commercial fleet TCO) with chart types, insights, and image captures. |
| **Analysis and Evidence** | Key Market Insights | ✅ Passed | *"Well-structured and evidence-backed analysis. Amazing!"* — 4 verifiable insights backed by internal CSV data, 20 external citations, and a **Sources & Traceability Index**. |
| **Reliability & Communication** | Strategic Implications & Summary | ✅ Passed | *"Perfect!"* — Actionable leadership decisions, 4 explicit **What Should Not Be Concluded** guardrails, and a 5–7 sentence Leadership Summary with confidence level. |
| **Reliability & Communication** | Confidence & Limitations | ✅ Passed | *"Excellent revision!"* — Multi-dimensional confidence ratings for all 4 insights plus 5 concrete limitations (sample size, geographic bias, pricing, tariffs, OEM volatility). |

> **Overall Reviewer Note:** *"Congratulations on successfully completing the Building a Market Research Agent project! I appreciate the depth of work you have demonstrated through your research, analysis, detailed reports, and supporting screenshots... I really appreciate how you applied the feedback and improved your work."*

## Known Limitations and Next Steps

1. **Expand Internal Sample Coverage:** The grounded CSV (`n = 11` across 6 Washington counties) reflects Pacific Northwest ACT-state conditions; refresh with multi-state commercial fleet registration data.
2. **Validate B2B Fleet Invoice Pricing:** Published Base MSRP (`$26,500–$74,990`) excludes negotiated fleet volume rebates, dealer markups, and commercial upfitting costs.
3. **Run Localized Utility & Climate Pilots:** Validate the projected 9%–24% TCO advantage against local utility demand-charge tariffs and 20%–30% winter range degradation during the Q1–Q2 2027 pilot.
4. **Track OEM NACS Schedules Quarterly:** Monitor legacy OEM capital restructuring (e.g., Ford's $19.5B EV charge) for potential delays in 2026–2028 native SAE J3400 port rollouts.

## Repository Structure

 .
├── Market_Intelligence_Research_Brief.md # Full brief, insights, citations & decision appendix
├── README.md # Project overview, architecture & evaluation summary
└── screenshots/ # QuickSuite evidence (config, grounding, research, charts)
├── 01_agent_configuration.png
├── 02_quick_index_grounding (1).png
├── 03_quick_research_outputs (1).png
├── 04_quick_chat_live_execution (1).png
├── 05_quick_spaces_organization (1).png
├── 06_ev_market_share_visual_evidence.png
├── 07_quick_research_sources.png
├── 08_quick_research_sources_10_to_20.png
├── 09_quick_chat_pie_chart_grounding (1).png
├── 10_quick_chat_scatter_plot.png
├── 11_tco_comparison_chart (1).png
└── 12_quick_chat_competitive_landscape.png



## Reproducing in Amazon QuickSuite

1. Create a Space named `Market Intelligence - EV Fleet Strategy` in **Quick Spaces**.
2. Upload `ev_market_population_data.csv` into **Quick Index** and wait for status `✓ Ready`.
3. Create the **Quick Chat Agent** (`Market Intelligence Agent - Electric Mobility`) with executive analyst instructions and strict `"Data not present in knowledge base"` fallback guardrails.
4. Run layered **Quick Research** queries for 2024–2027 North American EV pricing, NEVI/NACS infrastructure, and post-45W TCO benchmarks.
5. Synthesize outputs and generate charts inside **Quick Chat** linked to the indexed Space.

## Deliverables & Evidence Checklist

- [x] [`Market_Intelligence_Research_Brief.md`](Market_Intelligence_Research_Brief.md)
- [x] [`screenshots/01_agent_configuration.png`](screenshots/01_agent_configuration.png)
- [x] [`screenshots/02_quick_index_grounding (1).png`](screenshots/02_quick_index_grounding%20(1).png)
- [x] [`screenshots/03_quick_research_outputs (1).png`](screenshots/03_quick_research_outputs%20(1).png)
- [x] [`screenshots/04_quick_chat_live_execution (1).png`](screenshots/04_quick_chat_live_execution%20(1).png)
- [x] [`screenshots/05_quick_spaces_organization (1).png`](screenshots/05_quick_spaces_organization%20(1).png)

## Responsible Use

This project is an educational and strategic research proof of concept. All capital allocation, fleet procurement, and utility interconnection decisions should be validated through a localized 60-day operational pilot and current primary utility/OEM quotes.

## Author

**Abhik Mehta**
Udacity Generative AI / Amazon QuickSuite Capstone — Market Research Agent
