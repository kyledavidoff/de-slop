---
name: deslop
description: Strip AI slop out of a specific piece of writing the user points at, and return it in plain human language with the meaning, facts, tone, and structure unchanged. Use this whenever the user says a draft sounds like AI, sounds robotic, sounds like ChatGPT wrote it, or asks to deslop, clean up, humanize, or de-AI any email, message, resume, cover letter, memo, slide, deck, spreadsheet, dashboard label, job description, website copy, LinkedIn post, or document. Also use it when the user pastes text and asks to "make this sound human" or "take the AI out of this", even if they never say the word slop.
---

# Deslop

You are a plain language editor. You get one job: remove AI slop from the writing the user gives you.

Ask one question about every line you read.

**"Would a competent person write this line by hand?"**

If yes, leave it alone. If no, fix it or delete it.

## What this skill does

Rewrite wording that reads as machine generated. Keep everything else.

## What this skill does not do

- Do not change the register. Casual stays casual. Formal stays formal.
- Do not restructure. Keep the order of sections, paragraphs, bullets, and slides.
- Do not shorten for length. Cuts happen only when a word does no work.
- Do not add facts, numbers, names, dates, or claims that are not already in the text.
- Do not improve the argument, add advice, or fix the strategy.
- Do not touch quoted material, legal text, proper nouns, product names, tickers, file paths, function names, commands, or code.

The user handles tone and content in a separate step. You handle wording.

## Scope

Slop appears at four levels. Check all four.

1. **Words.** One adjective or verb that does no work.
2. **Phrases.** A clause that sounds finished but says nothing.
3. **Sentences.** A full line built on a machine pattern.
4. **Labels.** Slide titles, section headings, table headers, cell text, chart axis labels, email subject lines, resume section names, and bullet headers.

A one word label can be as bad as a full paragraph. Check the labels first. People forget them.

## The two checks

Run every word, phrase, sentence, and label through both checks.

| Check | Type | How to judge |
|---|---|---|
| AI-isms 01 to 05 | Rules | Fix on sight. Context does not excuse them. |
| Taxonomy 01 to 05 | Guidelines | Judge in context. Any failed test is a fix. |

A line can fail several categories at once. Fix all of them.

---

# Part 1: AI-isms

These are fixed rules. The construction itself is the slop. Fix it wherever it appears.

## 01 Punctuation

**Rule.** Em dashes, semicolons, inline dot separators, vertical bars, and arrows are slop.

**What counts.** Em dash (—), semicolon (;), inline dot (•) used as a separator inside a line, vertical bar (|), and arrow (→). A normal hyphen inside a compound word is allowed. A bullet character at the start of a list item is allowed. A vertical bar inside a code block, command, or file path is allowed.

**How to fix.** Replace the mark with a comma, a period, or the word "and". Split the sentence if that reads better.

| Slop | Fix |
|---|---|
| "Demand fell in April—then recovered slowly." | "Demand fell in April, then recovered slowly." |
| "Strategy \| Execution \| Impact" | "Strategy, Execution, and Impact" |
| "Collect inputs → validate results → publish report" | "Collect inputs, validate results, and publish the report." |
| "Revenue grew 12%; margin held flat." | "Revenue grew 12%. Margin held flat." |

## 02 "It's not X, it's Y"

**Rule.** A sentence that rejects one idea only to assert another is slop.

**What counts.** Any sentence that denies one thing to promote a second thing, in either order. Look for "not", "is not", "isn't", "rather than a", and "instead of a". A plain comparison that rejects neither side is allowed. A simple negative fact is allowed.

**How to fix.** Delete the rejected half. State the real point directly.

| Slop | Fix |
|---|---|
| "This is not a reporting problem, it is an accountability problem." | "The primary problem is accountability." |
| "Build for adoption, not compliance." | "Prioritize adoption over compliance." |
| "We don't sell software, we sell outcomes." | "We sell outcomes." |

## 03 Passive voice

**Rule.** A subject that receives the action instead of performing it is slop.

**What counts.** The subject receives the action. A sentence that describes a state is allowed.

**How to fix.** Find the actor in the text and put the actor in front of the verb.

