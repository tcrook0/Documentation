This repository contains articles on How to Do Stuff with Git, GitHub, MacOS Terminal commands, and Java Eclipse - all together...

At the time of this repository's creation, January 2023, the type of machine and various pieces of the software used were given, below.
The instructions in the articles refer to specific user accounts, files, folders, etc.
*Your actual user accounts, files, folders, etc., must be substituted in place of these*.
Keeping the documentation specific in this way also serves as a record of, at least, what did work - and in which environment.
As time goes on, so does change; if these articles aren't updated periodically, they will fall into decay...

It seems that the way the Git, GitHub, and Eclipse applications work is by embedding files that begin with '.' (dot files)
throughout the, presumed, hierarchical directory structure. These special files are used by the application. 
Apparently, there is some coordination between at least these applications because:

1. It looks like Eclipse automatically generates .gitignore files if it notices Git/GitHub dot files.
2. At least for the examples documented in this repository, these different dot files appear to coexist without conflict.

In short, at least for the examples documented, Git, GitHub, and Eclipse seem to work together.

Complexity piled on top of yet more complexity...

```
Machine: MacBook Pro
         Chip:   Apple M1 Pro
         macOS:  Ventura 13.1

Terminal:         version  2.13
Browser:  Safari, version 16.2

Git:    git version 2.37.1 (Apple Git-137.1)
GitHub: https://github.com

Eclipse IDE for Java Developers: Version:  2022-09 (4.23.0)
                                 Build id: 20220908-1902
```
