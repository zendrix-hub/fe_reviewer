# PhilNITS FE Review App — Chat Handoff / Product Brief

**Purpose:** Handoff document for Gemini (research/background source) and Claude (primary creator, evaluator, and product architect) to design/build an effective PhilNITS FE review website/app.

**Exam target:** PhilNITS / ITPEC Common Fundamental Information Technology Engineer (FE)  
**Target sitting:** 25 October 2026  
**Study start in this chat:** 20 September 2026  
**Current handoff point:** After Day 11, before Day 12

---

## 1. USER GOAL

The user is already registered for the **PhilNITS FE exam**.

The goal is no longer deciding whether to take FE. The goal is:

> **Understand the material deeply enough to solve unfamiliar FE questions, while building a repeatable daily review system that diagnoses weaknesses and improves them over time.**

The user wants an effective study/review website or app that can become the central system for:

- daily lessons
- spaced repetition
- adaptive review
- question practice
- error diagnosis
- weak-topic tracking
- mock exams
- progress tracking
- source-grounded explanations
- exam countdown
- Subject A + Subject B preparation

The user prefers learning through **active problem solving**, not long passive explanations.

Core study philosophy:

> **Learn → Explain → Solve → Commit an answer → Diagnose → Correct → Re-solve → Review later**

The app should optimize for **demonstrated understanding**, not the feeling of familiarity.

---

## 2. SOURCE / RESEARCH WORKFLOW

Three-AI workflow:

### Gemini = Research / Background Check

Gemini is used as the primary deep-research engine.

Responsibilities:

- verify PhilNITS/ITPEC/IPA facts
- gather official syllabus information
- identify official past papers/resources
- research concepts
- identify source-backed exam scope
- distinguish current ITPEC FE from Japan's domestic IPA FE
- collect official references
- produce a structured research knowledge base

### Claude = Primary Creator / Auditor

Claude is the main creator of the study website/app.

Claude should:

- consume Gemini's research
- independently challenge questionable claims
- use the Claude audit as a reliability layer
- design the information architecture
- design the learning/review engine
- create the study workflow
- build the actual app/website
- preserve source hierarchy
- avoid unsupported claims
- keep uncertain items explicitly marked

### ChatGPT / SENSIE = Daily Study Coach

This chat is the actual teaching layer.

Responsibilities:

- teach daily lessons
- ask questions before revealing answers
- evaluate reasoning
- maintain error log
- identify recurring misconceptions
- decide what needs remediation
- generate adaptive follow-up drills
- run mock exams
- maintain the user's mastery state

The intended app should reproduce the useful parts of this coaching workflow.

---

## 3. TRUST / SOURCE RULES

The Claude audit found that Gemini's original research was strong on hard exam facts but weaker on inference and topic-weighting claims.

Important corrections from the audit:

- Subject A/B format, timing, question counts, 16+4 Subject B split, notation, dates, fees, removal policy, and Japan HSP relevance were substantially verified.
- The original research incorrectly mixed the ITPEC scale with the Japan IPA 600/1,000 scale. The ITPEC outline states 100 total / 60 pass points; subject-level application still required direct confirmation.
- The original research claimed a "current post-2024 ITPEC syllabus," but the accessible English FE syllabus is IPA FE Syllabus Ver. 4.0 (2016). Subject A scope is unchanged, while Subject B changed in 2024. Subject B should therefore be grounded primarily in the 2023 ITPEC Outline and official Subject B sample/notation, not blindly in old language-specific syllabus sections.
- Past-paper frequency claims in the original report were not sufficiently cited. Do not turn "appeared before" into "guaranteed to appear."
- Official post-change papers are 2024S, 2024A, 2025S, 2025A, and 2026S; the official papers are hosted as ZIP/PDF resources, with answer keys but no worked solutions.
- Exam-day details such as calculator rules, permit/ID mechanics, delivery mode, exact pass implementation, and certain venue details remained unverified in the audit. The app must not invent them.

The audit's overall conclusion was:

> reliable for exam logistics after corrections, but not reliable as a topic-weighting knowledge base until the real papers are tallied.

Source file:
`philnits_fe_audit_2026-09-20.md`

Relevant verified sections include the audit's Bottom Line, Verified Information, corrected Subject A/Subject B maps, and corrected study strategy.

---

