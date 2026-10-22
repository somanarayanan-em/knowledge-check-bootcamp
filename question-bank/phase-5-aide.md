# Intro to A.I.D.E. Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

**Status: first draft, for training team review.**

- This question bank contains 14 MCQs. They are not split into categories.
- ***Use all 14 as the quiz. They mix understanding and scenario questions.***
- Source: *Intro to A.I.D.E.* (v8).
- **Naming convention for this bank:** unlike the other banks, these questions name skills and files (for example `/analyze-repository`, `/navigate-knowledge-base`, `AGENTS.md`) where A.I.D.E. does. The questions test what each one is for and when to use it. They do not test memory of command names.

---

**1.** What is A.I.D.E.?

- A. A command-line tool that is installed as a dependency of each source repository
- B. A hosted service that reviews pull requests and writes code on the team's behalf
- C. A set of skills, written as markdown files, that the team's existing coding agent discovers and follows
- D. A code library that is added to the application so that it can call AI models

**Answer:** C

**Why:** A.I.D.E. (AI Integrated Delivery Enablement) is not a tool, service, library, dependency or CLI. Nothing runs and there is no command to call. It is a set of skills, written as plain markdown files with the templates and configuration that go with them, that the coding agent reads and follows. It sits beside the source repositories, not inside them.

**Why not:** A is wrong because there is no installer or command-line tool to run. B describes a hosted service, and A.I.D.E. has no server side. D is wrong because nothing is added to the application's code.

---

**2.** A team member is not sure how to use a skill, or which skill fits their goal. What is the easiest way to find out?

- A. Open the skill's `SKILL.md` and ask the assistant to explain it, or ask the assistant which skill fits the goal
- B. Read every step file in the skill's folder before running anything
- C. Ask a colleague to run the skill and report back on what it does
- D. Run the skills one at a time until one produces something useful

**Answer:** A

**Why:** The assistant knows the skills and can read them. The team can open a skill's `SKILL.md` and ask for an explanation, or describe the goal and ask which skill fits. A skill can then be run by name (`/<skill-name>`), or the team can describe the goal and let the agent choose. The team does not need to read the whole folder first.

**Why not:** B is slow, and the step files only make sense once a skill has been chosen. C hands the learning to someone else and leaves this person no wiser. D runs skills that may not fit, and each run can produce documents that nobody wanted.

---

**3.** You ask your AI assistant for something in plain English, without naming a skill. How does it know which skill to run?

- A. It reads every step file in every skill folder and picks the closest match
- B. It matches your request against each skill's name and "when to use it" description in the skill's frontmatter
- C. It searches each skill's reference files for the words in your request
- D. It runs whichever skill sits in the same repository as the code you are working on

**Answer:** B

**Why:** The top of each skill's main file (its frontmatter) holds a name and a "when to use it" description. The assistant matches your request against those descriptions to find and choose a skill. Step files and references are loaded only after a skill has been chosen. That is why a clear description matters more than a long procedure.

**Why not:** A and C describe content that is read only after a skill has been picked. D is wrong because discovery depends on where the IDE scans for skills and on the description, not on sitting beside the code.

---

**4.** The team wants the agent to follow a guardrail in every request, for example "never force-push". Where does that belong?

- A. In a new skill that the agent runs when the work calls for it
- B. In behaviour guidelines, such as `AGENTS.md` or the IDE's own local rules, that apply to every request
- C. In a reference file inside a skill, which the agent loads only when needed
- D. In the first message of each chat, which the team pastes in again each time

**Answer:** B

**Why:** A skill is a procedure for one task. `AGENTS.md` (called `CLAUDE.md` on some hosts) and local IDE rules hold behaviour that colours every request, skill invocations included. For example, a local rule that says "never force-push" holds across every session.

**Why not:** A is wrong because a skill runs only when its task comes up, and a guardrail needs to hold all the time. C loads only when needed, so it would not apply to every request. D works for one session but is easy to forget and does not persist.

---

**5.** A team stops partway through a flow on Friday afternoon. How can it pick up again on Monday?

- A. Explain the work to the agent again in a new chat, from memory
- B. Start the flow again from the first skill
- C. Carry on from the documents the earlier skills already saved, because skills hand off to each other through them
- D. Ask the agent to recall the earlier chat and carry on from there

**Answer:** C

**Why:** Skills hand off to each other by name, at fixed points, and each hand-off is a named document saved in the repository. It is not a conversation that someone has to remember. That is what makes it possible to stop halfway and pick up the next day: the next skill reads the document the last one saved.

**Why not:** A relies on memory, and details will be lost or changed. B repeats work that is already done. D relies on a chat history that a new chat does not have, and the team's documents are the memory.

---

