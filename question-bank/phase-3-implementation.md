# Implementation Package Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

- This question bank contains 20 MCQs in five categories of four.
- ***To build a quiz of 5, draw one question from each category.***

---

## Plan versus code, and traceability

**1.** What is the Implementation Package, and what does it contain?

- A. A set of code files that the team generates in one large implementation task
- B. A single document that merges the requirements and the design for developers
- C. A phased plan of what will be built and how each phase is verified, which refers to the requirements and design
- D. A list of bugs and fixes that the team collects once coding has finished

**Answer:** C

**Why:** The package turns the requirements (what) and the solution design (how) into a plan for the build. It holds a phase index, detailed phase specifications and an execution workflow. Each phase is independently executable and verifiable, and the work builds up step by step toward the complete system.

**Why not:** A is the opposite of the idea: the package is not a pile of code files or one big "implement everything" task. B is wrong because the plan refers to the earlier documents and does not merge them. D describes the bugs log, which only appears once coding starts.

---

**2.** A reviewer finds that each phase in a plan contains a full copy of the requirements text and the design text. What is the concern?

- A. The plan should refer to the requirements and design and not duplicate them, so the copies cannot drift from the source
- B. The plan should hold only the code, since the requirements and design belong to earlier stages
- C. There is no concern, because copied text makes each phase easier for AI to read
- D. The plan is too long, so it should hold only the phase names and nothing else

**Answer:** A

**Why:** The plan specifies what will be built and how it will be verified. It references the requirements and the solution design and does not duplicate them. Copies can fall out of step with the documents they came from.

**Why not:** B is wrong because the code is produced later, when the plan is run. C ignores the risk that copies diverge. D goes too far: the plan still needs detailed phase specifications, not only names.

---

**3.** During a review, the team finds a phase that builds behaviour that no Functional Requirement (FR) lists. What is the best response?

- A. Keep it, because AI may have found a useful improvement
- B. Add a new FR in the plan so that the phase has something to map to
- C. Mark the phase as foundational so that it needs no mapping
- D. Question whether it should exist, and if it is needed, change the requirements first and then map it

**Answer:** D

**Why:** If code cannot trace to a requirement, question whether it should exist. FRs are used as written in the plan. If something must change, update the requirements first.

**Why not:** A lets scope grow without anyone deciding it. B invents FRs inside the plan, which the package does not allow. C misuses the foundational exception, which is meant for work such as project scaffolding.

---

**4.** The first phase of a plan sets up the project structure and implements no business requirement. Is it acceptable for it to have no FR?

- A. No, every phase must list at least one FR, so the setup should be merged into another phase
- B. Yes, foundational work may state "None (foundational)", while the other phases must list the FRs they implement
- C. Yes, any phase may skip the mapping when the team is short of time
- D. No, the team should invent a requirement so that the setup phase has a mapping

**Answer:** B

**Why:** Every phase lists the FRs it implements, but foundational phases such as project scaffolding may say "FR Mapping: None (foundational)". Implementing one FR across several phases is also allowed, and that is how work is split into chunks.

**Why not:** A and D treat the mapping rule as having no exceptions. D also invents a requirement. C stretches the exception to any phase, which would remove traceability.

---

## Skills, templates and the plan workflow

**5.** Which description of skills and templates is correct?

- A. A skill is a ready-made structure with sections to fill in, and a template is the know-how for doing the task
- B. A template is a ready-made structure with sections to fill in, and a skill is the know-how for doing the task
- C. A skill is a single chat message, and a template is a finished code file
- D. The two terms mean the same thing, and the name depends only on the tool being used

**Answer:** B

**Why:** A template sets the sections, headings and required details up front, so the output has a consistent structure. A skill is reusable know-how that the AI applies to a task. Used together, they keep the output consistent and on-standard, and the team stays in charge of approving the result.

**Why not:** A swaps the roles of the skill and the template. C describes neither: a skill is written down once and reused, and a template is a starting structure, not finished code. D is wrong because each has a different job, which is why they are used together.

---

**6.** Why is it better to write "how we do this task" once as a skill than to explain it in every prompt?

