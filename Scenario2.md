# Scenario 2 - Committing Changes
[back to overview](README.md)
## `git diff`
Outputs a comparison between the previous commit that the current working tree is based of (`HEAD`) and the current working tree.
`git diff` alone won't compare files that are in the current staging area. If you want to compare the `HEAD` to the staging area you have to use `git diff `**`--staged`**.
## `git log`
Lists the commit history of the repository.
### formatting
`git log --pretty=format:"%h %an %ar - %s"` can be used to format the git log to suite your taste
## `git show`
Shows information about a commit. If no commit hash is passed it will show the `HEAD` commit.