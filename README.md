# List Hygiene Checker

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Check any spreadsheet or list for duplicates, missing fields, stale entries and rows that aren't real records, without changing anything.

## Why

Any list that several people add to over time collects the same quiet problems. The same person appears twice under different spellings. A required field is blank. Nobody removed a test row. An entry looks complete but nobody has touched it in years. This finds those and hands them to a person to deal with.

[![Five outcomes from a list hygiene review.](assets/diagrams/19-list-hygiene-checker.svg)](SKILL.md)

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini or similar), then paste in the list you want checked and say which fields are required. It produces:

- Likely duplicates, based on more than one shared identifier, never on name similarity alone
- Possible duplicates, kept visibly separate and flagged for a person to confirm
- Rows that aren't real records, such as test entries or placeholders, kept apart from incomplete real ones
- Stale entries, including ones that look complete but haven't moved in a long time
- Clean rows called clean, not buried under invented problems

[The worked example](example/) is a fictional running club membership list with five deliberate traps. They include a confident duplicate, a merely possible one and a record that looks complete but is stale. [The second worked example](example-two/) tests the edge of the duplicate rule: two clearly different people who share the same household email and phone number.

<details>
<summary><strong>See what it produces</strong></summary>

1. A summary table of issue type against rows affected
2. Likely duplicates, with the shared identifiers that make them confident
3. Possible duplicates, kept visibly separate and flagged for you to confirm
4. Rows that aren't real records at all, kept apart from incomplete real ones
5. Stale entries, including ones that look complete but haven't moved
6. Clean rows, named as clean

</details>

Use [the blank checklist](templates/hygiene-checklist.md) for your own list, and [the review checklist](checks/checklist.md) before you act on anything flagged.

You don't need to install anything, set up a project or write code to try it.

## Before You Use It

This flags issues; it doesn't act on them. Confirm any suggested duplicate before you merge anything, and make every field correction or deletion yourself.

## Feedback

Run it on a real list? [Start a discussion](https://github.com/shaunmarsden/list-hygiene-checker/discussions) if it missed something or flagged something that was fine.

## Part of a Family

This is one of a family of free tools that take patterns from [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) beyond sales. [sibling-projects](https://github.com/shaunmarsden/sibling-projects) lists the rest. Not sure which one fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/), which shows clickable cards, or paste a description into an AI chat with [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md).
