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

> > -**show current working directory path**<br/>
*pwd*<br/>
-**creating a directory**<br/>
*mkdir*<br/>
-**deleting a directory**<br/>
*rm -r*<br/>
-**creating a file using touch command**<br/>
*touch filename.txt*<br/>
-**deleting a file**<br/>
*rm*<br/>
-**renaming a file**<br/>
*mv oldname.txt newname.txt*<br>
-**listing hidden files**<br>
*ls -a*<br/>
-**copying a file from one directory to another**<br/>
*cp direct1/filename.txt direct2/*<br/>
-**copying all the files from one directory to another directory**<br/>
_cp direct1/* direct2_<br/>
-**copying all the txt files that starts with 'a' to another directory**<br/>
_cp a*.txt direct2_<br/> 

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

> > `ls` list all the files in current directory <br/>
`ls -a` list all the files including all the hidden ones(whose name starts with .) <br/>
`ls -l` list files in long format (including detailed information of them) <br/>
`ls -lh` list files in long format and print sizes in human readable format <br/>
`ls -lah` list files including all the hidden ones and in long and human readable size formats <br/>
`ls -t` list all the files and order them by modification time <br/>
`ls -Glp` list all the files in long formats with color with all the directories ending with / <br/>

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > Option | Description
__________ | ___________  
---------- | -----------  
-a | Displays all files.  
-d | Displays only directories.  
-g | Displays the long format listing, but exclude the owner name.  
-F | Flags filenames  
-o | Displays the long format listing, but excludes group name.  
---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > __xargs__ is a command on Unix and most Unix-like oprating systems used to build and execute commands from standard input. It converts input from standard input into arguments to command  
One use case of xargs command is to remove a list of files using the _rm_ command  
`find /path -type f -print | xargs rm`  
the find utility feeds the input of `xargs` with a long list of file names. `xargs` then splits this list into sublists and calls `rm` once for every subilist  



