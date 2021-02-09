# Keyboard actions

Below the symbol `C-x` represents simultaneously pressing the `control` and `x` keys then releasing the keys.
`S-` represents the `shift` key.

Keys                 | Action
:---                 | :-----
`F10`                | open the hotkey menu below the main window
`C-H`¹               | page the help file
`Up`, `Down`         | change which line is current
`PageUp`, `PageDown` | scroll the list
`TAB`                | mark the current line selected
`S-TAB`              | unmark the current line
`ENTER`              | locate the files in the selected lines --the current line if no line was selected; see `F4_FILE_LOCATE_COMMAND`
`C-O`¹               | open the files in the selected lines; see `F4_FILE_OPEN_COMMAND`
`C-L`                | page through the error logs for `ENTER`, `C-O` and the `find` command
`C-R`                | replay `find` and refresh the search results --the current query is still in effect
`C-S`²               | save the current list state to a file in your cache folder
`C-Z`²               | like `C-S` but without backup
`ESC`                | quit f4 --`C-C`, `C-G`, `C-Q` also quit; see `F4_HOTKEY_ESC`
`ESC`³               | close the current GUI sub-dialog window
`F1`º                | reveal and focus the Help button; with repeated presses focus switches cyclically between the button and the search prompt
`F2`º                | open the folder browser
`F3`º                | edit keep-out paths
`F4`                 | open the cache folder if it exists--keep quiet if it does not


¹ Inside the pager:

Keys                 | Action
:---                 | :------
`ENTER`              | close and return to the search list
`Up`, `Down`         | next/previous file
`S-Up`, `S-Down`     | scroll one line
`PageUp`, `PageDown` | scroll one page
`C-W`                | toggle line wrapping

² `$F4_CACHE_PATH/+filename`.  `+filename` is obtained from the current search path by keeping all alphanumerics, dash, underscore and dot characters and replacing all other characters with `+`, e.g. `/root/Documents` becomes `+root+Documents`. If you press `C-S` an existing file will be backed up and a new file will be created in its place.  If you press `C-Z` an existing file will be overwritten.  

³ This key acts on GUI dialogs.  It cannot be redefined.  Note that you should use `ENTER` to close the `C-H` help preview in the terminal because using `ESC` would quit f4.

º Read about redefining hotkeys in section `F4_HOTKEY_ESC` of [options and configuration](options-configuration.md).  

----

[index](index.md)