## 4. VERIFIED EXAM BASELINE

Use these as the current baseline, but preserve source attribution:

- Target exam: **ITPEC Common FE administered in the Philippines by PhilNITS**
- Next sitting at the time of the audit: **25 October 2026**
- Subject A: **60 compulsory multiple-choice questions, 90 minutes**
- Subject B: **20 compulsory multiple-choice questions, 100 minutes**
- Subject B scope: **16 algorithm/programming + 4 information security**
- Subject B uses the ITPEC universal pseudo-language
- Important notation:
  - `←` assignment
  - `=` equality/comparison
  - `≠`
  - `× ÷ mod`
  - `> < ≥ ≤`
  - `and / or / not`
  - `if / elseif / else / endif`
  - `for / while / do...while`
  - arrays commonly start at 1 unless the stem says otherwise
  - `undefined`
- FE fee listed by PhilNITS: ₱2,500
- Removal fee listed: ₱1,200
- Removal policy listed as one year from exam date
- Subject A average pacing: ~90 seconds/question
- Subject B average pacing: ~5 minutes/question
- Japan HSP relevance is documented by ITPEC/IPA, but immigration-specific details should remain source-cited rather than paraphrased loosely.

These baseline facts were extracted from the Claude audit's verified-information section.

---

## 5. STUDY SYSTEM DESIGN

### Daily study structure

The corrected study strategy recommends a weekday structure around:

1. **15 min retrieval / flashcards / error-log warm-up**
2. **45–60 min main topic**
3. **30–45 min Subject B tracing**
4. **~5 min error-log update**

Weekends can use a longer timed set + forensic review.

The user's practical learning preference developed in this chat is:

> **Short explanation → example → user attempt → grading → correction → similar problem**

Do not dump an entire chapter before the learner demonstrates anything.

### Mastery should be evidence-based

Each topic should have a state:

- **RED** — dangerous conceptual gap
- **YELLOW** — partially understood / inconsistent
- **GREEN** — reliable under unfamiliar questions

A topic should only move to GREEN after successful performance across varied questions, not because the user can repeat a definition.

---

## 6. ERROR LOG SYSTEM

Every wrong answer should be classified as exactly one primary cause unless multiple causes are clearly present:

### K — Knowledge / Concept

The underlying rule was not understood.

Example:
- confusing union and intersection
- not understanding LRU
- not knowing what MTTR means

### C — Calculation / Arithmetic

Correct method, incorrect arithmetic/unit.

Example:
- 20/5 incorrectly calculated
- forgot seconds → milliseconds
- arithmetic slip in variance

### N — Notation

Misread exam notation.

Example:
- `←` vs `=`
- 1-based indexing
- `mod`
- pseudo-language loop boundary

### M — Misread / State-tracking

Question was understood incorrectly or current variable state was lost.

Example:
- swapping final x/y
- using original variable value after it was changed
- answering a different quantity than asked

### T — Time

Concept understood but too slow.

The app should preserve these cause tags because different causes require different remediation.

---

## 7. IMPORTANT LEARNING PATTERNS DISCOVERED IN THIS CHAT

### Recurring weakness: two's complement

The user repeatedly struggled with:

- encoding negative integers
- decoding negative two's-complement bit patterns
- remembering invert + 1
- distinguishing signed two's complement from unsigned binary
- the 8-bit range

The user improved but remained inconsistent until later sessions.

App requirement:

> Keep a short two's-complement retrieval drill active until the user can both encode AND decode negative values correctly across multiple variants.

Mental procedure:

**Encoding negative:**
1. Convert positive magnitude to binary
2. Invert bits
3. Add 1

**Decoding negative:**
1. Detect MSB = 1
2. Invert
3. Add 1
4. Convert magnitude
5. Apply negative sign

8-bit signed range:
**−128 to +127**

### Recurring weakness: variable-state tracing

The user initially lost the updated values of variables during Subject B pseudocode.

App requirement:

> Use desk-check/state tables for tracing exercises.

Recommended table:

| Step | variable 1 | variable 2 | variable 3 |
|---|---:|---:|---:|

The learner should update state after every assignment.

### Recurring weakness: subnetting details

The user learned:

- CIDR host bits
- total addresses
- usable hosts
- subnet masks
- network / first usable / last usable / broadcast

