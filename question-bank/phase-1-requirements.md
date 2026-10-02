# Requirements Package Quiz Bank

Trainer copy: contains answers and explanations. Do not share with Champions.

- This question bank contains 20 MCQs in five categories of four.
- ***To build a quiz of 5, draw one question from each category.***

---

## Requirements vs solution design

**1.** Which best describes what the Requirements Package captures?

- A. The technology choices and architecture the team will build with
- B. Stable business logic: the "what" and "why", not the "how"
- C. The screens and layouts users will see
- D. The plan for building and testing the product

**Answer:** B

**Why:** The Requirements Package holds stable business logic: what the product must do and why. It stays valid whatever technology is chosen.

**Why not:** A is technology and architecture, which is solution design. C is also solution design, because screens and layouts can change without the business need changing. D belongs to a later stage.

---

**2.** A team is arguing about whether a statement belongs in the requirements or in the solution design. Which is the most reliable sign that it belongs in the requirements?

- A. It is short enough to fit in a single sentence
- B. A developer needs it before they can start coding
- C. It would still be true if the team switched frameworks and redesigned every screen
- D. It describes something the user can see on screen

**Answer:** C

**Why:** Requirements hold what stays stable regardless of technology or presentation. If a statement would survive a change of framework or a redesign, it is a business need. If it would change, it is solution design.

**Why not:** A says nothing about stability. B fits design as well, since developers need design decisions before coding. D describes screens, which are solution design.

---

**3.** A team is writing requirements for an insurance product. Which statement belongs in the Requirements Package?

- A. "Applicants over 80 are not eligible for this insurance."
- B. "Eligibility is worked out by subtracting date of birth from the current year and comparing the result to 80."
- C. "If the eligibility check fails, the service returns an error in JSON."
- D. "A red banner appears on the form when an applicant is not eligible."

**Answer:** A

**Why:** This is a business rule. It would stay true if the framework, the screens or the colours changed.

**Why not:** B is how the rule is calculated, which is solution. C is an API contract. D is a screen design.

---

**4.** Non-functional requirements are part of the package, but only when they reflect a real business need. Which of these belongs in the Requirements Package?

- A. "Add a Redis cache in front of the database to handle peak load."
- B. "Run the application in three containers behind a load balancer."
- C. "Use a message queue so report requests are handled one at a time."
- D. "The application must meet accessibility standards (WCAG), so people can use it with a screen reader or with a keyboard alone."

**Answer:** D

**Why:** It states a standard the product must meet without saying how to build it. Accessibility is a real business need, whether it comes from users or from legal obligations, and it holds whatever technology is used.

**Why not:** A, B and C are technology and architecture choices. However sensible they are, they are decisions for solution design.

---

## Why documents matter, and how AI behaves

**5.** Why do written requirements documents matter so much when you work with AI?

- A. They are the only record of who changed what
- B. AI can forget earlier conversations, while documents keep your context and work persistent and shareable across sessions and people
- C. They make AI generate code faster in later phases
- D. They replace the need for a solution design

**Answer:** B

**Why:** AI does not remember between conversations. Written documents are what let the next session, phase or person pick up where things were left.

**Why not:** A describes version history, which is a different job. C is not what the documents are for. D is wrong because requirements say what to build, and design still has to say how.

---

**6.** You return to an existing project and open a fresh AI session. What should you have AI do first?

- A. Have AI read the existing documents, summarize them and verify understanding
- B. Regenerate the documents so they are up to date
- C. Continue from the last chat, because AI will recall it
- D. Propose any requirements it thinks are missing

**Answer:** A

**Why:** The documents are the project's persistent memory. Having AI read them, summarize them and confirm it understood re-establishes the context before any new work starts.

**Why not:** B throws away work that already exists. C ignores that AI does not remember earlier sessions. D adds new material before the existing material is even loaded.

---

**7.** You ask AI to "put together the workflow" for the requirements, and it starts producing UI mockups. What is the best reading and response?

- A. Let it finish, then move the mockups into a separate folder for the design stage
- B. Mockups are a normal part of a requirements package, so let it finish
- C. The model is too small, so switch to a larger one
- D. AI often does more than asked, so stop it and restate: requirements only, no mockups

**Answer:** D

**Why:** AI tends to do more than it is asked, including adding mockups. Stop it and restate what is in and out of scope.

**Why not:** A lets AI keep working outside the requirements and spends effort on design too early. B is wrong because mockups are solution design. C blames the model when the cause is how AI behaves.

---

**8.** You ask AI, "Tell me everything about the employee tool." The answer is broad and shallow. What is the best next step?

