# DmenuFM

A bash script serving as a simple file manager using the dmenu dynamic menu app from suckless.org (tools.suckless.org/dmenu)

## Usage:
Select directory to enter it, select file to open it, 'Esc' to exit. Entering command/app name runs it (if no file selected). Entering a command/app name after a selected file runs the command/app on the selected file. Adjust default directory, terminal/file manager command, app to open files and dmenu options in the script.
Additional features:
* Tilde (~) to jump to default directory
* '..' to jump to parent directory
* '\\' to run terminal/file manager in the current directory
* '/.' to toggle hidden file view
* 'add [Name]' to bookmark the current directory under [Name]
* '\' to enter the bookmark mode (Esc to leave the bookmark mode); In the bookmark mode select bookmark to jump to it and
  ** '[Bookmark] rm' to remove [Bookmark]
  ** '[Bookmark] top' to move the [Bookmark] to the top of the list
* Copy and move functionality:
  ** 'file1 cp file2' copies file1 to file2
  ** 'file1 mv file2' moves file1 ot file2


## Note:
* The script does a rather primitive input parsing (with sed) and doesn't process filenames with spaces that well. For safety purposes, remove command on files wasn't implemented. In case of ambiguity cp and mv commands should fail, but still be careful!
* You probably want to set up a shortcut in your window manager/desktop enviroment for this script to use it efficiently.
* Script starts in previously active directory saved in fm.log in the same directory as the script (if file doesn't exists it is created).
* Script saves the bookmarks in the file fm_bookmark in the same directory (if file doesn't exists it is created); Format for each entry is 'Bookmark name, [path to directory]'

## Dependencies:
* Dmenu >= 4.6

## Authors:
Tonci Antunovic