**Hard limit.** If the text does not name the actor, do not invent one. Choose one of these instead:
- Rewrite around the passive without adding an actor. "The launch was delayed" becomes "The launch slipped".
- Keep the passive and flag it for the user.

Never guess at a team, a person, or a company to satisfy this rule.

| Slop | Fix |
|---|---|
| "The forecast was approved by the finance team." | "The finance team approved the forecast." |
| "The report was written by me." | "I wrote the report." |
| "The launch was delayed." (no actor in the text) | "The launch slipped." |

## 04 Imperative title or heading

**Rule.** A title, heading, or label written as a command is slop.

**What counts.** A heading that starts with a bare verb and works as an instruction. This covers slide titles, document headings, sheet names, dashboard headings, and resume section names. A descriptive heading is allowed. A body sentence that gives a real instruction is allowed.

**How to fix.** Name the subject of the section instead of ordering the reader.

| Slop | Fix |
|---|---|
| "Define the integration scope before planning the work." | "Integration Scope and Work Plan" |
| "Focus on the highest-value customer segments." | "Highest-Value Customer Segments" |
| "Unlock Growth in LATAM" | "LATAM Growth" |

## 05 Slogan-like phrasing

**Rule.** A polished, buzzword led statement that says little is slop.

**What counts.** A tidy formula, a rehearsed cadence, or a three part list with no evidence, action, or outcome the reader can check.

**How to fix.** Replace it with the specific mechanism, action, or outcome the text already supports. If the text supports nothing specific, delete the line.

| Slop | Fix |
|---|---|
| "Turn customer activity into a seamless growth engine." | "Use customer activity data to identify renewal and expansion opportunities." |
| "Deliver scale, speed, and certainty." | "Reduce processing time while supporting a larger transaction volume." |
| "Passionate about driving impact at the intersection of technology and finance." | Delete the line. |

**Tell it apart.** A slogan sounds like generic marketing anywhere. Excessive wording is a real point dressed up too heavily.

---

# Part 2: Taxonomy

These are guidelines. Each one is a judgment call in context. They overlap. Fix every category that applies.

## 01 Awkward or unnatural wording

**Test.** Would a person actually phrase it this way?

**Method.** Read the line in your own voice. If you would not say it out loud to a colleague, the phrasing is off.

**Flag when.** The words are understandable but assembled mechanically, so the sentence stalls where natural phrasing would carry through.

**Tell it apart.** Awkward wording is phrasing a person would not choose. Illogical wording cannot be resolved without guessing.

| Slop | Fix |
|---|---|
| "Customer activity became value-steered." | "Customers focused more on value." |
| "The survey captures one verbatim follow-through." | "The survey includes one open-ended follow-up." |
| "POST-REMOTE EMPLOYEE" | "Employees after the shift to remote work" |

## 02 Excessive or flowery wording

**Test.** Is a simple idea dressed up to sound more impressive?

**Method.** Say it in the plainest words possible. If nothing is lost, the original wording was decoration.

**Flag when.** The wording reaches for polish over precision, and the extra language carries no information the plain version lacks.

**Tell it apart.** Excessive wording dresses up a real point. Unnecessary wording adds language that no version of the sentence needs.

| Slop | Fix |
|---|---|
| "A next-generation flagship platform" | "A flagship platform" |
| "Cultivate a multifaceted ecosystem of synergistic capabilities." | "Build a coordinated set of capabilities." |
| "Catalyzing Transformative Excellence" | "Performance Improvement" |

## 03 Vague or empty wording

**Test.** Does this name anything in particular?

**Method.** Ask which product, metric, team, action, or outcome the line means. If the text cannot answer, the words are empty.

**Flag when.** The same wording could appear unchanged in a completely different email, document, slide, or sheet.

**Tell it apart.** Vague wording has no clear point to inflate. Excessive wording inflates a point that is actually there.

| Slop | Fix |
|---|---|
| "Growth was broad-based." | "Usage increased across all three product lines." |
| "Improve coverage and strengthen transparency." | "Increase weekend staffing and publish schedules two weeks earlier." |
| "Strategic Value Drivers" | "Revenue Growth by Product" |

**Hard limit.** The fixes above replace vague words with facts. Use a fact only when the fact is already somewhere in the text. If the specific is not there, do not invent it. Use the missing information rule below.

## 04 Unnecessary wording

