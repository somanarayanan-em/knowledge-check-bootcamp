# Champion Knowledge Check: Scope Document

| | |
|---|---|
| **Status** | Draft v0.1, for review |
| **Owner** | Electric Mind (training team) |
| **Audience for the knowledge check** | Named Champions at CLIENT_A |
| **Last updated** | 2026-10-02 |

> **Data handling:** This repo holds templates and question content only. Do not store completed Champion records (real names, scores, personas) in it. Completed records go in an approved, access-controlled location. Use `CLIENT_A` for the client's name in all files. Questions: the Data Security Policy or helpdesk@electricmind.com.

---

## 1. Purpose

Before the close of the Bootcamp, each named Champion completes an **individual knowledge check** demonstrating understanding of the complete Model-2 lifecycle. Electric Mind produces a **named knowledge check record per Champion, including persona**, and provides the records to CLIENT_A at the close of the Bootcamp.

This is the one hard gate in the engagement. Everything else is practiced; this is assessed and recorded.

## 2. Requirements we are aligning to

The brief contains seven expectations. Six are competencies a Champion must show. The seventh is the mechanism that measures them.

| # | Requirement | What a Champion must be able to do | Type |
|---|---|---|---|
| R1 | End-to-end process literacy | Explain the full lifecycle (requirements → solution design → implementation → KB setup) accurately. Describing it is enough; mastery is not required. | Understand / explain |
| R2 | Hands-on execution of at least one stage | Has personally executed, not only observed, at least one stage. Driver rotation means every Champion drives. | Can do |
| R3 | AIDE Skills Framework fluency | Describe what AIDE is and how it is used. Mastery of every skill is not required. | Understand / explain |
| R4 | Knowledge Base / context repository setup | Stand up a KB or context repo correctly, as a repeatable task for Wave 1. | Can do |
| R5 | Operating model and role literacy | Articulate their own role in the POD, how the two-in-the-box model works, and where they sit in the Product Group Hub. | Understand / explain |
| R6 | Failure-point recognition | Recognize when something is going wrong in the lifecycle and know the intervention or escalation step. This tests judgment, not only technical knowledge. | Judge / decide |
| R7 | Demonstrated via knowledge check | Complete an individual, assessed and recorded knowledge check covering the complete Model-2 lifecycle. Named, with persona, delivered to CLIENT_A. | Gate |

## 3. How the quiz measures each requirement

A written quiz can fully measure "understand" and "judge" competencies. It can only partly measure "can do" competencies (R2, R4). The honest position for this phase:

| Req | Assessed by the quiz in this phase | Deferred |
|---|---|---|
| R1 | Yes, in full | n/a |
| R2 | Partly: written questions on how to run a stage and what good output looks like. This shows knowledge of the stage, not that the Champion drove it. | Practical sign-off (observed or attested execution) |
| R3 | Yes, in full | n/a |
| R4 | Partly: questions on what a KB / context repo contains and the correct setup sequence. | Practical sign-off (a working KB stood up) |
| R5 | Yes, in full, **subject to receiving source material** (see section 7) | n/a |
| R6 | Yes, in full, using scenario questions | n/a |
| R7 | The quiz is the gate. Its output feeds the per-Champion record. | Practical section of the record |

Questions for R2 and R4 will be tagged so a practical sign-off can be added later without rewriting the quiz.

## 4. What we are going to build

All deliverables are Markdown in this `knowledge-check/` folder. Formatting and export come later.

| # | Deliverable | Description |
|---|---|---|
| D1 | **Blueprint** (`01-blueprint.md`) | Maps R1–R6 to question counts, question types, difficulty and weighting. Includes scoring and pass rules. Every item traces to a source slide or document. |
| D2 | **Question bank** (one file per competency) | R1 lifecycle, R2 stage execution, R3 AIDE, R4 KB setup, R5 operating model and role, R6 failure points. Each question carries a competency tag, a persona tag where relevant, a source reference, and a rationale. |
| D3 | **Persona-specific scenarios** | Scenario questions written from each role's seat, so the quiz is fair to business and technical Champions alike. |
| D4 | **Learner quiz, versions A and B** | Clean papers with no answers. Two equivalent versions so Champions sitting together do not get identical questions. |
| D5 | **Answer key and rationale** | Correct answers, why distractors are wrong, and the source slide for each. |
| D6 | **Record template** (`record-template.md`) | One page per Champion: name, persona, date, score per competency, overall result, assessor sign-off. Includes a reserved, clearly marked practical section for R2 and R4. A blank template only. |
| D7 | **Optional: per-module mini quizzes** | Short quizzes after each practice session. Included only if confirmed (see section 7). |

### Proposed folder layout

```
knowledge-check/
├── 00-scope.md                  <- this document
├── 01-blueprint.md
├── question-bank/
│   ├── r1-lifecycle.md
│   ├── r2-stage-execution.md
│   ├── r3-aide.md
│   ├── r4-kb-setup.md
│   ├── r5-operating-model.md
│   └── r6-failure-points.md
├── persona-scenarios.md
├── quiz-version-a.md
├── quiz-version-b.md
├── answer-key.md
└── record-template.md
```

