# 1. Requirements
In this assignment you will write your own versions of classic Unix text-processing programs.  The tools you write for this assignment are not intended to be perfect clones of the programs they are mimicking.  I have relaxed requirements that your code should meet.
This assignment is essentially a re-implementation of simple Unix text-processing programs in Python.  Each tool will be a Python function which takes as input a list of arguments supplied by the user from the command line.

This program will be run from the command line as a command of the form:

    $ python src/tt.py TOOL [OPTIONS] FILENAME...

This form of command should feel familiar to you after having used `git` over the past weeks.

1.   `python` invokes the Python interpreter
2.   Next comes the name of the driver program `src/tt.py`
3.   `TOOL` is the name of one of the available text tools listed in the table below.  The name of the tool must be spelled exactly as shown in the table, in lower-case.
4.   Some tools may take an option, which is entered in the position of `[OPTIONS]` *(Note that the user does not type the square brackets; in documentation for command-line programs brackets indicate optional arguments)*
5.   Each tool must be given at least one filename.  The ellipsis indicates that one or more filenames are acceptable.

Your program **must not** prompt the user for any input.  Your program **should not** use the `input()` function.

When `src/tt.py` is launched without naming a `TOOL`, or when an invalid `TOOL` is given, a usage message is printed.

# 2. Design
The approach to the design is purely functional; all Unix commands will be implemented with their python function counterparts, as stated in the requirements.

## Concatenate.py
These functions will read input from a file by opening a file and calling the .read() method and print to the screen, cat being in order and tac reversing the output.

## CutPaste.py
paste() will extract data from files and print to standard out. The function will open each file, append them to a list,
and have a for loop iterate through each, and print() to the screen.

cut() will remove columns from a file and display them to standard output. The function will open each file specified,
and extract a specified amount of columns by iterating through each file object and print them to standard output. (OPTION = -f)

## Grep.py

grep() will parse each string in a file and display the results to standard out. The specified file will be opened, have each line read and stored into a list,
and then iterated through to print() to the screen. (OPTION = -v)

## Partial.py

head() opens every file specified, reads the lines into a list until less than or equal to 10, then iterates through the list and prints to standard out.

tail() is similar to head(), but will extract lines in reverse. (OPTION = -n)

## Sorting.py

sort() will read each line from every file specified, save to a list, iterate over the list and print to standard output.

## tt.py

The command to be used will be extracted from sys.argv. The structure will be a chain of if, elif, else statements.

## WordCount.py 

wc() will read each line and save to a list, iterate with a for loop, and increment line, word, and character values.
The variables will then print() to standard out.

# 3. Implementation

# 4. Validation
Tests will run the data provided in the /data directory. Error handling will be checked and correct output will be analyzed.
The debugger from PyCharm will be used if needed.