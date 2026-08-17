# Editorial and Design Principles

**Through-line:** 
Use one thesis, one voice, and one visual system. Give each fact one home.

---

## I. Voice and register

1. **Use one register per document.**
   Match the register to the document’s purpose and audience.
   Keep technical reference prose precise and descriptive.
   Omit reader directives unless the document is instructional.

2. **Separate voices by purpose.**
   Keep specification language in algorithms and formal descriptions,
   teaching language in examples and advisory language in warnings and risk discussions.

1. **Use imperatives when action is the point.**
   Keep descriptive prose focused on system behavior.
   Use checklists for review actions.

1. **Cut hedging.**
   Remove qualifiers unless they change the claim.

1. **Define specialized operations and terms once.**
   Thereafter, use the established name consistently.

1. **Order information by use.**
   Put the facts needed to understand or use the subject before secondary concerns and edge cases.
   Name sections by topic.

---

## II. The opening

1. **Lead with the invariant, rule, or central claim.**
   Put supporting detail afterward.

2. **Prefer short sentences to stacked noun phrases.**
   State the claim, its scope, and its main consequence.

3. **Keep numbered lists homogeneous.**
   Do not append unrelated facts beneath a list.
   Put each fact in the section that owns it.

4. **Place common misconceptions early when they affect understanding.**
   State each misconception and its correction briefly.
   Point to the relevant section instead of repeating the explanation.

5. **Treat metadata as secondary.**
   Edition, status, and audience should not compete with the main claim.

6. **Let diagrams illustrate or replace prose.**
   Do not use both to repeat the same information.

---

## III. Terminology and metaphor

1. **Choose one metaphor when it improves understanding.**
   Retire competing metaphors and synonyms.

2. **Treat the glossary as a contract.**
   Use every defined term. Define every specialized term unless it is standard enough to require no definition.

3. **Write definitions as concise fragments when possible.**

4. **Do not create separate glossary entries for synonyms**
   or for concepts already represented by a property, operation, or established term.

5. **Lock terminology before final polishing.**
   A retired term appearing in a title, comment, appendix, table, or example is a consistency defect.

---

## IV. Information architecture

1. **Give each fact one home.**
   Use each layer for its designated purpose:

   | Layer | Job |
   | --- | --- |
   | Summary | State the central claim and its immediate consequences. |
   | Quick reference | Explain what to use or choose. |
   | Algorithm | Specify the procedure and order of operations. |
   | Contract table | Provide the source of truth for behavior across states or inputs. |
   | Detail sections | Explain facts that need additional context. |
   | Hazards | Describe failure modes and risks. |
   | Checklist | State review criteria and required actions. |
   | Appendix | Provide supporting references, history, and detailed mappings. |

2. **Delete duplicated facts.**
   If a paragraph restates a table cell, remove the paragraph. If a callout restates a list, keep the clearest representation.

3. **Use one running example across related sections**ù
   when it improves comparison. Introduce a new example only when the subject requires it.

4. **Demote material that does not support the central thesis.**
   Move secondary details into tables, notes, or appendices.

5. **Keep explanatory facts only when they establish something**
   that the surrounding example, table, or list does not already show.

6. **Put production-relevant distinctions beside the concepts they affect,**
   not only in a final checklist.

---

## V. Diction

1. **Use plain verbs in explanatory prose.**
   Prefer direct verbs such as *read*, *write*, *reset*, *copy*, *ignore*, *start*, and *leave*.

2. **Keep lists grammatically parallel.**
   Use the same structure throughout each list.

3. **State special cases as consequences of the main rule.**
   Prefer direct statements of what happens.

4. **Name failures by their observable results.**
   Distinguish false positives, false negatives, fail-open behavior, fail-closed behavior, missed detection, and other terms according to the actual outcome.

5. **Keep comments calm and diagnostic.**
   Describe the state, operation, or result rather than dramatizing the scenario.

6. **Keep references clean.**
   Do not repeat citation markers or source names unnecessarily.

---

## VI. Visual system

Lock these choices once per document.

1. **Use one heading case.**
   Choose title case or sentence case and apply it consistently.

2. **Use one section-numbering convention.**
   Do not mix formats.

3. **Use a small, stable set of callout labels.** 
   For example:

     | Label | Use |
     | --- | --- |
     | Note | Optional information. |
     | Warning | Failure, error, or non-termination. |
     | Hazard | Shared state, security-sensitive behavior, or dangerous side effects. |

