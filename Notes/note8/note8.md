# note 8

## How to begin:

Insert the following line in any text editor:  #!/bin/bash
echo : used as a COUT in c++ or print in python.
read : used as a CIN in c++.

## If/else statement:

if: starts the condition being tested
then: starts the portion of code specifying what to do if the condition evaluates to true:
else: Starts the portion of code specifying what to do if the condition evaluates to false

if command
then
    command
else
    command
fi.
## Case statement:
Uses one variable to specify multiple values and matches a portion of the script to each value.
example:

>case $answer in
    1) command
    2) command
    3) command
esac

## Looping:

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