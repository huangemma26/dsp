# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * `pwd` - show current working directory path 
* `mkdir` - creating a directory
* `rm -r DIRECTORY` deleting a directory
* (`touch FILENAME.txt`) - creating a file using `touch` command
* `rm` - deleting a file
* `mv NEWNAME OLDNAME` - renaming a file
* `ls -a` - listing hidden files
* `cp DIRECTORY/SOURCEFILE.txt NEWDIRECTORY/` - copying a file from one directory to another
* `cd` - switches you into the directory you specify
* `cp * DIRECTORY` - selects all files in a directory
* `mv FILE.txt DIRECTORY/` - moves a file from one directory to another

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`
`ls -a`
`ls -l`
`ls -lh`  
`ls -lah`  
`ls -t`
`ls -Glp`  

> > `ls` - lists all files and directories in the working directory
`ls -a` - lists all contents, including hidden files and directories
`ls -l` - lists all contents of a directory in long format
`ls -lh` - lists all contents of a directory in long format with human readable sizes
`ls -lah` - lists all contents of a directory in long format with human readable sizes, including hidden files and dictionaries
`ls -t` - order files and directories by the time they were last modified
`ls -Glp` - doesn't display group, lists long format, and displays '/' after dictionaries 

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > * `ls -d` Displays only directories
* `ls -m` - Displays the names as a comma-separated list
* `ls -R` - Displays subdirectories as well
* `ls -x` - Displays files as rows across the screen
* `ls -1` - Displays each entry on a line

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` helps to compute command line arguments. It reads words as arguements separated by spaces. Many commands in command line need to be read as arguements, which can be done with `xargs`. It contains the template of another command and adds agruments from standard input in order to complete the command. For example:  
`ls | xargs -n 3`  
This will displace the objects in your current directory in 3 columns. An `echo` command is used by the command by default, although it could be added in at the end of the command as xargs is using it to complete the command anyway.
