# Scenario 5 - Fixing Merge Conflicts
[back to overview](README.md)

## `git merge`
Is used to merge two branches into one commit. Can also be used to merge together changes a remote branch and the local version of that branch.

## `git checkout`
[link to `git checkout`](Scenario4.md#git-checkout)

In case of a merge conflict the following two parrameters can be used to decide which version to keep.
### `--ours`
Picks the local version of a file over the remote version (overwrites remote changes with local changes). Opposite of [`git checkout --theirs`](#--theirs).
### `--theirs`
Picks the remote version of a file over the local version (overwrites local changes with remote changes). Opposite of [`git checkout --ours`](#--ours).

## `git rebase`
Instead of creating a new commit based of of the two commits we want to merge (with [`git merge`](#git-merge)), `git rebase` creates copies of deviating commits and puts them on top of the current selected commit.

> *NOTE:* By using this technique, the copied commits will have a new commit hash.