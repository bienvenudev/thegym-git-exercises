# Git Advanced Exercises History

## Part 1 (Challenge 8) - Part 2 Challenge 1
``` bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log -p
commit f52b92687549dd73b2db849c6c7672b8ac20d9af (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 14:38:46 2025 +0200

    Create third and fourth files

    Create Third File

    Create fourth file

diff --git a/test3.md b/test3.md
new file mode 100644
index 0000000..e69de29
diff --git a/test4.md b/test4.md
new file mode 100644
index 0000000..e69de29

commit db62affe4d35097c710d2f5ac2924793b0d9e4e4
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

diff --git a/test1.md b/test1.md
new file mode 100644
index 0000000..e69de29
diff --git a/test2.md b/test2.md
new file mode 100644
index 0000000..e69de29

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git rebase -i HEAD
error: nothing to do

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git rebase -i HEAD~
Successfully rebased and updated refs/heads/main.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git rebase -i --root
Successfully rebased and updated refs/heads/main.


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log
commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

commit d83950218d1b0f53e832b96ab167910d3343f8f2
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 14:38:46 2025 +0200

    Create third and fourth files

:...skipping...
commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

commit d83950218d1b0f53e832b96ab167910d3343f8f2
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 14:38:46 2025 +0200

    Create third and fourth files

    Create Third File

    Create fourth file
~
~

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log
commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

commit d83950218d1b0f53e832b96ab167910d3343f8f2
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 14:38:46 2025 +0200

    Create third and fourth files

    Create Third File

    Create fourth file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout -b ft/branch
Switched to a new branch 'ft/branch'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ touch test5.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git status
On branch ft/branch
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test5.md

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git add test5.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch cae9514] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log
commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

commit d83950218d1b0f53e832b96ab167910d3343f8f2
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 14:38:46 2025 +0200

    Create third and fourth files

    Create Third File

    Create fourth file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/branch 
Switched to branch 'ft/branch'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git log
commit cae9514e7f0b778c45bef31b558a00a6f7c28320 (HEAD -> ft/branch)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 16:00:56 2025 +0200

    Implemented test 5

commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Mon Mar 3 12:26:16 2025 +0200

    chore: Create first and second files

    chore: Create initial file

    chore: Create second file

commit d83950218d1b0f53e832b96ab167910d3343f8f2

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git log --oneline
cae9514 (HEAD -> ft/branch) Implemented test 5
3ec78ad (main) chore: Create first and second files
d839502 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/branch)
$ git checkout main
Switched to branch 'main'
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git cherry-pick --no-commit cae9514

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --graph
* commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
| Author: bienvenudev <cbienvenu007@gmail.com>
| Date:   Mon Mar 3 12:26:16 2025 +0200
|
|     chore: Create first and second files
|
|     chore: Create initial file
|
|     chore: Create second file
|
* commit d83950218d1b0f53e832b96ab167910d3343f8f2
  Author: bienvenudev <cbienvenu007@gmail.com>
  Date:   Mon Mar 3 14:38:46 2025 +0200

      Create third and fourth files

:...skipping...
* commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
| Author: bienvenudev <cbienvenu007@gmail.com>
| Date:   Mon Mar 3 12:26:16 2025 +0200
|
|     chore: Create first and second files
|
|     chore: Create initial file
|
|     chore: Create second file
|
* commit d83950218d1b0f53e832b96ab167910d3343f8f2
  Author: bienvenudev <cbienvenu007@gmail.com>
  Date:   Mon Mar 3 14:38:46 2025 +0200

      Create third and fourth files

      Create Third File

      Create fourth file
~
~
~


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --graph --oneline
* 3ec78ad (HEAD -> main) chore: Create first and second files
* d839502 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --graph --oneline --decorate
* 3ec78ad (HEAD -> main) chore: Create first and second files
* d839502 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --graph
* commit 3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f (HEAD -> main)
| Author: bienvenudev <cbienvenu007@gmail.com>
| Date:   Mon Mar 3 12:26:16 2025 +0200
|
|     chore: Create first and second files
|
|     chore: Create initial file
|
|     chore: Create second file
|
* commit d83950218d1b0f53e832b96ab167910d3343f8f2
  Author: bienvenudev <cbienvenu007@gmail.com>
  Date:   Mon Mar 3 14:38:46 2025 +0200

      Create third and fourth files

      Create Third File

      Create fourth file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git reflog
3ec78ad (HEAD -> main) HEAD@{0}: checkout: moving from ft/branch to main
cae9514 (ft/branch) HEAD@{1}: checkout: moving from main to ft/branch
3ec78ad (HEAD -> main) HEAD@{2}: checkout: moving from ft/branch to main
cae9514 (ft/branch) HEAD@{3}: commit: Implemented test 5
3ec78ad (HEAD -> main) HEAD@{4}: checkout: moving from main to ft/branch
3ec78ad (HEAD -> main) HEAD@{5}: rebase (finish): returning to refs/heads/main
3ec78ad (HEAD -> main) HEAD@{6}: rebase (pick): chore: Create first and second files
d839502 HEAD@{7}: rebase (pick): Create third and fourth files
6a2ffb0 HEAD@{8}: rebase (start): checkout 6a2ffb0c30a46322cc52367055e3cd44fdc11be7
f52b926 HEAD@{9}: rebase (finish): returning to refs/heads/main
f52b926 HEAD@{10}: rebase (start): checkout HEAD~
f52b926 HEAD@{11}: rebase (finish): returning to refs/heads/main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'
```

