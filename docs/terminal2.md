# Using the CLI correctly and efficiently

## POSIX Command pattern
```
[program/utility] [option/flag] [argument]
```

## How to know the usage of a program/utility

### Looking for the program/utility
For example you are looking for a file Downloader tool. You can do 
```
apropos downloader # to see the ones existing in your system

# or

apt search downloader # to search packages 
```
It might not give you promissing results. therefore, like any other penguin user [Google it](https://www.google.com/search?q=cli+file+downloader+linux) click on any relevant result, and learn what you need. 

### Man page
`man` is the shorten term for Manual. It is used to see the extentive manual for a program/utility
```
man [program/utility]
```
for example
```
man apt-get  # open manual for Debian package manager
man man      # manual for the manual
```
also try
```
man intro
```
### Help pages
An alternatie to man pages are the help option. Help pages are often less informative than man pages. Example usage-
```
wget -h
# or
wget --help
```

## Shell techniques (Bash)

### Operators
You might have too run one command after another. To run upcoming command with out waiting for the previous one to end.

**Run Unconditionally (regardless of success/failure)**  
Use a semicolon (;) between the commands. The shell executes the first command, waits for it to finish, and then proceeds to the second. 
```
command1 ; command2 ; command3
```
**Run Conditionally (only if the first command succeeds)**  
Use a double ampersand (&&) operator. The second command will only execute if the first command exits with a successful (zero) exit status. This is useful for chained operations where the second step depends on the first one working correctly. 
```
command1 && command2 && command3
```
**Run Conditionally (only if the first command fails)**  
Use a double pipe (||) operator. The second command will only execute if the first command exits with a non-zero (failure) exit status. 
```
command1 || command2
```
**Inputing output of another command**  
Use pipe (|) operator. The second command will take the output of previous command as input.
```
command1 | command2
```
**Example**  
Sync package list with repo, then if it was successful run system update, while automaticly agreeing to evrything, and shutdown afterwards regardless if the update was successful send error to a `txt` file if there was any.
```
sudo apt update && sudo apt -y upgrade ; /sbin/shutdown -h now 2>error.txt
```
**Paging long output**  
This command lists files in /usr/bin and sends the output to less, allowing you to scroll through the long list one page at a time.  
```
ls -l /usr/bin | less
```
**Filtering results**  
This command lists all running processes and pipes the output to grep, which filters and displays only the lines containing the word "bash". 
```
ps aux | grep "bash"
```

### Others

**Path Completion**  
The `TAB` key can help you in path completion and typing a path without error. You can type `cd ~/Pic` and press `TAB` to complete the path `cd ~/Pictures.`. Using wildcards `*` also works. Exampli gratia: `cd ~/Pic*`

**For more usage and techniques see the [The Bash Reference Manual](https://www.gnu.org/software/bash/manual/bash.html)**


[All commands](https://en.wikipedia.org/wiki/List_of_POSIX_commands)

