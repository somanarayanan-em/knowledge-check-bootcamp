# Solution Design Package Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

- This question bank contains 20 MCQs in five categories of four.
- ***To build a quiz of 5, draw one question from each category.***
- Six reserve questions sit at the end. Use them as swap-ins when building Versions A and B. They are not part of the 20.

---

## Requirements to design, and traceability

**1.** What does the Solution Design Package do for a team, and what tends to go wrong without it?

- A. It records the business goals; without it, the team forgets why the product exists
- B. It lists the test cases; without it, defects reach users
- C. It turns the requirements (the "what") into a technical blueprint (the "how"); without it, developers and AI make ad-hoc decisions that lead to inconsistency and rework
- D. It replaces the requirements once the project starts; without it, the requirements stay vague

**Answer:** C

**Why:** The Solution Design Package is the bridge between requirements and code. It translates what the business needs into how it will be built. Without it, people and AI make decisions on the fly, which leads to inconsistency, hallucinations, rework and integration failures.

**Why not:** A describes the requirements, not the design. B describes testing, which is a different job. D is wrong because design builds on the requirements and never replaces them.

---

**2.** A requirement says: "Each allocation must record who approved it and when." This is a data requirement. Which design decision does it mainly drive?

- A. How information is stored: the database tables and how they relate
- B. How the system copes with heavy use: caching and scaling
- C. Who is allowed to see which screens: access rules
- D. How the system talks to other systems: error formats and contracts

**Answer:** A

**Why:** Data requirements drive the database design: what is stored and how the pieces relate to each other.

**Why not:** B is driven by non-functional requirements such as performance. C is driven by permissions and roles. D is driven by integration requirements.

---

**3.** One requirement says, "Managers can approve or reject allocation requests." The design package covers it in several places: the interfaces between systems, what is stored, who may approve, the screens and the notifications. A reviewer asks why one requirement needs so much. What is the best answer?

- A. The design team added extras that the requirement did not call for
- B. Each of those parts should have been written as its own requirement
- C. AI tends to produce more than it is asked, so the extra parts can be ignored
- D. A single requirement usually has consequences in several parts of the design, and each part needs its own design decision

**Answer:** D

**Why:** One requirement can drive an interface design, a data design, a security rule, a screen design and a notification design. That is why you do not jump straight to code: there are many design decisions between the requirement and the build.

**Why not:** A is wrong because every part traces back to the one requirement. B confuses the "what" with the "how", because those parts are design, not business needs. C blames AI when the spread is normal for any requirement.

---

**4.** Why is it good practice to mark each design section with the requirement it implements, for example "Implements: FR3.1"?

- A. So AI remembers earlier sessions
- B. So every design decision can be traced to a requirement, and anything that cannot be traced can be questioned
- C. So the design can be approved faster
- D. So the requirements can be thrown away once the design is finished

**Answer:** B

**Why:** Tagging makes the link visible. Every design decision points to the requirement it serves, so if a design section cannot name one, you question whether it is needed. It also makes the design easier to check against the requirements.

**Why not:** A confuses tagging with memory, because the documents are the memory. C is not the purpose of tagging. D is wrong because the requirements stay in place and remain the source of every design decision.

---

## Loading context before designing

**5.** You are starting the design stage, and the requirements are already written and saved in the project. What should AI do before any design work starts?

- A. Propose the structure of the design documents
- B. Read the requirements and summarize them back (the project, the users, the functional areas and the non-functional requirements), so you can check the summary
- C. Ask you to explain the business background again from the beginning
- D. Choose the technology for the project

**Answer:** B

**Why:** In design, the context already exists in writing. AI must read it and summarize it before one line of design work starts. If this step is skipped, AI designs for requirements it imagined.

**Why not:** A skips the check, so the structure would rest on an unverified understanding. C wastes effort, because the business context is already in the requirements and you are loading what is written. D is a decision for you to give AI, not one to leave to it.

---

**6.** AI's summary of the requirements covers the project, the users and the functional areas, but it says nothing about the non-functional requirements. What is the best next move?

- A. Carry on, because the gap will show up in the design review
- B. Add the non-functional requirements to the design yourself and skip the re-check
- C. Start again in a new conversation
- D. Have AI re-read the requirements, check specifically for non-functional requirements and flag any real gaps

**Answer:** D