- A. A skill guarantees correct output, so the result needs no checking
- B. A skill replaces the need for templates
- C. It is written once, applied the same way each time, and can be shared through the repo
- D. A skill makes AI load every instruction on every message so that nothing is missed

**Answer:** C

**Why:** Ad-hoc prompting means re-explaining each time, results that drift and instructions trapped in one chat. A skill is captured once, gives the same workflow and format each run, lives in the repo where it is versioned and shared, and loads only when needed.

**Why not:** A is wrong because a skill improves consistency but does not guarantee correct output, so the team still verifies. B is wrong because skills and templates do different jobs and work together. D is the opposite of the idea, since a skill loads only when it is relevant.

---

**7.** In a draft plan, the team finds that Phase 3 can only be tested once Phase 5 has been built. What is the best response?

- A. Rework the phases so that each one depends only on earlier phases and can be verified on its own
- B. Keep the order, and test Phase 3 together with Phase 5 once both are built
- C. Keep the order, and mark Phase 3's gates as passed so that work can continue
- D. Merge all the phases into one so that nothing waits for anything else

**Answer:** A

**Why:** Each phase should be independently executable and verifiable, with clear dependencies on earlier phases. Phases build on each other, like a foundation before walls. A phase that cannot be verified until a later one exists breaks both rules.

**Why not:** B gives up on verifying each phase as it is built. C removes the check that the phase exists to provide. D is not a fix for a dependency problem. Whether to combine phases is a separate sizing decision for the team, and merging them all would make verification harder.

---

**8.** The team asks AI to build the plan. Its summary does not mention the phase shape file the team pointed it to. What should the team do?

- A. Carry on, since AI will pick up the structure as it goes
- B. Rewrite the requirements so that they include the phase shape
- C. Accept the plan and fix any inconsistent phases at the end
- D. Pause and ask it to review the shape and confirm what belongs in each phase before continuing

**Answer:** D

**Why:** The verification step asks the AI to summarize the scope, key FRs and constraints, and to confirm what belongs in each phase, including that it actually read the shape file. The team confirms this before moving on.

**Why not:** A and C leave the phases open to inconsistent structure, which the shape is meant to prevent. B changes the wrong document: the requirements do not define the phase shape.

---

## Running a phase

**9.** Before AI writes any code for a phase, what should happen?

- A. AI presents a brief of the phase, and implementation starts only when the team says GO
- B. AI starts coding at once and presents a brief afterward
- C. AI commits an empty skeleton so that the team can review it in the repo
- D. The team writes the code and AI reviews it

**Answer:** A

**Why:** In phase education, AI prepares the phase details, the game plan, the implementation tasks, the definition of done and the test coverage. The team decides when implementation begins.

**Why not:** B removes the team's chance to catch problems before code exists. C commits before anything has been approved. D changes the roles: the team directs and verifies, and AI does the building.

---

**10.** A phase depends on an earlier phase that is not complete yet. What should the team do?

- A. Start anyway, because AI will create the missing pieces as it needs them
- B. Start anyway and log the missing dependency as a bug afterward
- C. Merge the two phases without reviewing them
- D. Hold the phase until its dependencies are complete

**Answer:** D

**Why:** Phases build on each other, so the walls cannot go up before the foundation. Before a phase starts, all of its dependencies must be complete.

**Why not:** A lets AI make up what the plan should have supplied. B treats a known sequencing problem as a defect. C changes the plan's phase boundaries without a review.

---

**11.** In the phase brief, the team sees an approach that does not match the solution design. What should the team do?

- A. Say GO and fix it during the human gate
- B. Let AI finish the first chunk and then correct it
- C. Say NO-GO, discuss it, revise the plan if needed, and review the brief again
- D. Delete the phase from the plan

**Answer:** C

**Why:** The go/no-go decision exists so that problems are caught before code is written. If something looks wrong in the plan, say NO-GO and discuss. The team can also ask whether dependencies are met, which code standards apply and whether the phase meets the functional and solution design.

**Why not:** A and B let AI continue with a known problem. D removes work that the requirements may still need.

