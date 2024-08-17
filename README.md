cristiano@cris ~/D/i/github> pwd
/Users/cristiano/Documents/impacta/github
cristiano@cris ~/D/i/github> mkdir exercicio01
cristiano@cris ~/D/i/github> cd exercicio01/
cristiano@cris ~/D/i/g/exercicio01> git config --global user.name "Cristiano"
cristiano@cris ~/D/i/g/exercicio01> git config --global user.email "cristiano@gmail.com"                                     
cristiano@cris ~/D/i/g/exercicio01> git init 
Initialized empty Git repository in /Users/cristiano/Documents/impacta/github/exercicio01/.git/
cristiano@cris ~/D/i/g/exercicio01 (main)> ls -la
total 0
drwxr-xr-x  3 cristiano  staff   96 Aug  9 17:40 ./
drwxr-xr-x  3 cristiano  staff   96 Aug  9 17:39 ../
drwxr-xr-x  9 cristiano  staff  288 Aug  9 17:40 .git/
cristiano@cris ~/D/i/g/exercicio01 (main)> ls -la .git/
total 24
drwxr-xr-x   9 cristiano  staff  288 Aug  9 17:40 ./
drwxr-xr-x   3 cristiano  staff   96 Aug  9 17:40 ../
-rw-r--r--   1 cristiano  staff   21 Aug  9 17:40 HEAD
-rw-r--r--   1 cristiano  staff  137 Aug  9 17:40 config
-rw-r--r--   1 cristiano  staff   73 Aug  9 17:40 description
drwxr-xr-x  15 cristiano  staff  480 Aug  9 17:40 hooks/
drwxr-xr-x   3 cristiano  staff   96 Aug  9 17:40 info/
drwxr-xr-x   4 cristiano  staff  128 Aug  9 17:40 objects/
drwxr-xr-x   4 cristiano  staff  128 Aug  9 17:40 refs/
cristiano@cris ~/D/i/g/exercicio01 (main)> date
Fri Aug  9 17:41:14 -03 2024


cristiano@cris ~/D/i/g/exercicio01 (main)> ls -l
total 0
cristiano@cris ~/D/i/g/exercicio01 (main)> echo 01 > arquivo.txt
cristiano@cris ~/D/i/g/exercicio01 (main)> ls -l
total 8
-rw-r--r--  1 cristiano  staff  3 Aug  9 17:44 arquivo.txt
cristiano@cris ~/D/i/g/exercicio01 (main)> git add .
cristiano@cris ~/D/i/g/exercicio01 (main)> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   arquivo.txt

cristiano@cris ~/D/i/g/exercicio01 (main)> git commit -m "Add arquivo txt"
[main (root-commit) 91b6ad5] Add arquivo txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
cristiano@cris ~/D/i/g/exercicio01 (main)> git status
On branch main
nothing to commit, working tree clean
cristiano@cris ~/D/i/g/exercicio01 (main)> 
cristiano@cris ~/D/i/g/exercicio01 (main)> 
cristiano@cris ~/D/i/g/exercicio01 (main)> echo 02 > arquivo.txt 
cristiano@cris ~/D/i/g/exercicio01 (main)> git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
cristiano@cris ~/D/i/g/exercicio01 (main)> git add .
cristiano@cris ~/D/i/g/exercicio01 (main)> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt

cristiano@cris ~/D/i/g/exercicio01 (main)> git diff
cristiano@cris ~/D/i/g/exercicio01 (main)> echo 03 > arquivo.txt 
cristiano@cris ~/D/i/g/exercicio01 (main)> git diff 
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03
cristiano@cris ~/D/i/g/exercicio01 (main)> git restore .
cristiano@cris ~/D/i/g/exercicio01 (main)> git status 
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt

cristiano@cris ~/D/i/g/exercicio01 (main)> git commit -m "Primeiro Commit | Exercicio 01"
[main ddaaf47] Primeiro Commit | Exercicio 01
 1 file changed, 1 insertion(+), 1 deletion(-)
cristiano@cris ~/D/i/g/exercicio01 (main)> git log 
commit ddaaf47b8ffe9b1d204c84d7976c1781530f0434 (HEAD -> main)
Author: Cristiano <crisaquino097@gmail.com>
Date:   Fri Aug 9 17:48:53 2024 -0300

    Primeiro Commit | Exercicio 01

commit 91b6ad5605b5953a1aca933aa10812ee670c76fa
Author: Cristiano <cristiano@gmail.com>
Date:   Fri Aug 9 17:45:28 2024 -0300

    Add arquivo txt
cristiano@cris ~/D/i/g/exercicio01 (main)> 
cristiano@cris ~/D/i/g/exercicio01 (main)> echo "*.txt" >.gitignore
cristiano@cris ~/D/i/g/exercicio01 (main)> cat .gitignore 
*.txt
cristiano@cris ~/D/i/g/exercicio01 (main)> echo > novo.txt 
cristiano@cris ~/D/i/g/exercicio01 (main)> git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore
cristiano@cris ~/D/i/g/exercicio01 (main)> date
Fri Aug  9 18:08:48 -03 2024    