**Why:** The summary is the checkpoint. The omission may be a miss in the summary, or the requirements may genuinely be silent on non-functional needs. Having AI re-read the requirements and check specifically for non-functional requirements tells you which. Correct the summary if it was a miss, or flag the gap if the requirements are silent, then proceed. Non-functional requirements shape the architecture, so a hole here causes problems in the design later.

**Why not:** A lets the gap spread into the design, where it is more expensive to fix. B invents requirements the business never stated, and it skips the check that protects the rest of the work. C throws away context you could have corrected.

---

**7.** In a brownfield project (one that changes an existing system), why is a knowledge base needed before design starts?

- A. So the design is guided by an accurate picture of what is already built, giving the most effective solution for that system
- B. So the business goals that the requirements leave out are recorded in one place, where they can be referred to while designing
- C. So the requirements no longer need to be kept for an existing system, because the knowledge base covers everything needed to design the changes
- D. So the code for the change can be written faster, because AI has already seen how the existing system was built

**Answer:** A

**Why:** The requirements say what the business needs, but not what is already built. AI cannot infer the existing system from the requirements alone. The knowledge base, drawn from the code, gives the team a way to show AI what exists (its technology, architecture, dependencies and patterns), so the design can be guided to the most effective solution for that system. Without it, AI works without understanding what already exists or the impact of the project's changes.

**Why not:** B is wrong because a knowledge base is about code, not business, and business goals stay in the requirements. C is wrong because the requirements still define what has to change. D is wrong because the knowledge base is there to support the design, and this stage is about design, not writing code.

---

**8.** Which statement best describes a knowledge base for an existing system?

- A. A record of business decisions and sign-offs, written once and then archived
- B. A copy of the requirements package, updated whenever the requirements change
- C. A code-derived picture of what the system does (its interfaces, architecture, dependencies and existing patterns), mostly generated from the source code and updated as the code changes
- D. A wish list of the technologies the team would like to use next

**Answer:** C

**Why:** A knowledge base is built mostly by reverse engineering the source code, with extra context added where documentation exists. It must evolve with the solution so it reflects what is actually running.

**Why not:** A describes a decision log. B describes the requirements, which are a different document with a different source. D describes future plans, while a knowledge base describes what exists now.

---

## Technology constraints

**9.** A team gives AI the requirements but says nothing about the technology to use. What is the most likely problem?

- A. AI will refuse to start until the technology is chosen
- B. AI will work out the right technology from the requirements
- C. AI may suggest technology that does not fit: mismatched versions, a needlessly complex setup, or tools the organization does not use
- D. The requirements will have to be rewritten

**Answer:** C

**Why:** AI does not guess your technology correctly. Without constraints, it may propose incompatible library versions, over-complex architectures, patterns that do not fit your infrastructure, or technologies your organization does not use.

**Why not:** A is wrong because AI will carry on and fill the gap with its own choices. B is wrong because requirements describe business needs, not technology. D is wrong because the requirements are fine, and the technology is a design decision.

---

**10.** You are now in solution design. The requirements have been loaded and AI's summary of them has been checked. In a greenfield project, what is the first thing to settle before AI is asked to propose the design structure?

- A. The technology constraints: the tech stack to use, the exact versions of each tool, and what must not be used
- B. The list of design documents and the headings in each one
- C. A knowledge base describing the code of the existing system
- D. The content of the first design section, such as the data design

**Answer:** A

**Why:** In a greenfield project there is no existing system to learn from, so every technology constraint is a decision the team makes and writes down. Only after the constraints are set should the structure be proposed. That means naming the tech stack (the frontend, backend, database, infrastructure, authentication and standards to follow), pinning the exact version of each tool, and stating what must not be used. You may not have every answer, and "we do not know the hosting platform yet, but it will not be X" is a valid exclusion.

**Why not:** B is the next step, because the structure is proposed once the constraints are set. C applies to brownfield, since a greenfield project has no existing code to describe. D comes later, because content is filled in only after the structure is agreed.

---

**11.** Which is the best way to give AI its technology constraints?

- A. "Use modern, popular technologies."
- B. Describe the business goals and let AI choose the tools
- C. List the technology names without versions, so AI picks the latest
- D. Name each technology with its exact version, say what must not be used, and state the overall approach (for example, one application rather than many small services)

**Answer:** D

**Why:** Be specific and comprehensive. Pin versions, state exclusions and be explicit about the architecture approach. Exclusions stop AI from overreaching.

**Why not:** A is vague, so AI fills the gaps with its own choices. B leaves the choice to AI, which is what constraints are meant to prevent. C leaves out versions, which invites incompatibility.