---

**12.** While running a phase, AI starts adding features that the phase does not call for. What best prevents this?

- A. Allow it, because extra features save time later
- B. Tell it what not to do, and point it to existing reference files and patterns
- C. Ask it to hold all code until the end of the project
- D. Enlarge the phase so that the extra features fit inside it

**Answer:** B

**Why:** Scope control means saying what not to do. Following existing patterns means pointing AI to reference files. Together they keep the work inside the phase.

**Why not:** A lets scope grow without a decision. C does not address the scope problem and delays verification. D changes the plan to match unrequested work.

---

## Verification gates and approval

**13.** What is the difference between the AI Gate and the Human Gate?

- A. The AI Gate checks intent, and the Human Gate checks mechanics
- B. They check the same things, and the Human Gate is only a repeat
- C. The AI Gate checks requirements, and the Human Gate checks code style
- D. The AI Gate checks mechanics such as build and tests, and the Human Gate checks whether the result meets the intent

**Answer:** D

**Why:** The AI Gate asks "does the code work?": build, tests, linting, coverage and API responses. The Human Gate asks "does it meet the requirements?": business rules, user experience, messages and edge cases.

**Why not:** A swaps the two. B is wrong because each gate catches things the other cannot. C is wrong because style checks, such as linting, are automated and requirements need human judgment.

---

**14.** When is a phase ready to be committed?

- A. As soon as the automated checks pass
- B. When both gates have passed and the team has explicitly approved
- C. When AI reports that it is confident in the result
- D. When the next phase has been planned

**Answer:** B

**Why:** Both gates must pass before a phase is committed and complete. The commit then waits for the team's explicit approval.

**Why not:** A skips the human check of intent. C relies on AI's own judgment. D has no bearing on whether this phase is verified.

---

**15.** The AI Gate fails: some tests do not pass. What should the team do?

- A. Send the work back to AI to fix, and move to the Human Gate only after the AI Gate passes
- B. Move to the Human Gate and let the reviewers find the problem
- C. Commit now and fix the tests in the next phase
- D. Remove the failing tests so the gate passes

**Answer:** A

**Why:** If the AI Gate fails, it goes back to the AI to be fixed. The team does not skip ahead to human review.

**Why not:** B wastes human time on work that is mechanically broken. C commits unverified work. D hides a problem without fixing it.

---

**16.** All automated checks pass, and AI commits the code at once without waiting. What is wrong?

- A. Nothing, because passing tests are enough to commit
- B. The commit should have been made before the checks ran
- C. AI should have stated that it had not committed, and waited for the team's explicit approval
- D. AI should have asked for approval before running the tests

**Answer:** C

**Why:** The critical rule is that AI does not commit until the team explicitly approves. AI presents a summary and says it has not committed, the team reviews, and only after the team says "approved" or "commit" does AI commit. The team keeps full control over what enters the codebase.

**Why not:** A treats mechanical checks as the only test. B has the order backward. D mixes up the approval point: the approval comes after verification and covers the commit.

---

## Bugs and judgment

**17.** In manual testing, the team finds that a form rejects an input that users would reasonably enter. The requirements never mention that input. What is the best response?

- A. Tell AI to change the behaviour right away, since users will expect it
- B. Leave it until after release
- C. Raise it with the requirements owner, update the specification, record the change, and then implement it
- D. Edit the FR in the plan so that it matches the code

**Answer:** C

**Why:** If the specification is wrong or missing, behaviour should not be changed silently. The team talks to the requirements owner (for example the product owner or business analyst), updates the specification, creates a change record and then implements the change.

**Why not:** A changes behaviour with no decision behind it. B leaves a known gap. D edits the FRs inside the plan, which is not allowed. Requirements are changed at the source.

---

**18.** In manual testing, a team member sees behaviour that seems wrong. What should the team do first?

- A. Describe the behaviour and ask AI to check it against the functional and solution design, because the team could be mistaken
- B. Tell AI that the code is wrong and ask it to try again
- C. Log a bug immediately, without checking anything
- D. Ask AI to rewrite the phase from the start

**Answer:** A

