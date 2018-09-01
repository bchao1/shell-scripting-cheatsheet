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

