# Table of Contents

- [Description](#description)
- [Create a new GitHub Repository](#create-a-new-github-repository)
- [Clone the New Repository on Local Machine](#clone-the-new-repository-on-local-machine)
- [Create a New Java Eclipse Project in the Repository](#create-a-new-java-eclipse-project-in-the-repository)
- [Verify the Project Runs](#verify-the-project-runs)
- [.gitignore](#gitignore)
- [add](#add)
- [commit](#commit)
- [push](#push)
- [Verify the Source Code for the Project is Now in GitHub](#verify-the-source-code-for-the-project-is-now-in-github)
- [Verify the Project Still Runs](#verify-the-project-still-runs)
- [Delete the Repository on GitHub](#delete-the-repository-on-github)
- [Delete the Cloned Local Repository](#delete-the-cloned-local-repository)

# Description

Instructions on how to create a `Java Eclipse Project` on a local machine and then store the source code for that project in a `GitHub` repository.

Note: these instructions are repeatable; they include steps deleting what was created.

# Create a new GitHub Repository

- go to the `GitHub` website: https://github.com
- sign in to `GitHub` as `tcrook0`
- click `tcrook0` drop-down, upper right corner
- click `Your repositories`
- click `New` button, below `tcrook0` drop-down
- enter the following in `Repository name` field: `IntegratedProjects`
- click `Create repository` button, near bottom
- note the new window with the title `tcrook0/IntegratedProjects`, near top
- the new `GitHub` repository, `IntegratedProjects`, has been created

# Clone the New Repository on Local Machine

bring up a `Terminal` window and issue the following commands:

```
cd /Users/tomcrook/Documents/_ACME
git clone https://github.com/tcrook0/IntegratedProjects.git
```

response:

```
Cloning into 'IntegratedProjects'...
warning: You appear to have cloned an empty repository.
```

from `Terminal`:

```
cd IntegratedProjects
ls -al
ls -al .git
git status
git config --list
```

Response to the above indicates the cloned directory/respository, `IntegratedProjects`, which is connected to the `GitHub` repository of the same name, has been created, consisting of one directory named `.git`.

# Create a New Java Eclipse Project in the Repository

from `Terminal`:

```
mkdir -p UCSCext/CMPR_X412/Week1
```

bring up `Eclipse`:

`Browse...` to the following `Workspace` (full path):

```
/Users/tcrook/Documents/_ACME/IntegratedProjects/UCSCext/CMPR_X412/Week1
```

Note: from an `Eclipse` perspective, ...`/Week1` is the `Workspace`.

- click `Open` button
- click `Launch` button
- click `Hide` button
- click `Create a Java Project` link, found in `Package Explorer`
- enter the following in the `Project name` field: `Homework1`

near bottom, turn off the following two checkboxes:
1. `Create module-info.java file`
2. `Generate comments`

- click `Finish` button
- click `File` drop-down, from menu bar, top
- click `New` (first item in drop-down menu)
- click `Class`

This brings up a `New Java Class` window.

- enter the following in the `Name` field: `Homework1`
- click `Finish` button

This results in a new `Homework1.java` tab with an editor field.

- Delete any content in this field.
- Copy and paste the entire contents of the following file into this field (`Finder` works well for navigating to this file which may be opened by double-clicking on it):

```
Macintosh HD > Users > tomcrook > Documents > _ACME
             > EclipseJavaWorkSpaces 
             > USCSext
             > 2019_4thQtr_CMPR_X412.(21)_JavaProgrammingForBeginners
             > Week1
             > Homework1
             > src
             > Homework1.java
```

- click `File` drop-down, from menu bar, top
- click `Save`

# Verify the Project Runs

from `Eclipse`:

- click `Run` drop-down, from menu bar, top
- click `Run` (first item in drop-down menu)

A `Console` window should appear with output.

close `Eclipse`

# .gitignore

From `Terminal`, issue `ls -al` commands to explore the cloned directory/respository, `IntegratedProjects`, revealing the following:

```
.../IntegratedProjects
  .git
  UCSCext
         CMPR_X412
                  Week1
                       .gitignore
                       .metadata
                       Homework1
                                .classpath
                                .gitignore
                                .project
                                .settings
                                bin
                                   Homework1.class
                                src
                                   Homework1.java
```

Note: this is what the cloned directory/respository, `IntegratedProjects`, looked like before the above `Eclipse` actions:

```
.../IntegratedProjects
  .git
  UCSCext
         CMPR_X412
                  Week1
```

Creating the `Java Eclipse Project`, `Homework1`, generated new files; Only one of which, `Homework1.java`, is to be copied over to the `GitHub` repository `IntegratedProjects`:

```
.../IntegratedProjects
  .git
  UCSCext
         CMPR_X412
                  Week1
                       Homework1
                                src
                                   Homework1.java
```

It would be nice to have a relatively easy way to prevent other files, most of which begin with a dot (`.`), from being copied over...

One way to do this is to create a `.gitignore` file, directly under `.../IntegratedProjects` and therefore adjacent to both `.git` and `UCSCext`.

In this file, the names of files and directories to be excluded from being copied over are listed. There are many different ways to write this `.gitignore` file. Here's one way that works: create and save the new `.gitignore` file, typing in the following:

```
.DS_Store
.classpath
.gitignore
.metadata
.project
.settings
bin
```

from `Terminal`:

```
git status
```

response:

```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	UCSCext/

nothing added to commit but untracked files present (use "git add" to track)
```

# add
from `Terminal`:

```
git add UCSCext
git status
```

response:

```
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   UCSCext/CMPR_X412/Week1/Homework1/src/Homework1.java
```

# commit

from `Terminal`:

```
git commit
```

This brings up the `vi` editor... Append the following to the `.../.git/COMMIT_EDITMSG` file:

```
Commit the following Java Eclipse Project: Homework1.
```

response:

```
 1 file changed, 201 insertions(+)
 create mode 100644 UCSCext/CMPR_X412/Week1/Homework1/src/Homework1.java
```

from `Terminal`:

```
git status
```

response:

```
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
```

# push

from `Terminal`:

```
git push
```

response:

```
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
(base) tomcrook@Toms-MacBook-Pro IntegratedProjects % git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 10 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (8/8), 2.07 KiB | 2.07 MiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/tcrook0/IntegratedProjects.git
 * [new branch]      main -> main
```

from `Terminal`:

```
git status
```

response:

```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

# Verify the Source Code for the Project is Now in GitHub

- to avoid any potential refresh issues, sign off from `GitHub` then sign back on
- click `tcrook0` drop-down, upper right corner
- click `Your repositories`
- find `IntegratedProjects` in the list of repositories displayed and click on it.

Not quite halfway down the page, to the right of `tcrook0`, the text entered earlier in the `.../.git/COMMIT_EDITMSG` file is displayed:

```
Commit the following Java Eclipse Project: Homework1.
```

Click on this and you will see that the following file was copied over:

```
UCSCext/CMPR_X412/QWeek1/Homework1/src/Homework1.java
```

...and none of the other files were copied over - the `.gitignore` file, created above, prevented that from happening.

# Verify the Project Still Runs

bring up `Eclipse`:

`Browse...` to the following `Workspace` (full path):

```
/Users/tcrook/Documents/_ACME/IntegratedProjects/UCSCext/CMPR_X412/Week1
```

- click `Open` button
- click `Launch` button
- click `Run` drop-down, from menu bar, top
- click `Run` (first item in drop-down menu)

A `Console` window should appear with output generated by the following new `Java Eclipse Project` just created, `Homework1`.

close `Eclipse`

# Delete the Repository on GitHub

from `GitHub`:

- click `tcrook0` drop-down, in the upper right corner
- click `Your repositories`
- find `IntegratedProjects` in the list of repositories displayed and click on it.

A few lines down from the top, there is a horizontal display of icons:

```
* Code * Issues * Pull requests * Actions * Projects * Wiki * Security * Insights * Settings
```

- click on right-most one: `Settings'
- scroll down to bottom
- click on `Delete this repository` button
- follow the instructions to confirm...

Notes:

- The page listing all of the repositories for `tcrook0` comes back.
- The `GitHub` repository `IntegratedProjects` no longer exists.

sign out from `GitHub`

# Delete the Cloned Local Repository

from `Terminal`:

```
cd /Users/tomcrook/Documents/_ACME
ls -al
```

Note: the existence of the cloned directory/respository, `IntegratedProjects`.

from `Terminal`:

```
rm -fr IntegratedProjects
ls -al
```

Note: the cloned directory/respository, `IntegratedProjects`, no longer exists.
