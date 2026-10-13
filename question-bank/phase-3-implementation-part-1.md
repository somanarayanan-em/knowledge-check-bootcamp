# Implementation Package (Part 1) Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

- This question bank contains 20 MCQs in five categories of four.
- ***To build a quiz of 5, draw one question from each category.***

---

## What the package is, and traceability

**1.** What is the Implementation Package, and what should it be?

- A. The finished code files for the product, saved together in one place
- B. One large task that tells AI to implement everything at once
- C. Working software planned in phases, where each phase can be run and checked on its own and builds toward the complete system
- D. A flexible list of features that the team adds to as ideas come up

**Answer:** C

**Why:** The package is a system of delivery, not a pile of code. Work is organized into phases with clear milestones, traced to requirements and verified at each step. Every phase is independently executable and verifiable, and the phases build incrementally toward the whole system.

**Why not:** A describes a pile of code files, which is what the package is not. B is the "implement everything" approach the phased plan is meant to avoid. D describes ad-hoc feature development, with no traceability and no checks.

---

**2.** The team is deciding what goes into the implementation plan. Which description fits best?

- A. A list of phases, each written in the eight standard sections, linked to the requirements and design
- B. The full text of the requirements and design, so the whole project can be read in one file
- C. The finished code and tests for every phase, so the plan shows exactly what was built
- D. A set of bug-fix phases prepared in advance, so problems found later have a place to go

**Answer:** A

**Why:** The plan states what will be built and how it will be verified. It references the requirements and the design and does not duplicate them. It holds a phase index (the list of all phases), a detailed specification for every phase in the list (each written in the eight standard sections) and an execution workflow.

**Why not:** B copies upstream documents into the plan, which creates a second version to keep in step. C is wrong because code and tests are produced when the plan is run, not written into it. D is wrong because bugs surface once coding starts, so a bug-fix phases section does not belong in the plan.

---

**3.** While reviewing a plan, a team finds a phase that builds a capability no requirement mentions. What is the best response?

- A. Keep it, because working capability is always an advantage
- B. Add a new requirement inside the plan, so the phase has something to point to
- C. Leave it in and ask AI to write a matching requirement after the build
- D. Question whether it should exist, and if the capability is really needed, change the requirements first

**Answer:** D

**Why:** Everything traces back: requirement, solution design, implementation design, then code and tests. If something cannot be traced to a requirement, question whether it should exist. Requirements are not changed inside the plan. If something truly has to change, update the requirements first.

**Why not:** A treats untraceable work as free, but it adds effort, review and risk with no business need behind it. B invents a requirement in the wrong place, because the plan uses requirements as written. C reverses the order, so the requirement would be written to fit work that was already done.

---

**4.** A phase sets up the project structure and does not implement any functional requirement. How should its FR mapping be handled?

- A. Remove the phase, because every phase must map to a requirement
- B. Mark it as foundational (FR Mapping: None), and keep a requirement listed on every feature phase
- C. Write a requirement for it, so the field is never empty
- D. Link it to the nearest feature requirement, so the field is filled in

**Answer:** B

**Why:** Every phase has a purpose and lists the functional requirements it implements. The exception is foundational work such as project scaffolding, which may be marked as foundational with no mapping. A feature phase with no mapping is the signal to ask whether it is really foundational or whether it should come out.

**Why not:** A is wrong because scaffolding has to happen before anything else can be built. C invents a requirement, which the package never does. D records a link that is not true, and it hides the fact that the phase is foundational.

---

## Skills and templates

**5.** Which description of skills and templates is correct?

- A. A skill is a ready-made structure with sections to fill in, and a template is the know-how for doing the task
- B. A template is a ready-made structure with sections to fill in, and a skill is the know-how for doing the task
- C. A skill is a single chat message, and a template is a finished code file
- D. The two terms mean the same thing, and the name depends only on the tool being used

**Answer:** B

**Why:** A template sets the sections, headings and required details up front, so the output has a consistent structure. A skill is reusable know-how that the AI applies to a task. Used together, they keep the output consistent and on-standard, and the team stays in charge of approving the result.

**Why not:** A swaps the roles of the skill and the template. C describes neither: a skill is written down once and reused, and a template is a starting structure, not finished code. D is wrong because each has a different job, which is why they are used together.

---

**6.** Why is a skill better than typing the same instructions into a chat each time?

- A. It lets the work go ahead without anyone reading the documents
- B. It guarantees that AI will never make a mistake
- C. It lets AI decide what to do without checking in with the team
- D. It is written once, gives the same steps each run, and can be shared through the repository