---

**12.** How do technology constraints come about in a new project (greenfield) compared with an existing system (brownfield)?

- A. Greenfield: discovered from the code. Brownfield: chosen by the team.
- B. Greenfield: there is no code to learn from, so the team decides and writes it down. Brownfield: the existing code largely decides, so you discover what is in use and pin it.
- C. In both cases they are worked out from the requirements.
- D. In both cases they are left to AI's defaults.

**Answer:** B

**Why:** In greenfield, every constraint is a decision, and silence is the risk, because unstated constraints are where AI overreaches. In brownfield, most constraints already exist, so you discover them (from build files, dependency lists and configuration), confirm the versions in use and pin them. New choices are only for where you go beyond the current stack.

**Why not:** A has the two the wrong way round. C is wrong because requirements stay free of technology, which is why a stack change does not reopen business sign-off. D is the risk, not a method.

---

## What is in the package, and how to build it

**13.** The team needs to document the user interface. Which document in the Solution Design Package does it belong in?

- A. Solution overview: the executive view, business context and scope
- B. Backend design: the service layer, the domain model and error handling
- C. Solution architecture: system diagrams and how components fit together
- D. Frontend design: the UI structure, state management and navigation

**Answer:** D

**Why:** Frontend design covers the UI architecture, state management and routing: how the screens are structured, how users move between them, and how the application keeps track of what is shown. Each document in the package has a defined job, which makes it easy to find and easy to review.

**Why not:** A gives the high-level view for business readers. B covers what happens behind the screens. C shows how the major parts fit together, not the detail of one part.

---

**14.** A teammate pastes the full list of possible design documents (from the overview through to testing strategy) into AI and says, "Create all of these." What is the main risk?

- A. AI will refuse the request, because the list is too long for it to handle in one go
- B. Documents may contain decisions that were never agreed and that could clash with the organization's requirements and policies
- C. The package will be more complete, because AI is given every possible option to work from
- D. Version control will not be able to store that many files in a single project

**Answer:** B

**Why:** Not all projects need all documents, so scope the package to what is relevant. Asking for every document at once means decisions get made on topics nobody asked about, such as security, integrations or deployment, and these may not suit the organization's requirements and policies. Ask AI to propose which documents are necessary, then confirm the list before anything is written.

**Why not:** A is wrong because AI will attempt it, and the issue is the quality of the result. C is the common belief, but a big request produces documents the project does not need and decisions nobody agreed, not a more complete package. D is untrue, because version control handles many files easily.

---

**15.** The team needs to document how a request moves through its stages (Submitted → Approved, or Submitted → Rejected) and the rules that govern each move. Which document in the Solution Design Package does it belong in?

- A. Workflow and business rules design: the stages an item moves through and what triggers each move
- B. Integration design: how the system exchanges information with external systems
- C. Dashboard and reporting design: the metrics and visualizations people will see
- D. Deployment and DevOps design: the environments and release process

**Answer:** A

**Why:** Workflow and business rules design covers state machines and automation: the stages something moves through and the rules for each move. It follows from the business rules in the requirements, which drive validation logic, state machines and workflows. Each document in the package has a defined job, which makes it easy to find and easy to review.

**Why not:** B covers how the system connects to other systems. C covers how information is shown as metrics and charts. D covers how the system is released and run.

---

**16.** Halfway through the design, the team decides to use a different version of one of its tools. What is the best way to handle it?

- A. Start the design again from the requirements, because the technology is part of the business sign-off
- B. Leave the design documents as they are and note the change for the build stage to pick up
- C. Ask AI what the change affects in the design, then update those documents, leaving the requirements as they are
- D. Ask AI to switch to the new version everywhere, and trust it to catch every place it applies

**Answer:** C

**Why:** Design is easy to revise. Asking AI for the impact of the change shows which documents are affected, and the team then updates them. Technology decisions live in the solution design and not in the requirements, so a stack change does not reopen business sign-off.

**Why not:** A confuses technology with business needs, because the requirements stay stable when the technology changes. B leaves the documents out of step with each other, and the build would then work from outdated decisions. D skips the impact check, and a change made everywhere without checking can leave some documents inconsistent.

---

## Design pitfalls and judgment

**17.** You asked AI for a solution design, and it starts writing code. What should you do?

- A. Stop it and restate the instruction: "Design only. Do not write code." Start a new chat if needed.
- B. Let it finish, then delete the code afterwards
- C. Accept it, because code is the most precise form of design
- D. Switch to a larger model

