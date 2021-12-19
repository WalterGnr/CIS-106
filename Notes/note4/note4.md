# Note 4:

## Creating files and directories:

mkdir : create directories
touch : create files
rm: delete files/directories

## Moving and copying files and directories:

mv : moves and renames directories
cp : copies files or directories

## Working with links:

ln : Create a hard link
ln -s : Create a soft link.

## Using wildcards:

### * Wild Card:
Matches anything and nothing and matches any number of characters.
example: ls *.txt will match any .txt file.

### ? Wild Card:
Matches precisely one character.

### [] Wild Card:
matches a single character in a range of values.
example: ls*[0-9]* will match all files whose name has at least one number.
### Using Brace Expansion:
It is not considered a wildcard but allows you to generate arbitrary string to use with commands. 
example: mkdir -p music/{jazz,rock} 
