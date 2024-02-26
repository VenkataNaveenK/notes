# OS operations
## glob module
The glob module, which is short for global, is a function that’s used to search for files that match a specific file pattern or name. It can be used to search CSV files and for text in files. 

We can use glob to search for a specific file pattern, or perhaps more usefully, use wildcard characters to search for files where the file name matches a certain pattern.

These patterns are similar to regular expressions but much simpler.

- **Asterisk (*)**: Matches zero or more characters.
- **Question mark (?)**: Matches exactly one character.

Example:
```py
import glob

path = 'input'
files = glob.glob(path+'/*.csv')
```
## os module
| Method | Description |
| -------| ------------|
os.chdir(path) | Change the current working directory
os.getcwd() | Returns the current working directory
os.getenv(key, default=None) | Return the value of the environment variable key as a string if it exists, or default if it doesn’t. key is a string.
os.listdir(path='.') | Returns a list of the names of the entries in a directory
os.mkdir(path, mode=0o777, *, dir_fd=None) | Creates a directory (with a specified mode)

## os.path module
| Method | Description |
| -------| ------------|
os.path.basename(path) | Return the base name of pathname path
os.path.abspath(path) | Return a normalized absolutized version of the pathname path
os.path.dirname(path) | Return the directory name of pathname path
os.path.exists(path) | Return True if path refers to an existing path or an open file descriptor
os.path.getsize(path) | Return the size, in bytes, of path
os.path.isfile(path) | Return True if path is an existing regular file
os.path.isdir(path) | Return True if path is an existing directory
os.path.join(path, *paths) | Join one or more path segments intelligently
os.path.normcase(path) | Normalize the case of a pathname. On Windows, convert all characters in the pathname to lowercase, and also convert forward slashes to backward slashes. On other operating systems, return the path unchanged.
os.path.normpath(path) | Normalize a pathname by collapsing redundant separators and up-level references so that A//B, A/B/, A/./B and A/foo/../B all become A/B. This string manipulation may change the meaning of a path that contains symbolic links. On Windows, it converts forward slashes to backward slashes. To normalize case, use normcase().

## shutil module
| Method | Description |
| -------| ------------|
shutil.copy2(src, dst, *, follow_symlinks=True) | Identical to copy() except that copy2() also attempts to preserve file metadata
shutil.copytree(src, dst, symlinks=False, ignore=None, copy_function=copy2, ignore_dangling_symlinks=False, dirs_exist_ok=False) | Recursively copy an entire directory tree rooted at src to a directory named dst and return the destination directory. All intermediate directories needed to contain dst will also be created by default.
shutil.rmtree(path, ignore_errors=False, onerror=None, *, onexc=None, dir_fd=None) | Delete an entire directory tree; path must point to a directory (but not a symbolic link to a directory)
shutil.move(src, dst, copy_function=copy2) | Recursively move a file or directory (src) to another location and return the destination.