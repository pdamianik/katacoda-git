# Scenario 6 - Experiments Using Branches
[back to overview](README.md)

## `git branch`
Used to manage branches.

Without any parameters git will just list all the branches in the repository and highlight the current branch.

Without any flags git will try to create a new branch with the passed name e.g. `git branch new_branch` creates a new branch with the name `new_branch`.
### `-a`
Includes the remote branches in the list.
### `-v`
Includes the commit information of the last commit on that branch (a short form of the commit hash and the commit message).
### `-d`
With this flag passed the `git branch` command will delete a passed branch.
## `git checkout`
[link to `git checkout`](Scenario4.md#git-checkout)
### `-b`
The `-b` flag enables you to create a branch if didn't exists and then checks it out.