- A. Repeat the same question until the answer gets longer
- B. Paste the answer back and ask AI to confirm it is correct
- C. Make the question more specific, so AI knows exactly what you want covered
- D. Start a new conversation and ask the same question again

**Answer:** C

**Why:** Broad questions get shallow answers, and specific questions get depth. Being clear about what you want gives AI something concrete to work with.

**Why not:** A and D keep the same broad question, so the answer stays shallow. B is a useful check, but it does not fix the shallowness.

---

## The workflow and verification

**9.** A team gave AI the project background and business goals, then immediately asked it to propose the document structure. What should they have done first?

- A. Start a new conversation
- B. Verify that AI has understood the project
- C. Commit the work so far
- D. Choose the technology stack

**Answer:** B

**Why:** Before building on the context, AI should summarize what it understood so any misunderstanding is caught early. Everything that follows depends on it.

**Why not:** A isn't needed here, because nothing has gone wrong with the conversation. C is a regular habit, but it doesn't protect the structure. D is a solution-design decision and doesn't belong in requirements.

---

**10.** Why ask AI to summarize its understanding before it generates content?

- A. To confirm which technology AI should use
- B. To get a first draft of the final document
- C. To make AI remember the project permanently
- D. To catch a misunderstanding before it turns into wasted work

**Answer:** D

**Why:** Checking understanding first prevents output that misses your intent, whole sections being redone, and effort spent on a misunderstanding. The longer a misunderstanding lives, the more expensive it is to fix.

**Why not:** A is wrong because technology is a solution-design decision, and the summary is about understanding the project. B confuses a summary with a draft. C is wrong because AI does not remember between sessions.

---

**11.** You are setting context at the start of the requirements stage. Which opening message is best?

- A. The project background, business goals and expected product: what you are building and why
- B. The programming language, framework and database you plan to use
- C. A request to produce the full requirements package straight away
- D. The list of every document the package could contain

**Answer:** A

**Why:** At the start, give the project background, the business goals and the expected product. Stick to business needs: what you are building and why.

**Why not:** B is technology, which does not belong in requirements. C skips verification and scaffolding. D invites AI to fill every heading, which leads it to invent content.

---

**12.** AI's summary of the project leaves out one of your user groups. What is the best next move?

- A. Carry on; the gap will show up when the content is reviewed
- B. Start again in a new conversation
- C. Add the missing group yourself in the final document and skip the re-check
- D. Correct the summary and have AI restate it, then continue once it is right

**Answer:** D

**Why:** AI repeating its understanding back is where gaps get caught, and it can take a round or two. Correct it, have it restate, and proceed once it is right.

**Why not:** A lets the misunderstanding spread into the content, which gets more expensive to fix. B throws away context you could have corrected. C skips the check that protects the rest of the work.

---

## Scaffolding before content

**13.** Instead of asking AI to "create the requirements package" in one go, what is the better first request?

- A. Ask it to propose the document structure
- B. Ask it to write the executive summary
- C. Give it a template and tell it to fill every heading
- D. Ask it to start with the functional requirements

**Answer:** A

**Why:** Have AI propose the structure, refine it until it is right, lock it, and then fill in the content section by section.

**Why not:** B and D start writing content before the structure is agreed. C is the "do all of this" approach that makes AI invent content.

---

**14.** A team has agreed the structure with AI and now asks it to create the files, before any content is written. What should exist afterwards?

- A. A complete first draft, to be edited afterwards
- B. A summary of what AI understood
- C. Headers and placeholder files, with no content
- D. A list of open questions for the business to answer

**Answer:** C

**Why:** Scaffolding locks the structure before content exists, so the content can then be filled in and checked one section at a time.

**Why not:** A is the later content step. B is the earlier verify step. D can be useful, but it is a different task and not what creating the scaffolding produces.

---

**15.** A teammate lists every section they can think of for the requirements package and tells AI to write all of them in one go. What is the main risk?

- A. AI will refuse the request, because it is too long to process
- B. The content will be shallow and high-level, and difficult to verify
- C. The result will be more thorough, because AI sees the whole picture at once

**Answer:** B

**Why:** Asking for everything at once produces shallow, high-level content that misses detail, and there is too much to check properly. Smaller requests give more depth and are easier to verify.

**Why not:** A is wrong because AI will attempt the request, and the problem is the quality of what comes back. C is a common belief, but a big request gets a shallow answer, not a thorough one.

---

**16.** AI has put all the requirements into one large file. Why is it better to split them into clearly named files, such as one for business rules?

- A. Smaller files look more professional in a review
- B. Version control cannot store a file that large
- C. Clearly named files are easier to review, and cheaper and quicker for AI to search later

