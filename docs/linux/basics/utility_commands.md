# Utility commands
## find 
The find command is used to find a particular file within a directory. It also supports various options to find a file such as byname, by type, by date, and more.

The following symbols are used after the find command:

(.) : For current directory name

(/) : For root
```
find . -name "*.pdf"  
```
## locate 
The locate command is used to search a file by file name. It is quite similar to find command; the difference is that it is a background process. It searches the file in the database, whereas the find command searches in the file system. It is faster than the find command. To find the file with the locates command, keep your database updated.
```
locate <file name>  
```
## date 
The date command is used to display date, time, time zone, and more.
```
date  
```
## cal 
The cal command is used to display the current month's calendar with the current date highlighted.
```
cal<
```
## sleep 
The sleep command is used to hold the terminal by the specified amount of time. By default, it takes time in seconds.
```
sleep <time>
```
## time 
The time command is used to display the time to execute a command.
```
time
```
## df
The df command is used to display the disk space used in the file system. It displays the output as in the number of used blocks, available blocks, and the mounted directory.
```
df
```
## exit 
Linux exit command is used to exit from the current shell. It takes a parameter as a number and exits the shell with a return of status number.
```
exit
```
## clear 
Linux clear command is used to clear the terminal screen.
```
clear
```
