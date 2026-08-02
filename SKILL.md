---
name: list-hygiene-checker
description: Audit any spreadsheet or list for duplicates, missing fields, stale entries and rows that are not real records at all, without changing anything. Use for a mailing list, a contact database, a membership list, an inventory, or any list that has been added to by more than one person over time. Do not use this to judge why a specific record is inactive or what to do about it; it only flags structural issues for a person to act on.
---

# List Hygiene Checker

You do not need to install anything to try this once: copy this whole file, paste it as your first message in any AI chat tool, then paste in the list you want checked.

Most lists that have been added to by more than one person over time accumulate the same quiet problems: the same person entered twice under a slightly different spelling, a required field left blank, a test row nobody removed after setup, an entry that looks complete but has not actually been touched in years. This finds those, without merging, deleting, or changing anything itself.

## Gather the Inputs

- The list or export to check, with whatever fields exist (name, contact details, dates, status, whatever the list actually has)
- What counts as a required field for this specific list; that varies, a mailing list needs an email, an inventory needs a location, decide this before scanning rather than assuming

## Scan the List

1. Check every row for missing required fields.
2. Look for likely duplicates: the same real entity entered more than once, under a slightly different spelling or format. Keep these visibly separate from merely possible duplicates, a similar-sounding name with no other shared detail is not the same as a shared email or phone number under two names.
3. Flag rows that are not a real record at all, a test entry, a placeholder, an obvious internal artefact left over from setup, kept separate from a real record that is merely incomplete.
4. Check for staleness properly: a row can look unhealthy because every field is blank, or look healthy because every field is filled in while quietly having had no activity in a long time. Check both, do not assume a complete-looking row is a current one.
5. Note any date or status field that is internally inconsistent, a status that implies recent activity next to a last-activity date that contradicts it.

## Apply the Guardrails

- Every finding is a suggestion; nothing is merged, deleted, or changed here, that stays with a person
- Never merge a possible duplicate into a confident one on name similarity alone; require a second shared, specific detail
- Keep non-real-record findings separate from missing-field findings; a test row and an incomplete real entry need different actions
- State any staleness threshold used as illustrative, not a fixed rule, since what counts as stale genuinely varies by list
- Call genuinely clean rows clean; a review that finds a problem on every row will not be trusted on the ones that actually have one

## Stop When the Task Is Unsafe

Do not produce a hygiene review when:

- The list is missing enough structure, no way to tell what a duplicate would even look like, that a check cannot be done with any real confidence
- The request is to merge, delete, or update records directly rather than flag them for a person to action
- The request is to judge why a specific record went stale or what to do about it; that needs more context than a structural check alone provides

## Require Human Review

Confirm any suggested duplicate before merging anything. Every field correction, deletion, or status change stays a direct, deliberate action by a person, not something this check does on its own.

For a fictional worked example, read [the worked example](example/). Use [the blank checklist](templates/hygiene-checklist.md) once you have your own list to run through.
