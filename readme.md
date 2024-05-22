# Part 1
## Challenge 6
```bash
 git add unwanted.txt
 git commit -m 'Unwanted commit'
[main f8e3afb] Unwanted commit
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt
 git rebase -i --root
Successfully rebased and updated refs/heads/main.
 git reflog
0f72441 (HEAD -> main) HEAD@{0}: rebase (finish): returning to refs/heads/main
0f72441 (HEAD -> main) HEAD@{1}: rebase: fast-forward
1d736f2 HEAD@{2}: rebase: fast-forward
06c46fa HEAD@{3}: rebase: fast-forward
c11ad69 HEAD@{4}: rebase (start): checkout c11ad69d0776fb22c5f083721840c114558690cd
f8e3afb HEAD@{5}: commit: Unwanted commit
0f72441 (HEAD -> main) HEAD@{6}: rebase (finish): returning to refs/heads/main
0f72441 (HEAD -> main) HEAD@{7}: rebase (pick): chore: Create fourth file
1d736f2 HEAD@{8}: rebase (pick): chore: Create third file
06c46fa HEAD@{9}: rebase (squash): chore: Create initial file
88fe284 HEAD@{10}: rebase: fast-forward
7ccd276 HEAD@{11}: rebase (start): checkout 7ccd276f4d1b5eb7826182bba855e646828314b9
a337adc HEAD@{12}: rebase (finish): returning to refs/heads/main
 git log
commit 0f724410151b39f65cb5d80d5bf30f43efee58ef (HEAD -> main)
Author: Alexia Christelle <christellealexia53@gmail.com>
Date:   Tue May 21 17:25:32 2024 +0200

    chore: Create fourth file

commit 1d736f267eff3300ca7c7592e6f63e8a2f99aa97
Author: Alexia Christelle <christellealexia53@gmail.com>
Date:   Tue May 21 17:15:48 2024 +0200

    chore: Create third file

commit 06c46fafae1a711bae3e6879d1deedc59cd0fe43
 
 git log --oneline 
0f72441 (HEAD -> main) chore: Create fourth file
1d736f2 chore: Create third file
06c46fa chore: Create initial file
 
```
## Challenge 7
```bash
 git rebase -i --root
interactive rebase in progress; onto 85356b4
Last commands done (3 commands done):
   pick 1d736f2 chore: Create third file
   pick 1d736f2 chore: Create third file
  (see more in file .git/rebase-merge/done)
No commands remaining.
You are currently rebasing branch 'main' on '85356b4'.
  (all conflicts fixed: run "git rebase --continue")

Untracked files:

  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git rebase --skip'
Could not apply 1d736f2... chore: Create third file
 git rebase --abort
 git rebase -i --root
Successfully rebased and updated refs/heads/main.
 git log --oneline
196e5b8 (HEAD -> main) chore: Create third file
0853d8e chore: Create initial file
3e91478 chore: Create fourth file
 
```
### Challenge 8
```bash
 git checkout -b ft/branch
Switched to a new branch 'ft/branch'
 git add test5.md
 git commit -m 'Implemented test 5'
[ft/branch 5adcb9a] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
 git log --oneline
5adcb9a (HEAD -> ft/branch) Implemented test 5
196e5b8 (main) chore: Create third file
0853d8e chore: Create initial file
3e91478 chore: Create fourth file
 git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)
 git cherry-pick 5adcb9a
[main e682db3] Implemented test 5
 Date: Wed May 22 15:32:21 2024 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
 
```