# Basic-Shell-Scripting-Tutorial

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
Before the shell executes a command, it first *parses* the command. The first token in the command is the *action* the shell makes, and the following tokens, seperated by whitespaces, are the arguments. In both examples above, `echo` is the action (print something), and the arguments are `Hello` and `World`. `echo` prints the arguments seperated by a space, hence the result.

To print several spaces between words, we enclose the string we wich to print with `"`.
```
$ echo "Hello     World"
Hello     World
```
`echo` now treats `Hello     World` as one argument, and thus we can preserve the whitespaces between the words.

## Variables 
Like any other programming language, we can also assign values to **variables** in shell scripts. Consider the following commad
```
$ var=10
```

