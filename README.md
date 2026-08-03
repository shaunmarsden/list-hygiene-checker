# List Hygiene Checker

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Audit any spreadsheet or list for duplicates, missing fields, stale entries and rows that are not real records at all, without changing anything.

## Why

Any list added to by more than one person over time accumulates the same quiet problems: the same person entered twice under a different spelling, a required field left blank, a test row nobody removed, an entry that looks complete but has not actually been touched in years. This finds those and hands them to a person to actually action.

[![Five outcomes from a list hygiene review.](assets/diagrams/19-list-hygiene-checker.svg)](SKILL.md)

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini, or similar), then paste in the list you want checked, along with what counts as a required field for it. It produces:

- **Likely duplicates**, based on more than one shared identifier, never name similarity alone
- **Possible duplicates**, kept visibly separate, flagged for a human to confirm
- **Rows that are not real records**, test entries or placeholders, separate from incomplete real ones
- **Stale entries**, including ones that look complete but have not moved in a long time
- **Clean rows called clean**, not buried under manufactured problems

See [the worked example](example/): a fictional running club membership list built with five deliberate traps, including a confident duplicate, a merely possible one, and a record that looks complete while actually being stale. [The second worked example](example-two/) tests the boundary of the duplicate rule itself: two clearly different people sharing the exact same household email and phone number.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. A summary table: issue type against rows affected
2. Likely duplicates, with the specific shared identifiers that make them confident
3. Possible duplicates, kept visibly separate, flagged for you to confirm
4. Rows that are not real records at all, kept separate from incomplete real ones
5. Stale entries, including ones that look complete but have not moved
6. Genuinely clean rows, named as clean

</details>

Use [the blank checklist](templates/hygiene-checklist.md) for your own list, and [the review checklist](checks/checklist.md) before acting on anything flagged.

No installation, project, or coding required to try it once.

## Before You Use It

This flags issues, it does not act on them. Confirm any suggested duplicate before merging anything, and make every field correction or deletion directly yourself.

## Feedback

Run it on a real list? [Start a discussion](https://github.com/shaunmarsden/list-hygiene-checker/discussions) if it missed something or flagged a false positive.

## Part of a Family

This is one of a family of free tools generalising [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) patterns beyond sales. See [sibling-projects](https://github.com/shaunmarsden/sibling-projects) for the rest, or use [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md) if you are not sure which one actually fits.
