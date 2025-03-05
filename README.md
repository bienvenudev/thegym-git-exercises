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

## Part 2 Challenge 8 - Challenge 10

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