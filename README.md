# AI Job Application Assistant — Conversation Flow

![Topic](https://img.shields.io/badge/Topic%204-Conversation%20Flow-111827) ![Status](https://img.shields.io/badge/Assessment-Complete-16a34a) ![Tests](https://img.shields.io/badge/Tests-4%2F4%20PASS-16a34a)

A reviewer-friendly evidence package for Topic 4 — Conversation Flow & User Experience, built around the **AI Job Application Assistant** Custom GPT.

## 🚀 Quick Access

| Resource | Link |
|---|---|
| 🤖 Custom GPT | [Open AI Job Application Assistant](https://chatgpt.com/g/g-6ab32eeab8c88191915986ea8efad18d-ai-job-application-assistant) |
| 🎥 Loom Demo | [Watch the Topic 4 walkthrough](https://www.loom.com/share/27a95bc5e1524778bf8f81625c602943) |
| 📄 Assessment Report | [Open PDF](./Topic_4_Conversation_Flow_Assessment.pdf) |
| 🧭 Flow Design | [flow_design.md](./flow_design.md) |
| 🧪 Test Observations | [test_observations.md](./test_observations.md) |

> The Custom GPT link requires appropriate ChatGPT access. The Loom video demonstrates the implementation and testing.

## 🎯 Objective

The design provides a logical conversation flow for first-time and returning users, targeted clarification for incomplete or ambiguous requests, and completion/confirmation logic. The assessment evidence describes the first-time path as brief orientation → understand goal → check required information → clarify when necessary → execute → confirm, with a shorter context-driven path for returning users.

## 🧠 Conversation Architecture

```text
START
  |
  +--> First-Time User --------> Brief orientation
  |                                  |
  +--> Returning User ----------> Use existing context
                                     |
                                     v
                              Understand user goal
                                     |
                              Required info ready?
                               /             \
                             YES              NO
                              |                |
                              v                v
                         Execute task     Clarify only
                              |           what is missing
                              |                |
                              |                v
                              |          Re-check request
                              |                |
                              +-------<--------+
                                       |
                                       v
                               Present + confirm
                                       |
                                      END
```

## 🔍 Clarification Strategy

The GPT uses focused questions instead of a fixed questionnaire. Examples include identifying the target job/application, requesting the job description, asking for a resume/background when comparison or tailoring requires it, clarifying the requested type of application support, and asking for a specific missing requirement. The design explicitly says not to ask all questions automatically.

## 🧪 Validation

Four practical scenarios were tested:

| # | Scenario | Expected behavior | Result |
|---:|---|---|---|
| 1 | “Help me with my application.” | Ask for target job/application and relevant materials. | ✅ PASS |
| 2 | “Improve my resume for this job.” | Request job description and current resume. | ✅ PASS |
| 3 | “Analyze this job for me.” | Request missing job description. | ✅ PASS |
| 4 | “Analyze this job description and compare its requirements with my resume.” | Request both missing inputs before comparison. | ✅ PASS |

See [`test_observations.md`](./test_observations.md) for the recorded observations.

## 📦 Repository Structure

```text
.
├── README.md
├── flow_design.md
├── test_observations.md
├── Topic_4_Conversation_Flow_Assessment.pdf
├── LICENSE
└── .gitignore
```

## 🎥 Demo

[![▶ Watch Loom Demo](https://img.shields.io/badge/▶%20Watch-Loom%20Demo-625df5?style=for-the-badge)](https://www.loom.com/share/27a95bc5e1524778bf8f81625c602943)

## 📄 Assessment Evidence

[![Open Assessment PDF](https://img.shields.io/badge/📄%20Open-Assessment%20PDF-111827?style=for-the-badge)](./Topic_4_Conversation_Flow_Assessment.pdf)

[![Open Flow Design](https://img.shields.io/badge/🧭%20Open-Flow%20Design-2563eb?style=for-the-badge)](./flow_design.md)

[![Open Test Observations](https://img.shields.io/badge/🧪%20Open-Test%20Observations-16a34a?style=for-the-badge)](./test_observations.md)

## ✅ Assessment Coverage

- First-time user flow mapped
- Returning user flow mapped
- Clarification questions defined
- Flow logic integrated into the Custom GPT
- Incomplete/ambiguous input testing completed
- Flow design documented
- Test observations documented
- Loom demonstration linked

## 👤 Author

**SHAIK MOHAMMAD SHAHEED**  
GitHub: [@shaikshahid777](https://github.com/shaikshahid777)

---

This repository is an assessment evidence and documentation package. The Custom GPT itself is configured in ChatGPT; no private credentials or secrets are stored here.
