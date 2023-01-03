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



