Mutt Cheat Sheet
================

## General

These key bindings will work on almost any menu you are in.

| command    | description |
|------------|-------------|
| *          | Move to last entry
| =          | Move to first entry
| :          | Enter muttrc command
| >          | Scroll down one line
| <          | Scroll up one line
| [          | Scroll up half a page
| ]          | Scroll down half a page
| ?          | Help
| ;          | Apply next function to tagged messages only
| !          | Invoke command in subshell
| return   | Select the current entry
| esc + /  | Search up
| /          | Search down
| H          | Move to top of page
| j          | Move to next entry
| k          | Move to previous entry
| ctrl + l | Redraw screen
| L          | Move to bottom of page
| M          | Move to middle of page
| n          | Move to next match of search
| q          | Exit menu
| t          | Tag current entry
| z          | Move to next page
| Z          | Move to previous page

## Index Menu

When you first open mutt you are in the index menu.

| command       | description |
|---------------|-------------|
| &             |  Link tagged message to current one
| #             |  Break the thread in two
| %             |  Toggle whether mailbox will be rewritten
| .             |  List mailboxes with new mail
| $             |  Save changes to mailbox
| @             |  Display full address of sender
| |             |  Pipe message to a shell command
| esc + tab |  Jump to previous new or unread message
| return      |  Display message
| tab         |  Jump to next new or unread message
| a             |  Create alias from message sender
| b             |  Remail message to another user
| esc + c     |  Open a different folder (Read Only)
| c             |  Open a different folder
| esc + C     |  Make text/plain copy
| C             |  Copy message to another file/mailbox
| esc + d     |  Delete all messages in subthread
| d             |  Delete current message
| ctrl + D    |  Delete all messages in thread
| D             |  Delete messages matching a pattern
| esc + e     |  Use the current message as a template for a new one
| e             |  Edit the raw message
| ctrl + E    |  Edit attachment content type
| f             |  Forward message with comments
| ctrl + F    |  Wipe passphrase from memory
| F             |  Toggle the important flag for message
| g             |  Reply to all
| G             |  Retrive mail from POP server
| h             |  Display message and toggle header weeding
| j             |  Move to next undeleted message
| esc + k     |  Mail a PGP key
| k             |  Move to previous undeleted message
| ctrl + K    |  Extract supported public keys
| esc + l     |  Show current limit pattern
| l             |  Only show messages matching a pattern
| L             |  Reply to specific mailing list
| m             |  Compose new message
| esc + n     |  Jump to next subthread
| ctrl + N    |  Jump to next thread
| N             |  Toggle new flag
| o             |  Sort messages
| O             |  Sort messages in reverse order
| Q             |  Query external program for addresses
| q             |  Save changes to mailbox and quit
| r             |  Reply to message
| ctrl + P    |  Jump to previous thread
| esc + p     |  Jump to previous subthread
| p             |  Print current message
| esc + P     |  Check for classic PGP
| P             |  Jump to parent message in thread
| ctrl + R    |  Mark current thread as read
| R             |  Recall a postponed message
| esc + r     |  Mark current subthread as read
| esc + s     |  Save text/plain copy and delete
| s             |  Save message/attachment to mailbox/file
| esc + t     |  Tag current thread
| ctrl + T    |  Untag messages matching a pattern
| T             |  Tag messages matching pattern
| esc + u     |  Undelete all messages in subthread
| u             |  Undelete current entry
| ctrl + U    |  Undelete all messages in thread
| U             |  Undelete messages matching pattern
| esc + v     |  Collapse/uncollapse current thread
| v             |  Show mime attachments
| esc + V     |  Collapse/uncollapse all threads
| V             |  Show mutt version number and date
| w             |  Set a status flag
| W             |  Clear status flags from message

## Pager Menu

| command | description |
|---------|-------------|
| # | |
| a | |
| b | |
| c | |
| esc + c | |
| C | |
| esc + C | |
| d | |
| ctrl + D | |
| esc + d | |
| w | |
| W | |
| e | |
| ctrl + E | |
| f | |
| F | |
| g | |
| h | |
| j | |
| J | |
| k | |
| K | |
| & | |
| L | |
| ctrl + L | |
| m | |
| n | |
| N | |
| ctrl + N | |
| esc + n | |
| o | |
| O | |
| p | |
| ctrl + P | |
| esc + p | |
| Q | |
| q | |
| r | |
| R | |
| ctrl + R | |
| esc + r | |
| esc + e | |
| s | |
| S | |
| esc + s | |
| t | |
| T | |
| u | |
| esc + u | |
| ctrl + U | |
| v | |
| V | |
| \\ | |
| @ | |
| | | |
| ? | |
| space | |
| - | |
| ^ | |
| $ | |
| ! | |
| : | |
| . | |
| / | |
| esc + / | |
| return | |
| P | |
| esc + P | |
| esc + k | |
| ctrl + K | |
| ctrl + F | |

## Useful key remaps

These need to be placed in your `muttrc` file. I use vim and so I want to use some of the
same commands to manage my mail.

```muttrc
# Does not replace and currently mapped keys and acts like the vim command gg and takes
# you to the top of the page
bind index gg first-entry

# Replaces the retrieval of mail from a POP server. This will take you to the bottom of
# the page, just like it does in vim
bind index G last-entry
```

## Flags

When viewing messages in the index menu, you will see various flags such as `N` which mean
the messages is new and `D` which means that the message is to be deleted. This is a short
list of those flags.

| flag | description |
|------|-------------|
| ! | Message is flagged
| * | Message is tagged
| + | Message is To: you and only you
| C | Message is Cc: to you
| d | Message has attachments marked for deletion
| D | Marked for deletion
| F | Message is From: you
| K | Contains PGP key
| L | Message is sent to a subscribed mailing list
| n | Thread contains new messages (Only when thread is collapsed)
| N | Message is new
| o | Thread contains old messages (Only when thread is collapsed)
| O | Message is old
| P | Message is PGP encrypted
| r | Message has been replied to
| s | Message is signed
| S | Message is signed and verified
| T | Message is to you and has others in To: or Cc:
