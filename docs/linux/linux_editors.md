# Text Editors in linux
### vi/vim editor
The vi editor is elaborated as visual editor. It is installed in every Unix system. In other words, it is available in all Linux distros. It is user-friendly and works same on different distros and platforms. It is a very powerful application. An improved version of vi editor is vim.

**Installation**
```
sudo apt update
sudo apt install vim -y
vim --version
```

**The vi editor has two modes:**

* **Command Mode:** In command mode, actions are taken on the file. The vi editor starts in command mode. Here, the typed words will act as commands in vi editor. To pass a command, you need to be in command mode.

* **Insert Mode:** In insert mode, entered text will be inserted into the file. The Esc key will take you to the command mode from insert mode.

By default, the vi editor starts in command mode. To enter text, you have to be in insert mode, just type **'i'** and you'll be in insert mode. Although, after typing **'i'** nothing will appear on the screen but you'll be in insert mode. Now you can type anything.

To exit from insert mode press **Esc** key, you'll be directed to command mode.

```py
vi ./file.txt
```

| Commands	  | Action   |
| ----------- | -------- |
:wq |	Save and quit 
:w	| Save
:q	| Quit
:w fname	| Save as fname
ZZ	| Save and quit
:q!	| Quit discarding changes made
:w!	| Save (and write to non-writable file)

**Command to cut, copy and paste:**

| Commands	  | Action   |
| ----------- | -------- |
dd | Delete a line
yy |	(yank yank) copy a line
p  |	Paste after the current line
P  |	Paste before the current line

### Nano editor
Nano is a straight forward editor. It is designed for both beginners and advanced users. It has many customization features.

Some advanced features of a nano text editor are as following:

* It has highly customizable key bindings
* It supports syntax highlighting
* It has undo and redo options
* It provides full line display on the standard output
* It has pager support to read from standard input

To open file with nano editor, execute the command as follows:
```
nano <file name>  
```
In the nano editor, the useful options are given at the bottom, use the **CTRL+ option** to perform an operation. For example, to **exit** from the editor, use **CTRL +X** keys. 