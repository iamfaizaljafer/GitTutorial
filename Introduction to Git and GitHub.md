# Git

Git is a Distribution version control system. It was developed to enable team members to work together at the same time.
Git was created by Linux Torvalds in 2005 to develop the Linux kernel.


## What does Version control systems do ?

- Maintains a history of every version.
- Undo changes
- Who did what commit


## Features of Git:

- Open source
- Scalability
- Distributed
- Speed

## Why Git?

- Over 70% of developers use Git!
- Developers can work together from anywhere in the world.
- Developers can see the full history of the project.
- Developers can revert to earlier versions of a project.

# Install git

Download the package from the below link and install the same.
https://git-scm.com/downloads

- Once installed exceute the below command to check if its installed.
git --version


## Usage of git

- Versioning
- Tracking
- Easy Roll back.
- Comparing
- Collaboration
- Code review

# Git Basics:


## git init

Using "git init" we change the normal folder to a git repository.

- Create a folder for the project “project1”
- Exceute the command - git init
- It initializes a empty repository in the folder.

![image](https://user-images.githubusercontent.com/91851332/164649139-56889398-fa3f-43fa-b58f-30a3a33a52ee.png)

## Git Configuration:

You must configure your username and email ID for git to understand who is making the commits. This needs to be done only once in your system.

- git config --global user.name "themohamedfaizal"
- git config --global user.email "themohamedfaizal@gmail.com"

## Git Stages:

![image](https://user-images.githubusercontent.com/91851332/164325805-973c2e84-1705-437b-85bb-f37ab787fc6d.png)

- Step 1 − You modify a file from the working directory.
- Step 2 − You add these files to the staging area.
- Step 3 − You perform commit operation that moves the files from the staging area. After push operation, it stores the changes permanently to the Git repository.

## First commit

```
mkdir proj
cd proj
git init
touch file1
git add file1
git commit -m “hello world”
```


## git commit output explanations:

We can see if the new file is created or even if the file is modified like below,

```
$git commit -m "hello world"

[main (root-commit) bb7cbd6] hello world
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 proj/file1
```
```
$git commit -m second file1 

[main (root-commit) eef9495] second
 1 file changed, 1 insertion(+)
 create mode 100644 file1
```

## Checking commits:

- git log (Take the first 4 digits of the commit-id that you want to see; by using the commit message as the referrence.)

```
$git log


commit eef949588fe04e68e29648fdba036de6cf0b5bd4 (HEAD -> main)
Author: iamfaizaljafer <iamfaizaljafer@gmail.com>
Date:   Tue Jan 3 22:18:37 2023 +0530

    second
```

- git show

```
$ git show eef94



commit eef949588fe04e68e29648fdba036de6cf0b5bd4 (HEAD -> main)
Author: iamfaizaljafer <iamfaizljafer@gmail.com>
Date:   Tue Jan 3 22:18:37 2023 +0530

    second

diff --git a/file1 b/file1
new file mode 100644
index 0000000..ce01362
--- /dev/null
+++ b/file1
@@ -0,0 +1 @@
+hello
```


# We can collaborate with others using GitHub:
Local Repository ?
In your local system, when you exceute the command “git init” it becomes a Local Repository.
Remote Repository
When we create a Repository in a remote server, which enables us to share our code with everyone; It becomes a Remote Repository.
Types of Version Control system

## Examples of Distributed Remote Repositories
- GitHub
- Bitbucket
- GitLab
- GitHub
- GitHub is a repository hosting service. It provides web-based GUI.

## Features of GitHub
- Collaboration.
- Integrated issue and bug tracking.
- Graphical representation of the branches.
- Git repo hosting.
- Project / team management.
- Code hosting.
- Track and assign tasks.

## What does GitHub do ?
- Manage projects with Repositories
- Clone a project to work on a local copy
- Control and track changes with Staging and Committing
- Branch and Merge to allow for work on different parts and versions of a project
- Pull the latest version of the project to a local copy
- Push local updates to the main project

## Create a GitHub Account
Please go to the website https://github.com/ and create an account for yourself. This could be used as the remote repository.

## Config and pushing code to remote Repo
We can add GitHub to out git as remote.
```
git remote add origin https://github.com/iamfaizaljafer/proj1.git
git remote -v
origin  https://github.com/iamfaizaljafer/proj1.git (fetch)
origin  https://github.com/iamfaizaljafer/proj1.git (push)
```
We can push our code to GitHub using the below command.
```
git push origin master
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 430 bytes | 215.00 KiB/s, done.
To https://github.com/iamfaizaljafer/proj1.git
 * [new branch]      master -> master
```
Make some changes and try pushing it again.
```
$ cat>> file1
have a great day!
$ git add file1
$ git commit -m "third commit"
[master 70b4d50] third commit
 1 file changed, 1 insertion(+)
$ git push origin master
Writing objects: 100% (3/3), 269 bytes | 269.00 KiB/s, done.
   68cab96..70b4d50  master -> master
```

## What is origin?
When we add the GitHub URL as remote, we give a short reference for this link as origin. So instead of using the whole link, we can use the reference origin.
```
$ git remote -v
origin  https://github.com/iamfaizaljafer/proj1.git (fetch)
origin  https://github.com/iamfaizaljafer/proj1.git (push)
$ git remote remove origin
$ git remote -v
$ git remote add faizal https://github.com/iamfaizaljafer/proj1.git
$ git remote -v
faizal  https://github.com/iamfaizaljafer/proj1.git (fetch)
faizal  https://github.com/iamfaizaljafer/proj1.git (push)
$ git push faizal master
Everything up-to-date
```
- git pull
We can pull the code from GitHub using the below command.
```
mkdir testpull
cd testpull/
git init
git remote add origin https://github.com/iamfaizaljafer/git-class.git
git pull origin master
```
