# Saving and reusing results

The `C-S` and `C-Z` [keys](keyboard-actions.md) let you save the current search list.  The list is saved to a file in your cache folder.  We refer to this kind of file as a _cached list file_, _cached file_ or _list file_.   You can save a cached file, which lists the pathnames inside the current search path, and even keep a collection of cached files, which represent your favorite folders.  If you pass f4 the path of a cached file instead of a folder, f4 will search inside the cached file. It will start faster.  This is particularly convenient when the search path leads to a large folder, such as the whole tree under `/`.  These are the steps to save and reuse a cached list for `/`:

```sh
# passing a folder (/) to build an on-the-fly list
f4 /   # wait for f4 to generate the list then press
       # C-S (or C-Z) to save the list to your cache folder
       # finally press ESC to exit f4

# passing a cached file to re-use the saved list
f4 ~/.cache/f4/+
```

The particular name of the cached file depends on the current search path as explained in note 1 of section [Keyboard actions](keyboard-actions.md).
`C-Z` saves the file overwriting an existing list file, if any.
`C-S` saves the file after making a backup of the existing file.  Backups are kept indefinitely until you purge them from your cache folder.

When you pass f4 a file, f4 disables all advanced controls inside the "Advanced..." expander. This is because they cannot apply to a cached list, unlike when f4 is started with a folder path, and the controls modify the live search performed in the folder to build an on-the-fly list.  Understand that the saved list is a snapshot of a file tree taken at a specific time.  The snapshot reflects the current state of the file tree filtered by all advanced options and fuzzy search terms.

The advantage of searching in a saved list is speed because f4 does not need to scan the disk to build the list of pathnames.  Typing fuzzy search terms to narrow down the list works whether f4 is passed a folder or a file.

Cached files can be read with common text utilities, such as `grep`, `awk`, etc. A list file consists of a simplified [YAML](https://en.wikipedia.org/wiki/YAML) header followed by an empty line then the compressed list file.

Drawing a parallel with the `locate` command, working with cached files is similar to what one would do for `locate`, where locate's database is updated periodically by running `updatedb` and searched in with `locate`.  `C-S` (`C-Z`) is f4's equivalent of updatedb. You can update the database as you perform a search by pressing `C-S` to keep a history of snapshots for the current search path.

----

[index](index.md)

