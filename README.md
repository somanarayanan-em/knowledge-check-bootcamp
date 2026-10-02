# Champion Knowledge Check

Question content and planning documents for the individual knowledge check that each named Champion at CLIENT_A completes before the close of the Bootcamp. The check covers the Model-2 lifecycle: requirements, solution design, implementation and knowledge base setup.

| | |
|---|---|
| **Owner** | Electric Mind (training team) |
| **Audience** | Named Champions at CLIENT_A |
| **Status** | Draft, in progress |
| **Last updated** | 2026-10-02 |

> **Data handling:** This repo holds templates and question content only. Do not store completed Champion records (real names, scores, personas) here. Completed records go in an approved, access-controlled location. Use `CLIENT_A` for the client's name in all files. Questions: the Data Security Policy or helpdesk@electricmind.com.

## What is in this repo

```
knowledge-check/
├── README.md                          <- this file
├── 00-scope.md                        <- scope, requirements (R1-R7), deliverables, open items
└── question-bank/
    ├── phase-1-requirements.md        <- Requirements Package quiz bank (trainer copy)
    ├── phase-1-source-map.md          <- internal: slide source for each Phase 1 question
    ├── phase-2-solution-design.md     <- Solution Design Package quiz bank (trainer copy)
    └── phase-2-source-map.md          <- internal: slide source and accuracy flags for Phase 2
```

Start with [00-scope.md](00-scope.md). It explains what the knowledge check is for, what a written quiz can and cannot prove, and what is still to be built.

## Question banks

Each bank has 20 multiple-choice questions in five categories of four. Each question has the answer, a short "Why" and a "Why not" for each wrong option.

| Bank | Source deck | Categories |
|---|---|---|
| [Phase 1: Requirements](question-bank/phase-1-requirements.md) | Deck 3, Requirements Package | Requirements vs solution design; why documents matter and how AI behaves; the workflow and verification; scaffolding before content; pitfalls and practical habits |
| [Phase 2: Solution Design](question-bank/phase-2-solution-design.md) | Deck 4, Solution Design | Requirements to design and traceability; loading context before designing; technology constraints; what is in the package and how to build it; design pitfalls and judgment |

### Building a quiz from a bank

To build a quiz of 5, draw one question from each category. For a longer quiz, draw the same number from every category so the weighting stays even.

### Trainer copy and source maps

- The question banks are **trainer copies**. They contain answers and explanations. Never share them with Champions.
- The source maps are **internal tracking**. They record which slide or speaker note each question comes from, so the training team can check accuracy. They also carry **accuracy flags** for anywhere a question extends or paraphrases the deck. Never include them in learner papers.

## What the quiz measures

The scope document defines seven requirements. The question banks tag every question against them in a traceability matrix at the end of each file.

| Req | What a Champion must show | In the written quiz |
|---|---|---|
| R1 | End-to-end process literacy | Yes |
| R2 | Hands-on execution of at least one stage | **No.** Evidenced by practical sign-off only, because a written quiz cannot show that a Champion drove a stage |
| R3 | AIDE Skills Framework fluency | Deferred |
| R4 | Knowledge base / context repository setup | Conceptual touchpoints only. A working KB needs practical sign-off |
| R5 | Operating model and role literacy | Not yet. Needs source material (open item O1) |
| R6 | Failure-point recognition | Yes |
| R7 | Demonstrated via knowledge check | The quiz is the gate and feeds the per-Champion record |

Phases 1 and 2 are both tagged R1 and R6 (10 questions each).

## Writing conventions

These are the rules the existing banks follow. Follow them when adding questions.

- **Format:** stem, four options (A to D), one correct answer, "Why", and a "Why not" covering every wrong option. No "all of the above".
- **Answer positions:** spread the correct answer evenly across A to D within a bank.
- **Option length:** keep the four options close in length, so the longest is not the answer.
- **Plain language:** write for business and technical Champions alike. Persona-specific scenarios are a later deliverable.
- **Generic technology:** do not name tools or stacks in questions. Say "a frontend framework" or "a database". Version examples may use numbers ("version 17 in one document, version 18 in another").
- **The team guides AI:** write questions so the team makes the decisions and AI works from what it is given. Avoid wording that has AI deciding or changing things on its own.
- **No assumed cause:** do not word a question as if a problem always has one cause. For example, a gap may be in AI's summary or in the requirements themselves.
- **Traceable:** every question traces to a slide or speaker note. Where a question extends the deck, say so in the source map.
- **No client-identifying information:** use `CLIENT_A`. Do not put real credentials, personal data or client names in any file.

## What is built and what is next

| # | Deliverable | Status |
|---|---|---|
| D1 | Blueprint (`01-blueprint.md`) | Not started |
| D2 | Question bank, one file per competency | Phase 1 and Phase 2 banks drafted. Banks for the other decks and for R3, R4 and R5 still to do |
| D3 | Persona-specific scenarios | Not started. Needs the persona list (O3) |
| D4 | Learner quiz, versions A and B | Not started |
| D5 | Answer key and rationale | Not started (the banks hold answers and rationale for now) |
| D6 | Record template (`record-template.md`) | Not started. Needs confirmation of what CLIENT_A expects in the record (O6) |
| D7 | Per-module mini quizzes | Optional. Pending confirmation (O4) |

Open items and inputs that are still needed are listed in section 7 of [00-scope.md](00-scope.md). The build sequence is in section 10.

## Known gaps

- **Operating model content is not in the decks.** R5 cannot be written without source material from the training team.
- **Knowledge base setup has thin coverage.** The decks introduce it only as a concept, so R4 depends on what the Bootcamp activity covers.
- **Lifecycle wording differs** between the decks and the brief. The scope document explains how it is mapped.
- **Crash Course versus Bootcamp.** Some decks carry both lab variants. Questions are written so they do not depend on which one a Champion attended.
- **Accuracy flags are open.** The source maps list wording choices that the training team should confirm before the questions are final.

## Working in this repo

- Edit the Markdown files directly. Formatting, branding and export (Word, PDF, forms) come later.
- If you edit a file in an editor while another tool is also changing it, reload the file from disk first. A stale open copy can overwrite recent changes.
- Keep the question banks and their source maps in step. When you change a question's wording, update its source-map entry and, if the tags change, the traceability matrix and totals.
