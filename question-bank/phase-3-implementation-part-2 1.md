# Implementation Package (Part 2) Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

- This question bank contains 9 MCQs in three categories of three.
- ***To build a quiz of 3, draw one question from each category.***

---

## Where implementation fits, and how a phase starts

**1.** Where does Implementation sit in the lifecycle?

- A. It executes the plan that requirements and solution design already produced
- B. It replaces solution design once the requirements are approved
- C. It is the stage where the team chooses the approach for the build
- D. It runs alongside requirements to save time

**Answer:** A

**Why:** Requirements tell us what to build and why, solution design tells us how, and implementation does it. By this stage the plan has been created and all that remains is to execute it. The approach is already chosen, because the decision is built into the phase specification.

**Why not:** B is wrong because solution design is its own stage, and it is the one that produces the how. C is wrong because choosing the approach happened in the plan, so implementation does not reopen it. D is wrong because implementation depends on the requirements and design that come before it.

---

**2.** In this workflow, what is a skill such as the Phase Execution Guide?

- A. A certification a developer earns before they may use AI
- B. A one-off prompt written fresh for each phase
- C. Reusable instructions that make AI follow the same workflow every time
- D. A test suite that checks the code AI produces

**Answer:** C

**Why:** A skill is a set of reusable instructions. The Phase Execution Guide is the skill that takes every phase through the same steps, so execution is consistent from one phase to the next.

**Why not:** A confuses a skill with a qualification for a person. B is the opposite of reusable, because a skill is written once and used for every phase. D describes a set of tests, which belongs to the verification gates and is not what a skill is.

---

**3.** Before implementation begins, AI prepares a full phase brief, and the team decides when implementation starts. Which of these is one of the items in that brief?

- A. A production deployment schedule
- B. A list of defects found in the previous phase
- C. Release notes for end users
- D. A definition of done that lists all success criteria for the phase

**Answer:** D

**Why:** The Phase Education brief has five parts: the phase details, the game plan, the implementation plan, the definition of done and the test coverage. The definition of done holds all the success criteria. The brief gives the team what it needs to decide whether to start.

**Why not:** A and C are about releasing the product, and neither is part of the brief that prepares a phase for execution. B is wrong because defects are recorded in the Bugs and Issues Log, not in the brief for the next phase.

---

## Verification gates and approval

**4.** Once a chunk of a phase has been implemented, what is the correct order of steps?

- A. Human Gate, then AI Gate, then commit
- B. AI Gate, then Human Gate, then commit
- C. AI Gate, then commit, then Human Gate
- D. Commit, then AI Gate, then Human Gate

**Answer:** B

**Why:** The AI Gate verifies first, then the Human Gate verifies and approves, and only then is the phase ready to commit. AI does not commit until the team explicitly approves, so you control what enters the codebase.

**Why not:** A puts the person's review before the automated checks, so they would review work that has not passed the mechanical checks. C and D commit before the team has approved, which breaks the rule that nothing enters the codebase until you approve it.

---

**5.** Which check needs human judgment at the Human Gate, and cannot be left to the AI Gate?

- A. Does the build succeed?
- B. Is code coverage above the threshold?
- C. Does linting pass?
- D. Does the implementation match the Functional Requirement?

**Answer:** D

**Why:** The AI Gate checks mechanics and the Human Gate checks intent. Whether the implementation matches the Functional Requirement is the traceability check, and only a person who knows the requirement can judge it. AI provides a manual test plan, and the team runs it.

**Why not:** A, B and C are mechanical checks. AI can run them and report the results, so they belong in the AI Gate.

---

**6.** After the AI implements a chunk of a phase, the AI Gate reports that the build succeeds but two unit tests fail. What should you do?

- A. Move on to the manual test plan, because a person can judge whether the failing tests matter
- B. Send it back to the AI to fix the failures, and have the AI Gate run again before any human testing
- C. Approve the commit, because the build succeeds and the failures are only advisory
- D. Move on to the Human Gate and log the two failing tests there as bugs

**Answer:** B

**Why:** The AI Gate checks mechanics: the build, the tests, linting, coverage and the API responses. If it fails, you send the work back to the AI to fix and run the gate again. You do not skip ahead to the Human Gate. Both gates must pass before a phase is committed and complete, and the Human Gate only starts once the AI Gate has passed.

**Why not:** A and D both skip to the Human Gate, so a person would spend time reviewing work that has not passed the mechanical checks. C is wrong for two reasons: a failed AI Gate is not advisory, and AI does not commit until you explicitly approve.