**Answer:** A

**Why:** AI often does more than it is asked. Design only means design only. Stop it, restate the scope clearly, and start a fresh conversation if it keeps going.

**Why not:** B lets AI spend effort and context outside the task. C mixes up stages: code belongs to implementation, which comes after design. D blames the model when the cause is how AI behaves.

---

**18.** A small tool will be used by about 100 people. AI proposes an architecture of many separate services, each deployed on its own. What is the best response?

- A. Accept it, because a more scalable design is always better
- B. Ask AI to add more detail about each service
- C. Ask AI to switch to the newest technology
- D. Challenge it: ask whether this complexity is necessary for the scale of the requirements

**Answer:** D

**Why:** Over-engineering is a pitfall. Ask AI directly whether the approach is justified by what the requirements need. For a small tool, simpler is better.

**Why not:** A treats scale as free, but complexity has costs in effort and maintenance. B adds detail to a design that is already too big. C changes the technology without addressing the real problem.

---

**19.** A reviewer finds that one design document specifies version 17 of a tool and another document specifies version 18 of the same tool. What is the likely cause, and how is it prevented?

- A. AI made a copying mistake, so regenerate all the documents
- B. This is normal, because each document is independent
- C. The technology was not set and pinned in one place first, so set the constraints before scaffolding
- D. The requirements were ambiguous, so rewrite them

**Answer:** C

**Why:** Inconsistent technology across documents is a design pitfall. When constraints are stated up front, with versions pinned, every document works from the same decisions.

**Why not:** A treats a symptom and not the cause, and it would happen again. B is wrong, because documents must agree with each other. D is wrong because versions are a design decision, not a business need.

---

**20.** A team plans to leave security design until the end, after everything else is designed. Why is this a problem?

- A. Security is only a testing concern, not a design concern
- B. Security decisions (who can do what, what data is protected) shape other parts of the design, so leaving them last risks gaps and rework
- C. AI cannot design security
- D. A security design is too small to be a separate document

**Answer:** B

**Why:** Security as an afterthought is a design pitfall. Design security early, not last, because it affects data, interfaces and screens. Building the security pieces can come later, in implementation, as long as they were designed up front.

**Why not:** A is wrong because security needs design decisions before anything is built. C is untrue. D is wrong because the size of a document is not the test of whether it is needed.

---

## Reserve questions

Use these as swap-ins when building Versions A and B. They are not in the traceability matrix below.

**R-1.** You join a project partway through, and the requirements were written by another team. While designing, you notice a gap: the requirements do not say what happens to open requests when a user is deactivated. What is the best response?

- A. Quietly rewrite the requirements to fill the gap
- B. Design from what is written, and note the gap clearly so it can be resolved, without silently expanding the scope or rewriting the requirements
- C. Ignore the gap and hope it does not matter
- D. Stop all work until the other team rewrites their requirements

**Answer:** B

**Why:** The artifacts are the memory. You design from what the previous team wrote and do not rewrite it. If a gap is real, record it so the right people can decide.

**Why not:** A changes the business statement without sign-off. C leaves a known risk unrecorded. D halts work that can continue, and the gap can be noted in the meantime.

---

**R-2.** AI's design includes a login screen and a role system, but the requirements do not mention either. What is the best response?

- A. Keep them, because most systems need them
- B. Keep them, but label them as optional
- C. Remove them only if they cause problems later
- D. Ask which requirement each part implements, and remove anything that cannot be traced to one

**Answer:** D

**Why:** If a design cannot trace to a requirement, question whether it is needed. The exception is a design that serves a stated non-functional need such as stability or recovery, and if you cannot name one, it does not belong.

**Why not:** A assumes needs the business never stated. B keeps untraced work in the package. C waits for a failure instead of checking against the requirements.

---

**R-3.** On a training slide, a team sees an example technology setup. They want to adopt it for their own project. What is the better approach?

- A. Treat it as an example of how specific to be, then choose technology to suit your own team skills, standards and hosting, and pin the versions
- B. Adopt it as is, because the training deck is the authority
- C. Ask AI to pick a setup for them
- D. Use it, but leave the versions unpinned so AI can update them

**Answer:** A

**Why:** The example shows the level of detail needed, not the answer. Constraints come from your own context: team skills, organizational standards, licensing and hosting.

**Why not:** B treats an example as a requirement. C hands the decision to AI, which is the risk. D leaves out version pinning, which prevents incompatibility.

