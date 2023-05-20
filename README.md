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
<h1>
	Bundle3 -1
</h1>

```

$ git checkout -b ft/team-page

Switched to a new branch 'ft/team-page'

$ git add team.html 

$ git commit -m "updating team.html"
"
[ft/team-page 26b6d14] updating team.html
 1 file changed, 10 insertions(+), 1 deletion(-)

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 

$ git push -u origin ft/team-page 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 29, done.
Counting objects: 100% (28/28), done.
Delta compression using up to 4 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (25/25), 6.21 KiB | 2.07 MiB/s, done.
Total 25 (delta 9), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (9/9), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/team-page
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.

$ git checkout master 

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

$ git checkout -b ft/contact-page

Switched to a new branch 'ft/contact-page'

$ git checkout ft/team-page 

Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

$ git log

commit 26b6d14ef5871baf5ec2bd00927903b03e3051c8 (HEAD -> ft/team-page, origin/ft/team-page)
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:38:39 2023 +0200

    updating team.html

commit 14a2862c65c8515380497e68a99257e8d9d2e571 (origin/master, master, ft/contact-page)
Merge: f98734b 69c527f
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:20:13 2023 +0200

    Merge remote-tracking branch 'refs/remotes/origin/master'

commit f98734b03641a8b380a9e53b83a0134a48d0fa47
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:18:34 2023 +0200

    service.html v2

commit 69c527f0b9c37626f54a5b78a6f7a0a63cde04d7
Author: yves173 <59310013+yves173@users.noreply.github.com>
Date:   Tue May 16 14:39:04 2023 +0200

$ git checkout ft/contact-page 

Switched to branch 'ft/contact-page'

$ git cherry-pick 26b6d14ef5871baf5ec2bd00927903b03e3051c8

[ft/contact-page ad01b9d] updating team.html
 Date: Fri May 19 14:38:39 2023 +0200
 1 file changed, 10 insertions(+), 1 deletion(-)

$ git add contact.html 

$ git commit -m "add contact.html"

[ft/contact-page 4bd95c2] add contact.html
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html

$ git push -u origin ft/contact-page 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 31, done.
Counting objects: 100% (30/30), done.
Delta compression using up to 4 threads
Compressing objects: 100% (26/26), done.
Writing objects: 100% (27/27), 6.40 KiB | 2.13 MiB/s, done.
Total 27 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/contact-page
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.

$ git checkout -b ft/faq-page

Switched to a new branch 'ft/faq-page'

$ git add faq.html 

$ git commit -m "add faq.html"

[ft/faq-page 77fdf1c] add faq.html
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

$ git push -u origin ft/faq-page 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 33, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 4 threads
Compressing objects: 100% (28/28), done.
Writing objects: 100% (29/29), 6.57 KiB | 1.64 MiB/s, done.
Total 29 (delta 11), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (11/11), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/faq-page
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.

$ git checkout ft/team-page 

Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

$ git log

commit 26b6d14ef5871baf5ec2bd00927903b03e3051c8 (HEAD -> ft/team-page, origin/ft/team-page)
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:38:39 2023 +0200

    updating team.html

commit 14a2862c65c8515380497e68a99257e8d9d2e571 (origin/master, master)
Merge: f98734b 69c527f
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:20:13 2023 +0200

    Merge remote-tracking branch 'refs/remotes/origin/master'

commit f98734b03641a8b380a9e53b83a0134a48d0fa47
Author: yves173 <ykwizera67@gmail.com>
Date:   Fri May 19 14:18:34 2023 +0200

    service.html v2

commit 69c527f0b9c37626f54a5b78a6f7a0a63cde04d7
Author: yves173 <59310013+yves173@users.noreply.github.com>
Date:   Tue May 16 14:39:04 2023 +0200

$ git revert 26b6d14ef5871baf5ec2bd00927903b03e3051c8

[ft/team-page c46d5f1] Revert "updating team.html"
 1 file changed, 1 insertion(+), 10 deletions(-)

$ git push -u origin ft/team-page 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
To https://github.com/yves173/bundle1_2.git
 ! [rejected]        ft/team-page -> ft/team-page (fetch first)
error: failed to push some refs to 'https://github.com/yves173/bundle1_2.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

$ git pull origin 

remote: Enumerating objects: 27, done.
remote: Counting objects: 100% (24/24), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 15 (delta 6), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (15/15), 6.59 KiB | 1.32 MiB/s, done.
From https://github.com/yves173/bundle1_2
   26b6d14..d412f3c  ft/team-page        -> origin/ft/team-page
   4bd95c2..ab8f04e  ft/contact-page     -> origin/ft/contact-page
   d594089..9ad1a7c  ft/service-redesign -> origin/ft/service-redesign
   14a2862..3ab6129  master              -> origin/master
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

Auto-merging team.html
CONFLICT (content): Merge conflict in team.html
Automatic merge failed; fix conflicts and then commit the result.

$ git merge

fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

$ git add .

$ git commit -m "merged update"

[ft/team-page 37e2b9b] merged update

$ git push -u origin ft/team-page 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 601 bytes | 601.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/yves173/bundle1_2.git
   d412f3c..37e2b9b  ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.

```