---

## Go/No-Go, bug types and the log

**7.** While reviewing the Phase Education brief, you notice that the game plan includes a feature that appears nowhere in the functional requirements. What is the best action?

- A. Say "No-Go", raise the gap, and discuss and revise the plan before any code is written
- B. Say "Go", because AI read the upstream documents and the feature is probably intended
- C. Let implementation start and check the extra feature at the Human Gate
- D. Ask AI to commit the phase so the team can review the finished code afterwards

**Answer:** A

**Why:** If something looks wrong in the plan, the answer is No-Go, followed by discussion. This catches issues before code is written and keeps the decision about when implementation starts with the team. Asking whether the plan meets the functional and solution design plans, and excluding scope creep, are exactly the checks this is for.

**Why not:** B trusts that AI read the documents instead of checking its brief. C waits until the code exists, when the extra feature has already been built. D commits before any review, which breaks the rule that AI waits for your approval.

---

**8.** A test fails because the validation rejects a name containing a space. The Functional Requirement never mentions spaces, so the specification is silent on this case. What is the correct way to handle it?

- A. Ask AI to quietly change the validation so the test passes, and mention it later
- B. Fix it straight away and commit, because it is a small change
- C. Do not just fix it. Talk to the Product Owner or Business Analyst, update the specification and create a change record, then implement
- D. Leave the code as it is, because the requirement does not mention spaces, so the current behaviour must be right

**Answer:** C

**Why:** When the specification is wrong or missing, the behaviour cannot be changed silently. If a fix requires a change to a specification, you update the specification first and then implement. Talking to the PO or BA and recording a change record keeps the documents and the build consistent.

**Why not:** A is the failure of silently changing behaviour to make a test pass, which leaves the specification out of step with the code. B treats a specification gap as an ordinary implementation miss, but the fix itself changes what the system is meant to do. D dismisses valid input being rejected, which is exactly the “validation works but rejects valid input” case that should be raised and logged.

---

**9.** Which set of details does every bug in the Bugs and Issues Log get?

- A. A number, a date, a phase reference and an impact classification
- B. A number, a date, an assignee and a due date
- C. A date, a phase reference, a severity score and a screenshot
- D. A number, a priority ranking, an assignee and a fix estimate

**Answer:** A

**Why:** Every bug gets a number, a date, a phase reference and an impact classification. The impact classification is one of four types: badly implemented requirement, missed requirement, new requirement discovered, or issue found during testing. The entry also records a summary, a status, where the problem lives and which documents it affects.

**Why not:** B, C and D each include fields that are not required for every bug, such as an assignee, a due date, a severity score, a screenshot, a priority ranking or a fix estimate. Each of them also leaves out at least one of the four required details.

---

## Training requirements covered

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: covered for the implementation execution stage
- **R2** Hands-on execution of a stage: not in this quiz (it is assessed by practical sign-off, and this quiz tests knowledge only)
- **R6** Failure-point recognition: covered for the implementation execution stage
- **R7** Knowledge check record: contributes
- **R3, R4, R5**: not in this quiz (R3 is deferred; the skill question is about a building block used in this stage and does not test AIDE; R4 and R5 need source material, and the log question tests a step in the execution workflow, not knowledge base setup)

## Training requirement traceability matrix

| Question      | R1      | R2     | R3               | R4               | R5               | R6      | R7          |
| ------------- | ------- | ------ | ---------------- | ---------------- | ---------------- | ------- | ----------- |
| 1             | ✓       |        |                  |                  |                  |         | ✓           |
| 2             | ✓       |        |                  |                  |                  |         | ✓           |
| 3             | ✓       |        |                  |                  |                  |         | ✓           |
| 4             | ✓       |        |                  |                  |                  |         | ✓           |
| 5             | ✓       |        |                  |                  |                  |         | ✓           |
| 6             |         |        |                  |                  |                  | ✓       | ✓           |
| 7             |         |        |                  |                  |                  | ✓       | ✓           |
| 8             |         |        |                  |                  |                  | ✓       | ✓           |
| 9             | ✓       |        |                  |                  |                  |         | ✓           |
| **Questions** | 6       | 0      | 0                | 0                | 0                | 3       | 9           |
| **Status**    | Covered | Not in this quiz | Not in this quiz | Not in this quiz | Not in this quiz | Covered | Contributes |

Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (practical sign-off, not assessed in this quiz)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check
