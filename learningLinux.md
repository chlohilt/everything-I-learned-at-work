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

### Standard Out/In/Error
echo Hello > text.txt = puts Hello into text.txt file, > is a redirection operator
echo Hello ?? text.txt = puts Hello at the bottom of text.txt file, doesn't allow it to overwrite
cat < peanuts.txt > banana.txt = gives peanuts.txt as stdin redirection for cat
stderr prints stuff out to the screen but is a different stream from stdout -> file descriptor for stdin, stdout, stderr is 0,1,2 respectively
    - to redirect stderr to a file -> ls /fake/directory 2> peanuts.txt
    - to see both stderr and stdout in file? -> ls /fake/directory > peanuts.txt 2>&1
    - short cut for above ^^ -> ls /fake/directory &> peanuts.txt
    - to get rid of stderr messages completely, use special file /dev/null which will discard any input

### Pipe and Tee
pipe operator (|) lets us get stdout of command and make that stdin to another process 
`ls -la /etc | less`
to write the output of command to two different streams, use tee command
`ls | tee peanuts.txt`

