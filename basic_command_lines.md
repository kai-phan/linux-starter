# Command line

## The echo
### The shell
The shell is a command line tool to display the current shell. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $SHELL
```

### The prompt
The prompt is a command line tool to display the current prompt. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $PS1
```

### The PATH
The PATH is a command line tool to display the current PATH. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $PATH
```

### The home directory
The home directory is a command line tool to display the current home directory. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $HOME
```

### The current directory
The current directory is a command line tool to display the current directory. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $PWD
```

### The user
The user is a command line tool to display the current user. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $USER
```

### The hostname
The hostname is a command line tool to display the current hostname. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ echo $HOSTNAME
```

---------------------------------------

### The history
The history is a command line tool to display the current history. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ history
```

## The date
``` bash
$ date
```

## The calendar
The calendar is a command line tool to display a calendar. It is part of the GNU Coreutils package and is implemented by calling the function strftime(3) with the appropriate format string and a time zone of UTC0.
``` bash
$ cal
```

## The time
The time is a command line tool to display the current time. It is part of the GNU Coreutils package and is implemented by calling the functions gettimeofday(2) and localtime(3), with a time zone of UTC0.
``` bash
$ time
```

## The current directory
The current directory is a command line tool to display the current directory. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ pwd
```

## The list
The list is a command line tool to display the current directory. It is part of the GNU Coreutils package and is implemented by calling the function getpwuid(3).
``` bash
$ ls [-a | -l | -R | -t | -S | -r | -h | -i | -d | -F | -1] [<dir>]
```

- a : all
- l : long
- R : recursive
- t : time
- S : size
- r : reverse
- h : human
- i : inode
- d : directory
- F : file type
- 1 : one

## Change directory
The change directory is a command line tool to change the current directory. It is part of the GNU Coreutils package and is implemented by calling the function chdir(2).
``` bash
$ cd [. | .. | ~ | - | <dir>]
```
- . : current directory
- .. : parent directory
- ~ : home directory
- \-: previous directory

## Make file
The make file is a command line tool to make a file. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ touch <file>
```

=> touch can modify the timestamp of a file.

## File
The file is a command line tool to display the type of file. It is part of the GNU Coreutils package and is implemented by calling the function stat(2).
``` bash
$ file <file>
```

```bash
$ file basic_command/target/parent/children/abc.txt
```

## Read file
The read file is a command line tool to read a file. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ cat <file>
```

=> cat can read multiple files.
```bash
$ cat basic_command/target/parent/children/abc.txt basic_command/target/parent/children/abc.json
```

## Read file with line number
The read file with line number is a command line tool to read a file with line number. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ nl <file>
```

## Read file with line number and tab
The read file with line number and tab is a command line tool to read a file with line number and tab. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ nl -s "	" basic_command/target/parent/children/abc.json
```

## Read file with line number and tab and header
The read file with line number and tab and header is a command line tool to read a file with line number and tab and header. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ nl -s "	" -b a basic_command/target/parent/children/abc.json
```

## Read file with line number and tab and header and footer
The read file with line number and tab and header and footer is a command line tool to read a file with line number and tab and header and footer. It is part of the GNU Coreutils package and is implemented by calling the function open(2).
``` bash
$ nl -s "	" -b a -f basic_command/target/parent/children/abc.json
```

## Copy 
The copy is a command line tool to copy files and directories. It is part of the GNU Coreutils package and is implemented by calling the function copy(2).
``` bash
$ cp [-i | -f | -r] <source> <destination>
```
Can use wildcards.

``` bash
$ cp basic_command/target/parent/children/*.txt basic_command/result
```

Recursive copy
``` bash
$ cp -ri basic_command/target/parent/children basic_command/result
```

- i : interactive
- f : force
- r : recursive

## Move
The move is a command line tool to move files and directories. It is part of the GNU Coreutils package and is implemented by calling the function move(2).
``` bash
$ mv [-i | -f | -u | -b] <source> <destination>
```

- i : interactive
- f : force
- u : update
- b : backup

=> Can update a file with a newer version.
``` bash
$ mv basic_command/target/parent/children/abc.txt basic_command/target/parent/children/abcd.txt
```

=> Can move multiple files.
``` bash
$ mv -i basic_command/target/parent/children/move.t basic_command/result/children
```

=> Can use wildcards.
``` bash
$ mv -i basic_command/target/parent/children/*.txt basic_command/result/children
```

## Make directory
The make directory is a command line tool to make a directory. It is part of the GNU Coreutils package and is implemented by calling the function mkdir(2).
``` bash
$ mkdir [-p | -v] <dir>
```

## Remove
The remove is a command line tool to remove files and directories. It is part of the GNU Coreutils package and is implemented by calling the function remove(2).
``` bash
$ rm [-i | -f | -r] <file>
```

- i : interactive
- f : force
- r : recursive

=> Can use wildcards.
``` bash
$ rm -i basic_command/result/children/*.txt
```

## Remove directory
The remove directory is a command line tool to remove a directory. It is part of the GNU Coreutils package and is implemented by calling the function rmdir(2).
``` bash
$ rmdir [-i | -f | -r] <dir>
```

## Find
The find is a command line tool to find files and directories. It is part of the GNU Coreutils package and is implemented by calling the function find(2).
``` bash
$ find <dir> [-name | -type | -size | -empty | -perm | -user | -group | -mtime | -mmin | -newer | -exec | -ok] <pattern>
```

- name : name
- type : type (d: directory, f: file, l: link)