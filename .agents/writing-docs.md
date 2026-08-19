# Writing docs pages

Every skill in any skill category (i.e.`engineering/`, `productivity/`) has a human-facing **docs page** at `docs/{category}/{skill-name}.md`. The docs tree mirrors those two bucket folders under `skills/`.

Most of these skills are **user-invoked**: the agent will never fire them for you, so _you_ are the index that has to remember they exist and when to reach for them. That memory is **cognitive load**. The job of a docs page is to relieve it: to orient one reader around one skill so they can hold it in their head, know When to use it, and see where it sits in the system. The pages are collectively a distributed router; each is a node.

A rename moves the file too (`docs/{category}/{old}.md` → `docs/{category}/{new}.md`), because the published URL tracks the name; a skill that moves between `engineering/` and `productivity/` moves its docs file to the matching folder. Skills in `misc/`, `in-progress/`, and `deprecated/` get no page, because none of those buckets is promoted. A skill moving _out_ of one of them into `engineering/` or `productivity/` gains a page; one moving the other way loses it.

## Page structure

Fill the template below, keeping its order. The **fixed frame** (`## What it does`, `## When to use it`, `## Where it fits`) appears on every page. `## Prerequisites` and the free-form substance sections carry only what this particular skill needs; delete the rest.

Four sections make a page worth reading: `What it does`, `When to use it`, `It's working if`. The first two orient the reader; the last two are where the page stops summarizing the skill and starts answering the reader's own situation. Each of the last two has a bar to clear, below, but treat a page that clears neither as unfinished, not as finished-and-short.

<page-template>

## What it does

One or two plain-language paragraphs. Lead with the skill's one-sentence job, then state the **defining constraint**: the single fact that makes this skill behave differently from the obvious default (for `to-spec`: it does not interview the user again, it synthesises what is already known). Write it as a plain declarative sentence, never a labelled aside like "The defining constraint:" or "The key thing:"; the formula reads as filler. This line is the most valuable on the page; never omit it.

## When to use it

How and when you reach for the skill, in two beats that are both effectively always present:

- **Invocation mode.** State whether you type it or the agent fires it. A user-invoked skill: "You invoke this by typing `/{name}`, and the agent won't reach for it on its own." A model-invoked skill: "Type `/{name}`, or the agent reaches for it automatically when a task fits."
- **Trigger boundary.** The index entry: "reach for this when …". Where the skill is confusable with a sibling, add the other half: "for <X> instead, use [{sibling}]({file-path-to}/{sibling})."

## Prerequisites

Optional: include only when the skill needs something in place to be functional; omit the heading entirely otherwise. Covers: a **workspace it writes into**, **prior setup**, or **repo-specific tooling**. A stateless skill that runs anywhere has no prerequisites, so drop the section.

## <free-form middle>

One to three short sections, in the skill's _own vocabulary_, that make it click. Choose whatever headings fit the skill: the loop it runs, the artifact it produces, the fork it makes, the one anti-pattern it kills. There is no prescribed heading; the skills are too heterogeneous for one.

The single non-negotiable: **surface the skill's leading word / defining idea** (`tight` feedback loop, `deep module`, throwaway-code-answers-a-question, red-green). It pays off twice: the reader learns what the skill _is_, and learns the word they'll later think with to _reach for_ it.

## It's working if

A few bullets naming what the reader sees when the skill is doing its job. The bar on each is that the reader can check it without opening `SKILL.md`: a signal in their own work, or in the trace in front of them. "The document gets shorter as it gets better" passes; "the library section is byte-identical to `template.sh`" is a compliance check on the skill's internals wearing this section's name. Include it wherever the tells are crisp; omit the heading where they stay vague.

## Where it fits

Always present. Situate the skill in the system in a sentence or two:

- **Role.** Name it: a **chain step** (`iterative-plan → execute-plan → documentation-create`), a **run-once setup**, **periodic maintenance** (`audit-repo`, "every few days"), or a **reach-for-it-anytime standalone** (`pr-review`, `pr-description`, `adr-create`). A standalone's map is one honest sentence, which is far better than omitting the section.
- **Neighbors.** The one or two siblings that matter, each with a because-clause, linked absolutely.

</page-template>

## Conventions

- Explain the **why**, not the process. The page orients and situates the skill; it never reproduces the `SKILL.md` steps or template dumps: a human choosing a tool does not need the runbook.
- **Never name the author.** The page is a technical document, not a record of who said what. "John says", "John's own answer", "his position is", a quoted reply: all of it goes.
- **Branches go in a table or a list, never in a paragraph.** Where the page presents a choice (two artifacts the skill can produce, four situations that trigger it, five options at a boundary), the reader is scanning for the one row that matches their situation. A paragraph makes them read all of it to find out. A short markdown table (condition in the left column, what to do in the right) or a numbered list gives it back in one glance. This applies wherever the branch appears, most often in `## When to use it` and the free-form middle.
- Use numbered lists for easy reference. Never nest bullets under numbered lists, always use numbered sub-lists. The reader can say "step 3" and the agent can say "step 3.2" without ambiguity.

## Done when

- The page exists at `docs/{category}/{name}.md`, and no stale page survives a rename or category move.
- The page carries no source link and writes no install command of its own.
- `## What it does` states the defining constraint, as plain prose rather than a labelled aside.
- The page names no author and quotes no author: every claim stands on its own.
- `## When to use it` states invocation mode and the trigger boundary.
- `## Where it fits` names the role and links to `ask-matt`.
- A prerequisite (workspace, prior setup, tooling) is stated where one exists, and the section is absent where none does.
- The middle surfaces the leading word.
- Every multi-way branch is a table or a list, not a paragraph the reader has to read in full.
- Every `## It's working if` bullet is checkable without opening `SKILL.md`.
- The sections appear in the template's order.