4. **Mark choices with words.**
   Symbols may reinforce meaning but should not carry meaning alone.

5. **Use one notation for each recurring kind of value, range, dash, and identifier.**

6. **Keep trees and diagrams structurally consistent.**
   Use one grammatical form for parallel operations.

7. **Make comments prove a claim or identify a result.**
   Do not repeat the surrounding prose.

8. **Generate alternate table layouts from the same source data.**
   Do not maintain separate content models.

---

## VII. Tables

1. **Make each cell concise.**
   If a cell needs a long explanation, move that explanation to a detail section.

2. **Remove rows that add no information.**
   Use a footnote when the same rule applies everywhere.

3. **Split behavioral tables when the split exposes a meaningful semantic distinction.**

4. **Keep reference-table headers short and predictable.**
   Give avoidance guidance a reason.

5. **Do not make a clean table larger merely to match a noisy one.**
   Keep each column focused on one kind of fact.

6. **Keep historical information out of behavioral tables**
   unless history is the subject. Use a note or appendix instead.

---

## VIII. Listings

1. **Let the listing carry the claim when it can.**
   Avoid introductory prose that merely narrates the code.

2. **Never present a non-terminating operation as runnable.**
   Mark it clearly or isolate it behind a safe demonstration mechanism.

3. **Identify side effects in probes and helper operations**
   when they affect the result.

4. **Classify helper operations**
   when their purpose differs from that of the main operation.

5. **Align comparison comments and outputs**
   so readers can scan them quickly.

---

## IX. Security and precision language

1. **Distinguish fail-closed from fail-open behavior.**
   Describe the actual outcome rather than assigning a generic security label.

2. **State necessary preconditions once,**
   after the worked example that demonstrates the issue.

3. **Explain each example once.**
   Use comments, a short explanation, or a precondition list rather than repeating the same analysis.

4. **Label heuristics as heuristics.**
   State when an observable property, string representation, or probe can be spoofed or can change state.

---

## X. Cross-cutting form

1. **Use one citation scheme.**
   Put citations on claims that need support and keep source details in the reference list.

2. **Verify correctness before polishing.**
   Wrong behavior, inverted outcomes, and unsafe examples are correctness defects, not style problems.

3. **Represent exception behavior systematically.**
   Use a table of outcomes when multiple cases must be compared.

4. **Keep low-level implementation details in detail sections**
   unless they are necessary to understand the central claim.

---

## XI. Edit order

Use this sequence for each substantial revision.

1. **Correctness.** 
   Verify claims, edge cases, failure behavior, and operation order.

2. **Terminology.**
   Remove retired synonyms and inconsistent names.

3. **Layering.**
   Remove duplication and move secondary material to its proper layer.

4. **Front matter.**
   Put the central claim first and keep introductory material focused.

5. **Visual consistency.**
   Fix headings, callouts, notation, tables, diagrams, and comments.

6. **Local diction.**
   Tighten sentences, make lists parallel, and remove unnecessary qualifiers.

7. **Stop.**
   Stop when further edits only create stylistic variation.

---

## XII. When to stop

A pass that only invents synonyms is a regression.

Publish when all of the following are true:
- The central terminology is consistent.
- Each fact has one home.
- The opening states the central claim clearly.
- Examples demonstrate rather than repeat the explanation.
- Tables separate different kinds of facts.
- Failure behavior is described accurately.
- Security language matches the actual outcome.
- Visual conventions are consistent.

Do not restyle for variety once the document has the right density.
The highest-leverage final edits are to remove the last synonym,
delete the last echo and fix the last incorrect diagnostic.

---

## XIII. One-page checklist for a new document

- State the central claim early.

- Use one terminology system and retire competing synonyms.

- Keep examples focused and nonredundant.

- Give every reference-table avoidance rule a reason.

- Put each procedure in one place.

- Give each fact one home.

- Move secondary material to a table, note, or appendix.

- Use plain verbs and parallel lists.

- Keep callout labels and visual conventions consistent.

- Make comments prove claims rather than narrate them.

- Identify state-changing probes and side effects.

- Describe failures by their actual outcomes.

- Keep citations consistent and verifiable.

- Verify correctness before and after polishing.
