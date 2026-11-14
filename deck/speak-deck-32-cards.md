# The Speak Software Deck — 32 cards

Thirty-two cards of code discipline for people who will never hand-write code:
you describe, an agent builds, and you decide whether it's true. Distilled from
*Speak Software: Programming at the Natural-Language Layer*. Sections:
**The Department** (5), **Speak** (5), **Verify** (5), **Guard** (8),
**Taste** (4), **Run** (5).

One card type: why it goes wrong, the move, the line.

**You describe. It builds. You decide whether it's true.**

---

## THE DEPARTMENT · One agent, promoted three times

### 01 · The intern
**Why it goes wrong:** The agent announces, in fluent confident prose, that the thing it just made works — when it does not.

**The move:** Treat one agent as an intern who has read everything ever published, works in seconds, costs pennies, never sleeps — and has zero judgement about your business, no memory beyond this conversation, and no shame about inventing facts.

*"Confidence and correctness are different qualities. The intern has only the first."*

### 02 · The repository rule
**Why it goes wrong:** Work happens in chats, and chats evaporate. What isn't recorded cannot be checked, handed over, or resumed.

**The move:** A repository is the department's filing cabinet. A manager needs four things: a repository, a way to brief, a way to check, and a record of decisions.

*"If it is not in the repository, it does not exist."*

### 03 · The specialist
**Why it goes wrong:** Every session re-explains the same preferences, standards and decisions — a tax paid in every chat, forever.

**The move:** A folder of markdown instructions in the repository, read at the start of every session: standards, decisions, the never-list. AGENTS.md is the front door. One topic, one file, one ruling. When behaviour is wrong, fix the file, not the agent.

*"Re-explaining is the tax. The context folder abolishes it."*

### 04 · The filing cabinet
**Why it goes wrong:** Skills kept in an agent's memory, or in one person's prompting habits, are favours that expire.

**The move:** One skill, one folder: when to use it, inputs, procedure, never, done means. Precision belongs in scripts; judgement belongs in the markdown. And appoint a librarian: once a quarter, read the whole cabinet, because skills drift.

*"The most sophisticated AI orchestration is a well-organised folder."*

### 05 · The mini CEO's four duties
**Why it goes wrong:** The job feels like it should be reading every line the department produces. At AI volume that was always a fantasy.

**The move:** Set the standard before the work. Build systems that enforce the standard. Judge the results — evidence, not code. Own the outcomes, including when the department is out of its depth. Notice what is missing from that list: heroics.

*"Delegation is not absolution."*

---

## SPEAK · Specification is authorship

### 06 · The spec is the program
**Why it goes wrong:** The brief lives in a conversation, so the real program is the chat history — which no one can rerun.

**The move:** Close the gaps in a written spec. Test it with the replication test: would a stranger, with only this document, produce the same thing? If the answer depends on the conversation you had before the document, the document is not the program. The conversation was.

*"Prompting is improvisation. Specification is authorship."*

### 07 · Done means
**Why it goes wrong:** "Done" left undefined gets defined by whoever is asked — usually the agent, optimistically.

**The move:** SPEC.md carries a "done means" section written as runnable checkboxes, each checkable by a specific action. Words like nice, clean, user-friendly and robust are not done; they are wishes.

*"Done is undefined until it is runnable."*

### 08 · The hostile read
**Why it goes wrong:** Your own spec reads clearly to you because you have the conversation in your head.

**The move:** Read your spec hunting for the word "it" and any word you would have to gesture at to explain. Every one is a gap. Replace it with the example that would settle a disagreement.

*"Every gesture-word is a gap."*

### 09 · Wishes into checks
**Why it goes wrong:** "Should handle bad input" feels like a requirement, but nothing can pass or fail it.

**The move:** Rewrite each wish as an observable check: "Submitting an empty form shows an error and nothing is sent." The whole discipline of this deck is turning wishes into checks.

*"The whole discipline is turning wishes into checks."*

### 10 · What you said, what you meant
**Why it goes wrong:** The agent takes the brief literally, and literally is never what you meant. A vague brief run three times produces three different products.

**The move:** Write the spec first, then brief. The AI knows what you said; the spec is where you say what you meant.

*"The AI knows what you said. It does not know what you meant."*

---

## VERIFY · Trust is fine; trust is not verification