But repeatedly confused:
- /26 vs /27 vs /28 masks
- total addresses vs usable hosts
- actual address ranges

App requirement:

> Subnet practice should include both arithmetic and actual address-range questions.

Example pattern:

`192.168.10.0/26`

- host bits = 6
- total addresses = 64
- usable hosts = 62
- network = .0
- first usable = .1
- last usable = .62
- broadcast = .63

### Recurring weakness: variance / standard deviation

At Day 10–11, the user understood mean/median/mode but forgot the variance process.

Required procedural memory:

1. Find mean
2. Subtract mean from each value
3. Square each deviation
4. Sum squared deviations
5. Divide by `n` under the user's stated IPA convention
6. Square root for SD

Mental model:

> SD = how spread out values are around the mean.

Transformation rules:
- adding a constant changes nothing
- multiplying by `a` multiplies SD by `|a|`

### Strength: Subject B simple tracing

Across Days 1–11 the user became consistently strong at:
- arrays
- 1-based indexing
- loops
- if conditions
- arithmetic updates
- simple filtering

App should keep Subject B active daily rather than delaying it.

### Strength: Boolean logic

The user performed well on:
- AND
- OR
- XOR
- NAND
- NOR
- NOT
- compound expressions
- truth tables
- propositions
- converse/inverse/contrapositive

### Strength: reliability / availability

The user became strong at:
- MTBF
- MTTR
- availability
- series vs parallel
- FIFO/LRU
- RAID identification

### Strength: networking protocol recognition

Strong associations:
- MAC → Data Link → switch
- IP → Network → router
- DNS → name to IP
- DHCP → configuration
- ARP → IP to MAC
- ICMP → diagnostic / ping
- NAT → address translation
- TCP → reliable / connection-oriented
- UDP → connectionless

---

## 8. DAY-BY-DAY PROGRESS TO DATE

### Day 1 — Subject B notation + binary/hex

Covered:
- FE pseudo-language notation
- assignment vs comparison
- 1-based array indexing
- variable-state tracing
- binary → decimal
- decimal → binary
- binary ↔ hex

Observed:
- numeric conversions were strong
- initial variable-tracing errors
- initial indexing confusion
- initially used irrelevant reasoning for a condition

Status:
- number conversion: GREEN
- basic tracing: improving

---

### Day 2 — Two's complement + shifts + overflow

Covered:
- two's complement
- signed range
- left shift
- logical right shift
- arithmetic right shift
- overflow

Observed:
- recurring negative-value encoding/decoding weakness
- shift operations stronger
- overflow concept improved

Status:
- two's complement: RED/YELLOW
- shifts: GREEN
- overflow: improving

---

### Day 3 — Boolean logic

Covered:
- NOT
- AND
- OR
- XOR
- NAND
- NOR
- truth tables
- compound expressions

Observed:
- very strong overall
- two's complement remained the weak retrieval topic

---

### Day 4 — Sets + propositions

Covered:
- union
- intersection
- difference
- complement
- propositions
- implication
- converse
- inverse
- contrapositive

Observed:
- proposition logic strong
- initial union/intersection confusion
- complement confusion
- two's complement remained weak

---

### Day 5 — CPU architecture/performance

Covered:
- clock cycle
- CPI
- CPU execution time
- MIPS
- pipeline
- cache hierarchy
- cache hit/miss
- EAT

Observed:
- EAT good
- average CPI good
- MIPS and unit conversion needed work
- pipeline throughput needed explanation

---

### Day 6 — Memory management

Covered:
- paging
- page vs frame
- page offset
- page-number bits
- internal/external fragmentation
- page fault
- FIFO
- LRU
- FCFS
- SJF
- Round Robin
- Priority

Observed:
- scheduling strong
- FIFO/LRU strong
- paging architecture initially weak

---

### Day 7 — Paging remediation

Covered:
- paging calculations
- program pages vs frames
- page faults
- fragmentation
- FIFO/LRU

Observed:
- major improvement in paging architecture
- remaining issue: arithmetic/round-up details
- two's-complement encoding still weak

---

### Day 8 — Reliability / availability / RAID

Covered:
- reliability vs availability
- MTBF
- MTTR
- availability formula
- series systems
- parallel redundancy
- RAID 0/1/5/6/10
- response time vs throughput

Observed:
- reliability math became strong
- RAID recognition strong
- response-time/throughput initially reversed

