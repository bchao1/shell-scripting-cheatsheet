# Basic-Shell-Scripting-Tutorial

## Table of Contents 
- First Script
- Basic Printing
- Variables
- Loops
- Special character usage: `$`, `*`, and etc.

## First Script
Since there are various kinds of shells in a Unix system, we usually define the type of shell we want to use in our shell script before we actually get into the main content. In the first line of your script, type
```
#!./bin/sh
```
Usually the shell is located in the `./bin` directory, the `!#` is followed by the path to the shell we wish to use. In this case, we are using the **Bourne shell**. We can also use **bash**, which is short for **Bourne-Again shell**, by typing
```
#!./bin/bash
```
After we have configured the shell to run our script, we can start writing our first shell script. To print something one the terminal, we use the command `echo`. In your script, type
```
echo Hello World
```
To run the shell script, simply type `./<name of the script>` in your terminal. In my case, I named by shell script `first_script.sh`.
```
$ ./first_script.sh
```
In the terminal, you should see 
```
$ ./first_script.sh
Hello World
$
```
You have now written your first shell script!

## Basic Printing
As seen in the example above, the `echo` command is to print something on the terminal. It is essentially the same as `print` in **Python** (since Python is also a scripting language, it is obvious to make this analogy). The content following `echo`, or any other shell commands, are called **arguments**. 
```
$ echo Hello World
Hello World
$ echo Hello     World
Hello World
```
Before the shell executes a line, it first *parses* the line. The first token in the line is the *command*, and the following tokens, seperated by whitespaces, are the arguments. In both examples above, `echo` is the command (print something), and the arguments are `Hello` and `World`. `echo` prints the arguments seperated by a space, hence the result.

To preserve the whitespaces between the two words, we enclose the string we wish to print with `"`.
```
$ echo "Hello     World"
Hello     World
```
`echo` now treats `"Hello     World"` as a single argument.

## Variables 
Like any other programming language, we can also assign values to **variables** in shell scripts. Consider the following command
```
$ var=10
```
The value `10` is **assigned** to the **variable** `var`. 
Note that no spaces should appear around `=`. For the line 
```
$ var = 10
```
The shell would treat `var` as a command and `=`, `10` as arguments. Apparently there are no shell commands named `var`, hence you would recieve an error message
```
$ var = 10
var: no command found
```
Printing the value of the variable is similar to printing a string, except we add a `$` in front of the variable.
```
$ echo "The value of var is $var"
The value of var is 10
```
The command `read` assigns user input to a variable. Type the following in your shell script, then run the script on the terminal.
``` 
echo "What is your name?"
read USERNAME
echo "Hello $USERNAME
```
You should see the following
```
$ ./test.sh
What is your name? 
```
Enter your name and see
```
$ ./test.sh
What is your name? Brian
Hello Brian
```
### Variable Scopes

## Loops
Most shells support the `while` and `for` loop, just like any other programming language.
### For loops
`for` loops itereate through a list of values. Try to run the following script on your terminal
```
for NUMBER in 1 2 3 4 5
do 
echo "NUMBER is $NUMBER"
done
```
You should see
```
$ ./test.sh
NUMBER is 1
NUMBER is 2
NUMBER is 3
NUMBER is 4
NUMBER is 5
```
In each iteration, the variable (should be defined between `for` and `in`) will be assigned to one of the arguments in the argument list (located after `in`). 