### 11 · The demo illusion
**Why it goes wrong:** "It works" — one path through the software, walked once, by the person who already knows where the stepping stones are.

**The move:** Software is done when the paths you never imagined have been tried, not when one path works.

*"'It works' is the beginning of the sentence, not the end."*

### 12 · Receipts
**Why it goes wrong:** The agent reports success in the same confident voice whether or not the thing works.

**The move:** Demand three-part receipts for every acceptance item: the exact command run, the exact output observed, and PASS or FAIL against the checklist. No summaries. Nothing marked PASS that was not actually run in the conversation.

*"The explanation is not the evidence."*

### 13 · Check one at random
**Why it goes wrong:** The agent will sometimes report a pass that is not real — and a report you spot-check occasionally keeps every report honest.

**The move:** Pick one receipt at random and rerun the command yourself, every session. The spot-check is cheap; the habit is the control.

*"Check one at random. Every time."*

### 14 · The fake test
**Why it goes wrong:** The agent's checks can be wrong in the agent's favour: too few cases, a fake-defeatable comparison, an expected value copied from the program's output instead of the spec.

**The move:** Ask of every check: would it still pass if the product were replaced with a hardcoded fake that prints the expected answers? Rewrite any check that a fake could defeat so it tests the real behaviour.

*"A check that a fake could pass is checking nothing."*

### 15 · "It sounds right"
**Why it goes wrong:** Fluency and accuracy are different axes, and fluency is the one that gets trusted.

**The move:** Trust first — trusting is cheap. Verify always — confidence is not evidence. Run it on a known input; explain how it works in your own words; poke an edge case the agent did not mention.

*"'It sounds right' is the most expensive sentence in AI-assisted work."*

---

## GUARD · The blast radius and the five gates

### 16 · The blast radius
**Why it goes wrong:** Process gets decided by enthusiasm at the start and regret at the end, instead of by two questions.

**The move:** Ask: what is the blast radius if this breaks silently at the worst moment — and how long will it live? Low stakes, short life: check the output and vibe on. Anything real users touch, that stores data, that someone depends on: reviewed, tested, explained. No black boxes.

*"Radius, not language or framework, decides how much process you owe."*

### 17 · Managed vibe coding
**Why it goes wrong:** Vibe coding gets treated as either a sin or a lifestyle, when it is a gear selection.

**The move:** Vibe coding is legitimate for prototypes with a small blast radius. Production code written by AI gets a higher bar than human code — it arrives with no context, so it must prove itself entirely through checks — met with guardrails, not heroics.

*"Vibe coding is one gear in a car that also has brakes, mirrors, and a licence."*

### 18 · The five gates
**Why it goes wrong:** You cannot read every line the department writes, so quality depends on stamina — and stamina loses.

**The move:** Every change passes the same five gates in the same order, whether you made it or the agent did: style and obvious errors, behaviour tests, a coverage floor, a forgotten-promises sweep, and a change-size budget.

*"You cannot read every line. You can refuse to ship without a gate."*

### 19 · Commission the gate
**Why it goes wrong:** A gate built by the agent that nobody can explain gets silently disabled the first time it inconveniences anyone — which is slop defending itself.

**The move:** Have the agent build the gate script from your spec, then read it once: you should be able to explain every gate in one sentence. If not, send it back — "explain each gate, then simplify."

*"A gate nobody understands gets disabled."*

### 20 · Tune the budget, keep the gate
**Why it goes wrong:** The thresholds (80% coverage, five TODOs, 400 changed lines) are starting points — and the first emergency argues them down quietly.

**The move:** Tighten thresholds when the department earns it. Never widen them silently to let one change through; if it must be done, it happens in a commit that says so.

*"Widening the gate to pass a change is the exact move this deck exists to prevent."*

### 21 · The flight recorder
**Why it goes wrong:** Fear of breaking things keeps the department moving in half-steps, and the fear never gets tested.

**The move:** Commit, branch, revert — three moves. One policy: if you can describe the change in one sentence, commit it in one sentence; if you cannot, split it. Run the fire drill until "we can always go back" is something you believe, because you have personally done it.

*"One wrong move ruins nothing, if everything is recorded."*

### 22 · The three secrets
**Why it goes wrong:** Credentials, personal data and marked-confidential material enter prompts one rushed paste at a time.