**6.** Most stages have one skill that creates a document and a separate skill that reviews it. Who decides whether the work is good enough to move to the next stage?

- A. The review skill, because it checks the document independently
- B. The skill that created the document, once it has checked its own work
- C. The team, using the review skill's findings to inform the decision
- D. Nobody, because the next stage starts as soon as the review finishes

**Answer:** C

**Why:** A.I.D.E. calls this "AI proposes, human disposes". The creating skill drafts the document, and the review skill gives an independent check of it. The people stay the decision-makers: there are human gates in execution, and nothing merges itself.

**Why not:** A and B hand the decision to a skill, which A.I.D.E. rules out. D removes the decision altogether, but each stage ends with a person deciding before the next one starts.

---

**7.** A team has to add a feature to an existing system that nobody on it wrote or has read. Which flow fits, and what is its route?

- A. Greenfield: go straight to requirements, because the feature is new
- B. Brownfield: reverse engineer the code, build the knowledge base, then follow the greenfield route on that grounding
- C. Quick-dev: write one combined spec, plan lightly and execute
- D. Any flow, because each flow uses its own set of skills

**Answer:** B

**Why:** Brownfield is for existing code. The agent is grounded first (reverse engineering, then the knowledge base) and then requirements, design, planning, quality and execution run on that base. Without it, an agent pointed at an unfamiliar codebase produces something plausible but wrong.

**Why not:** A skips the grounding step, so the work would rest on guesses about the code. C is for a small, scoped change, which is not what a new feature in unfamiliar code is. D is wrong because the flows use the same set of skills by a different route, and the flow is declared once in `project.toml`.

---

**8.** A change is a small, scoped fix. Which route should the team use?

- A. Use the quick-dev route, so the change stays inside the framework with one combined spec and a light plan
- B. Skip the framework and make the change directly, since a small fix does not need a process
- C. Run the full requirements, design, implementation and quality path every time
- D. Run reverse engineering again on all repositories before making the change

**Answer:** A

**Why:** Every change goes through one of two paths: quick-dev for a simple change, or the full path for a complex one. Quick-dev uses one combined spec, a light plan with a clarity gate, and then execution with a hand-off for the knowledge base update. A one-line fix does not need a full spec package, and quick-dev keeps small changes inside the framework instead of routed around it.

**Why not:** B routes the change around the framework, which is exactly what quick-dev is meant to prevent. C is too heavy for a small change. D is not needed for a small change when the knowledge base already exists.

---

**9.** The team has a repository it has never seen and is not sure which reverse-engineering skill fits. What should it do?

- A. Pick the skill whose name sounds closest, and check the result afterwards
- B. Run all of the reverse-engineering skills, and keep the best result
- C. Ask A.I.D.E. to analyse the repository, or run `/analyze-repository`, which classifies it and dispatches the right reverse-engineering skills in the right order
- D. Skip reverse engineering, and start with requirements

**Answer:** C

**Why:** `/analyze-repository` is the dispatcher. It classifies the repository and names which of the eleven domain skills to run and in what order. The team can run it by name, or ask the assistant to analyse the repository and let it pick the skill. This matters because choosing the wrong member of a pair (for example an application skill for a component library) does not fail. It produces a document that nobody wanted. If nothing fits the stack, the generator skill writes a new reverse-engineering skill.

**Why not:** A risks the quiet wrong-skill problem described above. B wastes effort and produces documents for readers who do not exist. D skips the grounding that stops the agent from guessing about code it has not read.

---

**10.** Every reverse-engineering extraction produces two document sets. Which description is correct?

- A. Internal docs are for people who will change the code and land in the source repository, and consumer docs are for people who will call it and land in the knowledge base
- B. Internal docs are for people who call the code, and consumer docs are for people who change it
- C. Both sets are written to the knowledge base, because that is where the agent reads
- D. Both sets are written to the source repository for the developers

**Answer:** A

**Why:** Internal docs (Part A) explain how the code works inside, for whoever will change it, and are written to the source repository. Consumer docs (Part B) describe what the code exposes, depends on and owns, for whoever will call it, and are written to the knowledge base. Each extraction closes with an attestation, and nothing reaches the knowledge base unattested.

**Why not:** C and D each send both sets to one place, but the two sets have different readers and different destinations. B reverses the two readers.

---

**11.** What is a knowledge base in A.I.D.E.?

- A. A vector database of embeddings that the agent queries by meaning
- B. A hosted service that the team has to run and keep available
- C. A map of the whole solution in plain markdown, held in its own repository, and reviewed in pull requests like any other change
- D. A copy of every repository's source code held in one place

**Answer:** C

