* 1. [Linux terminal](#Linuxterminal)
	* 1.1. [two ways to access:](#twowaystoaccess:)
		* 1.1.1. [Bash shell is the most common shell used.](#Bashshellisthemostcommonshellused.)
		* 1.1.2. [SUDO - APT - COMMAND:](#SUDO-APT-COMMAND:)
		* 1.1.3. [Navigating using CLI](#NavigatingusingCLI)
* 2. [Creating files and directories:](#Creatingfilesanddirectories:)
* 3. [Moving and copying files and directories:](#Movingandcopyingfilesanddirectories:)
* 4. [Working with links:](#Workingwithlinks:)
* 5. [Using wildcards:](#Usingwildcards:)
	* 5.1. [* Wild Card:](#WildCard:)
	* 5.2. [? Wild Card:](#WildCard:-1)
	* 5.3. [[] Wild Card:](#WildCard:-1)
	* 5.4. [Using Brace Expansion:](#UsingBraceExpansion:)
* 6. [Cat command:](#Catcommand:)
* 7. [Tac Command:](#TacCommand:)
* 8. [More Command:](#MoreCommand:)
* 9. [Less command:](#Lesscommand:)
* 10. [head command:](#headcommand:)
* 11. [tail command:](#tailcommand:)
* 12. [cut command:](#cutcommand:)
* 13. [Paste command:](#Pastecommand:)
* 14. [Sort command:](#Sortcommand:)
* 15. [wc command:](#wccommand:)
* 16. [tr command:](#trcommand:)
* 17. [diff command:](#diffcommand:)
* 18. [Grep command (Holy Grail)](#GrepcommandHolyGrail)
* 19. [Input and Output](#InputandOutput)
* 20. [Vim Text editor:](#VimTexteditor:)
* 21. [Tar Program:](#TarProgram:)
* 22. [CPIO Program :](#CPIOProgram:)
* 23. [File ownership:](#Fileownership:)
* 24. [users:](#users:)
* 25. [groups:](#groups:)
* 26. [How to begin:](#Howtobegin:)
* 27. [If/else statement:](#Ifelsestatement:)
* 28. [Case statement:](#Casestatement:)
* 29. [Looping:](#Looping:)


# Notes 2:

![chsht](/Notes/note2/0001.jpg)

![chsht](/Notes/note2/0002.jpg)

# Notes 3:
##  1. <a name='Linuxterminal'></a>Linux terminal
###  1.1. <a name='twowaystoaccess:'></a>two ways to access:
* terminal emulator
* linux terminal
  
####  1.1.1. <a name='Bashshellisthemostcommonshellused.'></a>Bash shell is the most common shell used.
Some commands: date (shows date) - cal (calendar) - clear (clear screen) - uname (system info)

####  1.1.2. <a name='SUDO-APT-COMMAND:'></a>SUDO - APT - COMMAND:
Sudo: Root Permisions
APT: Advanced package tool
commands:
    - update: updates information about every source configured previously.
    - upgrade: update the program installed before.
    - install : install a program located in a source configured previously.
    - remove: uninstall programs
    - purge: uninstall programs erasing residual files.
    - search: search a package in the repositories.
  
####  1.1.3. <a name='NavigatingusingCLI'></a>Navigating using CLI
    - pwd: shows you where are you working.
    - ls : list all files (including directories) in the current directory.
    - cd : lets you navigate through directories.

![cheatsheet](/Notes/note3/lscheat.png)
# Note 4:

##  2. <a name='Creatingfilesanddirectories:'></a>Creating files and directories:

mkdir : create directories
touch : create files
rm: delete files/directories

##  3. <a name='Movingandcopyingfilesanddirectories:'></a>Moving and copying files and directories:

mv : moves and renames directories
cp : copies files or directories

##  4. <a name='Workingwithlinks:'></a>Working with links:

ln : Create a hard link
ln -s : Create a soft link.

##  5. <a name='Usingwildcards:'></a>Using wildcards:

###  5.1. <a name='WildCard:'></a>* Wild Card:
Matches anything and nothing and matches any number of characters.
example: ls *.txt will match any .txt file.

###  5.2. <a name='WildCard:-1'></a>? Wild Card:
Matches precisely one character.

###  5.3. <a name='WildCard:-1'></a>[] Wild Card:
matches a single character in a range of values.
example: ls*[0-9]* will match all files whose name has at least one number.
###  5.4. <a name='UsingBraceExpansion:'></a>Using Brace Expansion:
It is not considered a wildcard but allows you to generate arbitrary string to use with commands. 
example: mkdir -p music/{jazz,rock} 
# note5:

##  6. <a name='Catcommand:'></a>Cat command:
Displays the content of one or two files.
cat + file1 + file2

##  7. <a name='TacCommand:'></a>Tac Command:
It is the same thing as CAT but it displays the content of the file in reverse order.
tac + file1 + file2

##  8. <a name='MoreCommand:'></a>More Command:
A Pager pgram used for displaying the content of a text file one page at a time.
more + file

##  9. <a name='Lesscommand:'></a>Less command:
Same thing as more command. The only difference is that "less" uses less memory , because "more" loads the entire file and "less" does not.
less + file

##  10. <a name='headcommand:'></a>head command: 
Displays the top N number of lines of a file. By default prints 10.
head + option + file
example: head -5 file.txt   displays the first 5 lines.

##  11. <a name='tailcommand:'></a>tail command: 
Displays the last N number of lines of a file. By default prints 10.
tail + option + file
example: tail -5 file.txt   displays the last 5 lines.
##  12. <a name='cutcommand:'></a>cut command:
Used to extract a specific section of each line of a file.
cut + option + file
example: cut -d : -f1 /etc/passwd  Shows all the users using delimiters.

##  13. <a name='Pastecommand:'></a>Paste command:
Used to join files horizontally in columns.
paste + option + file

##  14. <a name='Sortcommand:'></a>Sort command: 
sort the content of the file in alphabetical order , reverse , by number or by month.
sort + option + file
example: sort -r file.txt   sort the file in reverse order.
##  15. <a name='wccommand:'></a>wc command:
used to print the number of lines , characters and bytes in a file.
wc + option + file
example: wc -c file.txt         displays the number of bytes in the file

##  16. <a name='trcommand:'></a>tr command:
Translate or delete characters from standard output.
output | tr + option + set + set
example: cat file.txt | tr '.' ',' file.txt     replace a period by a comma.

##  17. <a name='diffcommand:'></a>diff command:
Compares files and display the differences between them.
diff + option + f1 + f2

##  18. <a name='GrepcommandHolyGrail'></a>Grep command (Holy Grail)
Command used to match a string pattern from a file or standard output.

grep + option + pattern + file
example: grep "ip" file.txt     search for lines that contains "IP".

##  19. <a name='InputandOutput'></a>Input and Output

to save the output of a file:   ls > file.txt
save the output and append it   ls >> file.txt
 
The pipe "|" allows you to redirect the standard output of a command to the standard input of another.
example:  man ls | grep "human-readable"

# note 6:

##  20. <a name='VimTexteditor:'></a>Vim Text editor:

https://vim.rtorr.com "CheatSheet" 

##  21. <a name='TarProgram:'></a>Tar Program:
 Creates a file by combining files an directories into a single file.
create:
tar + option + archive name + files to add
extract:
tar + options + file to extract

##  22. <a name='CPIOProgram:'></a>CPIO Program ::
Creates an archive , restore files from an archive , or copies a directory hierarchy. requires a list of files.
example:
ls | cpio -ov > archive.cpio

##  23. <a name='Fileownership:'></a>File ownership:

chown command used for changing group owner.
chown user:group file
example:
chown john file.txt

chmod : used to change permissions on files and directories.
chmod + permissions file/directory

![chmod](/Notes/note6/note6.png)

# note7

The /etc/passwd file contains all information about users.

##  24. <a name='Users:'></a>Users:

To add an user:

sudo adduser "username"

To delete an user:

sudo userdel -r "username"

##  25. <a name='Groups:'></a>Groups:

to add a group:

sudo addgroup "groupname"

to delete a group:

sudo delgroup "groupname"

# note 8

##  26. <a name='Howtobegin:'></a>How to begin:

Insert the following line in any text editor:  #!/bin/bash
echo : used as a COUT in c++ or print in python.
read : used as a CIN in c++.

##  27. <a name='Ifelsestatement:'></a>If/else statement:

if: starts the condition being tested
then: starts the portion of code specifying what to do if the condition evaluates to true:
else: Starts the portion of code specifying what to do if the condition evaluates to false

if command
then
    command
else
    command
fi.
##  28. <a name='Casestatement:'></a>Case statement:
Uses one variable to specify multiple values and matches a portion of the script to each value.
example:

>case $answer in
    1) command
    2) command
    3) command
esac

##  29. <a name='Looping:'></a>Looping:

while loop: Do the command while the condition is true.
while [conditon]
do
    command
done

until loop: Do the command while the condition is false.
until [conditon]
do
    command
done

for loop: Repeats the commands between do and done a specified number of times. Every time the script carries out the commands in the loop , a new value is given to a variable.

for $variable in 1 2 3 4 5 .. N
do
    commands
done.