
# Gym Git Exercise Solutions
Exercises that help me test my skills already acquired while learning the git basics
## Bundle 1
### Exercise 1
```bash
   user@LAPTOP-KQSA7V3I MINGW64 ~
$ mkdir gitExercise

user@LAPTOP-KQSA7V3I MINGW64 ~
$ cd gitExercise

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise
$ git init
Initialized empty Git repository in C:/Users/user/gitExercise/.git/

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo > README.md

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo my name is Cynthia > index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ ls
README.md  index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo this repository is going to include a number of exercises done with an aim to check my git knowledge. >> README.md

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo This index file is going to help us with receiving an amount of text. >> index.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git status
On branch(dev

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   index.html


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git commit -m "Added new files to my repo and added content to them"
(dev (root-commit) b3f862d] Added new files to my repo and added content to them
 2 files changed, 3 insertions(+)
 create mode 100644 README.md
 create mode 100644 index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git clone https://github.com/cynthia-stac/Git-Knowledge.git
Cloning into 'Git-Knowledge'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev|REBASE 1/1)
$ git remote add origin https://github.com/cynthia-stac/Git-Knowledge.git
error: remote origin already exists.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev|REBASE 1/1)
$ git pull origin(dev --rebase
From https://github.com/cynthia-stac/Git-Knowledge
 * branch           (dev       -> FETCH_HEAD
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


$ git rebase --continue

Successfully rebased and updated refs/heads(dev.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git push origin(dev
fatal: unable to access 'https://github.com/cynthia-stac/Git-Knowledge.git/': Recv failure: Connection was reset

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git push origin(dev
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 427 bytes | 427.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/cynthia-stac/Git-Knowledge.git
   b5ffda9..8a7f10e (dev ->(dev

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git branch dev

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git checkout dev
M       Git-Knowledge
Switched to branch 'dev'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git branch test

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git checkout test
M       Git-Knowledge
Switched to branch 'test'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (test)
$ git checkout dev
M       Git-Knowledge
Switched to branch 'dev'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git branch -D test
Deleted branch test (was 8a7f10e).




```
### Exercise 2
```bash
user@LAPTOP-KQSA7V3I MINGW64 ~
$ cd gitExercise

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git checkout(dev)
M       Git-Knowledge
Switched to branch (dev)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo > home.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ code /

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ code .

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Git-Knowledge (modified content)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

no changes added to commit (use "git add" and/or "git commit -a")

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git add home.html
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash
Saved working directory and index state WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo > about.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git add about.html
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash
Saved working directory and index state WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ echo > team.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git add team.html
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash
Saved working directory and index state WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash list
stash@{0}: WIP on(dev: 8a7f10e Updated files)
stash@{1}: WIP on(dev: 8a7f10e Updated files)
stash@{2}: WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash pop stash@{1}
On branch(dev)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Git-Knowledge (modified content)

Dropped stash@{1} (47c77d1a6b658042ba2bb986b655b140c1b16011)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 2 entries

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash list
stash@{0}: WIP on(dev: 8a7f10e Updated files)
stash@{1}: WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash pop stash@{1}
On branch(dev)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Git-Knowledge (modified content)

Dropped stash@{1} (827beddc6d61aabe66f87fd61e7a0ee4b791308d)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git commit -m "Added new files"
(dev b5c6fdd] Added new files)
 2 files changed, 19 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev|MERGING)
$ git commit -m "Added a readme file"
(dev 1f256b5] Added a readme file)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git push origin(dev)
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 996 bytes | 332.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/cynthia-stac/Git-Knowledge.git
   aaf72ac..1f256b5 (dev ->(dev))

   user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash list
stash@{0}: WIP on(dev: 8a7f10e Updated files)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git stash pop stash@{0}
On branch(dev)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Git-Knowledge (modified content)

Dropped stash@{0} (6bcfa8375468173fb52daedb01eec2e2b7660dcb)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git reset --hard
HEAD is now at 07a164b Added new lines to readme file

```

## Bundle 2
### Exercise 1

```bash
   user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git branch ft/bundle-2

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo services.html
services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo > services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git add services
fatal: pathspec 'services' did not match any files

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git commit -m "Added a new file and made some changes"
[main e8d9cee] Added a new file and made some changes
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
* dev
  ft/bundle-2
  main
~
(END)...skipping...


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (dev)
$ git checkout ft/bundle-2
M       README.md
Switched to branch 'ft/bundle-2'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git merge main
Updating 9f38f9c..e8d9cee
Fast-forward
 services.html | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git add services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git commit -m "New paragraph added"
[ft/bundle-2 98a727e] New paragraph added
 1 file changed, 1 insertion(+)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 341 bytes | 341.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/cynthia-stac/Git-Knowledge/pull/new/ft/bundle-2
remote:
To https://github.com/cynthia-stac/Git-Knowledge.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.


```

### Exercise 2

