# PHILNITS FE REVIEW APP — CLAUDE MASTER ARCHITECT DIRECTIVE
**Project:** Adaptive, Interactive PhilNITS / ITPEC FE Review Application (PWA)  
**Target Candidate:** 4th-Year BSIT Student (CIT-U) undergoing OJT  
**Target Exam:** PhilNITS / ITPEC Common Fundamental IT Engineer (FE) Examination  
**Exam Date:** Sunday, October 25, 2026  
**Directive Issued:** October 3, 2026 — **22 Days Remaining**  
**Current Progression Milestone:** End of Day 11 → Launching **Day 12**  
**Core Metaphor:** **Duolingo-style Bite-Sized Daily Missions + Anki-style Spaced Repetition (SRS)**  

---

## 1. MANDATE & ROLE FOR CLAUDE

You are the **Lead Software Architect and Learning Engineer** responsible for designing, evaluating, and building this PhilNITS FE Review Application in the [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app) directory.

### Your Responsibilities:
1. **Act as the Primary Creator & Auditor:**
   - Verify every factual claim and exam mechanic against the official sources provided in [`resources/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources).
   - Never fabricate ITPEC exam regulations or topic weights.
   - Distinctly differentiate the **ITPEC Common FE Examination** (administered in the Philippines via PhilNITS in English via paper-and-pencil OMR) from Japan's domestic CBT IPA FE exam.
2. **Execute the Core Learning Philosophy:**
   > **Retrieve → Brief Mental Model → Worked Example → User Commits Fresh Variant → Diagnose Error → Remediate → Schedule via SRS**
   - **Absolute Rule:** NEVER reveal an answer before the learner commits an answer.
   - Active problem-solving over passive reading. Fluency illusion is the enemy.
3. **Build an Offline-First, Responsive PWA:**
   - Must run effortlessly on both desktop PC (widescreen with desk-check split screen) and mobile smartphone (installable PWA, mobile browser, offline cache).
4. **Guide the 22-Day Sprint (Oct 3 – Oct 25):**
   - The user has only 22 days left. Every component, screen, and flashcard must serve high-yield cognitive triage.

---

## 2. SYNTHESIZED REPOSITORY CONTEXT & SOURCE HIERARCHY

All foundational files have been organized into the workspace. Use them as strict sources of truth:

| Source Path | Type | Purpose & Ground Truth Extracted |
|---|---|---|
| [`docs/PhilNITS_FE_Review_App_Handoff.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/PhilNITS_FE_Review_App_Handoff.md) | GPT Handoff Brief | **Primary learner profile:** Complete log of Days 1–11; error logs; verified strengths; persistent weak areas; Day 10/11 revised statistics boundary; error taxonomy. |
| [`resources/research/PhilNITS FE Exam Study Plan.pdf`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/research/PhilNITS%20FE%20Exam%20Study%20Plan.pdf) | Deep Research Report | **21-day tactical study plan:** OMR batch-bubbling strategies, no-calculator math tricks, high-yield formula breakdowns, 3-phase study roadmap (Deconstruction, Volume, Synthesis). |
| [`resources/research/Outline of ITPEC Common Examination.png`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/research/Outline%20of%20ITPEC%20Common%20Examination.png) | Official ITPEC Document | **Official exam structure:** Subject A (60 Q / 90 min) & Subject B (20 Q / 100 min). Compulsory multiple choice. |
| [`resources/books/FE_Exam_Preparation_Book_VOL1_Limite.pdf`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/books/FE_Exam_Preparation_Book_VOL1_Limite.pdf) | Official IPA/PhilNITS Book | **Technology Domain:** Discrete math, computer hardware, operating systems, networks, databases, security, software development. |
| [`resources/books/FE_Exam_Preparation_Book_VOL2_Limite.pdf`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/books/FE_Exam_Preparation_Book_VOL2_Limite.pdf) | Official IPA/PhilNITS Book | **Strategy & Management Domain:** Project management (PERT/CPM, EVM), service management (ITIL/SLA), system architecture, business strategy. |
| [`resources/portals/CIT_U_OpenLearning_LMS.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/portals/CIT_U_OpenLearning_LMS.md) | University Study Portal | **CIT-U Institutional Portal:** Links and cross-references to the official Cebu Institute of Technology – University PhilNITS v1 OpenLearning modules. |

---

## 3. DEEP RESEARCH: OCTOBER 2026 EXAM POSSIBILITIES & TACTICAL TRIAGE

### A. The Modern Post-April 2024 ITPEC FE Blueprint
The exam was overhauled in April 2024. In the October 2026 sitting:
- **Subject A (Morning): 60 questions in 90 minutes (~90 seconds per question)**
  - 4-choice single-answer multiple choice.
  - Distribution: ~30 questions Technology (Computer Systems, OS, Network, DB, Security), ~12 questions Mathematics & Data Structures, ~10 questions System Architecture & Dev Tech, ~8 questions Project Management & Business Strategy.
  - **Zero Calculators:** All arithmetic (Subnetting, AMAT, MTBF/MTTR, Variance, Break-even) cancels cleanly into integers or simple fractions.
- **Subject B (Afternoon): 20 questions in 100 minutes (~5 minutes per question)**
  - **16 Questions:** Universal ITPEC Pseudo-programming Language (Algorithms & Data Structures).
  - **4 Questions:** Information Security Scenarios (Threat vectors, access control matrices, PKI, firewall/filtering rules).
  - Individual programming languages (C, Java, Python) are **eliminated**. All algorithms are expressed in the ITPEC universal pseudo-language.

### B. ITPEC Universal Pseudo-Language Specifications to Render & Enforce
- **Assignment:** `←` (arrow), e.g., `x ← 5`
- **Comparison / Equality:** `=` and `≠`
- **Arithmetic:** `+`, `-`, `×`, `÷`, `mod`
- **Logical:** `and`, `or`, `not`
- **Conditionals:** `if ... elseif ... else ... endif`
- **Loops:** `for (var from start to end step inc) ... endfor`, `while (cond) ... endwhile`, `do ... while (cond)`
- **Indexing Convention:** **1-based array indexing** unless explicitly stated otherwise in the question stem.
- **Sentinel / Uninitialized State:** `undefined`

### C. Candidate Triage Directive (Cognitive Time Management)
Because the candidate is a 4th-year BSIT student with strong software development background:
- **BYPASS / ZERO PRIMARY STUDY TIME:** Basic SQL (`SELECT`, `JOIN`, `GROUP BY`) and standard OOP definitions (Polymorphism, Inheritance). These are already solid and will only be tested in passing.
- **AGGRESSIVE PRIORITY (Vulnerabilities):**
  1. **Two's Complement (Signed binary):** Encoding negative numbers, decoding MSB=1 patterns, 8-bit range `[-128, +127]`.
  2. **IPv4 Subnetting & CIDR:** Host bits, usable hosts ($2^h - 2$), network address, broadcast address, `/26`, `/27`, `/28`, `/29` masks.
  3. **Average Memory Access Time (AMAT):** $\text{AMAT} = h \cdot t_c + (1 - h) \cdot t_m$.
  4. **System Reliability Math:** $\text{MTBF} / (\text{MTBF} + \text{MTTR})$, Series: $R_1 \times R_2$, Parallel: $1 - (1 - R_1)(1 - R_2)$.
  5. **Descriptive Statistics:** Variance step-by-step ($x \to (x - \bar{x}) \to (x - \bar{x})^2 \to \sum / n \to \sqrt{\text{Var}}$). Remember: divided by $n$ per IPA convention!
  6. **Subject B Desk-Checking / Variable State Tracking:** Maintaining loop index updates and array states without swapping variables in memory.

---

## 4. PRODUCT VISION: DUOLINGO + ANKI FUSION (PWA)

The application will merge the best of two high-retention paradigms into an adaptive, gamified, source-grounded review app.

```
+-----------------------------------------------------------------------------------+
|                           PHILNITS FE MASTER REVIEW APP                           |
+-----------------------------------------+-----------------------------------------+
|        DUOLINGO-STYLE MISSIONS          |          ANKI-STYLE SRS ENGINE          |
|  - Daily Study Mission (Day 12 - 22)    |  - Algorithmic SuperMemo / SM-2 Queue   |
|  - "Your Turn" Active Commitment        |  - Flashcard Flipper (Again/Hard/Good)  |
|  - Step-by-Step Problem Progression     |  - Auto-surfaces RED/YELLOW Topics      |
|  - Daily Streak & Gamified Hearts/XP    |  - Filter by Domain / Formula Sheets    |
+-----------------------------------------+-----------------------------------------+
|                  SUBJECT B PSEUDOCODE INTERACTIVE WORKBENCH                       |
|  - ITPEC Syntax-Highlighted Display     |  - Interactive Desk-Check State Table   |
|  - 1-Based Array Memory Visualizer      |  - Step-by-Step Variable State Tracker  |
+-----------------------------------------+-----------------------------------------+
|                     EXAM & ERROR FORENSICS WORKBENCH                              |
|  - 22-Day Countdown & Readiness Score   |  - Error Log Taxonomy [K, C, N, M, T]   |
|  - Timed Subject A/B Simulators         |  - OMR Batch-Bubbling Strategy Rehearsal|
+-----------------------------------------+-----------------------------------------+
```

### Pillar 1: Duolingo-Style Daily Missions
- **Day-by-Day Path:** A visual path displaying Day 12 through Day 22.
- **The "Mission" Structure:**
  1. **Retrieval Warm-up (3-5 mins):** 3 rapid questions targeting the user's known RED/YELLOW topics (Two's complement, subnet masks, variance steps).
  2. **Micro-Lesson (5 mins):** 1 concise mental model or formula explanation (No walls of text!).
  3. **Worked Example (3 mins):** 1 crystal-clear walkthrough.
  4. **Active Challenge ("Your Turn"):** A fresh variant. The learner MUST select/enter an answer and press **Commit** before the explanation is revealed.
  5. **Subject B Tracing (10 mins):** 2 pseudocode tracing problems using the interactive desk-check table.
  6. **Mission Wrap-up:** XP earned, streak maintained, missed questions automatically sent to the Error Log.

### Pillar 2: Anki-Style Spaced Repetition (SRS)
- **Deck Engine:** Built-in SM-2 interval scheduling:
  - Intervals: 1 day (Again), 3 days (Hard), 7 days (Good), 14 days (Easy).
  - Error reset: Any incorrect attempt on a card immediately marks the topic as **RED** and resets interval to Day 0.
- **Card Categories:**
  - *Core Concepts:* Hardware, OS, Networking, DB, Security, Software Dev, PM, Strategy.
  - *Calculation Drills:* Rapid mental math (Subnetting, AMAT, MTBF, SD, CPI/MIPS, Break-even).
  - *Acronyms & Standards:* ISO 27001, PKI, OSI vs TCP/IP, RAID 0/1/5/6/10, COCOMO, PERT.
- **Active Recall Interface:** Front displays question/scenario; user attempts recall -> reveals back -> selects rating (Again / Hard / Good / Easy).

### Pillar 3: Subject B Interactive Pseudocode Workbench
- Formatted with ITPEC universal pseudo-programming language syntax.
- **Interactive Desk-Check State Table:**
  - Displays columns for `Step`, `Line`, loop variables (`i`, `j`), array indices, and flags.
  - Prompts the user: *"What is the value of `sum` after iteration 3?"* or *"Fill in the blank condition [A] to prevent an off-by-one error."*
- Explicit toggle highlighting: **"Remember: Arrays are 1-based (`array[1]` to `array[N]`)"**.

### Pillar 4: Error Forensic Taxonomy & Mastery Tracker
Every single error logged across Missions, SRS, or Quizzes must be classified into exactly one primary cause tag:
- **`[K]` Concept / Knowledge:** Missed rule, forgot formula, or fundamental lack of comprehension.
- **`[C]` Calculation / Arithmetic:** Right approach, but mental math or unit conversion slipped.
- **`[N]` Notation:** Tripped up by `←` vs `=`, 1-based indexing, or `mod` logic.
- **`[M]` Misread / State Tracking:** Swapped variables, misread question constraints, lost current state.
- **`[T]` Time:** Concept understood, but took longer than standard pacing (Subject A: >90s, Subject B: >5m).

**Mastery States:**
- 🔴 **RED:** Immediate vulnerability (e.g., negative two's complement encoding). App automatically injects this into daily warm-ups.
- 🟡 **YELLOW:** Partially mastered, inconsistent, or minor slips (e.g., subnet mask host bits). Scheduled for moderate review.
- 🟢 **GREEN:** Consistently reliable under unfamiliar variants. Scheduled for long-interval maintenance.

---

## 5. CANDIDATE PROFILE AT HANDOFF (OCT 3, DAY 12)

Claude must initialize the app with the candidate's exact performance history:

```json
{
  "candidate": {
    "name": "Zendrix",
    "institution": "Cebu Institute of Technology - University (CIT-U)",
    "program": "BS Information Technology (4th Year, OJT)",
    "exam": "PhilNITS / ITPEC FE Exam",
    "exam_date": "2026-10-25",
    "current_date": "2026-10-03",
    "days_remaining": 22,
    "current_stage": "Day 12"
  },
  "mastery_states": {
    "RED": [
      {
        "topic": "Two's Complement Encoding & Decoding",
        "issue": "Difficulty converting negative decimals to 8-bit two's complement (invert + 1) and recognizing signed bit boundaries [-128, +127].",
        "action": "Daily 3-minute warm-up drill until 5 consecutive flawless conversions."
      },
      {
        "topic": "Variance / Standard Deviation Calculation Process",
        "issue": "Understands mean/median/mode, but process gets forgotten: (x - mean)^2 -> sum -> divide by n -> sqrt. Must divide by n per IPA convention.",
        "action": "Step-by-step interactive calculation workbench."
      },
      {
        "topic": "Pseudocode State Tracking in Complex Loops",
        "issue": "Variable state swapping during nested loop desk checks.",
        "action": "Enforce interactive desk-check table for all Subject B drills."
      }
    ],
    "YELLOW": [
      {
        "topic": "IPv4 Subnetting & Mask Boundaries",
        "issue": "Confusing /26, /27, /28 total addresses vs usable hosts (-2 for net/bcast) and determining valid host ranges.",
        "action": "CIDR fast-drill flashcards."
      },
      {
        "topic": "Data Transfer Time & Unit Conversion",
        "issue": "Bytes vs bits (Mbps vs MB/s) and overhead calculation.",
        "action": "Formula card review."
      },
      {
        "topic": "Standard Deviation Linear Transformation",
        "issue": "Slip on negative multipliers (|a| * sigma).",
        "action": "Rapid concept check."
      }
    ],
    "GREEN": [
      "Binary / Hex / Decimal Conversions",
      "Boolean Logic & Truth Tables (AND, OR, XOR, NAND, NOR, De Morgan)",
      "Set Theory & Propositions (Converse, Inverse, Contrapositive)",
      "CPU Scheduling Algorithms (FIFO, SJF, Round Robin, Priority)",
      "Memory Page Replacement (FIFO, LRU)",
      "System Reliability & Availability Math (MTBF, MTTR, Series, Parallel)",
      "RAID Levels (RAID 0, 1, 5, 6, 10)",
      "Network Protocol & Layer Mapping (OSI 7 Layers, TCP vs UDP, DNS, DHCP, ARP, ICMP)",
      "Descriptive Measures (Mean, Median, Mode, Expected Value)",
      "Binomial Distribution Mean & Variance (np, npq)",
      "Normal Distribution Standardization (z = (x - mu) / sigma)",
      "Basic Linear Regression (y = ax + b)",
      "Basic Subject B 1-Based Array Iteration"
    ]
  }
}
```

---

## 6. DAY 12 THROUGH DAY 22 SPRINT ROADMAP

Claude must build the daily mission sequence according to this schedule:

| Date | Phase | Target Focus | Key Interactive Tasks |
|---|---|---|---|
| **Oct 3 (Day 12)** | Phase 1: Deconstruction | **Statistics Mastery & Two's Complement Retrieval** | 1. Two's complement encoding/decoding speed drill.<br>2. Step-by-step Variance/SD calculation drill.<br>3. Normal distribution z-score table interpretation.<br>4. Subject B: Stacks & Queue pointer tracing. |
| **Oct 4 (Day 13)** | Phase 1 | **CPU Performance & Paging Deep Dive** | 1. AMAT / Cache hit ratio calculations.<br>2. Paging offset, frame number, and internal fragmentation.<br>3. MIPS & CPI conversion drills.<br>4. Subject B: 1-based Array filtering & partitioning. |
| **Oct 5 (Day 14)** | Phase 1 | **Subnetting & Network Calculation Intensive** | 1. CIDR `/24` to `/30` usable host & broadcast calculations.<br>2. Subnet mask bit conversions without calculator.<br>3. Network transfer time problems.<br>4. Subject B: Bubble/Insertion sort state tracking. |
| **Oct 6 (Day 15)** | Phase 1 | **System Reliability, Storage & Security** | 1. Series/Parallel availability math.<br>2. RAID storage capacity & fault tolerance.<br>3. Asymmetric vs Symmetric encryption, PKI, digital signatures.<br>4. Subject B (Security): Access control matrix scenarios. |
| **Oct 7 (Day 16)** | Phase 1 | **Project Management & Business Strategy** | 1. PERT / Critical Path & Float calculations.<br>2. EVM metrics: CV, SV, CPI, SPI.<br>3. Break-Even point formula.<br>4. Subject B: Linked List node insertion & pointer updates. |
| **Oct 8–9 (Days 17–18)** | Phase 2: Volume | **High-Yield Past Question Drilling** | 1. 50 curated high-yield Subject A questions.<br>2. 6 complex Subject B algorithms (Binary Search Trees & Recursion).<br>3. Error Log tagging and review of all missed items. |
| **Oct 10–11 (Days 19–20)**| Phase 2 | **Full Mock Exam Simulations** | **Sat (Simulation 1):** Full 90-min Subject A timed set + OMR Batch-Bubbling rehearsal.<br>**Sun (Simulation 2):** Full 100-min Subject B timed set (16 pseudocode + 4 security).<br>Conduct forensic distractor analysis on all missed items. |
| **Oct 12–15 (Days 21–22)**| Phase 3: Synthesis | **Error Log Clearance & Speed Drills** | 1. Drill top 3 error categories exclusively.<br>2. Rapid 90-second Subject A blitz.<br>3. Clear all Anki SRS queues to 0 due cards. |
| **Oct 23–24** | Rest & Logistics | **Tapering & Mental Readiness** | 1. Formula & Acronym cheat sheet skim.<br>2. Pencil (Mongol 2), eraser, exam ticket preparation.<br>3. Zero high-stress studying; 8+ hours sleep. |
| **Oct 25** | **EXAM DAY** | **Execution Day** | Execute Batch-Bubbling (batches of 10), time boxing, zero unanswered questions (no negative marking). |

---

## 7. RECOMMENDED APPLICATION ARCHITECTURE (`app/`)

Claude should implement the web app in the [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app) folder with a modern, high-performance stack:

### Tech Stack Recommendation
- **Framework:** React 18+ with TypeScript (bootstrapped via Vite)
- **Styling:** Tailwind CSS or Vanilla CSS with modern dark-mode aesthetic (slate/indigo/emerald/rose palette, glassmorphism, crisp typography)
- **State Management:** Zustand or React Context + `localStorage` / `IndexedDB` persistence (zero backend needed; 100% client-side offline capability)
- **Icons:** `lucide-react`
- **PWA Support:** `vite-plugin-pwa` for service worker caching and home-screen installability on Android/iOS.

### Recommended Directory Structure for `app/`
```
app/
├── index.html
├── package.json
├── vite.config.ts
├── tailwind.config.js
├── src/
│   ├── main.tsx
│   ├── App.tsx
│   ├── types/
│   │   ├── question.ts       # Subject A/B Question schemas, choices, tags
│   │   ├── card.ts           # Anki card schema, ease factor, interval, due date
│   │   ├── mission.ts        # Daily mission units (Day 12 - Day 22)
│   │   ├── user.ts           # Streak, XP, hearts, mastery states
│   │   └── errorLog.ts       # [K, C, N, M, T] error records
│   ├── data/
│   │   ├── questionsA.json   # Curated Subject A high-yield question bank
│   │   ├── questionsB.json   # ITPEC Universal Pseudocode & Security scenarios
│   │   ├── srsCards.json     # Pre-populated Anki decks (Math, Net, Sys, Sec, PM)
│   │   ├── formulaVault.json # Cheat sheets for AMAT, MTBF, Subnet, Stats
│   │   └── missionsData.json # Pre-configured Day 12 through Day 22 lesson paths
│   ├── services/
│   │   ├── srsEngine.ts      # SuperMemo SM-2 interval calculator
│   │   ├── storage.ts        # LocalStorage persistence & export/import
│   │   └── timerService.ts   # Pacing tracker (90s / 300s clocks)
│   ├── components/
│   │   ├── common/           # Button, Modal, Badge, ProgressBar, StreakCounter
│   │   ├── dashboard/        # ExamCountdown, MasteryGrid, MissionCard, QuickStats
│   │   ├── duolingo/         # MissionRunner, QuestionCard, CommitButton, ExplanationModal
│   │   ├── anki/             # SrsDeckView, CardFlipper, RatingButtons, TagFilter
│   │   ├── subjectB/         # CodeViewer, DeskCheckTable, ArrayVisualizer, TraceStep
│   │   ├── formulas/         # InteractiveSubnetCalc, AmatCalc, VarianceStepCalc
│   │   └── exam/             # TimedExamSimulator, OmrBubbleSheet, ForensicModal
│   └── styles/
│       └── index.css         # Global dark theme, animations, fonts
```

---

## 8. STEP-BY-STEP EXECUTION PLAN FOR CLAUDE

When you initiate building, execute following this exact sequence:

1. **Phase 1: Project Scaffolding & Design System**
   - Initialize Vite + React + TypeScript inside [`app/`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/app).
   - Configure responsive layout (mobile-first bottom navigation + desktop sidebar).
   - Implement the visual theme: Clean dark mode, glowing mastery indicators (🔴 🟡 🟢), and dynamic streak counter.

2. **Phase 2: Core Data Engine & Storage**
   - Seed candidate state: Initialized with Zendrix's confirmed profile (Day 12 start, October 25 countdown, existing RED/YELLOW/GREEN topics).
   - Implement persistent storage so study progress, streak, and SRS queues survive browser refresh.

3. **Phase 3: Duolingo Daily Mission Runner (Day 12 First)**
   - Build the interactive Question Runner: Question display -> Answer selection -> **COMMIT ANSWER** button -> Instant grading feedback -> Detailed conceptual explanation -> Error classification prompt if incorrect.
   - Assemble **Day 12 Mission**:
     - *Retrieval:* Two's complement 8-bit negative conversion.
     - *Lesson & Variant:* Variance step-by-step calculation ($n$ divisor rule) & normal distribution standardization.
     - *Subject B:* 2 ITPEC pseudocode tracing exercises with desk-check table.

4. **Phase 4: Anki SRS Flashcard Engine**
   - Implement SM-2 algorithm: Next review date computed from user grade (`Again = 0`, `Hard = 3`, `Good = 4`, `Easy = 5`).
   - Populate pre-loaded cards for high-yield formulas, networking acronyms, CPU definitions, and candidate weak points.

5. **Phase 5: Subject B Trace Workbench & Interactive Formula Vault**
   - ITPEC Pseudocode viewer with line numbers and 1-based indexing highlight.
   - Interactive Desk-Check Table where users track variable changes line by line.
   - Interactive calculators: Subnetting mask analyzer and step-by-step Variance calculator.

6. **Phase 6: Exam Simulation & Final Polish**
   - Timed Subject A (90 min) & Subject B (100 min) test runner.
   - Post-test Forensic Review mode that groups missed questions by `[K, C, N, M, T]` and schedules them for immediate SRS drill.

---

## 9. USER INSTRUCTIONS FOR RUNNING CLAUDE

To have Claude review and build from this directive:
1. Provide Claude with this document: [`docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md).
2. Point Claude to the companion references:
   - [`docs/PhilNITS_FE_Review_App_Handoff.md`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/docs/PhilNITS_FE_Review_App_Handoff.md)
   - [`resources/research/PhilNITS FE Exam Study Plan.pdf`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/research/PhilNITS%20FE%20Exam%20Study%20Plan.pdf)
   - [`resources/research/Outline of ITPEC Common Examination.png`](file:///c:/Users/Zendrix/Desktop/fe/fe_reviewer/resources/research/Outline%20of%20ITPEC%20Common%20Examination.png)
3. Prompt Claude:
   > *"I have established our complete PhilNITS FE review plan, source hierarchy, and data model in `docs/CLAUDE_PHILNITS_FE_MASTER_DIRECTIVE.md`. Review this document and begin building the interactive PWA in `app/` starting with Day 12's mission and the Anki SRS engine."*
