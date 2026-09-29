# Review: Northbank Running Club Output

I checked [output.md](output.md) against what [list.md](list.md) was built to test.

## What Worked

It told a confident duplicate apart from a merely possible one. Rosa Alvarez/Alvarrez shared two independent identifiers (email and phone), so the output called it a likely duplicate with confidence. The two Tom Higgins rows shared only a name, and every other field differed. The output kept them separate for a person to check rather than merging them on the name alone. That's the mistake this skill is there to prevent.

It kept a fake record apart from incomplete real ones. It flagged "Test Runner" as not a real record, separate from Ben Foster and Sam Whitfield, who are real members with gaps. Treating a test row as "a member missing some fields" would have put it in the wrong category.

It caught the record that looked healthy but wasn't. Every field for Maria Kowalski was filled in, which could pass on a quick scan. The output caught the stale last-activity date behind the complete-looking row, which is the trap this row was built to test.

It called the clean row clean. It didn't invent an issue for Dev Patel to look thorough.

## What Still Needs a Human Check

- Someone who knows the club still needs to confirm whether the two Tom Higgins entries are the same person. The output rightly stops short of deciding.
- The staleness threshold here (roughly five years) is just for this list. A weekly mailing list would need a much shorter one than a running club membership.

## Verdict

No automatic failure. The output handled every category this list was built to test: a confident duplicate, a merely possible one, a fake record, two incomplete ones, and one that looked complete but was stale. It didn't merge, delete or change anything itself.