```bash
   user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/bundle-2)
$ git checkout main
M       README.md
Switched to branch 'main'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git pull
Already up to date.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git branch ft/service-redesign

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git add services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git commit -m "Added new content"
[ft/service-redesign 5e926f1] Added new content
 1 file changed, 3 insertions(+)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 363 bytes | 363.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/cynthia-stac/Git-Knowledge/pull/new/ft/service-redesign
remote:
To https://github.com/cynthia-stac/Git-Knowledge.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git add services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git commit -m "A heading was added"
[main 93d4e0d] A heading was added
 1 file changed, 1 insertion(+)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cynthia-stac/Git-Knowledge.git
   5b1cd62..93d4e0d  main -> main

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git diff main ft/service-redesign
diff --git a/services.html b/services.html
index 1fb47cd..d7a9d5d 100644
--- a/services.html
+++ b/services.html
@@ -1,3 +1,5 @@
 <p>  We offer very good services! Join us.</p>
 <p>This the addition paragraph</p>
-<h3>Rwanda</h3>
\ No newline at end of file
+<p>We haave to make new changes</p>
+
+

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        services.html
Please commit your changes or stash them before you switch branches.
Aborting

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git add services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git commit -m "Dropped a conflicting line"
[ft/service-redesign 6c946db] Dropped a conflicting line
 1 file changed, 1 insertion(+), 1 deletion(-)

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 297 bytes | 297.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cynthia-stac/Git-Knowledge.git
   5e926f1..6c946db  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.



user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main|MERGING)
$ git merge ft/service-redesign
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main|MERGING)
$ git add services.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main|MERGING)
$ git commit -m "Solved the conflict"
[main a8fca6e] Solved the conflict

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cynthia-stac/Git-Knowledge.git
   93d4e0d..a8fca6e  main -> main

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git merge ft/service-redesign
Already up to date.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/service-redesign)
$ git merge main
Updating 6c946db..a8fca6e
Fast-forward
 services.html | 4 +---
 1 file changed, 1 insertion(+), 3 deletions(-)

```

## Bundle 3

### Exercise 1

```bash
   user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ echo > team.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git add team.html
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git commit -m "Content added in a newly created file"
[ft/team-page 31c71b6] Content added in a newly created file
 1 file changed, 7 insertions(+)
 create mode 100644 team.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 171.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/cynthia-stac/Git-Knowledge/pull/new/ft/team-page
remote:
To https://github.com/cynthia-stac/Git-Knowledge.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git branch ft/contact-page

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git log
commit 31c71b63ed9147befd0a7a9cd7e33d2840010a0c (HEAD -> ft/team-page, origin/ft/team-page)
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 14:13:53 2025 +1100

    Content added in a newly created file

commit 2a7adadc8754a042aa68571511d44d79024dcac8 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 13:37:08 2025 +1100

    Submitted Exercise 2 bundle 2

commit a8fca6e630193adc4aae81b1736fd48eaf049b2f (ft/service-redesign)
Merge: 93d4e0d 6c946db
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 13:26:50 2025 +1100

    Solved the conflict

commit 6c946dbd1441493b4b0bf68e48d9a5d7de955cf6 (origin/ft/service-redesign)
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 13:07:21 2025 +1100

    Dropped a conflicting line

commit 93d4e0d21872724a79af110dee2a924b51d3c9bf
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 12:52:34 2025 +1100

    A heading was added

commit 5e926f140d1084a420ff0cfb5e52c17e581cfbf8
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 12:37:25 2025 +1100

    Added new content

commit 5b1cd62791c42a2f3ac610f188475d16a8b4c62c
Author: Cynthia Umubyeyi <umubnthia@gmail.com>
Date:   Thu Jul 31 12:17:41 2025 +1100

    Submitted exercise 1 bundle-2

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git log --oneline
31c71b6 (HEAD -> ft/team-page, origin/ft/team-page) Content added in a newly created file
2a7adad (origin/main, origin/HEAD, main, ft/contact-page) Submitted Exercise 2 bundle 2
a8fca6e (ft/service-redesign) Solved the conflict
6c946db (origin/ft/service-redesign) Dropped a conflicting line
93d4e0d A heading was added
5e926f1 Added new content
5b1cd62 Submitted exercise 1 bundle-2
98a727e (origin/ft/bundle-2, ft/bundle-2) New paragraph added
e8d9cee (dev) Added a new file and made some changes
9f38f9c Did a reset
744d998 Delete team.html
07a164b Added new lines to readme file
1f256b5 Added a readme file
b5c6fdd Added new files
aaf72ac Update README.md
8a7f10e Updated files
b5ffda9 Update README.md
0e6d30e Initial commit

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'




user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git cherry-pick 31c71b63ed9147befd0a7a9cd7e33d2840010a0c
[ft/contact-page 3f3f2cf] Content added in a newly created file
 Date: Thu Jul 31 14:13:53 2025 +1100
 1 file changed, 7 insertions(+)
 create mode 100644 team.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ echo > contact.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git add contact.html
warning: in the working copy of 'contact.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git commit -m "New content in a new branch"
[ft/contact-page 7aab5d1] New content in a new branch
 1 file changed, 2 insertions(+)
 create mode 100644 contact.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 597 bytes | 597.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/cynthia-stac/Git-Knowledge.git
   721af1b..7aab5d1  ft/contact-page -> ft/contact-page

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git branch ft/faq-page

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ echo > faq.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ git add faq.html
warning: in the working copy of 'faq.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ git commit -m "A band new file again"
[ft/faq-page 4fb93ac] A band new file again
 1 file changed, 1 insertion(+)
 create mode 100644 faq.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/cynthia-stac/Git-Knowledge/pull/new/ft/faq-page
remote:
To https://github.com/cynthia-stac/Git-Knowledge.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ git revert 31c71b63ed9147befd0a7a9cd7e33d2840010a0c
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

nothing to commit, working tree clean

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
Everything up-to-date

```
