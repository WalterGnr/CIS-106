# Lab 5 | Handling Text Files 

## Question 1 
Cat, head and tail commands are used for displaying the content of a file.
1. Display the content of the `/etc/passwd` file.
   ![q1-1](q1-1.png)
2. Display the content of the `/etc/passwd` file in reverse order.
   ![q1-2](q1-2.png)
3. Display the content of the `/etc/passwd` file with line numbers and the $ to indicate the end of every line.
   ![q1-3](q1-3.png)
4. Display the first 5 lines of a the `/etc/passwd` file.
5. Display the last 5 lines of the `/etc/passwd` file.
   ![q1-45](q1-45.png)

## Question 2
The cut command is very useful when working with files that are already formatted using a field separator. The cut command can show specific information about each line of text in a given file.

1. Display the first field of the `/etc/passwd` file.
   ![q2-1](q2-1.png)
2. Display the last 5 users in the `/etc/passwd` file.
   ![q2-2](q2-2.png)
3. Display a list of all the users and their designated login shell separated by an `=` sign.
   ![q2-3](q2-3.png)
4. The sort command is another amazing tool in any linux user’s tool box. Sort allows you to display data in a given order. Cut the first and 3rd field of the `/etc/passwd` field and sort the output.
   ![q2-4](q2-4.png) 
5. Repeat the previous command but this time only show the last 5 entries.
   ![q2-5](q2-5.png)


## Question 3
The wc command is used to count the number of lines, characters and words in a file.

1. How many lines does the `/etc/passwd` file have?
2. How many words does the `/etc/passwd` file have?

    ![q3-12](q3-12.png)

3. How many users can login with the `/bin/bash` shell?
4. How many users have the `/sbin/nologin` shell assigned?
   ![q3-34](q3-34.png)
5. Display your user’s information in `/etc/passwd` file
   ![q3-5](q3-5.png)


## Question 4


1. Run the `ip ad` command and display all the lines that match the string `inet`. How many lines did you get? 
   ![q4-1](q4-1.png)
2. Run the `ip ad` command and display all the lines that match the string `inet6`. Display the output in reverse order.
   ![q4-2](q4-2.png)
3. Run the `ip ad` command and display all the lines that match the string `inet` or `inet6` sort the output and save it to a file.
4. Run the `ip ad` command and display only the 3rd line that matches the string `inet`.
5. Run the `ip ad` command and display all the ipv4 addresses sorted.
   ![q4-345](q4-345.png)


## Question 5

1. Run the following command and save the output to a markdown file: `echo "# Information about my pc"`. You can use any naming convention you want for the file as long as it is a markdown file.
3. Run the following command and append the output to the markdown file you created earlier: `echo "## CPU Information"`
2. The `lscpu` command displays a lot of information about the CPU the computer has. Use the `lscpu`, `grep`, and the pipe (|) to extract, and append to the file you created earlier, the following information from the output of the `lscpu` command:
   * Architecture
   * Threads
   * Cores
   * Model name
   * CPU Frequency
   * Virtualiation technology supported
3. Run the following command and append the output to the markdown file you created earlier: `echo "## RAM Information"`
4. The command `lshw -c memory` displays information about the RAM installed in your system. Extract and append to the file the following information:
    * Memory size:
5. Display the content of the file you created earlier showing all the data that has been appended so far.
   ![q5](q5.png)

   ![q5-2](q5-2.png)