**The move:** Three categories never enter any prompt. Redact first, then paste — no blast-radius argument rescues them. And a key that was ever committed gets removed from history, not just deleted from the file. An unused key is an unlocked door: retire access on handover.

*"An unused key is an unlocked door."*

### 23 · Slopsquatting
**Why it goes wrong:** The agent suggests a package name with total confidence — and a fake package may be squatting on exactly that name.

**The move:** Before installing anything the agent suggested, look the package up in the official registry yourself. Vet every new dependency: maintainer, last release, licence, exact-name check. Fewer dependencies is better.

*"The agent's spelling is not evidence."*

---

## TASTE · The part that moved up the ladder

### 24 · The taste test
**Why it goes wrong:** Two builds can both work, both pass every check, and differ completely in whether a human would enjoy using them. "Best" is not objective.

**The move:** Taste is the judgement that one good option fits your situation better than another good option. The agent enumerates trade-offs fluently; it cannot know your client phones support at 11pm. That judgement, held and defended, is the deliverable.

*"'Best' is not objective. That is precisely why they need you."*

### 25 · CRITIQUE.md
**Why it goes wrong:** Preferences stay verbal, so they die with the conversation and the nephew's version wins by default.

**The move:** Keep CRITIQUE.md: position, why, what you gave up, what would change your mind. Every entry must be arguable — a reasonable person could disagree. The difference between you and the nephew is the file.

*"Take responsibility for a position, in writing, with reasons that survive your absence."*

### 26 · The four standing questions
**Why it goes wrong:** At every fork, the agent's reasoning gets adopted because it is fluent and present.

**The move:** Ask four questions of every version: what is each optimising for; who will maintain it and what do they know; what does each do when the input is strange; what does it cost to change later?

*"Delegate the menu. Keep the choosing."*

### 27 · The last 20%
**Why it goes wrong:** "It's basically done — just make it feel right" is where every practitioner smiles, because polish is the part that was never typing.

**The move:** Directing polish — spacing, wording, the empty state, the error message — is management work. Brief it with examples, verify it like any other check.

*"The first 80% is a demo. The last 20% is the product."*

---

## RUN · The department at scale

### 28 · Decomposition
**Why it goes wrong:** One big prompt asking for everything produces the confident average of a big thing: plausible, interlocking, and wrong in ways that surface when users arrive.

**The move:** The agent builds features; you build the sequence. Ten small briefs, each with a check, each landing on verified ground. Dispatch one issue per conversation, in order — parallel is how the fog gets back in.

*"Big things are not built in one go. They are decomposed, dispatched, and verified."*

### 29 · One idea per commit
**Why it goes wrong:** Commits grow into weekly dumps, and the history that was supposed to testify becomes noise.

**The move:** If you can describe the change in one sentence, commit it in one sentence. Each commit is one idea; each message says what happened. When the audit comes, the commit messages are the department's testimony.

*"Commit messages are the department's testimony."*

### 30 · The reviewer with fresh eyes
**Why it goes wrong:** One agent building while the same agent self-reviews is a conflict of interest: the reviewer shares the blind spots of the builder.

**The move:** Separate duties: a builder from the spec, a reviewer auditing the diff against the spec alone — never having seen the builder's self-assurance — and sometimes a third, hostile pass. Findings ordered by consequence: DROPPED, INVENTED, BROKEN, RISKY, CLEAN. Overrule in writing, in DECISIONS.md, with the reason.

*"Fresh eyes are not a compliment; they are a control."*

### 31 · The staff turnover
**Why it goes wrong:** The model gets upgraded, and the validated arrangement is assumed to still hold.

**The move:** On every model change: re-run the replication test on two representative specs, re-run the full gate, re-audit one landed stage, and record the model and date in DECISIONS.md. The specs, checks, gates and skills are the durable layer.

*"The model is staff, and staff turn over."*

### 32 · Ship something true
**Why it goes wrong:** The last gate is permission — waiting until the thing is officially blessed.

**The move:** Start from a real itch — yours, your club's, your workplace's. Fill the rollback sentence: "if this goes wrong, I will ___ and the users will see ___." If the blank takes more than a minute to fill, ship behind a smaller blast radius first.

*"You do not need permission to ship. You need evidence it is true."*

---

**You describe. It builds. You decide whether it's true.**
