
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

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo > README.md

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo my name is Cynthia > index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ ls
README.md  index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo this repository is going to include a number of exercises done with an aim to check my git knowledge. >> README.md

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ echo This index file is going to help us with receiving an amount of text. >> index.html

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   index.html


user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git commit -m "Added new files to my repo and added content to them"
[main (root-commit) b3f862d] Added new files to my repo and added content to them
 2 files changed, 3 insertions(+)
 create mode 100644 README.md
 create mode 100644 index.html
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git clone https://github.com/cynthia-stac/Git-Knowledge.git
Cloning into 'Git-Knowledge'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.
user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main|REBASE 1/1)
$ git remote add origin https://github.com/cynthia-stac/Git-Knowledge.git
error: remote origin already exists.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main|REBASE 1/1)
$ git pull origin main --rebase
From https://github.com/cynthia-stac/Git-Knowledge
 * branch            main       -> FETCH_HEAD
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


$ git rebase --continue

Successfully rebased and updated refs/heads/main.

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git push origin main
fatal: unable to access 'https://github.com/cynthia-stac/Git-Knowledge.git/': Recv failure: Connection was reset

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 427 bytes | 427.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/cynthia-stac/Git-Knowledge.git
   b5ffda9..8a7f10e  main -> main

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
$ git branch dev

user@LAPTOP-KQSA7V3I MINGW64 ~/gitExercise (main)
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


