# Learning Linux

## History
kernel = most important piece in operating system, allows the hardware to talk to the software
1969 - Ken Thompson and Dennis Ritchie of Bell Labs develop the UNIX operating system (later rewritten in C)
1991 - Linus Torvalds begins developing the Linux kernel

## Linux system
Divided into 3 main parts
1. hardware - all hardware that your system runs on as well as memory, CPU, disks, etc.
2. Linux kernel
3. User space - where users directly interact with the system

### Basic Commands
Already know = ls, cd, touch, cat, cp, mv, mkdir, rm, find, history
pwd = print working directory
file <fileName> = will tell what kind of file it is
you can combine files to look at 2 with cat -> cat <fileName1> <fileName2>
less <fileName> = almost like Vim but only looking - g to beginning, G to end, q to quit, /search
!! = rerun previous command
for cp, -r = recursive, -i = prompt before rewriting over a file with the same name
mkdir -p Documents/test/subdirectory = creates subdirectories at the same time (parent flag)
rmdir = remove directory
man <command> = manual pages built into most Linux operating systems that provide documentation about commands 
whatis <command> = gives your description into what that command does
alias foobar='ls -la' = creates an alias for a command, this does foobar for ls -la. Keep permanent aliases in ~/.bashrc
unalias foobar = undo above
exit = to exit from the shell