**Answer:** C

**Why:** One giant file is harder to review, and later AI spends effort hunting for what it needs. A file named business rules is easy to find, which makes it quicker and cheaper for AI to work with.

**Why not:** A is about appearance, not usefulness. B is untrue: version control stores large text files without trouble.

---

## Pitfalls and practical habits

**17.** Why is it worth committing your work frequently when AI is helping you write documents?

- A. So AI can remember earlier sessions
- B. So your progress is saved deliberately and you can roll back if something goes wrong
- C. Because AI can only write one section per session
- D. To get the package approved sooner

**Answer:** B

**Why:** Without commits, a lost context or a session timeout can lose your work. Committing saves progress deliberately, so you can roll back.

**Why not:** A confuses version control with memory. The documents are the memory. C is untrue, since AI can write several sections in a session. D confuses saving work with approving it.

---

**18.** You finish one task with AI and start a different one. What is the better practice?

- A. Keep the same conversation so AI retains all the context
- B. Ask AI to forget the previous task before starting
- C. Switch to a different AI model
- D. Start a new conversation so unwanted context does not carry over

**Answer:** D

**Why:** A new task is best started in a new conversation, so context from the old one does not carry over unwanted.

**Why not:** A is the opposite of good practice. B is not a reliable way to clear context. C does not address the problem.

---

**19.** A reviewer notices the requirements say "built with a React front end and a PostgreSQL database." What problem does this cause?

- A. The requirements are no longer technology agnostic, so they have to be changed every time the technology changes
- B. Nothing, because the team needs to know the technology from the start
- C. The requirements will be harder for AI to read

**Answer:** A

**Why:** Requirements should be technology agnostic, meaning they do not depend on any particular technology. Once a technology is written in, every technology change means the requirements have to be modified too.

**Why not:** B is a common view, but technology is decided in solution design, so the requirements stay stable without it. C is not the issue, because AI reads technical terms without difficulty.

---

**20.** AI returns a clean, confident section on business rules. What is the right approach?

- A. Accept it, since confident output usually means AI understood the business
- B. Ask the same AI to approve its own work, then move on
- C. Review it with the same scrutiny as human work: AI can miss edge cases and make assumptions

**Answer:** C

**Why:** AI sounds confident but does not truly understand your business. Review its output with the same scrutiny you would give human work.

**Why not:** A is the trap: confidence is not understanding. B relies on the same source that may have made the mistake.

---

## Training requirements covered

Requirement numbers follow [00-scope.md](../00-scope.md).

- **R1** End-to-end process literacy: covered for the requirements stage
- **R2** Hands-on execution of a stage: not in this quiz (it is assessed by practical sign-off, and this quiz tests knowledge only)
- **R6** Failure-point recognition: covered for the requirements stage
- **R7** Knowledge check record: contributes
- **R3, R4, R5**: not in this quiz

## Training requirement traceability matrix

| Question | R1 | R2 | R3 | R4 | R5 | R6 | R7 |
|---|---|---|---|---|---|---|---|
| 1 | ✓ | | | | | | ✓ |
| 2 | ✓ | | | | | | ✓ |
| 3 | ✓ | | | | | | ✓ |
| 4 | ✓ | | | | | | ✓ |
| 5 | ✓ | | | | | | ✓ |
| 6 | ✓ | | | | | | ✓ |
| 7 | | | | | | ✓ | ✓ |
| 8 | | | | | | ✓ | ✓ |
| 9 | | | | | | ✓ | ✓ |
| 10 | ✓ | | | | | | ✓ |
| 11 | ✓ | | | | | | ✓ |
| 12 | | | | | | ✓ | ✓ |
| 13 | ✓ | | | | | | ✓ |
| 14 | ✓ | | | | | | ✓ |
| 15 | | | | | | ✓ | ✓ |
| 16 | | | | | | ✓ | ✓ |
| 17 | | | | | | ✓ | ✓ |
| 18 | | | | | | ✓ | ✓ |
| 19 | | | | | | ✓ | ✓ |
| 20 | | | | | | ✓ | ✓ |
| **Questions** | 10 | 0 | 0 | 0 | 0 | 10 | 20 |
| **Status** | Covered | Not in this quiz | Not in this quiz | Not in this quiz | Not in this quiz | Covered | Contributes |

Key:

- **R1** End-to-end process literacy
- **R2** Hands-on execution of at least one stage (practical sign-off, not assessed in this quiz)
- **R3** AIDE Skills Framework fluency
- **R4** Knowledge Base / context repository setup
- **R5** Operating model and role literacy
- **R6** Failure-point recognition
- **R7** Demonstrated via knowledge check