**Why:** Describe the behaviour and ask whether it meets the functional or solution design. If it does not match, find out which specification is affected and how important the fix is. If it does match, the team's expectation may be what needs to change.

**Why not:** B asserts a fault without evidence. C may log something that is not a defect. D discards work that may be correct.

---

**19.** AI plainly did not do what the specification says, for example a field the spec lists is missing. Does the team need to log a bug for it?

- A. Yes, every miss must be logged before anything can be fixed
- B. No, the team can tell AI to fix it against the specification, and not every small slip needs a log entry
- C. No, the team should leave it, because AI will find it later
- D. Yes, and the phase must be put on hold

**Answer:** B

**Why:** When the implementation simply missed what the specification says, the team can tell AI to fix it against the specification. Logging is for items that need to be tracked or escalated to the team, such as unclear specifications, missed or new requirements, and integration problems.

**Why not:** A and D treat every slip as a logged defect. C leaves a known miss unfixed.

---

**20.** A bug has been confirmed. Which information should its log entry contain?

- A. Only a short description, so that the entry stays brief
- B. The name of the person who found it and the time it was found
- C. The code that fixes it, which is attached to the entry
- D. A number, a date, a summary, the phase, a status, where it sits, the documents affected and the type of impact

**Answer:** D

**Why:** Every bug gets a number, a date, a phase reference and an impact classification. The analysis adds where the problem sits, which documents are affected and the type of impact (for example a badly implemented requirement, a missed requirement, a new requirement or an issue found in testing).

**Why not:** A leaves out what is needed to prioritize and trace the bug. B records who found it but not what it affects. C is wrong because the fix is made afterwards, in a bug-fix phase, using the same execution guide.

---

## Training requirements covered

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: covered for the implementation stage
- **R2** Hands-on execution of a stage: not in this quiz (it is assessed by practical sign-off, and this quiz tests knowledge only)
- **R4** Knowledge base setup: not covered here
- **R6** Failure-point recognition: covered for the implementation stage
- **R7** Knowledge check record: contributes
- **R3, R5**: not in this quiz (R3 is deferred; R5 needs source material)

## Training requirement traceability matrix

| Question      | R1      | R2     | R3               | R4               | R5               | R6      | R7          |
| ------------- | ------- | ------ | ---------------- | ---------------- | ---------------- | ------- | ----------- |
| 1             | ✓       |        |                  |                  |                  |         | ✓           |
| 2             | ✓       |        |                  |                  |                  |         | ✓           |
| 3             | ✓       |        |                  |                  |                  |         | ✓           |
| 4             | ✓       |        |                  |                  |                  |         | ✓           |
| 5             | ✓       |        |                  |                  |                  |         | ✓           |
| 6             | ✓       |        |                  |                  |                  |         | ✓           |
| 7             |         |        |                  |                  |                  | ✓       | ✓           |
| 8             |         |        |                  |                  |                  | ✓       | ✓           |
| 9             | ✓       |        |                  |                  |                  |         | ✓           |
| 10            | ✓       |        |                  |                  |                  |         | ✓           |
| 11            |         |        |                  |                  |                  | ✓       | ✓           |
| 12            |         |        |                  |                  |                  | ✓       | ✓           |
| 13            | ✓       |        |                  |                  |                  |         | ✓           |
| 14            | ✓       |        |                  |                  |                  |         | ✓           |
| 15            |         |        |                  |                  |                  | ✓       | ✓           |
| 16            |         |        |                  |                  |                  | ✓       | ✓           |
| 17            |         |        |                  |                  |                  | ✓       | ✓           |
| 18            |         |        |                  |                  |                  | ✓       | ✓           |
| 19            |         |        |                  |                  |                  | ✓       | ✓           |
| 20            |         |        |                  |                  |                  | ✓       | ✓           |
| **Questions** | 10      | 0      | 0                | 0                | 0                | 10      | 20          |
| **Status**    | Covered | Not in this quiz | Not in this quiz | Not in this quiz | Not in this quiz | Covered | Contributes |

Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (practical sign-off, not assessed in this quiz)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check
