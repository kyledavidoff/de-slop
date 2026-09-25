# Deslop

A Claude skill that removes AI slop from a piece of writing. It returns the text in plain human language. The meaning, facts, tone, and structure stay the same.

## What it does

- Fixes wording that reads as machine generated.
- Checks words, phrases, sentences, and labels such as headings, slide titles, and table headers.
- Keeps numbers, names, dates, tickers, code, and quoted text exactly as they are.
- Never invents facts. When a fix needs a fact that is not in the text, it marks the gap with `[need: ...]` and asks you.

It does not change your tone, reorder your sections, shorten for length, or improve your argument. It only fixes wording.

## What it checks

**Fixed rules.** These are always slop:

1. Em dashes, semicolons, vertical bars, arrows, and inline dot separators
2. "It's not X, it's Y" sentences
3. Passive voice
4. Headings written as commands
5. Slogans and buzzword phrases

**Judgment calls.** These depend on context:

1. Awkward wording
2. Flowery wording
3. Vague or empty wording
4. Unnecessary wording
5. Illogical wording

## Install

**Claude apps.** Upload `de-slop.skill` in your Claude settings, in the Skills section.

**Claude Code.** Unzip the file into your skills folder:

```
unzip de-slop.skill -d ~/.claude/skills/
```

## How to use it

Paste your text and ask Claude to clean it up. Any of these prompts work:

- "Deslop this email."
- "This sounds like ChatGPT wrote it. Fix it."
- "Make this sound human."
- "Take the AI out of this cover letter."

It works on emails, messages, resumes, cover letters, memos, slides, spreadsheets, job descriptions, website copy, and LinkedIn posts.

## What you get back

1. The full cleaned text, in its original format, ready to paste.
2. **What changed.** One line for each fix.
3. **Open questions.** Facts the skill needs from you. This section appears only when there is a gap.

To get a list of problems without a rewrite, ask it to "find the slop" only.
