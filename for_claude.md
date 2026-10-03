# CLAUDE AUTONOMOUS EXECUTION DIRECTIVE: PHILNITS FE REVIEW PWA

> **INSTRUCTION FOR CLAUDE:**  
> You are operating in **Autonomous Implementation Mode**.  
> You do **not** need to stop between phases to ask *"Should I proceed?"*.  
> Read the specifications below, consult [`docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md) and [`docs/PhilNITS_FE_Review_App_Handoff.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/PhilNITS_FE_Review_App_Handoff.md), and autonomously execute **Phases 1 through 6** sequentially inside the [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app) directory.

---

## 🎯 MISSION OBJECTIVE
Build a fully working, responsive, offline-first **Progressive Web App (PWA)** in [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app) that fuses **Duolingo-style bite-sized daily missions** with an **Anki-style Spaced Repetition System (SRS)**, tailored for a 4th-year CIT-U BSIT candidate taking the **PhilNITS / ITPEC FE Exam on October 25, 2026** (22 days remaining, starting at **Day 12**).

---

## 📋 REPOSITORY CONTEXT TO INGEST FIRST
Before writing any code, examine these files for grounding:
1. [`docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md) — Master product specification, data models, and 22-day sprint plan.
2. [`docs/PhilNITS_FE_Review_App_Handoff.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/PhilNITS_FE_Review_App_Handoff.md) — Days 1–11 coaching log, error taxonomy (`[K]`, `[C]`, `[N]`, `[M]`, `[T]`), and candidate strengths/vulnerabilities.
3. [`resources/research/Outline of ITPEC Common Examination.png`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/research/Outline%20of%20ITPEC%20Common%20Examination.png) — Official ITPEC structure: Subject A (60 Qs / 90 min) & Subject B (20 Qs / 100 min).

---

## ⚙️ AUTONOMOUS EXECUTION PIPELINE (PHASES 1 TO 6)

Execute each phase in order. Complete each phase fully before progressing to the next.

```text
[Phase 1: Scaffolding] ──> [Phase 2: Core Data] ──> [Phase 3: Day 12 & SRS] ──> 
[Phase 4: Subject B & Formulas] ──> [Phase 5: Days 13-22 Content] ──> [Phase 6: Simulation & PWA]
```

---

### 🔹 PHASE 1: Project Scaffolding & Responsive Layout
1. In [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app), initialize a modern React + TypeScript + Vite application.
2. Install necessary dependencies: `lucide-react`, `canvas-confetti` (for Duolingo streaks), and styling dependencies.
3. Configure modern dark mode aesthetic (rich slate/indigo background, crisp typography, clean cards, glowing status tags: 🔴 RED, 🟡 YELLOW, 🟢 GREEN).
4. Create the dual-mode responsive layout:
   - **Desktop:** Left navigation sidebar (Dashboard, Missions, Anki SRS, Subject B Workbench, Formula Vault, Exam Simulator).
   - **Mobile:** Fixed bottom navigation bar with easy thumb access.
5. Create top header with:
   - **Exam Countdown:** Days remaining until **October 25, 2026** (22 Days).
   - **Daily Streak Counter:** Flame icon with active streak days.
   - **Mastery Readiness Indicator:** Overall % readiness.

---

### 🔹 PHASE 2: Core Data Models & Persistent Storage
1. Define TypeScript interfaces in `src/types/`:
   - `UserProgress`: Streak, current day (Day 12), XP, hearts, last active date.
   - `MasteryTopic`: Topic name, domain, state (`RED` | `YELLOW` | `GREEN`), failure count, last tested date.
   - `SrsCard`: Front, back, domain, ease factor, interval, repetitions, dueDate, errorTag (`[K]`, `[C]`, `[N]`, `[M]`, `[T]`).
   - `Mission`: Day number, title, focus area, warmups, microLesson, workedExample, challengeQuestion, subjectBTrace.
   - `ErrorLogItem`: Question text, user answer, correct answer, errorTag, timestamp.
2. Implement `storageService.ts` utilizing `localStorage` to persist all candidate state, attempts, and SRS card review intervals across sessions.
3. Pre-seed candidate state from `docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`:
   - Candidate: Zendrix, CIT-U BSIT, Day 12 start.
   - Initial 🔴 RED: Two's complement encoding/decoding, Variance/SD calculation process ($n$ divisor), Loop state tracking.
   - Initial 🟡 YELLOW: Subnetting mask boundaries (/26-/29), Data transfer time arithmetic.
   - Initial 🟢 GREEN: Number conversions, Boolean logic, CPU scheduling, FIFO/LRU, MTBF/MTTR, RAID.

---

### 🔹 PHASE 3: Duolingo-Style Mission Engine & Anki SRS (Day 12 First)
1. **Interactive Mission Runner (`components/duolingo/`):**
   - **Active Recall Law:** The explanation and correct answer MUST remain hidden until the user selects/enters an answer and clicks **"Commit Answer"**.
   - Immediate feedback upon commitment:
     - If correct: Positive sound/visual cue, streak increment, +XP.
     - If incorrect: Prompt user to tag error cause (`[K]` Concept, `[C]` Calculation, `[N]` Notation, `[M]` Misread, `[T]` Time), save directly into `ErrorLog`, and mark topic as 🔴 RED.