**Answer:** D

**Why:** An ad-hoc prompt lasts for one moment and stays in one person's chat history. A skill is a durable capability: it is captured once, versioned and shared, loads only when needed, and gives the same workflow and checklist each time. The team builds up institutional knowledge instead of retyping it.

**Why not:** A is wrong because the team still loads and verifies the upstream documents. B overstates what a skill does, because the team still checks the output. C is wrong because the team stays in charge and approves at each checkpoint.

---

**7.** A team member keeps retyping a long set of instructions for writing a phase specification. Each person's version differs a little, and the results vary from run to run. What is the best fix?

- A. Capture the instructions once as a shared skill, with a template for the shape, and keep both in the repository
- B. Keep the best version in a personal notes file and paste it each time
- C. Switch to a larger model, so the results stop varying
- D. Ask AI to remember the instructions for next time

**Answer:** A

**Why:** Re-explaining the same thing leads to drift, because a step gets forgotten or each person words it differently. A skill holds the know-how and a template holds the shape, and because they live in the repository, everyone uses the same version.

**Why not:** B helps one person, but the instructions stay out of the team's shared, reviewed place. C changes the model without fixing the cause, which is that the instructions are not written down once and shared. D relies on memory of a chat, and the team's documents are the memory.

---

**8.** The team asks AI to build the plan. Its summary does not mention the phase shape file the team pointed it to. What should the team do?

- A. Carry on, since AI will pick up the structure as it goes
- B. Rewrite the requirements so that they include the phase shape
- C. Pause and ask it to review the shape and confirm what belongs in each phase before continuing
- D. Accept the plan and fix any inconsistent phases at the end

**Answer:** C

**Why:** The verification step asks AI to summarize the scope, key FRs and constraints, and to confirm what belongs in each phase, including that it actually read the shape file. The team confirms this before moving on.

**Why not:** A and D leave the phases open to inconsistent structure, which the shape is meant to prevent. B changes the wrong document: the requirements do not define the phase shape.

---

## Building the plan: workflow and phase size

**9.** In a draft plan, the team finds that Phase 3 can only be tested once Phase 5 has been built. What is the best response?

- A. Keep the order, and test Phase 3 together with Phase 5 once both are built
- B. Keep the order, and mark Phase 3's gates as passed so that work can continue
- C. Merge all the phases into one so that nothing waits for anything else
- D. Rework the phases so that each one depends only on earlier phases and can be verified on its own

**Answer:** D

**Why:** Each phase should be independently executable and verifiable, with clear dependencies on earlier phases. Phases build on each other, like a foundation before walls. A phase that cannot be verified until a later one exists breaks both rules. Checking for sensible dependencies is part of verifying each section as the plan is filled in.

**Why not:** A gives up on verifying each phase as it is built. B removes the check that the phase exists to provide. C is not a fix for a dependency problem. Whether to combine phases is a separate sizing decision for the team, and merging them all would make verification harder.

---

**10.** The team is worried that each phase would produce too much code to review. What is the best approach?

- A. Accept the phases as they are, because AI writes code quickly
- B. Ask AI to write shorter phase descriptions, so there is less to read
- C. Set limits on phase size that work for your pod, so each phase produces a slice a person can test
- D. Remove some of the requirements until the phases are small enough

**Answer:** C

**Why:** This is where the team runs the plan and not the model. Imposing limits on size and scope addresses worries about review load and impact. AI is writing the code, so phases should be sized for human review, not for a human sprint. Each phase should produce a slice of functionality a person can test.

**Why not:** A ignores the review problem, because speed of writing does not make the code easier to check. B is wrong because shorter descriptions do not change how much code each phase produces. D changes the scope of the product instead of the size of the phases.

---

**11.** Another team is waiting on one of the APIs, so you ask AI to reorder the phases. It agrees and produces a new order straight away. What should you do next?

- A. Accept it, because AI is following your instruction
- B. Check the new order against the phase dependencies, because AI tries to please and the order may not make sense
- C. Ask AI to rewrite the requirements to match the new order
- D. Fix the order and skip the dependency check, since you chose it

**Answer:** B

**Why:** Specialists and other teams may call for a different order, and the team can reorder phases. But AI is eager to please and may produce an order that is not actually sound, for example one where a phase comes before something it needs. Negotiate the order, and then double-check it. Do not rubber-stamp.

