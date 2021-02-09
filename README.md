title: F4  
date: 2021-02-08  
homepage: <https://github.com/step-/f4>  

# f4

Fuzzy file finder CLI in a GTK dialog

## Benefits

* graphical application
* simple -- start searching immediately with sane defaults
* live search -- search as you type
* fuzzy search -- get that file you can only name approximately
* file manager integration -- press `ENTER` to locate the file
* fast -- save and reuse lists of search results

## Installing

This program can be installed from a command line shell prompt.
It should be installed to `/` for system-wide availability.

It can be started from a shell prompt.  The installer also adds an "f4"
entry in section "Filesystem" of the system application menu.

First, install according to [/usr/share/doc/f4/installing.md](usr/share/doc/f4/installing.md).

Then download the latest archive **attachment** from the release page[:1](#LINKS).
Unpack the archive into a folder of your choice.

Open a terminal window in that folder and run the following command: `install/bin/install.sh`.
This will start an interactive installer, which includes a Help screen.

Assuming a successful installation with default settings, enter command
`f4` in a shell prompt to start the program and `ESC` to exit.

**Important** --- After having completed the installation you **must** save file
`install.log`, which is located in folder `install/`, if you want to be able to
uninstall this program in the future.  Indeed, it is recommended to save the
whole folder `install/`, which holds the uninstall program and the log file.

## Uninstalling

From the folder where you unpacked the downloaded archive run the following
command: `install/bin/uninstall.sh`.
This will start an interactive uninstaller, which includes a Help screen.

<a name="basic"></a>

## Help

[/usr/share/doc/f4/index.md](usr/share/doc/f4/index.md)

Press `F1` then `ENTER` to read the HTML help file in your browser.

Press `Control+H` to read the text help page in f4's pager.

## Translations

[/usr/share/doc/f4/translations.md](usr/share/doc/f4/translations.md)

## AUTHOR

step

<a name="LINKS">

## LINKS

**Homepage**
[github.com/step-/f4](https://github.com/step-/f4)

**:1** release page
[github.com/step-/f4/releases](https://github.com/step-/f4/releases)

**:2** forum thread
[]()
