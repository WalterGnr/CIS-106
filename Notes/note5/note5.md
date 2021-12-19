# note5:

## Cat command:
Displays the content of one or two files.
cat + file1 + file2

## Tac Command:
It is the same thing as CAT but it displays the content of the file in reverse order.
tac + file1 + file2

## More Command:
A Pager pgram used for displaying the content of a text file one page at a time.
more + file

## Less command:
Same thing as more command. The only difference is that "less" uses less memory , because "more" loads the entire file and "less" does not.
less + file

## head command: 
Displays the top N number of lines of a file. By default prints 10.
head + option + file
example: head -5 file.txt   displays the first 5 lines.

## tail command: 
Displays the last N number of lines of a file. By default prints 10.
tail + option + file
example: tail -5 file.txt   displays the last 5 lines.
## cut command:
Used to extract a specific section of each line of a file.
cut + option + file
example: cut -d : -f1 /etc/passwd  Shows all the users using delimiters.

## Paste command:
Used to join files horizontally in columns.
paste + option + file

## Sort command: 
sort the content of the file in alphabetical order , reverse , by number or by month.
sort + option + file
example: sort -r file.txt   sort the file in reverse order.
## wc command:
used to print the number of lines , characters and bytes in a file.
wc + option + file
example: wc -c file.txt         displays the number of bytes in the file

## tr command:
Translate or delete characters from standard output.
output | tr + option + set + set
example: cat file.txt | tr '.' ',' file.txt     replace a period by a comma.

## diff command:
Compares files and display the differences between them.
diff + option + f1 + f2

## Grep command (Holy Grail)
Command used to match a string pattern from a file or standard output.

grep + option + pattern + file
example: grep "ip" file.txt     search for lines that contains "IP".

## Input and Output

to save the output of a file:   ls > file.txt
save the output and append it   ls >> file.txt
 
The pipe "|" allows you to redirect the standard output of a command to the standard input of another.
example:  man ls | grep "human-readable"