**Why not:** A trusts the answer because it agrees with you. C is wrong because a change in phase order is a planning decision, and the requirements do not change. D skips the check that catches a phase starting before its dependencies are complete.

---

**12.** After the implementation planning stage is complete, which files should the team expect to have?

- A. The implementation plan with its phases, and a phase status tracker
- B. The implementation plan, a bugs log and a change tracker
- C. The implementation plan, the code files and the test files
- D. A phase status tracker, a change tracker and the code files

**Answer:** A

**Why:** The package has several components, and not all of them exist at this point. When planning is complete, the team has the implementation plan, which lists the phases, and a phase status tracker that records the state of each phase. The bugs log, change tracker, code and tests do not exist yet, because they appear when coding starts. If AI creates empty folders for them, that is fine, but nobody should start filling them.

**Why not:** B lists two components that only appear once coding begins. C lists the code and tests, which come from running the plan. D leaves out the plan itself and includes components that only appear once coding begins.

---

## The eight-section phase shape

**13.** Why must every phase follow the same eight sections, in the same order?

- A. So phases are predictable and complete, each can be verified, and AI can follow a consistent structure
- B. So the plan looks tidy when it is read by someone outside the team
- C. So the plan is shorter, because fewer details are needed
- D. So AI can decide for itself which sections to leave out of each phase

**Answer:** A

**Why:** Without a standard shape, phases become inconsistent: some have detailed tests, some have none, some have clear goals and some are vague. A fixed shape gives predictability (you know what to expect), completeness (nothing is forgotten), verifiability (clear success criteria) and consistency for AI.

**Why not:** B treats it as appearance, when the purpose is quality and checking. C is wrong because the shape makes sure nothing is left out. D is wrong because all eight sections are mandatory, and the team does not leave sections out.

---

**14.** A good goal describes the state of the system after the phase. Which goal is written correctly for a phase?

- A. "Implement the assignment of employees to projects"
- B. "Write the service and the screens for project assignment"
- C. "Spend the phase working on the assignment feature"
- D. "The system can assign an employee to a project and remove them again, and the change is saved"

**Answer:** D

**Why:** A good goal describes the state of the system after the phase: what the system can do. It is not a description of the effort or activity.

**Why not:** A, B and C all describe work to be done and not the result. They do not say how the team would know the phase is complete.

---

**15.** Which check belongs in the human gate of a phase, and not in the AI gate?

- A. Running the automated tests and confirming they all pass
- B. Starting the application and confirming it runs
- C. Confirming that the messages shown to users are clear, and that the behaviour matches the business rules
- D. Confirming that a request to the new endpoint returns the expected status

**Answer:** C

**Why:** The AI gate checks mechanics: do the tests pass, does the application start, does the endpoint respond correctly. The human gate checks intent: does it match the design, are the messages usable, do the business rules hold. The plan tells AI to stop after its gate, show proof and wait for the team.

**Why not:** A, B and D are all mechanical checks that can be run and confirmed automatically, so they belong in the AI gate.

---

**16.** Which description fits well-written success criteria for a phase?

- A. A short paragraph on how well the phase went
- B. A binary checklist of done or not done, where each item can be checked on its own
- C. A percentage that shows how far the phase is complete
- D. A long list that covers every detail, so nothing is missed

**Answer:** B

**Why:** Success criteria are a binary checklist of done. Each item is either done or not done, with no partial credit, and each one can be verified independently. The team keeps the list short enough to check, and sets that size to suit the pod.

**Why not:** A is a narrative, which cannot be checked as done or not done. C allows partial credit, and the criteria are meant to be binary. D tries to cover every detail, which makes the list hard to check item by item.

---

## Pitfalls and judgment

**17.** While you are creating the implementation plan, AI starts writing application code. What should you do?

- A. Let it finish, then review the code with the plan
- B. Accept it, because early code saves time later
- C. Stop it and restate the scope: "Plan only. Do not create code." Start a new chat if needed.
- D. Ask it to write tests for the code it just produced

**Answer:** C

**Why:** The plan says what will be built and how it will be verified. The code is produced when the plan is run, in the next stage. AI often does more than it was asked, so stop it, restate that this is planning only, and start fresh if it keeps going.

**Why not:** A lets AI spend effort and context outside the task, and the code would be built without the plan being reviewed. B mixes up the stages. D adds more work that belongs to a later stage.

---

**18.** A draft phase specification repeats long passages from the requirements and from the solution design. What is the best response?

