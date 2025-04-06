# DevOps Lab 03
This is lab 1 below.

1- Initialize a local git repo.  
   * Add 6 files in separate commits.  
   * Write some content in the file and then commit changes  
2- Perform lab on lecture 2 slide 15  
3- Reset to commit 4 and discard 5th and 6th commit  
4- Try to restore file1 to commit 1.  
5- Perform lab on lecture 3 slide 4


### Point 1: Initialize a local git repo.
* Following are the steps for Initializing an git repo.
 * Create a folder/directory
   > mkdir DevOps_Lab_03  
   > #`DevOps_Lab_03` is folder name
 * Move to folder
   > cd DevOps_Lab_03 
 * Initialize the local git repo.
   ```
   git init
   Initialized empty Git repository in D:/Labs/DevOPs_Lab_03/.git/
* Add 6 files in separate commits.
 * Create 6 files
   ```
   touch file1.txt file2.txt file3.txt file4.txt file5.txt file6.txt

   # This will create 6 files (file1.txt, file2.txt, file3.txt, file4.txt, file5.txt, file6.txt)
 * Add file1.txt and commit.
   ```
   git add file1.txt
   git commit -m 'Add file1.txt'
 * Add file2.txt and commit.
   ```
   git add file2.txt
   git commit -m 'Add file2.txt'
 * Add file3.txt and commit.
   ```
   git add file3.txt
   git commit -m 'Add file3.txt'
 * Add file4.txt and commit.
   ```
   git add file4.txt
   git commit -m 'Add file4.txt'
 * Add file5.txt and commit.
   ```
   git add file5.txt
   git commit -m 'Add file5.txt'
 * Add file6.txt and commit.
   ```
   git add file6.txt
   git commit -m 'Add file6.txt'
* Write some content in the files and then commit changes:
  * Write content is each files  
  file1.txt content (This is file1.txt content)  
  file2.txt content (This is file2.txt content)  
  file3.txt content (This is file3.txt content)  
  file4.txt content (This is file4.txt content)  
  file5.txt content (This is file5.txt content)  
  file6.txt content (This is file6.txt content)  
  * Add files and commit.
    ```
    git add file1.txt file2.txt file3.txt file4.txt file5.txt file6.txt
    git commit -m 'Add files with content'
### 2: Perform lab on lecture 2 slide 15
* git log
  ```
  commit 3d6d562cb9cee03a6ca66ee165b2d6be20005d97 (HEAD -> master, origin/master)
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 09:02:46 2025 -0700

      Add files with content

  commit a61ee1ee7e033c39b29c6e04a0d0e90ba4d5ef8e
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 09:00:14 2025 -0700

      Add file6.txt

  commit a9b9cd1b94388d7dc3bcbbdabad44aba8100e433
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 09:00:03 2025 -0700

      Add file5.txt

  commit 4b57458a17561cddec77c5433911480e34cc4c32
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 08:59:55 2025 -0700

      Add file4.txt

  commit ec20018482ced5fa33d047974152211c569d538d
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 08:59:48 2025 -0700

      Add file3.txt

  commit 2c8434fe551809f93f225318d8a9ff7462c020ca
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 08:59:36 2025 -0700

      Add file2.txt

  commit 1b2f5d842bd129be81354717ac6e75d10833d1fa
  Author: Abdul <abdul.rehman.3091149236@gmail.com>
  Date:   Sun Apr 6 08:58:20 2025 -0700

      Add file1.txt
* git log --oneline
  ```
  3d6d562 (HEAD -> master, origin/master) Add files with content
  a61ee1e Add file6.txt
  a9b9cd1 Add file5.txt
  4b57458 Add file4.txt
  ec20018 Add file3.txt
  2c8434f Add file2.txt
  1b2f5d8 Add file1.txt
* git log --oneline  --reverse
  ```
  1b2f5d8 Add file1.txt
  2c8434f Add file2.txt
  ec20018 Add file3.txt
  4b57458 Add file4.txt
  a9b9cd1 Add file5.txt
  a61ee1e Add file6.txt
  3d6d562 (HEAD -> master, origin/master) Add files with content
### Point 3: Reset to commit 4 and discard 5th and 6th commit.
As 5th and 6th commit needed to discarded, `git reset` command will be used:
  > git reset 4b57458  
  > #`4b57458` is hash of commit 4.
### Point 4: Try to restore file1 to commit 1.
As we have only 4 commits remaining HEAD~3 will point to commit 1. To restore file1.
  > git restore --source=HEAD~3 file1.txt  
  > file1.txt is empty as this was on empty on commit 1
### Point 5: Perform lab on lecture 3 slide 4
* git remote add origin git@github.com:abdul-rehman-236/DevOps_Lab_03.git
* git remote -v
  ```
  origin  git@github.com:abdul-rehman-236/DevOps_Lab_03.git (fetch)
origin  git@github.com:abdul-rehman-236/DevOps_Lab_03.git (push)
* git push origin master  
 #Add changes to git.