---

### Day 9 — Networking

Covered:
- OSI
- TCP/IP
- MAC/IP
- switches/routers
- IPv4
- CIDR
- subnet capacity
- subnet masks
- DNS
- DHCP
- ARP
- ICMP
- NAT
- TCP/UDP
- transfer time

Observed:
- protocol recognition strong
- subnet range/mask details needed reinforcement
- two's-complement decoding still recurring
- basic Subject B tracing remained strong

---

### Day 10 — Probability & statistics

Initial session covered:
- probability basics
- complement
- union/intersection
- mutually exclusive
- independent
- permutation
- combination
- conditional probability
- expected value
- mean/median/mode
- variance concept
- SD concept
- correlation
- regression

Observed:
- probability basics mixed
- expected value strong
- mean/median/mode strong
- SD concept unclear
- correlation/causation distinction needed emphasis

User then provided a **revised Day 10 plan** anchored to:
- IPA FE Prep Book Vol.1 §7.3.5, pp.286–290
- Ch.7/past-exam items
- counting as a supplement because the book is silent on it
- regression as a supplement because the book lacks a regression section
- out-of-scope unless official ITPEC syllabus/source requires them: Poisson, hypothesis testing, confidence intervals

Important user rule from revised Day 10:
> **one concept → one worked example → one fresh variant of mine to solve before revealing anything**

---

### Day 11 — Revised probability/statistics

Covered:
- variance process
- SD
- SD transformation
- binomial distribution
- binomial mean/variance
- normal standardization
- correlation
- regression
- Subject B tracing

Observed:
- mean/median/mode: strong
- expected value: strong
- binomial mean/variance/SD: strong
- normal standardization: strong
- regression arithmetic: strong
- SD transformation: minor concept miss on negative multiplier
- tracing: one state-order mistake
- variance process still not automatic
- user explicitly said they forgot the variance process during final challenge

Current key statistics remediation:

> mean → deviations → squared deviations → sum → divide by n → square root for SD

---

## 9. REVISED DAY 10/11 SCOPE TO PRESERVE

Use this as a hard learning boundary for the probability/statistics module:

### Descriptive statistics
- mean
- median
- mode
- variance
- standard deviation
- population variance divided by `n` per the user's stated IPA convention
- SD transformation rules

### Counting / probability
- permutation
- combination
- ordered vs unordered
- conditional probability
- Bayes/table reasoning
- complement
- `1-(1-p)^n` complement trick

### Expected value / distributions
- expected value
- dice / lottery examples
- binomial distribution
- binomial mean
- binomial variance
- normal distribution
- standardization `u=(x-mu)/sigma`
- normal symmetry
- table reading when source material is available

### Correlation / regression
- correlation direction and strength
- `r` is not slope
- correlation is not causation
- simple linear model `y=ax+b`
- slope
- intercept
- prediction interpretation

### Explicitly out of scope unless official ITPEC syllabus/source requires them
- Poisson
- hypothesis testing
- confidence intervals

---

## 10. PRODUCT REQUIREMENTS FOR THE REVIEW WEBSITE / APP

The goal is not just a content website. It should behave like an adaptive FE study system.

### A. Dashboard

Show:

- exam countdown
- current study day
- daily target
- Subject A mastery
- Subject B mastery
- RED/YELLOW/GREEN topics
- due reviews
- recent errors
- streak / consistency
- upcoming mock exam
- "today's mission"

Avoid vanity metrics. Prioritize actionable data.

---

### B. Daily Review Engine

Every day:

1. Retrieval from previous weak topics
2. Main concept
3. One worked example
4. Fresh user-specific variant
5. User commits answer
6. Automatic grading
7. Reasoning check
8. Error classification
9. Remediation item
10. Spaced-repetition scheduling

The app must not reveal an answer before the user commits unless the user explicitly requests reveal/solution mode.

---

### C. Adaptive Difficulty

Questions should move through:

1. Recognition
2. Understanding
3. Application
4. Analysis
5. Unfamiliar FE-style problem

Difficulty should increase based on actual performance, not arbitrary levels.

---

### D. Error-driven learning

Every miss becomes a learning event.

Store:

- question
- topic
- user answer
- correct answer
- reasoning if available
- error type
- misconception
- corrective explanation
- follow-up question
- mastery state
- review dates