- A. Keep the passages, because the phase then holds everything it needs
- B. Replace the passages with references to the requirement and design sections, because the plan points to them and does not copy them
- C. Move the passages into a separate file, so the plan stays short
- D. Remove the passages and the references, so each phase stands alone

**Answer:** B

**Why:** The plan references the requirements and the solution design and does not duplicate them. A copy is a second version that can fall out of step with the original, so the plan stays lean and points to the source.

**Why not:** A creates copies that may later disagree with the originals. C still holds a copy, only in another place. D removes the link to the source, and the phase loses its traceability.

---

**19.** A teammate's phase has automated tests and a check that the application starts, but nothing for a person to review. What is missing?

- A. More automated tests, because tests are the strongest proof that a phase is complete
- B. A longer Outcome section, so reviewers know what to look for when they check
- C. A second set of mechanical checks, run by a different person to be sure
- D. A human gate, where a person checks the result against the design and the business rules

**Answer:** D

**Why:** Every phase has both gates, because they catch different things. The AI gate checks mechanics: do the tests pass and does the application start. The human gate checks intent: does the result match the design, are the messages usable, and do the business rules hold. Passing tests do not show that the phase does what was intended, and all eight sections are mandatory.

**Why not:** A adds more mechanical checking, but mechanics were never the gap. B lists deliverables, which does not verify whether they are right. C repeats mechanical checks by hand, and still does not check intent.

---

**20.** A phase's Outcome section reads: "Work on the project assignment screen." What should the Outcome describe instead?

- A. The things that will exist when the phase is done, each one measurable and able to be confirmed
- B. The effort involved, such as how many days the work is expected to take
- C. The steps AI will follow, written in the order it will do them
- D. The business reason for the phase, in the words of the requirement

**Answer:** A

**Why:** Outcomes are measurable deliverables, not activities. They are artifact-based: think of what files or things will exist when the phase is done. Each one can be verified on its own, like acceptance criteria. "Work on the screen" describes effort and does not say what will exist.

**Why not:** B describes effort, not a deliverable. C belongs in the Plan section, which holds the step-by-step instructions. D belongs in the requirements, and the phase refers to those and does not repeat them.

---

## Training requirements covered

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: covered for the implementation planning stage
- **R2** Hands-on execution of a stage: not in this quiz (it is assessed by practical sign-off, and this quiz tests knowledge only)
- **R6** Failure-point recognition: covered for the implementation planning stage
- **R7** Knowledge check record: contributes
- **R3, R4, R5**: not in this quiz (R3 is deferred; the skills and templates questions are about the building blocks used in this stage and do not test AIDE; R4 and R5 need source material)

## Training requirement traceability matrix

| Question      | R1      | R2     | R3               | R4               | R5               | R6      | R7          |
| ------------- | ------- | ------ | ---------------- | ---------------- | ---------------- | ------- | ----------- |
| 1             | ✓       |        |                  |                  |                  |         | ✓           |
| 2             | ✓       |        |                  |                  |                  |         | ✓           |
| 3             |         |        |                  |                  |                  | ✓       | ✓           |
| 4             | ✓       |        |                  |                  |                  |         | ✓           |
| 5             | ✓       |        |                  |                  |                  |         | ✓           |
| 6             | ✓       |        |                  |                  |                  |         | ✓           |
| 7             |         |        |                  |                  |                  | ✓       | ✓           |
| 8             |         |        |                  |                  |                  | ✓       | ✓           |
| 9             | ✓       |        |                  |                  |                  |         | ✓           |
| 10            |         |        |                  |                  |                  | ✓       | ✓           |
| 11            |         |        |                  |                  |                  | ✓       | ✓           |
| 12            | ✓       |        |                  |                  |                  |         | ✓           |
| 13            | ✓       |        |                  |                  |                  |         | ✓           |
| 14            | ✓       |        |                  |                  |                  |         | ✓           |
| 15            | ✓       |        |                  |                  |                  |         | ✓           |
| 16            | ✓       |        |                  |                  |                  |         | ✓           |
| 17            |         |        |                  |                  |                  | ✓       | ✓           |
| 18            |         |        |                  |                  |                  | ✓       | ✓           |
| 19            |         |        |                  |                  |                  | ✓       | ✓           |
| 20            |         |        |                  |                  |                  | ✓       | ✓           |
| **Questions** | 11      | 0      | 0                | 0                | 0                | 9       | 20          |
| **Status**    | Covered | Not in this quiz | Not in this quiz | Not in this quiz | Not in this quiz | Covered | Contributes |

Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (practical sign-off, not assessed in this quiz)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check
