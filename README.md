# GIT Exercise

## Bundle 1

### Exercise 1

```bash

$ git init
Initialized empty Git repository in C:/Users/PC/Downloads/gym-exercise1/.git/

 (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

 (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html.txt
        script.js.txt

nothing added to commit but untracked files present (use "git add" to track)

 (master)
$ git branch -m master main

 (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html.txt
        script.js.txt

nothing added to commit but untracked files present (use "git add" to track)

 (main)
$ git add .

 (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html.txt
        new file:   script.js.txt


 (main)
$ git commit -m "Add new files"
[main (root-commit) 621a549] Add new files
 2 files changed, 33 insertions(+)
 create mode 100644 index.html.txt
 create mode 100644 script.js.txt

 (main)
$ git remote add origin https://github.com/Will24300/gym-exercise1.git
git branch -M main
git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 883 bytes | 441.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Will24300/gym-exercise1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

 (main)
$ git checkout -b div
Switched to a new branch 'div'

 (div)
$ git branch -m div dev

 (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Will24300/gym-exercise1/pull/new/dev
remote:
To https://github.com/Will24300/gym-exercise1.git
 * [new branch]      dev -> dev

 (dev)
$ git checkout -b test
Switched to a new branch 'test'

 (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Will24300/gym-exercise1/pull/new/test
remote:
To https://github.com/Will24300/gym-exercise1.git
 * [new branch]      test -> test

 (test)
$ git checkout dev
Switched to branch 'dev'

 (dev)
$ git branch -d test
Deleted branch test (was 621a549).

 (dev)
$ git push origin --delete dev
To https://github.com/Will24300/gym-exercise1.git
 - [deleted]         dev
```