Example:

`Two's complement → Concept → RED`

Then generate fresh variants until reliability improves.

---

### E. Spaced repetition

Use the existing study cadence:

- Day 0
- Day 1
- Day 3
- Day 7
- Day 14

But make review **adaptive**:

- RED topics appear sooner/more often
- YELLOW topics appear moderately
- GREEN topics appear at longer intervals
- a new error resets or shortens the review interval

---

### F. Subject B special engine

Subject B deserves its own interaction mode.

Include:

- pseudo-code rendering
- variable-state table
- array visualization
- loop iteration tracker
- 1-based indexing reminder
- trace step-by-step
- recursion stack visualization later
- data structure visualization later
- timed sets

The user should be encouraged to trace manually before using any automated execution.

---

### G. Formula / Concept Sheet

Maintain a personalized sheet of only what the user actually needs.

Initial categories:

#### Number / logic
- two's complement
- signed range
- Boolean identities
- truth tables

#### CPU / memory
- CPU time
- CPI
- MIPS
- EAT
- paging
- fragmentation

#### Reliability
- MTBF
- MTTR
- availability
- series
- parallel

#### Networking
- CIDR
- host bits
- addresses
- usable hosts
- subnet mask
- transfer time

#### Statistics
- mean
- variance
- SD
- expected value
- binomial mean/variance
- z-standardization

#### Project management
- CV
- SV
- CPI
- SPI

---

### H. Exam modes

Need at least:

#### Learn Mode
Teaching + worked example + fresh variant

#### Drill Mode
Focused topic questions

#### Review Mode
Only due/recent errors

#### Timed Set
Timed FE-like practice

#### Mock Exam
Subject A and Subject B separately or full rehearsal

#### Forensic Review
After a mock, classify every miss and generate remediation

---

### I. Content provenance

Every official fact should store:

- source
- source type
- source date/version when available
- confidence
- whether official or secondary

For claims that are inference rather than official fact, label:

**FACT**  
**INFERENCE**  
**STUDY STRATEGY**  
**UNCERTAIN / NEEDS VERIFICATION**

Never allow unsupported frequency claims to masquerade as official exam weighting.

---

## 11. APP DATA MODEL SUGGESTION

Minimum entities:

### User
- id
- exam_date
- daily_goal
- current_day

### Topic
- id
- domain
- title
- description
- priority
- prerequisites
- source_refs

### Concept
- id
- topic_id
- explanation
- formula
- mental_model
- common_errors
- mastery_criteria

### Question
- id
- topic_id
- subject
- difficulty
- source
- question_text
- choices
- correct_answer
- explanation
- tags

### Attempt
- question_id
- user_answer
- correct
- time_spent
- confidence
- reasoning
- error_type
- timestamp

### Mastery
- topic_id
- status
- score
- consecutive_success
- last_seen
- next_review

### StudySession
- date
- topic
- duration
- questions_answered
- accuracy
- error_count
- notes

### ReviewSchedule
- item_id
- due_date
- interval
- ease / confidence
- status

---

## 12. CURRENT MASTER KNOWLEDGE MAP

### P1 Subject A areas already covered

- Number representation
- Boolean logic
- Sets/propositions
- Processor performance
- Cache/EAT
- Paging
- FIFO/LRU
- CPU scheduling
- Reliability/availability
- RAID
- Networking
- Probability/statistics

### P1 areas still ahead

From the corrected audit:

- data structures/algorithms
- system configuration/evaluation
- information security
- project management
- service management / audit
- other network areas
- development technology

### P2/P3 later areas

- database
- hardware logic circuits
- human interface/multimedia
- development technology in depth
- strategy/legal/accounting
- formal languages / control / lower-priority awareness areas

Do not treat these priorities as official ITPEC weightings. They are study-priority inferences from the audit and should be updated when the actual papers are tallied.

---

## 13. DESIGN PRINCIPLES FOR THE CREATOR

Claude should build the app around these principles:

1. **Source-grounded**
2. **Adaptive**
3. **Problem-first**
4. **Minimal passive reading**
5. **Error-driven**
6. **Spaced repetition**
7. **Subject B daily**
8. **Exam-realistic**
9. **Transparent about uncertainty**
10. **Simple enough to use every day**