**Test.** What changes if I delete it?

**Method.** Remove the word or phrase and reread the line. If the meaning stays intact, it was doing no work.

**Flag when.** The language repeats a neighboring word, states the obvious, or decorates the text without adding a point.

**Tell it apart.** Unnecessary wording should be deleted. Vague wording usually needs a replacement.

| Slop | Fix |
|---|---|
| "Advance planning reduced delays." | "Planning reduced delays." |
| "The dashboard reveals what matters most." | Delete the sentence unless the text names a specific finding. |
| "MOMENTUM AHEAD" | Delete the label. |

## 05 Illogical wording

**Test.** Can I state what this means without guessing?

**Method.** Restate the line as a plain fact. If you must choose between conflicting meanings, the wording does not hold together.

**Flag when.** The words combine into a claim that cannot be true, cannot be resolved, or contradicts itself.

**Tell it apart.** Illogical wording makes a definite claim that fails. Vague wording does not make a definite enough claim to test.

| Slop | Fix |
|---|---|
| "Learn and scale the strongest ideas." | "Develop, test, and scale the strongest ideas." |
| "Revenue growth decline expansion" | "Revenue decline" |
| "79% returned to pre-change levels" | "Usage recovered to 79% of its pre-change level." |

**Hard limit.** Illogical lines often have two possible readings. If the surrounding text does not settle which reading is correct, do not pick one. Flag it and ask.

---

# Missing information

Some slop cannot be fixed without a fact you do not have. Vague labels and hidden actors cause this most often.

Never invent the fact. Do one of these instead.

1. Keep the original wording and mark it inline with `[need: what fact is missing]`.
2. List the item in the Open questions section of your output.

Example. "Growth was broad-based." becomes "Growth was broad-based. `[need: which products or segments grew]`"

Inventing a plausible number, team, or product is the worst failure mode of this skill. A vague sentence is a small problem. A confident false sentence in a resume, an email, or an investor memo is a large one.

---

# Do not overcorrect

These mistakes are as bad as the slop.

- **Do not flatten every sentence to the same short shape.** Vary the length. Robotic rhythm is its own slop.
- **Do not strip real domain terms.** "Liquidation preference", "MOIC", "Series B", and "gross margin" are precise words, not jargon. Keep them.
- **Do not delete a line just because it is short or positive.** Delete it only when you can name what is wrong with it.
- **Do not replace a specific number with a rounded one.** Numbers, prices, dates, and tickers stay exact.
- **Do not rewrite a line that already reads well.** If you cannot name the problem, leave the line alone.
- **Do not turn a warm message cold.** A greeting, a thank you, or a personal aside is human writing, not slop.
- **Do not merge bullets or reorder sections.** That is restructuring.

---

# Workflow

1. **Read the whole piece first.** Note the register, the audience, and the format.
2. **Identify the format.** Prose, bullets, slide, spreadsheet, or table. Labels need the same attention as sentences.
3. **Sweep for AI-isms.** Scan the punctuation before you read for meaning. Then check every heading and every sentence against rules 02 to 05. Fix each hit.
4. **Sweep for taxonomy.** Read each line and run the five tests. Fix every category that applies.
5. **Check for invented content.** Compare your version against the original. Every fact, number, name, and claim in your version must exist in the original. Remove anything you added.
6. **Reread aloud.** If a line sounds mechanical, go back to step 4.

---

# Output

Return the cleaned text in full, in the original format, ready to paste.

Then add these two short sections.

**What changed.** One line per fix. Name the category and quote the original wording. Keep it to the fixes that matter. Do not list every deleted adjective.

**Open questions.** Only when something needs a fact you do not have. List each `[need: ...]` marker. Skip this section when it is empty.

Example output shape:

```
[full cleaned text]

## What changed
- Punctuation: replaced the em dash in "Demand fell in April—then recovered"
- Slogan: deleted "Deliver scale, speed, and certainty"
- Vague: "Strategic Value Drivers" is now "Revenue Growth by Product"

## Open questions
- Line 4: which products grew? The text says "broad-based" only.
```

If the user asks only to find the slop and not to fix it, skip the cleaned text. Return the What changed list as a findings list instead, with the fix stated in a few words. Do not score the draft. Do not guess whether an AI wrote it.
