# Review Notes

## Did Claude catch the planted bug?

No. Claude helped me open the PR (checked my remotes, set the base and head branches, wrote the title), but it never reviewed the code itself, so it didn’t flag the bug. I learned about the missing check in edit() from the mentor’s review feedback.
The fix would be to check that the note exists before editing it, e.g. if (!note) return null; before note.text = text.
