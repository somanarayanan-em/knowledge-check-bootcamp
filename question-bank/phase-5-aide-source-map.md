# Intro to A.I.D.E. Quiz: Source Map (internal tracking)

Internal only. Records where each question in `phase-5-aide.md` comes from, so the training team can check accuracy. Kept out of the quiz file on purpose. Never include it in learner papers.

Source: Deck 7, *Intro to A.I.D.E.* (v8), slides and speaker notes. Slide numbers are positions in the deck as saved. The Crash Course version of the deck was not used.

| Question | Source |
|---|---|
| 1 | Slide 11 and notes ("not a tool, service, library, dependency or CLI ... a folder of markdown files your existing coding agent discovers and follows ... sits beside your source repos"). The quiz says "a set of skills, written as markdown files", combining the deck's wording with the training team's preferred term. Skills, templates and configuration are what the deck says the files hold |
| 2 | Slide 4 ("Not sure how to use a skill? ASK! Open the SKILL.md and ask your assistant to explain. Or ask which skill fits your goal."); slide 16 ("TO RUN: /<skill-name> or just describe the goal"). Replaces an earlier question on why the team built A.I.D.E. rather than adopt another framework, which did not test use of the tool |
| 3 | Slide 5 and notes (frontmatter is the discovery mechanism); slide 8 quiz and answer ("step files and references load only once a skill has been chosen ... a good description matters more than a long procedure") |
| 4 | Slide 6 and notes (skill is a task, AGENTS.md is behaviour); slide 7 and notes (local rule "never force-push") |
| 5 | Slide 16 notes ("Skills hand off to each other by name, at fixed points ... Each hand-off is a named artifact on disk, not a conversation you have to remember. That is what makes it possible to stop halfway and pick up tomorrow."). The quiz says "documents saved in the repository" in place of "artifacts on disk" |
| 6 | Slide 16 notes (create-* paired with review-*); slide 22 ("AI proposes, human disposes"; "Nothing merges itself") |
| 7 | Slide 20 and notes (brownfield route); slide 26 notes ("plausible-but-wrong is the expensive failure") |
| 8 | Slide 50 and notes (quick-dev, three skills); slide 51 and notes (two paths for every change); slide 20 |
| 9 | Slide 26 and notes (analyze-repository dispatcher; generator for uncovered stacks); slide 27 notes (wrong member of a pair "works happily and produces a document nobody wanted"); slide 53 notes (let the dispatcher classify) |
| 10 | Slide 29 and notes (internal docs / Part A land in the source repo; consumer docs / Part B land in the KB; attestation) |
| 11 | Slide 31 and notes (markdown map, own repository, no vector database, no embeddings, nothing to operate, reviewed in PRs); slide 33 (contents) |
| 12 | Slide 34 and notes (navigate-knowledge-base returns the few components with a reason; "read those, not the codebase"; downstream skills use it too); slide 48 quiz |
| 13 | Slide 36 and notes ("A knowledge base nobody maintains is worse than none"; steward and cadence; no pipeline template shipped) |
| 14 | Slide 47 and notes (TDD, AI gate, human gate; execution leaves the tree uncommitted; create-pr "asks twice"; "Nothing reaches a remote without you saying yes"); slide 22 ("Nothing merges itself") |

## Accuracy flags for the training team

- **Bank size.** Cut from 24 to 14 at the training team's request. Removed: install into a workspace, new-joiner setup test, component layout, source control by hand, what a GO means, start-project, the two config files, thin knowledge base, context the code cannot tell, and the feature registry. The bank is now used whole as the quiz.
- **Naming rule relaxed.** This bank names skills and files where the deck does. The other banks do not. The README records this.
- **Skill names.** Q9 and Q12 name `/analyze-repository` and `/navigate-knowledge-base`, as the deck spells them.
- **Slide numbers in notes.** Several speaker notes still refer to older slide numbers. The map cites slide positions as saved.
- **Q2 and Q5 replaced earlier.** Q2 (why the team built A.I.D.E.) and an earlier skill-count question tested background and a number, not understanding or use of the tool. They were replaced with practical questions: how to learn what a skill does, and how a team resumes a flow. The distractors are ours.
- **Q3 reworded.** The stem now asks how the assistant picks a skill from a plain-English request, in the second person. The options were rewritten to match. The distractors are ours.
- **Q6 reworded.** The earlier stem asked what the create and review pairing "shows". It now asks who decides whether the work moves on. Options B and D are ours. "Most stages" follows the slide 16 notes, because the quality stage has five skills.
- **Q8.** The deck does not say a one-line fix must use quick-dev. It says every change goes through quick-dev (simple) or the full path (complex). Option D's reasoning is ours.
- **Q9.** Option B (run all eleven) is our distractor. The deck does not discuss it directly.
- **Q12.** The deck says the navigate skill returns at most seven component files. The question does not use the number, per the slide 34 wording note.
- **Q13 rewritten.** The earlier stem asked why the deck treats a stale knowledge base as a problem. It now asks what the team should do. Options B, C and D are ours. The deck says automation is real work for the team and that no pipeline template ships.
- **Q14.** The deck says execution leaves the tree uncommitted and the PR skill "asks twice more". The question says "asking again" and does not give the number. Option D is ours.
- **Not covered on purpose.** The quality skills in detail (the deck says they are for a follow-up course), the list of the eleven domain skills, mainframe skills, the meta skills list and the exercise brief.
- **Client and internal names.** The slide 14 install location and the exercise application name are left out on purpose.