<h1>
	Bundle3 -2
</h1>

```

$ git checkout ft/faq-page 

Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

$ git checkout -b ft/home-page-redesign

Switched to a new branch 'ft/home-page-redesign'

$ git checkout master

Switched to branch 'master'
Your branch is behind 'origin/master' by 12 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

$ git add .

$ git commit -m "update and change on main"

[master 0263d61] update and change on main
 2 files changed, 24 insertions(+)
 create mode 100644 contact.html
 create mode 100644 faq.html

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
To https://github.com/yves173/bundle1_2.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/yves173/bundle1_2.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

$ git pull origin

remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (5/5), 2.90 KiB | 1.45 MiB/s, done.
From https://github.com/yves173/bundle1_2
   3ab6129..3939fa8  master     -> origin/master
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
 README.md  | 398 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html |   9 +-
 home.html  |   9 +-
 team.html  |  12 ++-
 4 files changed, 425 insertions(+), 3 deletions(-)

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 463 bytes | 463.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/yves173/bundle1_2.git
   3939fa8..a31b104  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

$ git checkout ft/home-page-redesign

Switched to branch 'ft/home-page-redesign'

$ git rebase master ft/home-page-redesign 

Successfully rebased and updated refs/heads/ft/home-page-redesign.

$ git add home.html 

$ git commit -m "changes on home.html"

[ft/home-page-redesign c66bc2c] changes on home.html
 1 file changed, 1 insertion(+)

$ git push -u origin ft/home-page-redesign
 
Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 24, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 4.20 KiB | 2.10 MiB/s, done.
Total 12 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), completed with 4 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/home-page-redesign
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
Branch 'ft/home-page-redesign' set up to track remote branch 'ft/home-page-redesign' from 'origin'.

```

<h1>
	Bundle4 -1
</h1>

```

$ git checkout master 

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

$ git remote add git-copy https://github.com/yves173/bundle1_2_1.git

$ git add home.html 

$ git commit -m "add some changes on home.html"

[master d192630] add some changes on home.html
 1 file changed, 1 insertion(+)

$ git push -u origin master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 579 bytes | 579.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/yves173/bundle1_2.git
   7ab203f..5258cee  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

$ git push -u git-copy master 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 87, done.
Counting objects: 100% (87/87), done.
Delta compression using up to 4 threads
Compressing objects: 100% (83/83), done.
Writing objects: 100% (87/87), 20.52 KiB | 1.71 MiB/s, done.
Total 87 (delta 34), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (34/34), done.
To https://github.com/yves173/bundle1_2_1.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'git-copy'.

```

<h1>
	Bundle4 -2
</h1>

```
$ git checkout -b ft/footer

Switched to a new branch 'ft/footer'

$ git add .

$ git commit -m "add some changes on home.html"

[ft/footer 5e284e3] add some changes on home.html
 1 file changed, 1 insertion(+)

$ git add .

$ git commit -m "new change on home.html"

[ft/footer 36858ed] new change on home.html
 1 file changed, 1 insertion(+), 1 deletion(-)

$ git push origin ft/footer

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 27, done.
Counting objects: 100% (25/25), done.
Delta compression using up to 4 threads
Compressing objects: 100% (18/18), done.
Writing objects: 100% (18/18), 3.70 KiB | 1.85 MiB/s, done.
Total 18 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), completed with 3 local objects.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/footer
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/footer -> ft/footer

$ git checkout master 

Switched to branch 'master'
Your branch is up to date with 'git-copy/master'.

$ git checkout -b ft/squashing

Switched to a new branch 'ft/squashing'

$ git merge --squash ft/footer

Updating 5258cee..36858ed
Fast-forward
Squash commit -- not updating HEAD
 home.html | 1 +
 1 file changed, 1 insertion(+)

$ git status

On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   home.html

$ git commit -m "Footer changes squashing"

[ft/squashing fb3f95c] Footer changes squashing
 1 file changed, 1 insertion(+)

$ git push -u origin ft/squashing 

Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 311 bytes | 311.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/yves173/bundle1_2/pull/new/ft/squashing
remote: 
To https://github.com/yves173/bundle1_2.git
 * [new branch]      ft/squashing -> ft/squashing
Branch 'ft/squashing' set up to track remote branch 'ft/squashing' from 'origin'.

```


<h1>
	Bundle5 -1
</h1>
<br><br>
<span>To Check my github page Enabled:  <span>
<a href="https://yves173.github.io/bundle1_2/">Click here</a>
