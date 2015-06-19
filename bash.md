Bash Cheat Sheet
================

## Moving

| command  | description                    |
|----------|--------------------------------|
| ctrl + a | Goto BEGINNING of command line |
| ctrl + e | Goto END of command line       |
| ctrl + b | move back one character        |
| ctrl + f | move forward one character     |
| alt + f  | move cursor FORWARD one word   |
| alt + b  | move cursor BACK one word      |

## Other

| command  | description                    |
|----------|--------------------------------|
| ctrl + d          | Delete the character under the cursor |
| ctrl + l          | Clear the screen (same as clear command) |
| ctrl + p          | Fetch the previous command from the history list, moving back in the list (same as up arrow) |
| ctrl + n          | Fetch the next command from the history list, moving forward in the list (same as down arrow) |
| ctrl + u          | Clear all BEFORE cursor |
| ctrl + k          | Clear all AFTER cursor |
| ctrl + r          | Search backward starting at the current line and moving 'up' through the history as necessary |
| crtl + s          | Search forward starting at the current line and moving 'down' through the history as necessary |
| ctrl + c          | kill whatever is running |
| ctrl + d          | Exit shell (same as exit command) |
| ctrl + w          | delete the word BEFORE the cursor |
| ctrl + t          | swap the last two characters before the cursor |
| ctrl + y          | paste (if you used a previous command to delete) |
| ctrl + z          | Place current process in background |
| ctrl + _          | undo |
| esc + t           | Swap last two words before the cursor |
| esc + .           | |
| esc + _           | |
| alt + [Backspace] | delete PREVIOUS word |
| alt + <           | Move to the first line in the history |
| alt + >           | Move to the end of the input history, i.e., the line currently being entered |
| alt + ?           | |
| alt + *           | |
| alt + .           | print the LAST ARGUMENT (ie "vim file1.txt file2.txt" will yield "file2.txt") |
| alt + c           | |
| alt + d           | |
| alt + l           | |
| alt + n           | |
| alt + p           | |
| alt + r           | |
| alt + t           | |
| alt + u           | |
| ~[TAB][TAB]       | List all users |
| $[TAB][TAB]       | List all system variables |
| @[TAB][TAB]       | List all entries in your /etc/hosts file |
| [TAB]             | Auto complete |
| !!                | Run PREVIOUS command (ie `sudo !!`) |
| !vi               | Run PREVIOUS command that BEGINS with vi |
| cd -              | change to PREVIOUS working directory |
    
# Kill a job

n = job number, to list jobs, run `jobs`

```bash
kill %n
```

Example:

```bash
kill %1
```

## References

1. http://cnswww.cns.cwru.edu/php/chet/readline/readline.html