## 5. Out of scope (for now)

- Practical, hands-on sign-off for R2 and R4 (only the placeholder section in the record template).
- Final formatting, branding and export (Word, PDF, Forms, interactive HTML).
- Auto-scoring or any tooling.
- Completed Champion records or any real Champion data.
- Changing the existing training decks. We reference them but do not edit them.
- Training content for the operating model. We assess it but do not write it.

## 6. Draft parameters (to confirm)

These are starting proposals, not agreed requirements.

| Parameter | Proposal |
|---|---|
| Length | About 40 questions, about 45 minutes |
| Question types | Mostly single-answer multiple choice, some multi-select, and 6–8 scenario questions |
| Weighting | Heaviest on R6 (judgment) and R1 (lifecycle), then R3, R5, R2, R4 |
| Pass rule | At least 80% overall **and** at least 70% in every competency, so a strong area cannot hide a weak one |
| Versions | Two equivalent versions (A and B) |
| Retake | To be agreed with CLIENT_A |
| Personas | One quiz core for all, with persona-specific scenarios, list to be confirmed |

The pass thresholds should be confirmed with CLIENT_A before they are published to Champions.

## 7. Open items and inputs needed

| # | Item | Owner | Blocks |
|---|---|---|---|
| O1 | Source material for the operating model: POD structure, two-in-the-box, Product Group Hub, Champion role, Wave 1 | Training team (to share) | R5 questions, persona scenarios |
| O2 | Source material for KB / context repo setup: what the Bootcamp activity covers and the expected setup steps | Training team (to share) | R4 questions |
| O3 | List of personas (roles) the Champions fall into | Training team | D3, D6 |
| O4 | Whether per-module mini quizzes (D7) are wanted | Training team | D7 |
| O5 | Confirm or change the draft parameters in section 6 | Training team, then CLIENT_A | D1 |
| O6 | Confirm what CLIENT_A expects the record to contain beyond name and persona | Training team | D6 |
| O7 | Confirm which stage each Champion drives, if known in advance | Training team | R2 questions, future practical sign-off |

## 8. Source material

**Available now** (course decks in the workspace):

| # | Deck | Primary use |
|---|---|---|
| 1 | Kick Off | Course goals, two-day structure |
| 2 | Intro: Understanding AI Behaviour | Core vocabulary, the three stages, the 7-step workflow, sequence and completeness, version control (R1, R6) |
| 3 | Requirements Package | Requirements stage (R1, R2, R6) |
| 4 | Solution Design | Design stage, traceability, design pitfalls (R1, R2, R6) |
| 5 | Part 1 Implementation Package | Implementation stage (R1, R2, R6) |
| 6 | Part 2 Implementation Package | Implementation stage (R1, R2, R6) |
| 7 | Intro to A.I.D.E. | Skills, templates, three flows, navigator, gates (R3, R4) |

Decks 3, 5 and 6 still need a close read before the blueprint is finalized.

**Still needed:** material for R4 and R5 (items O1 and O2). The decks above do not cover the operating model, and KB setup is only introduced conceptually.

## 9. Known gaps and risks

- **Operating model content is not in the decks.** R5 cannot be written accurately without O1. Writing it from assumption would risk testing facts that are wrong for CLIENT_A.
- **Lifecycle wording differs.** The decks describe requirements → solution design → implementation plan → build and test. The brief describes requirements → solution design → implementation → KB setup. We will follow the brief and map the two explicitly in the blueprint.
- **KB setup has thin coverage.** The AIDE deck positions the knowledge base as a primer and points to resources. R4 depends on what the Bootcamp activity actually covers.
- **Failure points are not framed as a list.** Material exists in the decks (for example: the model writing code during design, a stack not pinned, skipping the summary step, copying an example wholesale, changing the solution without changing the requirement). We will organize it into failure point and intervention pairs, and the training team should confirm these match what CLIENT_A expects Champions to catch.
- **Crash Course versus Bootcamp.** Some decks carry both lab variants. We assume Champions followed the Bootcamp variants.
- **Quiz limits.** A written quiz cannot prove someone can build a KB or drive a stage. The record will state this clearly so the gate is not over-claimed.

## 10. Build sequence

1. Review and agree this scope (this document).
2. Receive O1–O3, confirm O4–O7.
3. Close-read decks 3, 5 and 6.
4. Write the blueprint (D1) and agree it.
5. Write the question bank (D2) and persona scenarios (D3).
6. Assemble the quiz versions (D4) and answer key (D5).
7. Create the record template (D6).
8. Review pass: coverage against R1–R7, source traceability, difficulty and fairness across personas.
9. Later phase: practical sign-off, formatting and export.

## 11. Acceptance criteria

The knowledge check is ready to hand to Champions when:

- Every competency R1–R6 has questions, and every question is traceable to a source.
- Each persona sees scenarios that fit their role.
- Versions A and B cover the same competencies at the same weighting.
- The answer key explains every answer.
- The record template captures name, persona, per-competency scores, overall result and assessor sign-off.
- The training team has reviewed the content for accuracy, and the pass rule has been confirmed with CLIENT_A.
