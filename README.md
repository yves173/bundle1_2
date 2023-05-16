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