## Part 2 Challenge 8 - 10

```bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch
  ft/branch
  ft/new-branch-from-commit
* main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git rebase ft/new-branch-from-commit 
Successfully rebased and updated refs/heads/main.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log
commit 5cb885aad7ebbda8915c8bef2702c74efceb7191 (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200

    Implemented core functionality for new feature

commit d87d82680f905dd4de0692a93c93bf1f7e10a0c0 (ft/new-branch-from-commit)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 14:19:48 2025 +0200

    Updated project readme

commit 1dbf205a0d0c23b256152f8682a7da6e4a77e8a8
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:58:16 2025 +0200


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch -m ft/new-branch-from-commit ft/improved-branch-name

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch
  ft/branch
  ft/improved-branch-name
* main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log
commit 5cb885aad7ebbda8915c8bef2702c74efceb7191 (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200

    Implemented core functionality for new feature

commit d87d82680f905dd4de0692a93c93bf1f7e10a0c0 (ft/improved-branch-name)
commit 5cb885aad7ebbda8915c8bef2702c74efceb7191 (HEAD -> main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200

    Implemented core functionality for new feature

commit d87d82680f905dd4de0692a93c93bf1f7e10a0c0 (ft/improved-branch-name)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 14:19:48 2025 +0200

    Updated project readme

commit 1dbf205a0d0c23b256152f8682a7da6e4a77e8a8
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:58:16 2025 +0200


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --oneline
5cb885a (HEAD -> main) Implemented core functionality for new feature
d87d826 (ft/improved-branch-name) Updated project readme
1dbf205 create readme file
3ec78ad chore: Create first and second files
d839502 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout 1dbf205
Note: switching to '1dbf205'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 1dbf205 create readme file
```

## Part 3 Challenge 1 - 10

```bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git stash list
stash@{0}: WIP on main: 0f03060 add part 2 bundles

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   readme1.md


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch
  ft/branch
  ft/improved-branch-name
* main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/improved-branch-name
M       readme1.md
Switched to branch 'ft/improved-branch-name'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/improved-branch-name)
$ git checkout main
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout -b ft/merge-conflict
Switched to a new branch 'ft/merge-conflict'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git checkout main
M       readme1.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch ft/
ft/branch                 ft/improved-branch-name   ft/merge-conflict 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git branch ft/branch 
fatal: a branch named 'ft/branch' already exists

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/branch
error: Your local changes to the following files would be overwritten by checkout:
        readme1.md
Please commit your changes or stash them before you switch branches.
Aborting

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   readme1.md

no changes added to commit (use "git add" and/or "git commit -a")

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git add readme1.md 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/merge-conflict 
M       readme1.md
Switched to branch 'ft/merge-conflict'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git add readme1.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git status
On branch ft/merge-conflict
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   readme1.md


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git checkout main 
M       readme1.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   readme1.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   readme1.md
rcises (main)
$ git add readme1.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git commit -m 'modify line 2'
[main d01c143] modify line 2
 1 file changed, 3 insertions(+), 1 deletion(-)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/merge-conflict
Switched to branch 'ft/merge-conflict'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git add readme1.md 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git commit -m "modify line 2 to cause conflict"
[ft/merge-conflict 4633b34] modify line 2 to cause conflict
 1 file changed, 2 insertions(+), 1 deletion(-)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/merge-conflict 
error: Your local changes to the following files would be overwritten by checkout:
        readme1.md
Please commit your changes or stash them before you switch branches.
Aborting

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/merge-conflict 
rcises (ft/merge-conflict)
$ git checkout -
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git merge ft/merge-conflict
Auto-merging readme1.md
CONFLICT (content): Merge conflict in readme1.md
Automatic merge failed; fix conflicts and then commit the result.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main|MERGING)   
$ git merge ft/merge-conflict 
Already up to date.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git checkout ft/merge-conflict 
Switched to branch 'ft/merge-conflict'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git pull origin main 
From https://github.com/bienvenudev/thegym-git-exercises
 * branch            main       -> FETCH_HEAD
Already up to date.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git log
commit 4633b344c67f86491ee6a93125c0bcec249609bb (HEAD -> ft/merge-conflict)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 11:39:28 2025 +0200

    modify line 2 to cause conflict

commit 0f03060f81b1017e011d430d0e5d9980279d4181 (origin/main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 11:29:29 2025 +0200

    add part 2 bundles

commit 5cb885aad7ebbda8915c8bef2702c74efceb7191
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200


cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git fetch origin main
From https://github.com/bienvenudev/thegym-git-exercises
 * branch            main       -> FETCH_HEAD

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git log
commit 4633b344c67f86491ee6a93125c0bcec249609bb (HEAD -> ft/merge-conflict)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 11:39:28 2025 +0200

    modify line 2 to cause conflict

commit 0f03060f81b1017e011d430d0e5d9980279d4181 (origin/main)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 11:29:29 2025 +0200

    add part 2 bundles

commit 5cb885aad7ebbda8915c8bef2702c74efceb7191
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200


rcises (ft/merge-conflict)
$ git merge main
Updating 4633b34..f57cae1
Fast-forward
 readme1.md | 2 ++
 1 file changed, 2 insertions(+)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (ft/merge-conflict)
$ git checkout -
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing added to commit but untracked files present (use "git add" to track)   

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git add .gitignore

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git commit -m "add tmp to git ignore"
[main f1cb349] add tmp to git ignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git tag v1.0

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --oneline 
f1cb349 (HEAD -> main, tag: v1.0) add tmp to git ignore
f57cae1 (ft/merge-conflict) Merge branch 'ft/merge-conflict'
4633b34 modify line 2 to cause conflict
d01c143 modify line 2
0f03060 (origin/main) add part 2 bundles
5cb885a Implemented core functionality for new feature
d87d826 (ft/improved-branch-name) Updated project readme
1dbf205 create readme file
3ec78ad chore: Create first and second files
d839502 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git tag
v1.0

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git show v1.0 
commit f1cb34988aeb5f8965548fa49602ef6e3ee7a7d4 (HEAD -> main, tag: v1.0)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 11:58:47 2025 +0200

    add tmp to git ignore

diff --git a/.gitignore b/.gitignore
new file mode 100644
index 0000000..cad2309
--- /dev/null
+++ b/.gitignore
@@ -0,0 +1 @@
+/tmp
\ No newline at end of file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ $ git log --pretty=oneline
bash: $: command not found

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git log --pretty=oneline
f1cb34988aeb5f8965548fa49602ef6e3ee7a7d4 (HEAD -> main, tag: v1.0) add tmp to git ignore
f57cae107581723a39a3e02319ce1a1e05d422f2 (ft/merge-conflict) Merge branch 'ft/merge-conflict'
4633b344c67f86491ee6a93125c0bcec249609bb modify line 2 to cause conflict       
d01c14324233ce24e262ffc2ea40451bb8251b62 modify line 2
0f03060f81b1017e011d430d0e5d9980279d4181 (origin/main) add part 2 bundles      
5cb885aad7ebbda8915c8bef2702c74efceb7191 Implemented core functionality for new feature
d87d82680f905dd4de0692a93c93bf1f7e10a0c0 (ft/improved-branch-name) Updated project readme
1dbf205a0d0c23b256152f8682a7da6e4a77e8a8 create readme file
3ec78ad1374b7a2fec7eb7f19c15f69989e92f4f chore: Create first and second files  
d83950218d1b0f53e832b96ab167910d3343f8f2 Create third and fourth files

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git tag -a v0.7 5cb885a

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git tag
v0.7
v1.0

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git show v0.7 
tag v0.7
Tagger: bienvenudev <cbienvenu007@gmail.com>
Date:   Wed Mar 5 12:03:48 2025 +0200

my version 0.7

commit 5cb885aad7ebbda8915c8bef2702c74efceb7191 (tag: v0.7)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Mar 4 12:59:44 2025 +0200

    Implemented core functionality for new feature

diff --git a/feature.txt b/feature.txt
new file mode 100644
index 0000000..b697352
--- /dev/null

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git tag -d v0.7 
Deleted tag 'v0.7' (was 774d47c)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git push origin main 
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (12/12), 1.17 KiB | 399.00 KiB/s, done.
Total 12 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), completed with 1 local object.
To https://github.com/bienvenudev/thegym-git-exercises.git
   0f03060..f1cb349  main -> main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/thegym-git-exercises (main)
$ git push
Everything up-to-date

```