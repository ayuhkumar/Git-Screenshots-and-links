Q1. Rebase, Merge & Merge Conflict

1. Definitions

Git Merge:

* Combines changes from two branches.
* Creates a merge commit in many cases.

Merge Conflict:

* Happens when Git cannot automatically combine changes.
* We have to resolve the conflict manually.

Git Rebase:

* Moves/replays commits of one branch on top of another branch.
* Keeps the history more linear.

2. Merge vs Rebase

Merge:

main:    A---B---C
\
feature:       D---E

main:    A---B---C---D---E---M

* Combines branches.
* May create a merge commit.

Rebase:

main:    A---B---C

feature:       D---E

After rebase:

main:    A---B---C

feature:           D'---E'

* Moves feature commits on top of main.
* Creates a cleaner, straight history.

3. Three Advantages of Rebase

* Keeps Git history clean and linear.
* Makes project history easier to understand.
* Reduces unnecessary merge commits.

4. Why Rebase is useful in real-life projects?

* Keeps feature branches updated with the latest main branch.
* Makes commit history easier to read.
* Helps developers review changes more easily.
* Useful before merging a feature into the main branch.

5. Rebase Commands

git rebase --continue

* Continues the rebase after resolving a conflict.

git rebase --abort

* Cancels the rebase.
* Returns the branch to its previous state.

git rebase --skip

* Skips the current commit causing the conflict.
* Continues the rebase.




Q2.
<img width="1156" height="257" alt="image" src="https://github.com/user-attachments/assets/5015d095-d06f-42f0-9f24-21f6e787a9bf" />
<img width="992" height="315" alt="image" src="https://github.com/user-attachments/assets/38bb5d31-ef6d-430d-ac4b-67e076cc577d" />
https://github.com/ayuhkumar/git-rebase-assignment-1
6. 
Two differences observed between Merge and Rebase
Commit history:
Merge: Creates a merge commit (Merge branch 'product-page').
Rebase: Creates a straight/linear history without a new merge commit.
Commit IDs:
Merge: Original commit IDs remain the same.
Rebase: Commits are re-created, so their commit IDs change.

Q3.

https://github.com/ayuhkumar/git-rebase-assignment-2
<img width="1531" height="960" alt="image" src="https://github.com/user-attachments/assets/8f41d219-0e7b-497d-b5c2-8d866467ee35" />
<img width="1502" height="907" alt="image" src="https://github.com/user-attachments/assets/2bf6c4b0-8ed6-4e3e-ae8b-83a587342bed" />

8.git rebase --abort cancelled the rebase process.
The student-profile branch returned to its previous state before the rebase.
The terminal no longer shows REBASE 1/2, meaning the rebase was successfully stopped.
From the git log, student-profile and main are now pointing to the same commit (5d55321).

In short: Rebase was cancelled, and the branch was restored to its previous state.


9.The skipped commit was:

Commit: d4a64b3
Message: Added email in the student-profile.txt file in student-profile Commit->G

It was skipped because Git could not apply this commit during the rebase.
After running git rebase --skip, Git ignored this commit and continued the rebase successfully.

<img width="1237" height="150" alt="image" src="https://github.com/user-attachments/assets/41a94ad1-6161-4b48-8c7f-18bd18546b55" />



<img width="1212" height="317" alt="image" src="https://github.com/user-attachments/assets/b082897e-9868-4093-ac79-9ded77f2d24e" />

<img width="1117" height="246" alt="image" src="https://github.com/user-attachments/assets/ce2a8d2c-2a5d-42e0-9bca-a0773042045b" />






















