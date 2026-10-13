# Implementation Package Quiz: Source Map (internal tracking)

Internal only. Records where each question in `phase-3-implementation.md` comes from, so the training team can check accuracy. Kept out of the quiz file on purpose. Never include it in learner papers.

Sources:
- Deck 5, *Creating the Implementation Plan with AI* (Part 1, Oct 2026), slides and speaker notes. Slide numbers below are positions in the deck as saved.
- Deck 6, *Implementing From the Implementation Package using AI* (Part 2, Sep 2026, Version 2), slides and speaker notes.

| Question | Source |
|---|---|
| 1 | Deck 5 slides 5 and 6 ("Not Just Code, A System of Delivery"; what belongs in the plan: phase index, phase specs, execution workflow); slide 14 and notes (bugs log appears when coding starts) |
| 2 | Deck 5 slide 6 and notes (guiding principle: "references requirements and solution design; it does not duplicate them") |
| 3 | Deck 5 slide 7 and notes ("If code cannot trace to a requirement, question whether it should exist"; "Never invent or modify FRs... Change requirements first") |
| 4 | Deck 5 slide 7 and notes (FR Mapping: None (foundational); partial implementation of an FR across phases is allowed) |
| 5 | Slide 10 and notes (skill = the know-how; template = the shape). The wording follows the team's earlier edited version of this question |
| 6 | Deck 5 slide 11 and notes (ad-hoc prompting versus skills; loads only when needed) |
| 7 | Deck 5 slide 5 ("Every phase is independently executable and verifiable"); slide 16 ("Has clear dependencies on previous phases"; "Is independently executable and verifiable"); slide 17 (phases build on each other) |
| 8 | Slide 13 and notes (step 2, verify understanding: "Confirm it actually read the shape file"); slide 31 circulation notes ("Did it summarize requirements, design, and the phase-shape file before it generated?"). Wording follows the team's earlier edited version |
| 9 | Slide 17 and notes ("You can't build the walls before the foundation"; "Before starting a phase, verify all dependencies are complete"); slide 16 (each phase has clear dependencies and is independently executable and verifiable); slide 13 step 6 (verify each phase for valid FR mappings and sensible dependencies). Wording follows the team's earlier edited version |
| 10 | Deck 5 slide 17 and notes ("Before starting a phase, verify all dependencies are complete"); Deck 6 slide 11 (extra question "Are all dependencies met?") |
| 11 | Deck 6 slide 11 and notes (Go/No-Go); slides 6 and 23 notes (if no, discuss and revise the plan) |
| 12 | Deck 6 slide 22 ("Follow existing patterns", "Scope control: say what NOT to do"); slide 10 (negotiate: exclude scope creep) |
| 13 | Deck 6 slides 14 and 15 and notes (AI Gate verifies mechanics; Human Gate verifies intent); Deck 5 slide 25 |
| 14 | Deck 6 slide 13 and 16 ("Both gates must pass before a phase is committed and complete" is from the earlier version of Deck 6; slide 13 now says "Only after both steps succeed is the phase ready to commit"); slide 16 (approval) |
| 15 | Deck 6 slide 14 notes ("If the AI gate fails, send it back to fix. Do not skip to humans.") |
| 16 | Deck 6 slide 16 and notes (Approval Gate, "AI does not commit until you explicitly approve") |
| 17 | Deck 6 slide 18 notes (spec wrong or missing: talk to PO/BA, update the specification, create a change record, then implement); Deck 5 slide 7 (do not modify FRs in the plan) |
| 18 | Deck 6 slide 18 and notes ("Describe the behaviour. Ask: does this meet the functional or solution design? You might be wrong.") |
| 19 | Deck 6 slide 18 notes ("Obvious implementation miss: tell it to fix against the spec. You do not have to log a bug for every typo.") |
| 20 | Deck 6 slide 19 and notes (bug entry format) and slide 18 (impact types) |

## Accuracy flags for the training team

- **Deck versions.** The decks in the workspace were updated after the plan was made (Deck 5 is now the Oct 2026 version, Deck 6 the Sep 2026 Version 2). Questions are written against these versions. The decks now say "FlowAI SDLC" and not "Model-2". The quiz files do not name the framework, so they are not affected, but the README still says "Model-2". Please confirm which name to use.
- **Q4 (foundational).** Slide 7 allows "None (foundational)" for foundational phases and gives scaffolding as the example. Option D is a deliberate trap that invents a requirement. The deck does not say what else counts as foundational.
- **Q7 (replaced).** The first draft tested the plan-building workflow ("agree structure, headers only, then fill chunk by chunk"). It was replaced because the phase shape is supplied up front, so "agree the structure first" was ambiguous, and a phase-size scenario was rejected because phase size is the team's decision (slide 27) and a simple requirement can fit in one phase. Q7 now tests the rule that every phase is independently verifiable and depends only on earlier phases. The scenario (Phase 3 testable only after Phase 5) is ours. Option D is a deliberate trap: merging phases is a sizing choice and does not fix a dependency problem. Q7 overlaps slightly with Q10 (starting a phase before its dependency is done). Q7 is about reviewing the plan and Q10 is about running a phase.
- **Q8.** The deck's notes ask the team to "confirm it actually read the shape file". The question applies that to a summary that does not mention the file. This is a mild extension. It does not assume why the summary is silent.
- **Q10.** The deck says to verify dependencies before starting. The options (start anyway, log as bug, merge phases) are our distractors, not deck content.
- **Q12.** The deck lists scope control and following patterns as takeaways but gives no scenario of AI adding features. The scenario is ours.
- **Q14.** The earlier Deck 6 had the line "Both gates must pass before a phase is committed and complete". The current Deck 6 slide 13 says the AI Gate verifies first and the Human Gate verifies and approves. The explicit-approval wording comes from slide 16. Please confirm that the "explicitly approved" combination is the intended rule.
- **Q15.** Option D (remove the failing tests) is our distractor. The deck only says to send the work back to fix.
- **Q17.** The deck's own example is validation that rejects valid input and an FR that never mentioned spaces. The question uses generic wording ("an input users would reasonably enter"). "Requirements owner" generalizes "PO / BA".
- **Q19.** The deck says not every typo needs a bug log, and gives no rule for the boundary. Please confirm that "a field the spec lists is missing" is a fair example of an obvious miss.
- **Q20.** The deck's bug example uses a specific table format. The question lists the fields in plain words and does not rely on the table layout.
- **Examples removed.** Deck examples that name specific tools, build commands or class names (for example the build commands on slide 14 and the example file names) are left out, per the generic-technology convention.
- **Crash Course and Bootcamp.** No question depends on the exercise variant, the lab timings or the employees-and-projects brief.
