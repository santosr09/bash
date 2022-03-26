Bash

Bash
Bash is a command language interpreter. It is widely available on various operating systems and is a default command interpreter on most GNU/Linux systems. The name is an acronym for the ‘Bourne-Again SHell’
https://linuxconfig.org/bash-scripting-tutorial-for-beginners

Bash is a Unix shell and command language which can run Shell Script files. You do not need to install Ubuntu or any other Linux Distros unless your scripts need the support of the real Linux kernel
link

SHELL
shell allows you by use of commands to interact with your computer

What is Bash?
echo $SHELL

-locate a full path to its executable binary using which command
which bash

shell interpreter definition: 
#!/bin/bash

PERMISSIONS AND EXECUTIONS
in order to execute shell script the file needs to be made executable by use of chmod +x FILENAME
By default, any newly created files are not executable regardless of its file extension suffix.

Script Execution:
 How the instructions are interpreted depends on defined shebang or the way the script is executed
./file.sh

Another way to execute bash scripts is to call bash interpreter explicitly eg. 
$ bash file.sh

hence executing the script without the need to make the shell script executable and without declaring shebang directly within a shell script


Relative vs absolute path
An absolute path is defined as specifying the location of a file or directory from the root directory(/). In other words,we can say that an absolute path is a complete path from start of actual file system from / directory. 
Relative path is defined as the path related to the present working directly(pwd)

Linux relative path:
./public_html/cgi-bin

Linux absolute path:
/home/users/c/computerhope/public_html/cgi-bin

