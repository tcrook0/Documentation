# Description

Instructions on how to create a Java Eclipse Project on a local machine and then store the source code for that project in a GitHub repository.

Note that these instructions are repeatable, that is, they include instructions on deleting what was created so that you may repeat the instructions again - as many times as you want to.

***Note that specific userids, file names, and folder names are used - no attempt has been made to generalize: extrapolate as you need to.***

# Create a new GitHub Repository

- goto the GitHub website: https://github.com
- sign in to GitHub as `tcrook0`
- click `tcrook0` drop-down, in upper right corner
- click `Your repositories` link
- click `New` button, below `tcrook0` drop-down
- enter the following in `Repository name` field: `IntegratedProjects`
- click `Create repository` button, near bottom
- note the new window with the title `tcrook0/IntegratedProjects`, near top
- the new GitHub repository, `IntegratedProjects` has been created

# Clone the New Repository on Local Machine

Bring up a `Terminal` window and issue the following commands:

```
cd /Users/tomcrook/Documents/_ACME
git clone https://github.dom/5d4ook0/IntegratedProjects.git
```

Response to the above:

```
Cloning into 'IntegratedProjects'...
warning: You appear to have cloned an empty repository
```

Issue commands:

```
ls -al
ls -al .git
git status
git config --list
```

Response to the above indicates a new directory, the cloned repository `IntegratedProjects`, which is connected to the GItHub repository of the same name, has been created, consisting of one directory named `.git`.

# Create a New Java Eclipse Project in the Repository

From the `Terminal` window:

```
mkdir -p UCSCext/CMPR_X412/Week1
```

bring up `Eclipse`:

`Browse...` to the following `Workspace` (full path):

```
/Users/to crook/Documents/_ACME/IntegratedProjects/UCSCext/CMPR_X412/Week1
```

Note: from an `Eclipse` perspective, ...`/Week1` is the `Workspace`.

click `Launch` button

click `Hide` button

click `Create a Java Project` link, found in `Package Explorer`

enter the follwing in the `Project name` field: `Homework1`

near the bottom, turn off the following two checkboxes:
1. `Create module-info.java file`
2. `Generate comments`

click `Finish` button

This results in a new window with a blank editor field. Copy and paste the entire contents of the following file into this field (`Finder` works well for navigating to this file which may be opened by double-clicking on it):

```
Macintosh HD > Users > tomcrook > Documents > _ACME
             > EclipseJavaWOrkSpaces 
             > USCSext
             > 2019_4thQtr_CMPR_X412.(21)_JavaProgrammingForBeginners
             > Week1
             > Homework1
             > src
             > Homework1.java
```

# Verify the Project Runs

# .gitignore

# add

# commit

# push

# Verify the Source Code for the Project is Now in GitHub

# Verify the Project Runs

# Delete the Repository on GitHub

# Delete the Cloned Local Repository