2. **Build Day 12 Mission Content:**
   - *Warm-up:* Two's complement negative conversion (e.g., encode -42 in 8 bits; decode 11010110).
   - *Micro-lesson:* Variance & Standard Deviation calculation steps ($n$ divisor rule under IPA convention).
   - *Worked Example:* Step-by-step table finding variance of `{4, 8, 6, 5, 7}`.
   - *Your Turn (Fresh Variant):* Fresh set `{3, 7, 5, 9, 6}` requiring step-by-step commit.
   - *Subject B Trace:* Stack pointer trace problem.
3. **Anki-Style SRS Flashcard Engine (`components/anki/`):**
   - Standard SuperMemo SM-2 interval algorithm (`Again`, `Hard`, `Good`, `Easy`).
   - Card flipper with domain badges.
   - Pre-populate 40+ high-yield cards:
     - Math & 2's complement cards.
     - Subnetting rapid calculation cards (/26, /27, /28 usable hosts).
     - AMAT & EAT cache formulas.
     - MTBF, MTTR, and series/parallel availability formulas.
     - PM formulas (EVM: CV, SV, CPI, SPI; PERT).

---

### 🔹 PHASE 4: Subject B Pseudocode Workbench & Interactive Formula Vault
1. **Subject B Workbench (`components/subjectB/`):**
   - Syntax-highlighted ITPEC universal pseudo-programming language viewer:
     - Assignment `←`, comparison `=`, `mod`, `undefined`.
     - Prominent reminder banner: **"⚠️ Note: ITPEC arrays are 1-based (`array[1]` to `array[n]`)"**.
   - **Interactive Desk-Check State Table:**
     - Dynamic table with columns for `Step`, `Line`, loop variables (`i`, `j`), and tracking variables.
     - Allows learner to fill in state row-by-row to verify trace accuracy.
2. **Interactive Formula Vault (`components/formulas/`):**
   - **Subnet Calculator:** Input IP/CIDR (e.g., `192.168.1.0/27`) → outputs subnet mask, host bits, total IPs, usable range, and broadcast address.
   - **AMAT / Cache Calculator:** Input Hit Ratio ($h$), Cache Speed ($t_c$), Memory Speed ($t_m$) → outputs AMAT.
   - **Step-by-Step Variance Workbench:** Input list of numbers → displays full deviation and squared-deviation calculation table with division by $n$.
   - **Reliability Calculator:** Series ($R_1 \times R_2$) and Parallel ($1 - (1-R_1)(1-R_2)$) availability.

---

### 🔹 PHASE 5: Full Mission Data Population (Days 13 through 22)
Populate `data/missionsData.json` with the complete sprint curriculum specified in Section 6 of [`docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md):
- **Day 13:** CPU Performance (AMAT, MIPS, CPI) & Memory Paging (page vs frame, offset, fragmentation).
- **Day 14:** IPv4 Subnetting Intensive (/24 to /30 masks, transfer time, OSI/TCP-IP).
- **Day 15:** System Reliability (MTBF/MTTR/RAID) & Information Security (PKI, digital signatures, access control).
- **Day 16:** Project Management (PERT/Critical Path, EVM metrics) & Business Strategy (Break-even).
- **Days 17–18:** High-Yield Past Question Volume Drills & Algorithm Tracing (Binary Trees & Recursion).
- **Days 19–20:** Full Simulation Rehearsal & Forensic Distractor Analysis.
- **Days 21–22:** Error Log Clearance & Rapid Speed Blitz (90s Subject A, 5m Subject B).

---

### 🔹 PHASE 6: Timed Exam Simulators & Offline PWA Finalization
1. **Exam Simulation Engine (`components/exam/`):**
   - **Subject A Mode:** 60 Questions, 90-minute countdown clock (~90s / Q).
   - **Subject B Mode:** 20 Questions (16 pseudocode + 4 security), 100-minute clock (~5m / Q).
   - **Batch-Bubbling Helper:** Practice bubbling answers in batches of 10 to simulate official OMR paper sheets.
   - **Post-Exam Forensic Review:** Diagnostic breakdown grouping all missed questions by `[K, C, N, M, T]` with one-click "Add to Anki SRS".
2. **PWA Offline Configuration:**
   - Configure Web App Manifest (`manifest.json`) with app icons and standalone display mode.
   - Configure Service Worker for 100% offline asset and question caching.
3. **Build & Quality Check:**
   - Run `npm run build` inside `app/` to ensure zero TypeScript or bundling errors.
   - Output clear instructions on how the user can start the app (`cd app && npm run dev`) and install it on mobile.

---

## 🚀 AUTONOMOUS EXECUTION START
Begin now with **Phase 1** in `app/`. Progress through each phase autonomously until the entire review application is verified and runnable.
