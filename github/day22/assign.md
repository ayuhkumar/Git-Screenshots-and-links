Q1. Theory — Understanding Cherry-Pick

1. What is git cherry-pick?
- It copies a specific commit from one branch to another.
- Useful when we need only one particular change.

2. Cherry-pick vs Merge

Cherry-pick:
- Copies selected commit(s).
- Does not combine the whole branch.

Merge:
- Combines the changes of two branches.
- Usually brings all commits from the other branch.

3. Does cherry-pick move the original commit?
- No.
- The original commit stays in its original branch.
- Cherry-pick creates a copy of that change on the current branch.

4. Why does cherry-pick create a new commit?
- Because the commit is applied to a different branch/history.
- Git creates a new commit with a new commit ID (hash).

5. Cherry-pick commands

git cherry-pick --continue
- Continues cherry-pick after resolving a conflict.

git cherry-pick --abort
- Cancels the cherry-pick.
- Returns the branch to its previous state.

git cherry-pick --skip
- Skips the current commit.
- Continues with the next commit.

6. Difference between:

git cherry-pick <start_commit>..<end_commit>
- Cherry-picks commits AFTER start_commit up to end_commit.
- start_commit is NOT included.

git cherry-pick <start_commit>^..<end_commit>
- Cherry-picks from start_commit up to end_commit.
- start_commit IS included.

Example:
A -> B -> C -> D

git cherry-pick B..D
- Picks C and D.

git cherry-pick B^..D
- Picks B, C and D.

Remember:
..     = start commit excluded
^..    = start commit included


Q2.


