Title: gdb Useful Commands
Date: 2010-12-18 12:26
Category: programming
Tags: debugging, gdb
Authors: Bhargav Bhat
Summary: Listing of Useful gdb Commands

Here's a list of very useful gdb commands:

- Debugging

	- From command prompt: `gdb prog.out`
	- From command prompt with args: `gdb --args prog.out <arg1> <arg2>`
	- Attach to process: `gdb` and then `attach <pid>`
	- From coredumps: `gdb prog.out -c <dumpfile>`

- Breakpoints

	- Break at function : `break <func_name>`
	- Break at line : `break <line_num>`
	- Break at source file & line : `break <src_file>.c <line_num>`
	- Show Breakpoints : `info breakpoints`
	- Remove Particular breakpoint : `delete <index>`
	- Toggle breakpoints : `enable <index>` or `disable <index>`
	- Remove all breakpoints: `delete`
	- Remove breakpoints in func : `clear <func_name>`
	- Remove brekapoints at line : `clear <line_num>`

- Running/Stepping

	- Start execution : `run` or `r`
	- Continue execution :  `cont` or `c`
	- Line by line execution :  `step` or `s` (will step-into functions)
	- Line by line execution : `next` or `n` (will step-over functions)
	- Run next few lines : `next <count>`
	- Stop program : `kill` or `^C`

- Callstack & State

	- View stack trace : `backtrace` or `bt`
	- View current state : `frame`
	- View local variables : `info locals`
	- View CLI args : `info args`
	- View Global and Static vars : `info variables`
	- View variable : `print <var_name>` (`print/x` to view as hex)
	- View arrays : `print <arr>[<idx>]` or `print *<arr>@<size>` 

- View Source
	
	- View code around current point : `list` or `l`
	- View code around line : `list <line>`
	- View code in func : `list <file>:<func>`

*Notes/Links*

```
https://beej.us/guide/bggdb/
https://linux.die.net/man/1/gdb
https://web.mit.edu/gnu/doc/html/gdb_toc.html
https://courses.cs.washington.edu/courses/cse378/97au/help/gdb-intro.html
```