Avoid:
- giant textbook pages
- generic gamification
- fake precision scores
- unsupported "high-frequency" claims
- mixing Japan's current domestic FE with ITPEC/PhilNITS
- revealing answers too early
- excessive animations that slow study
- requiring the learner to manually configure everything

---

## 14. RECOMMENDED DAILY UX

Opening screen:

> **DAY 12 — Your mission**

Then:

**1. Retrieval**
- 2–5 questions from RED/YELLOW topics

**2. Today's concept**
- concise explanation

**3. Worked example**
- one

**4. Your turn**
- fresh variant

**5. Subject B**
- 3–5 tracing problems

**6. Error correction**
- redo misses

**7. Review**
- SRS queue

**8. Progress**
- what improved
- what remains weak
- tomorrow's priority

This should feel like a personal FE coach, not an LMS.

---

## 15. CURRENT STATE AT HANDOFF

We are currently **before Day 12**.

Most recent confirmed state:

### GREEN
- binary/hex conversion
- Boolean logic
- propositions
- simple Subject B tracing
- scheduling
- FIFO/LRU
- reliability/availability
- RAID recognition
- network protocol identification
- mean/median/mode
- expected value
- binomial mean/variance/SD
- normal standardization
- basic regression arithmetic

### YELLOW
- subnet mask/range details
- transfer-time arithmetic
- SD transformation
- correlation interpretation
- variance procedure

### RED / REPEATED REMEDIATION
- two's-complement negative encoding/decoding was previously RED but is improving
- variance/SD procedure should remain heavily practiced until automatic
- variable-state tracing should remain in daily maintenance

---

## 16. DAY 12 RECOMMENDATION

Before introducing a new FE domain:

1. 3–5 minute two's-complement retrieval
2. variance/SD procedure from scratch
3. one fresh statistics variant
4. conditional probability/Bayes/table drill
5. normal-distribution interpretation
6. short Subject B trace
7. update error log

After that, move forward if performance supports it.

---

## 17. CREATOR PROMPT FOR CLAUDE

Use the following after providing this Markdown and the Gemini research:

> You are the primary creator and learning-system architect for my PhilNITS FE preparation app.
>
> Use this handoff document as the persistent context.
>
> Gemini is the research/background source.
>
> Claude is responsible for independently validating claims, designing the product, and building the actual app.
>
> The product must reproduce the effective teaching workflow developed in my study sessions:
>
> **retrieve → explain briefly → one worked example → learner commits a fresh variant → grade → diagnose → remediate → schedule review**
>
> Do not reveal answers before the learner commits.
>
> Treat errors as structured data.
>
> Use the error taxonomy:
> - concept
> - arithmetic
> - notation
> - misread/state tracking
> - time
>
> Use RED/YELLOW/GREEN mastery.
>
> Keep Subject B active every day.
>
> Keep current weak areas in spaced repetition.
>
> Do not fabricate exam facts.
>
> Do not confuse PhilNITS/ITPEC FE with Japan's domestic IPA FE.
>
> Do not claim topic frequency or weighting unless it is explicitly supported by an official source or clearly labeled inference.
>
> The app should be useful even if the learner only has 30–60 minutes available.
>
> Build the product as an adaptive FE study coach, not a static textbook.
>
> Before implementation, produce:
>
> 1. product architecture
> 2. information architecture
> 3. learning-state model
> 4. question/attempt/mastery data model
> 5. review algorithm
> 6. daily-session algorithm
> 7. UI/UX system
> 8. technology architecture
> 9. implementation roadmap
>
> Then build the application incrementally.
>
> Preserve this exact learning behavior as a core requirement.

---

## 18. SOURCE NOTES

Primary handoff source:
- `philnits_fe_audit_2026-09-20.md` — Claude independent audit of Gemini research

Other source context from this chat:
- Gemini deep-research report
- Claude independent audit
- Daily study sessions Day 1 through Day 11
- User's revised Day 10/11 Probability & Statistics scope
- The user's own demonstrated answers and error patterns

Use official ITPEC / PhilNITS / IPA material for factual exam claims whenever available.

---

## 19. ONE-SENTENCE PRODUCT VISION

> **Build me a source-grounded, adaptive PhilNITS FE training system that teaches concepts briefly, forces me to solve, learns from my mistakes, revisits my weak areas automatically, and prepares me to solve unfamiliar questions under exam conditions.**
