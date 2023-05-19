<h1>
Bundle1-2
</h1>

```
$ echo "<html><body><h1>Welcome to the Home Page</h1></body></html>" > home.html

$ git init

hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/green/Desktop/Magnun Opus/the gym/git projects/bundle 1/exercise 2/.git/
  
$ touch README.md
  
$ git add .
  
$ git commit -m "add home.html"
  
[master (root-commit) 1420caa] add home.html
 2 files changed, 1 insertion(+)
 create mode 100644 README.md
 create mode 100644 home.html
  
$ git stash save "stash changes for home.html"
  
Saved working directory and index state On master: stash changes for home.html
  
$ echo "<html><body><h1>About Us</h1></body></html>" > about.html
  
$ git add about.html 
  
$ git commit -m "add about.html"
  
[master fa1cad7] add about.html
 1 file changed, 1 insertion(+)
 create mode 100644 about.html
  
$ git stash save "stash changes for about.html"
  
Saved working directory and index state On master: stash changes for about.html
  
$ echo "<html><body><h1>Our Team</h1></body></html>" > team.html
  
$ git add team.html 
  
$ git commit -m "add team.html"
  
[master 026a93a] add team.html
 1 file changed, 1 insertion(+)
 create mode 100644 team.html
  
$ git stash save "stash changes for team.html"
  
Saved working directory and index state On master: stash changes for team.html
  
$ git stash list 
  
stash@{0}: On master: stash changes for team.html
stash@{1}: On master: stash changes for about.html
stash@{2}: On master: stash changes for home.html
  
$ git stash pop stash@{1}
  
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (09a2f4e2e7701dd659be1104e09d1a853b7a6424)
  
$ git stash list 
  
stash@{0}: On master: stash changes for team.html
stash@{1}: On master: stash changes for home.html
  
$ git stash pop stash@{1} 
  
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.html
	modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (12d65da90950af0dfa4e54c456494b8aac3c99f7)
  
$ git remote add origin https://github.com/yves173/bundle1_2.git
  
$ git push -u origin master 
  
Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 862 bytes | 862.00 KiB/s, done.
Total 10 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/yves173/bundle1_2.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
  
$ git stash pop stash@{0} 
  
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.html
	modified:   home.html
	modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{0} (dea6fb41963e88ce07371ccaad844d46fb1d1d36)
  
$ git log
  
commit 026a93a01a358a55ec93814a264be47870660bef (HEAD -> master, origin/master)
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue May 16 12:06:40 2023 +0200

    add team.html

commit fa1cad77549c50ba50e281b59a00da57269313e9
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue May 16 12:04:41 2023 +0200

    add about.html

commit 1420caa069a46f7526d93cf2c34108bfc8941499
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue May 16 12:02:09 2023 +0200

    add home.html
  
$ git reset HEAD^
  
Unstaged changes after reset:
M	about.html
M	home.html
  
$ git log
  
commit fa1cad77549c50ba50e281b59a00da57269313e9 (HEAD -> master)
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue May 16 12:04:41 2023 +0200

    add about.html

commit 1420caa069a46f7526d93cf2c34108bfc8941499
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue May 16 12:02:09 2023 +0200

    add home.html
```

<h1> 
Bundle2 -1
</h1>

```
$ git checkout -b ft/bundle-2

Switched to a new branch 'ft/bundle-2'

$ echo "<html><body><h1>Our Services</h1></body></html>" > services.html

$ git add services.html 

$ git commit -m "add service.html"

[ft/bundle-2 b61ff94] add service.html
 1 file changed, 1 insertion(+)
 create mode 100644 services.html
 
$ git push -u origin ft/bundle-2 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 874 bytes | 874.00 KiB/s, done.
Total 10 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/bundle-2
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
```

<h1>
	Bundle2 -2
</h1>

```

$ git checkout master 

M	about.html
M	home.html
Switched to branch 'master'
Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
  
$ git pull origin

remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (17/17), done.
remote: Compressing objects: 100% (14/14), done.
remote: Total 14 (delta 5), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (14/14), 5.04 KiB | 1.26 MiB/s, done.
From https://github.com/yves173/bundle1_2
   026a93a..69c527f  master     -> origin/master
Updating fa1cad7..69c527f
error: The following untracked working tree files would be overwritten by merge:
	team.html
Please move or remove them before you merge.
Aborting

$ git checkout -b ft/service-redesign

Switched to a new branch 'ft/service-redesign'

$ git add .

$ git commit -m "add service.html"

[ft/service-redesign d594089] add service.html
 4 files changed, 37 insertions(+), 2 deletions(-)
 create mode 100644 service.html
 create mode 100644 team.html

$ git push -u origin ft/service-redesign 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 720 bytes | 720.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/service-redesign
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
$ git checkout main
error: pathspec 'main' did not match any file(s) known to git

$ git checkout master 

Switched to branch 'master'
Your branch is behind 'origin/master' by 7 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

$ git status

On branch master
Your branch is behind 'origin/master' by 7 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	service.html

nothing added to commit but untracked files present (use "git add" to track)

$ git add service.html 

$ git commit -m "service.html v2"

[master f98734b] service.html v2
 1 file changed, 12 insertions(+)
 create mode 100644 service.html

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
To https://github.com/yves173/bundle1_2.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/yves173/bundle1_2.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

$ git pull origin 

hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge (the default strategy)
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.

$ git merge

Merge made by the 'ort' strategy.
 README.md     | 209 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 services.html |   1 +
 team.html     |   1 +
 3 files changed, 211 insertions(+)
 create mode 100644 services.html
 create mode 100644 team.html

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 732 bytes | 732.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/yves173/bundle1_2.git
   69c527f..14a2862  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

```
