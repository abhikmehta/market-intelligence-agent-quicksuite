# Market Intelligence Agent – Amazon QuickSuite Capstone

**Status:** ✅ Passed (Udacity Capstone Evaluation — October 30, 2026)

## Project Overview

This project implements an end-to-end, no-code market intelligence agent built inside **Amazon QuickSuite**. It analyzes internal quantitative data alongside external qualitative industry signals to produce an executive decision-grade brief.

### Evaluation Highlights
* **Research Framing:** Clear business objective, explicit inclusion/exclusion scope, and structured AI-assisted research workflow.
* **Analysis & Evidence:** 4 verifiable market insights backed by internal dataset metrics, external signals, and a **Sources & Traceability Index**.
* **Reliability & Communication:** Per-insight confidence assessments, concrete limitations/risks, and explicit non-conclusions for executive decision-making.

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
  * Ground truth provided by ingested Kaggle dataset (`Electric_Vehicle_Population_Data.csv`).
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
