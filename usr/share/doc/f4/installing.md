# Installing f4

## Dependencies

* [fzf](https://github.com/junegunn/fzf) **minimum recommended version 0.25.1**;
  if you must use an earlier version, 0.23.1 is recommended
* [gtkdialog](https://github.com/puppylinux-woof-CE/gtkdialog) built with [libvte](http://ftp.gnome.org/pub/GNOME/sources/vte/)
* [bash](https://www.gnu.org/software/bash/)
* any `find` (f4 is tested with [findutils](https://www.gnu.org/software/findutils/)' find)
* [GNU coreutils](https://www.gnu.org/software/coreutils/)'s `cp` for `C-S` (saving with backup); `C-Z` (saving without backup) does not need `cp`
* [procps-ng](https://gitlab.com/procps-ng/procps)'s `pgrep` (busybox's `pgrep` is not enough)
* `date`, `grep`, `gzip`, `sed`.

f4 is developed and tested on [Fatdog64 Linux](http://distro.ibiblio.org/fatdog/web/).

**Optional programs**

* [bat](https://github.com/sharkdp/bat) if installed, bat enhances the help pager
* [yad](https://github.com/v1cont/yad) used only for debugging. ([yad for GTK-+2](https://github.com/step-/yad))

## Fatdog64 810

* Start the Gslapt package manager applet located in Fatdog64's Control Panel's System tab:
 - update the list of available packages
 - install packages fzf and gtkdialog-vte.
* Download the [latest version of f4](https://github.com/step-/f4/releases/latest)
 - unpack the archive and run the installer following the included README file.

## FossaPup64 9.5

The Ubuntu repository provides a very old version of fzf that works with f4 with minor limitations.
Remember to upgrade fzf to the minimum recommended version or higher as soon as practical.

* Start the Puppy Package Manager:
 - update the database of available packages
 - install package fzf from the Ubuntu repository.
* Download the [latest version of f4](https://github.com/step-/f4/releases/latest)
 - unpack the archive and run the installer following the included README file.
* Run fixmenus from the system menu.
* Run `update-icon-caches /usr/share/icons/hicolor`

## DebianDog-Sid and FossaDog

The Debian repository provides a somewhat old version of fzf.
The Ubuntu repository provides a very old version of fzf.
Both versions work with f4 with minor limitations.
Remember to upgrade fzf to the minimum recommended version or higher as soon as practical.

* Start Synaptics package manager from the system menu:
 - reload the list of available packages
 - install package fzf
* Download the [latest version of f4](https://github.com/step-/f4/releases/latest)
 - unpack the archive and run the installer following the included README file.
* For DebianDog-Sid only run `update-icon-caches /usr/share/icons/hicolor`.
* FossaDog places the menu entry for f4 in the _Other_ category.
 - For DebianDog-Sid edit file `/usr/share/applications/f4.desktop` and change the category to `Category=Utility;`.
* Create the new file `/etc/profile.d/f4.sh` with the following content:

```sh
export F4_FILE_OPEN_COMMAND="pcmanfm \"\$F4_SEARCH_IN/\$1\""
```

This file will be sourced automatically for all shells after the next reboot.  Until then f4 will default to ROX-Filer for opening files with the Control-o key.

----

[index](index.md)

