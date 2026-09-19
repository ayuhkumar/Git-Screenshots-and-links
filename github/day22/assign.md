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
<img width="753" height="265" alt="image" src="https://github.com/user-attachments/assets/ee281af1-6fc1-4532-ab04-ef9c11924c36" />



Q3.
<img width="890" height="266" alt="image" src="https://github.com/user-attachments/assets/92af690f-1d2f-4e26-a0cf-7f9442a6f403" />


Q4.
<img width="755" height="203" alt="image" src="https://github.com/user-attachments/assets/11dfc214-b031-4c96-bf38-668407396899" />
<img width="785" height="341" alt="image" src="https://github.com/user-attachments/assets/a6a74f3d-d9e3-4d54-83db-8c6427988604" />
<img width="765" height="352" alt="image" src="https://github.com/user-attachments/assets/92257452-d7c9-45ae-881e-d3d341c618de" />
Difference:

git cherry-pick <start_commit>..<end_commit>
Start commit is NOT included.
Picks commits after start up to end.

Example:
B..D → picks C and D.

git cherry-pick <start_commit>^..<end_commit>
Start commit IS included.
Picks start commit up to end.

Example:
B^..D → picks B, C and D.

Remember:
.. = start excluded
^.. = start included

Q5.

<img width="841" height="917" alt="image" src="https://github.com/user-attachments/assets/c096e8f1-3272-44ce-9ae5-78e3b79b9946" />
<img width="868" height="908" alt="image" src="https://github.com/user-attachments/assets/f3ef967b-f1e0-447e-b2dd-c9e232a38fd1" />
<img width="717" height="255" alt="image" src="https://github.com/user-attachments/assets/eae33aa4-f084-43e8-8bd6-2cc12c7aae86" />

Q6.
1. Find commit history

Command:
git log --oneline

- Shows the commit history in short form.
- Shows commit ID and commit message.


2. Cherry-pick one commit

Command:
git cherry-pick <commit_id>

- Applies the changes of one specific commit to the current branch.
- Creates a new commit.


3. Cherry-pick multiple commits

Command:
git cherry-pick <commit_id1> <commit_id2>

- Applies changes from multiple selected commits.
- Creates new commits on the current branch.


4. Cherry-pick a range

Command:
git cherry-pick <start_commit>..<end_commit>

- Cherry-picks commits after the start commit up to the end commit.
- Start commit is NOT included.


5. Cherry-pick a range including the starting commit

Command:
git cherry-pick <start_commit>^..<end_commit>

- Cherry-picks from the start commit up to the end commit.
- Start commit IS included.


6. Continue after resolving a conflict

Command:
git cherry-pick --continue

- Continues the cherry-pick after resolving a conflict.
- Used after staging the resolved files.


7. Cancel cherry-pick

Command:
git cherry-pick --abort

- Cancels the current cherry-pick.
- Returns the branch to its previous state.


8. Skip the current commit

Command:
git cherry-pick --skip

- Skips the current commit.
- Continues with the next commit.








