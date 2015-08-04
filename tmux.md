Tmux Cheat Sheet
================

`ctrl + b` is default to enter before you enter the commands. `M` = Left Alt key
or ESC key

## Windows

| command | description |
|---------|-------------|
| c       | Create a new window.
| &       | Kill the current window.
| n       | Change to the next window.
| p       | Change to the previous window.
| ,       | Rename the current window.
| w       | Choose the current window interactively.
| M-n     | Move to the next window with a bell or activity marker.
| M-p     | Move to the previous window with a bell or activity marker.

## Panes

| command | description |
|---------|------------ |
| "       | Split the current pane into two, top and bottom.
| %       | Split the current pane into two, left and right.
| x       | Kill the current pane.
| ;       | Move to the previously active pane.
| o       | Select the next pane in the current window.
| !       | Break the current pane out of the window.
| q       | Briefly display pane indexes.

## Other

| command | description |
|---------|-------------|
| d       | Detach the current client.
| $       | Rename the current session.
| [       | Enter copy mode to copy text or view the history.
| f       | Prompt to search for text in open windows.
| r       | Force redraw of the attached client.
| L       | Switch the attached client back to the last session.
| $       | Rename Current Session
| :       | Enter the tmux command prompt
| ?       | List all key bindings
| f       | Search window titles and goto that window
| i       | Briefly display window information
| r       | Force redraw of the attached client.
| s       | Select a new session for the attached client interactively.
| t       | Show the time.
| =       | Choose which buffer to paste interactively from a list.
| ]       | Paste the most recently copied buffer of text.
| .       | Move window

## Create a new session

Any of these will work.

```bash
tmux
tmux new
tmux new-session
```

## Reattach to a session

Any of these commands will work.

```bash
tmux at
tmux attach
tmux attach-session
```

## List sessions

Any of these commands will work.

```bash
tmux ls
tmux list-sessions
```
    
## How to copy and paste

1. Enter copy-mode `C-b [`
2. Move to text, press `Space` to select text, move cursor to highlight text
3. Press `Enter`
4. Back at the command prompt, press `C-b ]` and the text you selected is pasted

## References

* http://www.openbsd.org/cgi-bin/man.cgi?query=tmux&sektion=1#KEY+BINDINGS

