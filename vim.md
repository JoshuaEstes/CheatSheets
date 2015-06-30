Vim Cheat Sheet
===============

## Open a file

| command             | description |
|---------------------|-------------|
| vim + file.ext      | Open file at last line
| vim +42 file.ext    | Open file at line 42
| vim +/^include_path | Open the file at the line that starts with include_path

## Exiting

| command | description |
|---------|-------------|
| :q      | Quit
| :wq     | Write and Quit
| :q!     | Quit without saving
| ZZ      | Write and quit
| ZQ      | Quit without saving

## Moving

| command         | description |
|-----------------|-------------|
| b               | Move to the BEGINNING of the word
| e               | Move to the END of the word
| ge              | Move to the END of the PREVIOUS word
| gg              | Move to START of buffer
| G               | Move to END of buffer
| h               | Move cursor LEFT
| j               | Move cursor DOWN
| k               | Move cursor UP
| l               | Move cursor RIGHT
| *n* gg OR *n* G | Move to n line (n represents a digit)
| w               | Move to the start of the next word
| ctrl+b          | Move BACK one page
| ctrl+f          | Move FORWARD one page

## Inserting Text

| command | description |
|---------|-------------|
| a       | append after the cursor
| A       | append at end of line
| i       | Insert before cursor
| I       | Insert before line
| o       | Create new line below and start editing
| O       | Create new line above and start editing
| gi      | Place cursor where you were last editing (Useful for when you exit Insert mode and then need to go back where you once were)

## Other Commands

| command  | description |
|----------|-------------|
| u        | undo
| ctrl + R | redo

## Buffers

| command | description |
|---------|-------------|
| :ls     | List current buffers
| :bn     | Next buffer
| :bp     | Previous Buffer
| :bd     | Close Buffer

## Tabs

| command | description |
|---------|-------------|
| :tabnew | create new tab
| :tabn   | move to NEXT tab
| :tabp   | move to PREVIOUS tab
| :tabfir | goto FIRST tab
| :tablas | goto LAST tab

## Windows

| command    | description |
|------------|-------------|
| ctrl + w s | Split window horizontally
| ctrl + w v | Split window vertically
| ctrl + w q | Close current window, if last window then exit vim
| ctrl + w c | Close current window, will not exit vim
| ctrl + w o | Make window the only window on the screen

## Spell Checking

```vimrc
" ~/.vimrc
" Enable spell checking
set spell
```

### Commands

| command | description |
|---------|-------------|
| ]s      | Move to next misspelled word
| [s      | Move to previous misspelled word
| z=      | Show list of possible replacements words

## Marcos

1. Press `q` then press another key that you want to assign it to. Example: `qq`
1. Enter commands
1. Press `q` when finished
1. To run the macro, press `@` and then the key that it is assigned to. Example `@q`
1. NOTE: Can be ran multiple times. Enter the number of times you want it to run then the macro. Example `10@q` will run the macro 10 times.

## Code Folding

| command | description |
|---------|-------------|
| zo      | OPEN code fold under cursor
| zc      | CLOSE code fold under cursor
| zR      | OPEN ALL code folds
| zM      | CLOSE ALL code folds

## Marks

| command     | description               |
|-------------|---------------------------|
| ma          | Create mark **a** in file |
| 'a          | Jump to mark **a**        |
| d'a         | Delete line mark **a**    |
| :marks      | List marks                |
| :delmarks a | Deletes mark **a**        |
| :delmarks!  | Deletes all marks         |

## Auto complete

| command           | description |
|-------------------|-------------|
| ctrl + x ctrl + o | Autocomplete current word
| ctrl + x ctrl + n | word completion next
| ctrl + x ctrl + p | word completion previous
| ctrl + x ctrl + f | Complete filename
| ctrl + x ctrl + l | Whole line completion

### Enable

```vimrc
" ~/.vimrc
autocmd FileType python set omnifunc=pythoncomplete#Complete
autocmd FileType javascript set omnifunc=javascriptcomplete#CompleteJS
autocmd FileType html set omnifunc=htmlcomplete#CompleteTags
autocmd FileType css set omnifunc=csscomplete#CompleteCSS
autocmd FileType xml set omnifunc=xmlcomplete#CompleteTags
autocmd FileType php set omnifunc=phpcomplete#CompletePHP
autocmd FileType c set omnifunc=ccomplete#Complete
```

## Reformat mixed indent files

```vim
" Goto first line in file
gg
" Enter visual line mode
shift+v
" Goto the last line of the file
shift+g
" Filter lines
=
```

## Multi Liners

```
:set tw=80                  Sets text width to 80 characters
    gg                      Goto first line
    gqG                     Format file till you reach the last line
```

## Remove trailing whitespace on the ends of every line

```vim
:%s/\s\+$//
```
