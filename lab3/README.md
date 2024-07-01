## Lab 3 - Buffer Overflows?|?d??|?d?Segmentation fault: 11
This assignment involves applying a series of buffer overflow attacks on an executable file called `bufbomb`.

### Learning Objectives
- Label and describe the utility of different parts of a x86-64 stack frame.
- Understand and explain what decisions are made at compile time and what modifications/decisions can occur when the program runs.
- Given a program, students are able to examine and execute x86-64 assembly instructions and use `gdb` commands (e.g., set and use breakpoints, print register values).
- Provide examples of several types of buffer overflow exploits and explain how they can affect a program.

### Format
You have been provided a vulnerable executable called `bufbomb` that we will perform a few variants of buffer overflow attacks on. The vulnerability comes from reading a string from standard input with the function `getbuf()`.

Full details at [Lab 3 Overview Page](https://courses.cs.washington.edu/courses/cse351/24sp/labs/lab3.html).
