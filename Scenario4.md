# Scenario 4 - Undoing Changes
[back to overview](README.md)
## `git checkout`
Used to move the `HEAD`/commit the working tree is based of of. Without a parameter this command will just list the current tracking information. (this command required some [extra research](https://git-scm.com/docs/git-checkout))
## `git reset`
Used to unstage files (move them from the staging area to the not staged/untracked area respecitvely)
### `--hard`
Combines [`git reset`](#git-reset) and [`git checkout`](#git-checkout) to remove all changes.
## `git revert`
Undoes commits by creating an invers commit to the commit(s) that have to be undone (new file -> delete file, delete file -> new file, modified -> modified back). This command requires a parameter of the commit to undo.
### navigating the commit history
The symbol `^` means one commit back and can be used multiple times in a commit descriptor
The symbol `~` incombination with a tailing number can be used to go multiple steps back in the history.
The symbols `...` can be used bewteen two commit descriptors to define a range of commits (from the commit before the `...` to the commit after the `...`).

commit descriptor | commit descriptor meaning
----------------- | -------------------------
`HEAD^`           | one commit before the `HEAD`
`HEAD^^`          | two commits before the `HEAD`
`HEAD~1`          | one commit before the `HEAD`
`HEAD~2`          | two commits before the `HEAD`

## `git log `**`--oneline`**
[link to `git log`](Scenario2.md#git-log).

Logs the commit history, but only shows the commit message and branches, tags, `HEAD`.