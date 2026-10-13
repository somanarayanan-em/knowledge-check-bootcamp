# Implementation Package (Part 1) Quiz: Source Map (internal tracking)

Internal only. Records where each question in `phase-3-implementation-part-1.md` comes from, so the training team can check accuracy. Kept out of the quiz file on purpose. Never include it in learner papers.

Source: Deck 5, *Creating the Implementation Plan with AI* (Part 1, Oct 2026), slides and speaker notes. Slide numbers are positions in the deck as saved.

| Question | Source |
|---|---|
| 1 | Slide 5 ("Not Just Code, A System of Delivery"; phased delivery; "Every phase is independently executable and verifiable") |
| 2 | Slide 6 (what belongs and what does not; "references requirements and solution design; it does not duplicate them"; bug-fix phases section is listed under what does not belong) and notes ("Bugs and change logs show up later"); slides 19 to 21 (each phase is written in the eight sections) |
| 3 | Slide 7 ("If code can't trace to a requirement, question whether it should exist"; "Never invent or modify FRs... update Requirements first") |
| 4 | Slide 7 and notes ("FR Mapping: None (foundational)"); slide 31 circulation notes ("Which FR? If none, is this foundational scaffolding, or should it come out?") |
| 5 | Slide 10 and notes (skill = the know-how; template = the shape). Wording follows the team's earlier edited version |
| 6 | Slide 11 and notes (ad-hoc prompting versus skills; "durable, shareable capabilities"; loads only when needed) |
| 7 | Slide 11 (drift, "trapped in one person's chat history", "lives in the repo, versioned, reviewed, shared"); slide 10 (template gives the shape). Scenario is ours |
| 8 | Slide 13 and notes (step 2, verify understanding: "Confirm it actually read the shape file"); slide 31 circulation notes. Wording follows the team's earlier edited version |
| 9 | Slides 16 and 17 and notes ("You can't build the walls before the foundation"; "verify all dependencies are complete"); slide 5 (independently verifiable); slide 13 step 6 (check phases for sensible dependencies). Wording follows the team's earlier edited version |
| 10 | Slide 27 and notes (impose phase size and scope limits; "Size phases for review, not for a human sprint"; each phase should result in a slice of human testable functionality); slide 31 circulation notes ("Phases too large to review") |
| 11 | Slide 27 notes ("you may reorder. Then double-check. It will try to please you and may produce an order that is not actually smart. Negotiate; do not rubber-stamp"); slide 17 (verify dependencies are complete) |
| 12 | Slide 14 and notes (expect the plan and a phase status tracker on day one; bugs log, change tracker, code and tests appear when coding starts; empty folders are fine); slide 15 |
| 13 | Slide 19 and notes (predictability, completeness, verifiability, AI consistency) |
| 14 | Slide 22 and notes (a goal describes system state, not effort; the bad example is "Implement allocation creation") |
| 15 | Slide 25 and notes ("AI gate checks mechanics. Human gate checks intent.") |
| 16 | Slide 26 and notes (binary, independent, "No partial credit") |
| 17 | Slide 31 circulation notes ("AI writes application code or scaffolds the app -> Stop button. 'Plan only. Do not create code.' New chat if needed."); slide 30 notes |
| 18 | Slide 6 ("reference requirements docs instead"); slide 31 circulation notes ("Reference them. Do not paste them.") |
| 19 | Slides 21 and 25 (the two gates are sections 6 and 7 of the eight); slide 31 circulation notes ("Missing AI gate or human gate -> Eight sections. Mechanics and intent. Both.") |
| 20 | Slide 24 and notes (outcomes are measurable deliverables, not activities; measurable, independent, artifact-based); slide 23 (the Plan section holds the step-by-step instructions); slide 6 (the plan references requirements and does not copy them) |

## Accuracy flags for the training team

- **Slide numbering in the deck's notes.** Slide 13's notes say "Slide 26 is where you take control", but the negotiating slide is slide 27. Slide 30's notes say "Click Slide 28". The questions cite slide numbers as they appear now.
- **Slide 28 duplicate wording.** The takeaways "FR mapping is mandatory" and "Canonical phase shape ensures consistency" carry the same sub-line. The second looks like a copy error. No question depends on it.
- **Q2 (option D).** Slide 6 lists a "bug-fix phases section" under what does not belong, and the notes say bugs and change logs appear later. The quiz uses it as a distractor. Please confirm this reading.
- **Q4.** The deck allows "FR Mapping: None (foundational)". The quiz shows it as "None". The "ask whether it is really foundational or should come out" part is from the lab circulation notes, not slide 7.
- **Q7.** The scenario is ours, built from the slide 11 contrast and the slide 10 roles. The deck says not to demo building a skill in this module, so the question only tests why one is useful.
- **Q10 (phase size).** The earlier source map for `phase-3-implementation.md` records that a phase-size scenario was rejected for its Q7, because phase size is the team's decision (slide 27) and a simple requirement can fit in one phase. This question keeps the topic but follows that point: the correct answer says to set limits "that work for your pod" and gives no number. The slide 27 notes' "two endpoints or two UI surfaces" example is left out on purpose. Training team: please confirm this question is acceptable, or swap it.
- **Q11.** The reorder scenario is ours, from the slide 27 notes about specialists and other teams waiting on an API. The deck says to double-check but not what to check. Linking that check to phase dependencies is our inference. Q9 and Q11 both touch dependencies, so one could be swapped.
- **Q12 (wording).** The question is neutral on whether the plan is held in one file or in several. It tests only which components exist when planning is complete (the plan with its phases, and the status tracker) and which appear once coding starts. The notes' "one file" guidance on slide 13 is deliberately not tested, because the team has not agreed on it.
- **Q14.** The stem states the rule ("A good goal describes the state of the system after the phase") so the question tests spotting a goal written that way. Uses generic wording in place of the deck's allocation example.
- **Q15 and Q19.** Both draw on the two gates. Q15 asks which check belongs in the human gate. Q19 asks what a phase is missing when it has no human gate. The training team may prefer to keep only one.
- **Q16.** The deck sets a limit of "4 to 8 items maximum". The quiz leaves the number out on purpose, so the team can set the size to suit the pod.
- **Q17.** A near neighbour of Phase 2 Q17 (AI writes code when asked for design). It stays because "plan only, no code" is a stage-specific failure point that the lab circulation notes call out. It can be swapped if the repeat is a concern.
- **Q18.** From the lab circulation notes on slide 31, not from a slide.
- **Q20.** Tests the Outcome section only. It is close in style to Q14 (Goal), because both correct an activity-style wording. Please confirm the training team is comfortable with that. Option C points to the Plan section, which slide 23 describes as step-by-step instructions.
- **Technology wording.** The deck's examples that name build commands, languages or class names are left out. No tool names appear in the questions.
- **Skills, templates and the word "agent".** The quiz does not use the word "agent". Skills and templates are not tagged R3, because the deck does not describe the AIDE Skills Framework here.
- **Not tested.** The hands-on exercise brief, timings, the Slido quiz and branch logistics. The example phase list on slide 17 is not tested as a list, because the order shown is an example and not a rule.
- **Crash Course versus Bootcamp.** No question depends on which lab variant a Champion attended.
