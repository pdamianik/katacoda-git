# Scenario 7
[back to overview](README.md)

## `git log`
### `-p`
Lists the changes made with the commit.
### `-n`
Limits the number of commits.
### `--since=` and `--until=`
Allows you to filter the commit log for a specific timespan e.g. `--since="2 weeks ago" --until="1 day ago"`
### `-m`
Removes all merging commits from the git log listing.
## `git bisect`
Allows you two efficiently search through a range of commits to find a bad commit. You start the search by executing the command `git bisect start`. This method works practically like binary search, where you define the latest known good commit with `git bisect good <commit-descriptor>` and the earliest known bad commit with `git bisect bad <commit-descriptor>` and git will one after the other checkout the commit exactly inbetween the latest known good commit and the earliest known bad commit and the you can decide with `git bisect good/bad` if the current commit is good or bad respectively and so git will update the latest known good commit/the earliest known bad commit and checkout you the new center, until the earliest bad commit (the one that introduced the error) has been found. `git bisect good/bad` without a commit descriptor will asume that you mean the current `HEAD`.
## `git blame`
Shows the latest changing commit for the lines in a file, line-by-line.
### `-L`
Can be used to only show the lines with a number inside of a specific range, e.g. `-L 6,8` shows the lines 6 till 8.