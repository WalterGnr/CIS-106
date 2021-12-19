# note 6:

## Vim Text editor:

https://vim.rtorr.com "CheatSheet" 

## Tar Program:
 Creates a file by combining files an directories into a single file.
create:
tar + option + archive name + files to add
extract:
tar + options + file to extract

 ## CPIO Program :
Creates an archive , restore files from an archive , or copies a directory hierarchy. requires a list of files.
example:
ls | cpio -ov > archive.cpio

## File ownership:

chown command used for changing group owner.
chown user:group file
example:
chown john file.txt

chmod : used to change permissions on files and directories.
chmod + permissions file/directory

![chmod](/Notes/note6/note6.png)