**Why:** It is a map of how the whole solution works, assembled from the documents of every repository: an index, one file per component and a dependency graph. There is no vector database, no embeddings and nothing to operate. Agents read it with plain read, grep and glob, which is why it can live in a Git repository and be reviewed in ordinary pull requests.

**Why not:** A and B describe infrastructure that a knowledge base does not need. D is wrong because it holds documentation about the code, not the code itself.

---

**12.** A defect fix touches one area of a large legacy system. How does the team find out which parts of the system the change will affect?

- A. Ask the agent to search the whole codebase for related terms
- B. Describe the change to `/navigate-knowledge-base` and read the few knowledge base components it returns, each with a reason
- C. Read the whole knowledge base from start to finish before starting
- D. Run `/analyze-repository` again to classify the repository

**Answer:** B

**Why:** `/navigate-knowledge-base` takes a plain description of a change and returns the few components it touches, with a reason for each. The team reads those and not the codebase. The requirements, design, planning and execution skills use it the same way, so each loads only the components it needs.

**Why not:** A is the hopeful searching through a huge codebase that the knowledge base is meant to replace. C defeats the point of the index. D classifies a repository and does not say what a change will touch.

---

**13.** A feature was merged last week, and nobody has updated the knowledge base since. What should the team do?

- A. Update the knowledge base for the merged change, and name a steward who keeps it current on an agreed cadence
- B. Leave it as it is, because the agent reads the source code directly whenever it needs to
- C. Leave it until the next full audit, because a single merge changes very little
- D. Wait for A.I.D.E. to update it automatically from its ready-made pipeline

**Answer:** A

**Why:** A knowledge base that nobody maintains is worse than none, because people and agents trust what it says. The skills help: update after each merge, detect drift, verify coverage periodically and audit in full. They are agent skills, not command-line tools, and A.I.D.E. ships no pipeline, so keeping the knowledge base current is the team's job. Naming a steward and agreeing a cadence, even a manual one, should happen from day one.

**Why not:** B is wrong because the agent is grounded in the knowledge base so that it does not have to read the whole codebase. C lets drift build up while people keep relying on content that is out of date. D is wrong because no pipeline template is provided.

---

**14.** An increment has passed its AI gate and the code is built. What happens next in execution?

- A. The code is pushed to the remote branch automatically, because the AI gate has passed
- B. The team's human gate comes next, and nothing is committed or pushed without the team's yes, with the pull request step asking again
- C. The pull request merges itself if the tests pass
- D. The human gate is skipped for small increments

**Answer:** B

**Why:** Execution takes one increment at a time through test-driven development, the AI gate and then the human gate. It deliberately leaves the working tree uncommitted. The pull request skill asks again before it commits and before it pushes. Nothing reaches a remote without the team saying yes.

**Why not:** A and C let work reach the remote or merge without a person deciding, which A.I.D.E. rules out ("nothing merges itself"). D is wrong because the human gate is part of every increment, and the gate is only worth what the person at it puts in.

---

## New criteria: rubric mapping (Rubrics 1, 3, 4)

Questions are mapped to the three readiness rubrics. Primary means the question directly tests that rubric outcome. Supporting means it also uses the rubric while the main test sits in another column. None means it does not test that rubric.

**Rubric outcomes used**

- **Rubric 1. Explain the Model 2 lifecycle and operating model:** give an accurate, role-relevant account of how work moves through the method, including activities, artefacts, hand-offs and escalation paths.
- **Rubric 3. Use FlowAI tools, context and knowledge assets effectively:** use the repository, the AI-assisted workflow, the knowledge base and context so the work is high quality.
- **Rubric 4. Exercise quality judgment and responsible AI practices:** evaluate AI-assisted work critically, and keep a person accountable for what is allowed to proceed.

## New criteria: mapping matrix

