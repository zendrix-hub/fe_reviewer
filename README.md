# PhilNITS FE Examination (ITPEC) — Master Review Suite & Adaptive App

An evidence-based, adaptive review system designed to prepare for the **PhilNITS / ITPEC Common Fundamental Information Technology Engineer (FE) Examination** on **October 25, 2026**.

---

## 🎯 Target Overview
- **Exam:** PhilNITS / ITPEC Common FE Examination (Philippines Sitting)
- **Exam Date:** Sunday, October 25, 2026
- **Current Study Date:** October 3, 2026 (**22 Days Remaining**)
- **Current Milestone:** Completed Days 1–11 with daily AI coaching → Launching **Day 12**
- **Candidate:** 4th-Year BSIT Student, Cebu Institute of Technology – University (CIT-U), currently on OJT (Internship)

---

## 📂 Repository Structure

```text
fe_reviewer/
├── docs/                                          # Architecture, directives & handoff documents
│   ├── CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md    # Master architecture & prompt for Claude
│   └── PhilNITS_FE_Review_App_Handoff.md          # Days 1–11 logs, error taxonomy, learner state
│
├── resources/                                     # Official syllabus, reference books & portals
│   ├── books/                                     # Official PhilNITS/IPA preparation volumes
│   │   ├── FE_Exam_Preparation_Book_VOL1_Limite.pdf  # Vol 1: Technology Domain
│   │   └── FE_Exam_Preparation_Book_VOL2_Limite.pdf  # Vol 2: Strategy & Management Domain
│   ├── research/                                  # Evidence-based research & official exam outlines
│   │   ├── PhilNITS FE Exam Study Plan.pdf        # 3-week tactical study plan & math tricks
│   │   └── Outline of ITPEC Common Examination.png# Official Subject A & B breakdown
│   └── portals/                                   # Institutional study portals
│       └── CIT_U_OpenLearning_LMS.md              # CIT-U PhilNITS v1 OpenLearning portal notes
│
├── app/                                           # [Target] Source code for the Review App (PWA)
│                                                  # (To be scaffolded and built by Claude)
│
└── README.md                                      # This repository guide
```

---

## 💡 App Concept: Duolingo + Anki Fusion

The application to be built in `app/` is a high-yield **Progressive Web App (PWA)** optimized for both desktop and mobile phone browsers:

1. **Duolingo-Style Daily Missions:**
   - Bite-sized interactive daily missions (Day 12 through Day 22).
   - "Solve before reveal" rule: Users commit an answer before seeing explanations.
   - Micro-streaks, instant grading, and active mental models.
2. **Anki-Style Spaced Repetition (SRS):**
   - SuperMemo SM-2 interval scheduling for rapid concept retrieval.
   - Algorithmic prioritization of candidate vulnerabilities (**Two's complement**, **Subnetting**, **Variance/SD steps**, **CPU AMAT**, **Reliability math**).
   - Error tagging using the standardized taxonomy: `[K]` Concept, `[C]` Calculation, `[N]` Notation, `[M]` Misread/State tracking, `[T]` Time.
3. **Subject B Pseudocode Interactive Workbench:**
   - Universal ITPEC pseudo-programming language support (`←`, 1-based array indexing).
   - Step-by-step desk-check variable state tables.
4. **Timed Simulation & OMR Batch-Bubbling Rehearsal:**
   - Full 90-minute Subject A (60 Qs) and 100-minute Subject B (20 Qs) simulators.
   - Pacing enforcement and post-exam forensic error analysis.

---

## 🤖 Instructions for Claude (Primary Creator & Architect)

1. Open and thoroughly read [`docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md).
2. Reference the detailed historical learner performance and error logs in [`docs/PhilNITS_FE_Review_App_Handoff.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/PhilNITS_FE_Review_App_Handoff.md).
3. Scaffold the PWA in [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app) using Vite + React + TypeScript + Tailwind CSS / Vanilla CSS.
4. Implement Day 12's Mission and the initial Anki SRS deck as the first interactive milestone.
