# Scenario 9
[back to overview](README.md)

## `git rebase --interactive`
This "interactive rebasing" is, as the name suggests, an interactive way to rebase. But instead of just offering the option to copy commits, this mode enables you to do a few more specific things:

 - p, pick = use commit -> copies the commit or, when on the same branch just leaves the commit as it is.
 - r, reword = pick, but edit the commit message
 - e, edit = pic, but stop for ammending
 - s, squash = pick, but meld into previous commit
 - f, fixup = squash, but remove the commit's log message
 - x, exec = run command using shell
 - d, drop = remove commit

Additionally, interactive rebasing enables you to reorder the commits by simply reordering the commit lines in the editor.

Git rebase can be used like a combination of [`git rebase`](Scenario5.md#git-rebase) and [`git cherry-pick`](Scenario8.md#git-cherry-pick), but interactively.

### Splitting commits
Opposite of squasing commits.
Steps:

 - `git rebase --interactive <commit-identifier>` where \<commit-identifier\> is the commit you want to split
 - set the commit you want to split to `edit`
 - `git reset HEAD^` to remove the commit, but not the files
 - `git add <files for the first commit>`
 - `git commit` commit the first split part
 - repeat previous two steps for all seperate changes
 - finally: use `git rebase --continue` to tell github that you are finished with the `edit` step as set in step 2

## `git commit --amend`
Can be used to change the latest commit.