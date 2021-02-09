# f4

**f4 - fuzzy file finder CLI in a GTK dialog**

f4 is powered by [fzf](https://github.com/junegunn/fzf), and
[gtkdialog](https://github.com/puppylinux-woof-CE/gtkdialog)
built with [libvte](http://ftp.gnome.org/pub/GNOME/sources/vte/).  
See section _[Installing f4](installing.md)_ for a complete list of dependencies.

[f4 home](https://github.com/step-/f4)  
[installing f4](installing.md)  
[keyboard actions](keyboard-actions.md)  
[saving and reusing](saving-reusing.md)  
[options and configuration](options-configuration.md)  
[translations](translations.md)  
[reporting bugs](https://github.com/step-/f4/issues)  

## Starting f4

> Usage: `[ F4_ENVIRONMENT ...] f4 [ FOLDER | FILE ]`

`F4_ENVIRONMENT` is where you can pass [options and configure](options-configuration.md) f4.  
`FOLDER` is the path of the folder to search in. Relative paths are supported.  
`FILE` is the path of an f4 search results file previously saved with the [save feature](saving-reusing.md).

## f4's value

f4 searches files using `find`.  In that sense, it is just a front-end for find, the file search command for the console.  So, what's more in f4?

* f4 is a _graphical_ application offering point-and-click search options
* it is a live search--changing an option changes the search results immediately
* it allows you to fuzzily search find's results to get that file you can only name approximately
* it starts a program of your own choosing when you activate a search result
* it can save and reuse lists of search results

## Searching with f4

In f4 you search in a list of partial results by typing some words, presumably fragments of the file name you are looking for.  The fuzzy finder (fzf) quickly narrows down the list to a few result candidates.  Keep typing until you can eyeball the line with your target file.  Select that line with the `ArrowUp` and `ArrowDown` keys¹ then press `ENTER` to activate the selection.  This opens the file manager² to show the location of the target file.

¹ Use the `TAB` key to select/unselect multiple targets.  
² By default ROX-Filer; it can be changed to any other command.  

To summarize, f4 performs a search in the file system using find then a word search in find's results using fzf.  You don't need to know find or fzf to perform a search, just type.

## Advanced searching

Do spend a few minutes reading about [fzf's search rules](https://www.mankier.com/1/fzf#Extended_Search_Mode) ([source](https://github.com/junegunn/fzf#search-syntax)). They can help narrow down the result list faster and more precisely to your advantage.

You can also reduce and fine-tune find's results before or while you are typing search terms.  Open f4's advanced dialog by clicking the "Advanced..." label or pressing `F1`.  Choose which type of objects to search for, and which paths to keep out.  Settings apply under the search path immediately.

## Keyboard actions

[keyboard actions](keyboard-actions.md)

## Saving and reusing results

[saving and reusing](saving-reusing.md)

## Options and configuration

[options and configuration](options-configuration.md)

## Translations

[translations](translations.md)