---

**R-4.** A team's design covers the screens, the data and the interfaces, but nothing about logging, deployment or recovery from errors. What is the best action?

- A. Leave it, because those are only operations concerns
- B. Add it after the product goes live
- C. Include the operational concerns (observability, deployment and error recovery) in the design where they are relevant
- D. Leave AI to decide during the build

**Answer:** C

**Why:** Forgetting operational concerns is a design pitfall. Include observability, deployment and error recovery, scoped to what the project needs.

**Why not:** A treats them as someone else's problem. B is too late for decisions that affect the design. D hands design decisions to the build stage, where they are harder to review.

---

**R-5.** You ask AI, "Design the whole system, every layer, in detail," and the answer is shallow. What is the best next step?

- A. Narrow the request to one specific chunk (for example, the stored data for the main entities), verify it, then move to the next
- B. Repeat the same large request
- C. Switch to a bigger model and ask the same question
- D. Accept the shallow answer and fill in the detail during the build

**Answer:** A

**Why:** Going too broad loses detail. The chunk-by-chunk discipline applies here too: smaller requests give more depth and are easier to verify. Even a large model stays shallow if asked for everything at once.

**Why not:** B repeats the problem. C changes the model but not the request. D pushes design decisions into the build, which is what design is meant to prevent.

---

**R-6.** Why is it better to split the design package into separate, clearly named files (such as API design and database design) than to keep one large file?

- A. Design files must match the number of requirement files
- B. AI can only read one short file at a time
- C. Each file can then be approved by a different business owner
- D. Later, when the team works on one area, AI can open just the relevant file instead of searching through everything, and each file is easier to review

**Answer:** D

**Why:** A file named for its content is easy to find. When the team later builds the interfaces, AI can open API design and not have to hunt through the whole package. Smaller files are also easier to check.

**Why not:** A is not a rule. B is untrue, because AI can read many files, but it works better when it can go straight to the right one. C is not the reason, because file structure is about findability and review.

---

## Training requirements covered

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: covered for the solution design stage
- **R2** Hands-on execution of a stage: partly (tests knowing how to run the stage, not that the Champion drove it)
- **R4** Knowledge base setup: conceptual touchpoint only (Q7 and Q8 cover what a knowledge base is and why it matters, not setup steps)
- **R6** Failure-point recognition: covered for the solution design stage
- **R7** Knowledge check record: contributes
- **R3, R5**: not in this quiz (R3 is deferred; R5 needs source material)

## Training requirement traceability matrix


| Question      | R1      | R2     | R3               | R4               | R5               | R6      | R7          |
| ------------- | ------- | ------ | ---------------- | ---------------- | ---------------- | ------- | ----------- |
| 1             | ✓       |        |                  |                  |                  |         | ✓           |
| 2             | ✓       |        |                  |                  |                  |         | ✓           |
| 3             | ✓       |        |                  |                  |                  |         | ✓           |
| 4             |         | ✓      |                  |                  |                  |         | ✓           |
| 5             |         | ✓      |                  |                  |                  | ✓       | ✓           |
| 6             |         |        |                  |                  |                  | ✓       | ✓           |
| 7             | ✓       |        |                  | c                |                  |         | ✓           |
| 8             | ✓       |        |                  | c                |                  |         | ✓           |
| 9             |         |        |                  |                  |                  | ✓       | ✓           |
| 10            |         | ✓      |                  |                  |                  | ✓       | ✓           |
| 11            |         | ✓      |                  |                  |                  |         | ✓           |
| 12            |         | ✓      |                  |                  |                  |         | ✓           |
| 13            | ✓       |        |                  |                  |                  |         | ✓           |
| 14            |         |        |                  |                  |                  | ✓       | ✓           |
| 15            | ✓       |        |                  |                  |                  |         | ✓           |
| 16            |         | ✓      |                  |                  |                  |         | ✓           |
| 17            |         |        |                  |                  |                  | ✓       | ✓           |
| 18            |         |        |                  |                  |                  | ✓       | ✓           |
| 19            |         |        |                  |                  |                  | ✓       | ✓           |
| 20            |         |        |                  |                  |                  | ✓       | ✓           |
| **Questions** | 7       | 6      | 0                | 0 (2 conceptual) | 0                | 9       | 20          |
| **Status**    | Covered | Partly | Not in this quiz | Conceptual only  | Not in this quiz | Covered | Contributes |


Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (knowledge side only)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup (c = conceptual touchpoint only)
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check

