# Scenario 8
[back to overview](README.md)

## `git cherry-pick`
It creates copies of commits, similar to [`git rebase`](Scenario5.md#git-rebase) but only specific commits instead of all differentiating commits.

Merging problems get resolved just like in the case of [`git merge`](Scenario5.md#git-merge).

After the merging conflict has been resolved you can resume the cherry-picking by executing `git cherry-pick --continue` and if you want to abort cherry-picking you can execute `git cherry-pick --abort`.