## Common used commands
### pwd
The pwd command is used to display the location of the current working directory.
```
pwd
```
### mkdir
The mkdir command is used to create a new directory under any directory..
```
mkdir <directory name>  
```
### rmdir
The rmdir command is used to delete a directory.
```
rmdir <directory name>
```
### ls
The ls command is used to display a list of content of a directory.
```
ls
```
### cd
The cd command is used to change the current directory.
```
cd <directory name>
```
### touch 
The touch command is used to create empty files. We can create multiple empty files by executing it once.
```
touch <file name>  
touch <file1>  <file2> ....  
```
### cat 
The cat command is a multi-purpose utility in the Linux system. It can be used to create a file, display content of the file, copy the content of one file to another file, and more.
```
cat [OPTION]... [FILE]..  
```
To create a file, execute it as follows:
```
cat > <file name>  
// Enter file content  
```
Press "CTRL+ D" keys to save the file. To display the content of the file, execute it as follows:
```
cat <file name>   
```
### rm 
The rm command is used to remove a file.
```
rm <file name>
```
### cp
The cp command is used to copy a file or directory.
```title='To copy in the same directory:'
cp <existing file name> <new file name>
```
### mv 
The mv command is used to move a file or a directory form one location to another location.
```
mv <file name> <directory path> 
```
### rename
The rename command is used to rename files. It is useful for renaming a large group of files.
```
rename 's/old-name/new-name/' files  
```
For example, to convert all the text files into pdf files, execute the below command:
```
rename 's/\.txt$/\.pdf/' *.txt  
```
### head 
The head command is used to display the content of a file. It displays the first 10 lines of a file.
```
head <file name>  
```
### tail
The tail command is similar to the head command. The difference between both commands is that it displays the last ten lines of the file content. It is useful for reading the error message.
```
tail <file name>
```
### tac 
The tac command is the reverse of cat command, as its name specified. It displays the file content in reverse order (from the last line).
```
tac <file name>  
```
### more 
The more command is quite similar to the cat command, as it is used to display the file content in the same way that the cat command does. The only difference between both commands is that, in case of larger files, the more command displays screenful output at a time.

In more command, the following keys are used to scroll the page:

**ENTER key:** To scroll down page by line.

**Space bar:** To move to the next page.

**b key:** To move to the previous page.

**/ key:** To search the string.
```
more <file name>
```
### cat
The cat command is also used as a filter. To filter a file, it is used inside pipes.
```
cat <fileName> | cat or tac | cat or tac |. . .   
```
### grep 
The grep is the most powerful and used filter in a Linux system. The 'grep' stands for "global regular expression print." It is useful for searching the content from a file. Generally, it is used with the pipe.
```
command | grep <searchWord> 
```
### wc 
The wc command is used to count the lines, words, and characters in a file.
```
wc <file name>
```
### sort 
The sort command is used to sort files in alphabetical order.
```
sort <file name>  
```
### gzip 
The gzip command is used to truncate the file size. It is a compressing tool. It replaces the original file by the compressed file having '.gz' extension.
```
gzip <file1> <file2> <file3>...  
```
### gunzip 
The gunzip command is used to decompress a file. It is a reverse operation of gzip command.
```
gunzip <file1> <file2> <file3>. .  
```
## Utility commands
### find 
The find command is used to find a particular file within a directory. It also supports various options to find a file such as byname, by type, by date, and more.

The following symbols are used after the find command:

(.) : For current directory name

(/) : For root
```
find . -name "*.pdf"  
```
### locate 
The locate command is used to search a file by file name. It is quite similar to find command; the difference is that it is a background process. It searches the file in the database, whereas the find command searches in the file system. It is faster than the find command. To find the file with the locates command, keep your database updated.
```
locate <file name>  
```
### date 
The date command is used to display date, time, time zone, and more.
```
date  
```
### cal 
The cal command is used to display the current month's calendar with the current date highlighted.
```
cal<
```
### sleep 
The sleep command is used to hold the terminal by the specified amount of time. By default, it takes time in seconds.
```
sleep <time>
```
### time 
The time command is used to display the time to execute a command.
```
time
```
### df
The df command is used to display the disk space used in the file system. It displays the output as in the number of used blocks, available blocks, and the mounted directory.
```
df
```
### exit 
Linux exit command is used to exit from the current shell. It takes a parameter as a number and exits the shell with a return of status number.
```
exit
```
### clear 
Linux clear command is used to clear the terminal screen.
```
clear
```
