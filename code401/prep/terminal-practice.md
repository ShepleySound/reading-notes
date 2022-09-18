# Prep - Terminal Practice

These notes are distilled from sections of [Ryan Chadwick's Command Line Tutorial](https://ryanstutorials.net/linuxtutorial/).

## The Command Line
The Linux/Unix command line, also known as the `terminal`, allows users to interact with the system in a text-based manner. The terminal has an extra component, the `shell`, which determines how the terminal will behave. Typically, the user enters commands into the terminal and it runs, or executes, the commands and displays some sort of output to the user.

## Basic Navigation
In most cases, commands given to the terminal uses the current location/directory in some manner. Thus, understanding how to navigate directories within the terminal is very important. Here's a few notes on the matter:  
1. `pwd` prints the path of the current directory.
2. `ls` displays the files or directories inside of the current (or given) directory.
3. `cd` moves the current directory to the given location.
4. Commands can be given using either absolute paths or relative paths. Relative paths are given in relation to the current location.

## More About Files
Something odd to wrap the mind around - everything in Linux is a file, and files are extensionless. Directories are just special types of files. Unlike Windows, the Linux system doesn't use the file extension to determine a file's type, so a file's extension could be changed and the system will treat it the same as before. The `file` command can be used to determine what type of file something is.  

Files and directories can be marked as hidden by placing a period in front of the name.  

## Manual Pages

Manual pages for each command can be used to see information about a command. It is accessed using the `man` command, followed by the command for which information is desired. The `man` command even has a man page!

## File Manipulation
A few commands for file manipulation:  
- `mkdir` creates a directory in the given location.
- `rmdir` removes a directory, as long as it is empty.
- `touch` creates an empty file.
- `cp` copies a file or directory to a new location.
- `mv` moves a file or directory to a new location. It can also be used to rename files or directories.
- `rm` removes files. The -r option can be added to recursively remove files and directories, allowing for the removal of directories that contain files.

## Cheat Sheet
| Command | Description |
|---------|---|
| pwd | Prints the current directory. |
| ls | Displays whatever is contained within the current (or given) directory |
| cd | Changes directories. |
| man | Displays a manual page for the given command. |
| man -k | Takes a search term, and searches through the manual pages. |
| mkdir | Creates a directory. |
| rmdir | Removes an empty directory. |
| touch | Creates an empty file. |
| rm | Removes a file. The -r command makes this recursive. |
| mv | Moves a file or directory. Can also be used to rename a file or directory. |