| Question | Rubric 1 / Lifecycle | Rubric 3 / Tools and context | Rubric 4 / Quality judgment | Why it maps |
| -------- | -------------------- | ---------------------------- | --------------------------- | ----------- |
| 1. What is A.I.D.E.? (C) | None | Primary | None | Tests what the framework is: skills as markdown files that the existing agent follows. |
| 2. Finding out how to use a skill (A) | None | Primary | None | Tests using the assistant and `SKILL.md` to learn which skill fits a goal. |
| 3. How the agent chooses a skill (B) | None | Primary | None | Tests how skills are discovered: name and "when to use it" description in the frontmatter. |
| 4. Where an always-on guardrail belongs (B) | None | Primary | Supporting | Tests `AGENTS.md` and local rules as context that applies to every request. The guardrail also keeps the agent inside agreed limits. |
| 5. Resuming on Monday (C) | Primary | Supporting | None | Tests hand-offs between skills through saved documents. The documents are also the context the next skill reads. |
| 6. Who decides the work is good enough (C) | Supporting | None | Primary | Tests "AI proposes, human disposes". The review skill informs, and the team decides at each stage gate. |
| 7. Feature in an unfamiliar system (B) | Primary | Supporting | None | Tests choosing the brownfield route. Grounding in reverse engineering and the knowledge base comes first. |
| 8. Small, scoped fix (A) | Primary | None | None | Tests the quick-dev path against the full path for the size of the change. |
| 9. Unfamiliar repository (C) | None | Primary | Supporting | Tests `/analyze-repository` as the dispatcher. Avoids quietly producing the wrong document. |
| 10. Internal and consumer docs (A) | Supporting | Primary | None | Tests the two document sets, their readers and their destinations (source repository and knowledge base). |
| 11. What a knowledge base is (C) | None | Primary | None | Tests the knowledge base as plain markdown in its own repository, reviewed through pull requests. |
| 12. Finding what a change affects (B) | None | Primary | None | Tests `/navigate-knowledge-base` as the way to load only the components a change touches. |
| 13. Stale knowledge base after a merge (A) | None | Primary | Supporting | Tests keeping the knowledge base current. A named steward stays accountable for its quality. |
| 14. After the AI gate passes (B) | Supporting | None | Primary | Tests the human gate. Nothing is committed, pushed or merged without the team's yes. |

## New criteria: coverage

| Rubric | Primary | Supporting | Status |
| ------ | ------- | ---------- | ------ |
| 1. Lifecycle and operating model | 5, 7, 8 | 6, 10, 14 | Covered |
| 3. Tools, context and knowledge assets | 1, 2, 3, 4, 9, 10, 11, 12, 13 | 5, 7 | Covered |
| 4. Quality judgment and responsible AI | 6, 14 | 4, 9, 13 | Covered, two primary questions |

Notes:

- Hands-on execution of a stage is not assessed in this quiz. It is covered by practical sign-off, and this quiz tests knowledge only.
- Escalation paths (Rubric 1) and role literacy are not tested here and need source material.

## Crosswalk: previous to new criteria

| Previous criterion | New rubric |
| ------------------ | ---------- |
| R1 End-to-end process literacy | Rubric 1 |
| R2 Hands-on execution | No equivalent (practical sign-off) |
| R3 Skills Framework fluency | Rubric 3 |
| R4 Knowledge base setup | Rubric 3 |
| R5 Operating model and role literacy | Rubric 1 (not tested here) |
| R6 Failure-point recognition | Rubric 1 and Rubric 4 |
| R7 Knowledge check record | No equivalent |

---

## Previous criteria: training requirements covered (R1–R7)

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: not tagged in this bank (the other banks cover the lifecycle stages)
- **R2** Hands-on execution of a stage: not in this quiz (it is assessed by practical sign-off, and this quiz tests knowledge only)
- **R3** AIDE Skills Framework fluency: covered by every question
- **R4** Knowledge base setup: conceptual touchpoints only (a working knowledge base needs practical sign-off)
- **R6** Failure-point recognition: covered by the scenario questions
- **R7** Knowledge check record: contributes
- **R5**: not in this quiz (needs source material)

## Previous criteria: traceability matrix (R1–R7)

| Question      | R1 | R2 | R3      | R4                    | R5 | R6      | R7          |
| ------------- | -- | -- | ------- | --------------------- | -- | ------- | ----------- |
| 1             |    |    | ✓       |                       |    |         | ✓           |
| 2             |    |    | ✓       |                       |    |         | ✓           |
| 3             |    |    | ✓       |                       |    |         | ✓           |
| 4             |    |    | ✓       |                       |    |         | ✓           |
| 5             |    |    | ✓       |                       |    |         | ✓           |
| 6             |    |    | ✓       |                       |    |         | ✓           |
| 7             |    |    | ✓       |                       |    | ✓       | ✓           |
| 8             |    |    | ✓       |                       |    | ✓       | ✓           |
| 9             |    |    | ✓       |                       |    | ✓       | ✓           |
| 10            |    |    | ✓       | ✓                     |    |         | ✓           |
| 11            |    |    | ✓       | ✓                     |    |         | ✓           |
| 12            |    |    | ✓       |                       |    | ✓       | ✓           |
| 13            |    |    | ✓       | ✓                     |    | ✓       | ✓           |
| 14            |    |    | ✓       |                       |    | ✓       | ✓           |
| **Questions** | 0  | 0  | 14      | 3                     | 0  | 6       | 14          |
| **Status**    | Not in this quiz | Not in this quiz | Covered | Conceptual only | Not in this quiz | Covered | Contributes |

Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (practical sign-off, not assessed in this quiz)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check