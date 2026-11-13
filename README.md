# Market Intelligence Agent – Amazon QuickSuite Capstone

**Status:** ✅ Passed (Udacity Capstone Evaluation — October 30, 2026)

## Project Overview

This project implements an end-to-end, no-code market intelligence agent built inside **Amazon QuickSuite**. It analyzes internal quantitative data alongside external qualitative industry signals to produce an executive decision-grade brief.

## Evaluation Result

The submitted project **Passed (6/6 Rubric Criteria Met)** on **Attempt 2 (October 30, 2026)**.

| Rubric Area | Criterion | Status | Reviewer Feedback Summary |
|---|---|---|---|
| **Research Framing** | Objective & Scope | ✅ Passed | Clear business question, explicit included/excluded scope, and defined timeframe, markets, competitors, and constraints. |
| **Research Framing** | AI-Assisted Research Approach | ✅ Passed | *"Well structured, detailed, and aligned with the project expectations. Great rework!"* — Praised for documenting question types, prioritization, QuickSuite tools, and full workflow screenshots. |
| **Analysis and Evidence** | Visual Evidence | ✅ Passed | *"Good job presenting visual evidence"* — 4 charts (EV market share, registration share, range vs. MSRP, commercial fleet TCO) with chart types, insights, and image captures. |
| **Analysis and Evidence** | Key Market Insights | ✅ Passed | *"Well-structured and evidence-backed analysis. Amazing!"* — 4 verifiable insights backed by internal CSV data, 20 external citations, and a **Sources & Traceability Index**. |
| **Reliability & Communication** | Strategic Implications & Summary | ✅ Passed | *"Perfect!"* — Actionable leadership decisions, 4 explicit **What Should Not Be Concluded** guardrails, and a 5–7 sentence Leadership Summary with confidence level. |
| **Reliability & Communication** | Confidence & Limitations | ✅ Passed | *"Excellent revision!"* — Multi-dimensional confidence ratings for all 4 insights plus 5 concrete limitations (sample size, geographic bias, pricing, tariffs, OEM volatility). |

> **Overall Reviewer Note:** *"Congratulations on successfully completing the Building a Market Research Agent project! I appreciate the depth of work you have demonstrated through your research, analysis, detailed reports, and supporting screenshots... I really appreciate how you applied the feedback and improved your work."*

## Repository Contents

* [`Market_Intelligence_Research_Brief.md`](Market_Intelligence_Research_Brief.md): Full executive brief, research scoping, strategic insights, decision matrix, confidence assessments, and reliability evaluation.
* [`screenshots/`](screenshots/): Visual verification of agent configuration, Quick Index grounding, Quick Research synthesis, live Quick Chat queries, and Quick Spaces organization.

---

## Chapter 2 Alignment: Agent Architecture & Mental Model

### 1. Agent vs. Chatbot Specification

* **Retriever (Chatbot):** Retrieves static paragraphs or links without goal-oriented planning.
* **Reasoner + Actor (Our Agent):** Breaks high-level business goals into sequential queries, consults indexed data, gathers external signals, and returns structured decision matrices.

### 2. The Three Architectural Pillars

* **Purpose (Quick Chat):**
  * *Persona:* Executive market intelligence analyst.
  * *Negative Constraints:* Declines off-topic tasks; states `"Data not present in knowledge base"` instead of hallucinating.
* **Knowledge (Quick Index):**
  * Ground truth provided by ingested Washington State BEV dataset (`ev_market_population_data.csv`).
* **Governance (Quick Spaces):**
  * Access-controlled workspace restricting sensitive project data to authorized stakeholders.

---

## Deliverables & Evidence Checklist

- [x] [`Market_Intelligence_Research_Brief.md`](Market_Intelligence_Research_Brief.md)
- [x] [`screenshots/01_agent_configuration.png`](screenshots/01_agent_configuration.png) (Quick Chat system instructions & guardrails)
- [x] [`screenshots/02_quick_index_grounding.png`](screenshots/02_quick_index_grounding.png) (Dataset linked in Quick Index)
- [x] [`screenshots/03_quick_research_outputs.png`](screenshots/03_quick_research_outputs.png) (External signals with citations)
- [x] [`screenshots/04_quick_chat_live_execution.png`](screenshots/04_quick_chat_live_execution.png) (Live multi-turn Q&A with citations)
- [x] [`screenshots/05_quick_spaces_organization.png`](screenshots/05_quick_spaces_organization.png) (Organized assets in Quick Spaces)
