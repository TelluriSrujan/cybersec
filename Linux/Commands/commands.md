# Linux Commands

Wildcards in shell :

Matches any sequence of characters :
`*`

Matches any single character :
`?`

Matches any one of the characters enclosed in brackets :
`[]`

Ex: `cp *.jpg /home` copies names ending with .jpg from current directory to 'home' directory

Note :
These wildcards can be used with many commands in the shell which support wildcards.

(1) To print working directory 
```
$ pwd 
```
(2) To change directory
```
$ cd
```
###Some important syntax shortcuts in `cd` command :

changing directory with absolute path :
`cd [Absolute Path]`

 Navigation to :
 
 current directory :
`cd .`

parent directory :
`cd ..`

home directory :
`cd ~`

previous directory :
`cd -`

going up 2 levels :
`cd ../..`

(3) To see the files and directories present in the working directory

```
$ ls
```
###Some important syntax shortcuts in `ls` command :

to see detailed list of all the directories and files :
`ls -l`

to see the detailed list of a specific directory :
`ls -l [directory]`

to show the file size in the human readable terms :
`ls -lh`

to view the hidden files :
`ls -a`

to sort the files acc to modification time :
`ls -t`

to sort the files acc to size :
`ls -S`

to list the directories instead of the contents :
`ls -d`

to show long format
`ls -l`

(4) To manage filestamps and create empty files
```
$ touch [Options] file
```
###Some important syntax and shortcuts in `touch` command :

to create a file that doesn't exist : 
`touch [File]`

to change only access time :
`touch -a [File]`

to change only modification time :
`touch -m [File]`

to accept date string instead of using current time :
`touch -d [File]`

to give same access and modification time as the reference folder :
`touch -r [Reference File] [Target File]`

to update an existing file and not create a new file if it doesn't exist :
`touch -c [File]`

Note :

Using the `touch` command on an existing file changes both the access time and modification time to current time.

(5) To identify the file's likely content without relying on the name or extension
```
$ file [File]
```
###Some important syntax and shortcuts in `file` command :

to expand to match non-hidden items and inspect each resulting operand :
`file *`

to show MIME-style info :
`file -i`

to use brief mode to omit the filename from the output :
`file -b`

to flow symbolic links and classify the targets :
`file -L`

to try examining the contents of compressed files :
`file -z`

Note:

An unusual, incomplete or damaged files may receive a broad description of 'data' instead of the precise type.

(6) To display files and join their contents
```
$ cat [File1] [File2]
```
###Some important syntax and shortcuts in `cat` command :

to concatenate the whole output to a new file named 'file' :
`cat [File1] [File 2] ... > [File]`

create a new file or overwrite an existing one using standard input :
`cat > [File]`

to add new output directly instead of replacing existing contents :
`cat >> [File]`

to number all output lines starting from 1 :
`cat -n`

to number only non empty lines :
`cat -b`

to squeeze multiple blank lines into one blank line :
`cat -s`

(7) To let the user read the entire file without scrolling till the end
```
$ less [File]
```
###Some important syntax and shortcuts in `less` command :

Navigation in `less` :

g --> Jump to beginning

G --> Jump to end

u --> Move up half screen

d --> Move down half screen

h --> Jump to built in help

Searching in `less` :

/search-term --> Searches forward for the term

?search-term --> Searches backward for the term

n --> Repeat the search in the same direction

N --> Repeat the search in opposite direction

q --> Quits the pager and restores the shell prompt

Starting `less` with options :

to show line numbers :
`less -N [File]`

to open the end of a file :
`less +G [File]`

to follow new content a it is added :
`less +F [File]`

to search and ignore cases until a pattern emerges :
`less -i [File]`

to ignore cases regardless of pattern :
`less -I [File]`

(8)To display and manage the record of commands entered
```
$ history
```

###Some important syntax and shortcuts in `history` command :

to recall earlier commands for review and editing :
'up arrow'

to expand and execute the most recent command :
`!!`

to run a command by the number :
`!(number)`

Ex: `!102` runs the command no. 102 from the history

to run a command by prefix :
`!(prefix)`

Ex: `!cat` runs the most recent command that started with cat

to begin a reverse instrumental search through command history :
'Ctrl+R'

to clear the current in-memory list :
`history -c`

to write the current list to a configured history file :
`history -w`

to delete the entry at the given entry position :
`history -d <offset>`

(9) To have a fresh visible terminal area :
```
$ clear
```

(10) To copy the files and directory trees while controlling overwrites and preserved attributes :
```
$ cp [Options] [Source File] [Destination File]
```

###Some important syntax and shortcuts in `cp` command :

to provide a new destination to an already existing directory :
`cp [Source] [Destination Filepath/new destination]`

to copy multiple files into a directory :
`cp [Source 1] [Source 2] ... [Destination File]`

to copy the whole contents of a directory into another :
`to -r`

to request recursive copying :
`cp -R`

to copy recursively while preserving any file attributes and links :
`cp -a`

to request confirmation before overwrite :
`cp -i`

to not overwrite an existing destination file :
`cp -n`

to preserve source file mode, ownership (when permitted) and timestamps :
`cp -p`

to copy source only when destination is missing or source is newer :
`cp -u`

to force overwrite by removing destination first if needed :
`cp -f`

to show each file as it is copied :
`cp -v`

Note: By default `cp` replaces an existing destination file.

(11) To rename and move a file without leaving the original pathname in place :
```
$ mv [Options] [Source File] [Destination File]
```

###Some important syntax and shortcuts in `mv` command :

to move multiple items into a directory :
`mv [Source 1] [Source 2] ... [Destination]`

to place target directory before the sources :
`mv -t [Destination File]/ [Source 1] [Source 2] ...`

to ask for confirmation before replacing an existing destination :
`mv -i`

to not override the existing destination :
`mv -n`

to make a backup of a destination which would otherwise be replaced :
`mv -b`

Note: The default backup suffix is '~'

to print each move as it happens :
`mv -v`

(12) To create directories for organising files and other directories :
```
$ mkdir [Options] [Directory Name]
```
Note :

If a directory already exists, `mkdir` reports an error and does not replace the existing directory.

###Some Important shortcuts and syntax in `mkdir` command :

to create multiple directories at once :
`mkdir [Directory1] [Directory2] ...`

to create missing parts of a filepath if an intermediary directory is missing :
`mkdir -p [Filepath]`

to specify permissions for a newly corrected directory :
`mkdir -m`

to print a message for each directory created :
`mkdir -v`


(13) To remove filesystem entries :
```
$ rm [Options] [Filepath]
```
###Some Important shortcuts and syntax in `rm` command :

to remove multip0el files at once :
`rm [File1[ [File2]....`

to ask for permission before each interval :
`rm -i`

to ignore missing operands and suppress prompts :
`rm -r`

to remove a directory tree and all of its contents :
`rm -r`

to remove an empty directory :
`rmdir`

Note : `rmdir` removes only empty directories and fails for non empty directories.

to report and send message after every single removal :
`rm -v`

(14) To search directory trees by name, type, size and time and act on verified matches :

```
$ find [Path] [Expression]
```
Note : By default `find` is recursive.

###Some Important shortcuts and syntax in `find` command :

to search in the current directory :
`find . [Expression]`

to match exact base names :
`find -name [Expression]`

to select directories :
`find -type d [Expression]`

to select files :
`find -type f [Expression]`

to match the size :
`find -size [Expression]`

to determine greater than less than in finding size :
`find -size +- [Expression]`

to print the matches :
`find -print`

to find and execute or directory and execute the command on files found :
`find -exec [Command]`

(15) To choose built-in help, program usage or manual pages for a command :
```
$ help [Built-in Name]
```
###Some Important shortcuts and syntax in `help` command :

to provide a usage summary of all the commands in list provided by `ls` command :
`ls --help`

(16) To open, navigate, search and select sections of installed manual pages :
```
$ man [Section] [Command]
```
###Some Important shortcuts and syntax in `man` command :

Navigating through `man` :

/pattern --> search forward for the pattern 

n --> repeat search for the same pattern

N --> repeat search in the opposite direction

q --> quit

Selecting manual section :

1 --> user commands

2 --> system calls

3 --> library functions

5 --> file formats

8 --> system administrator commands

9 --> kernel routines

Note :

Built in commands do not have a general man page. They can be accessed by :
`man builtins [Command]`

(17) To retrieve consice manual page descriptions and interpret their section numbers :
```
$ whatis [Command]
```

(18) To search manual page page names and keywords from a keyword :
```
$ aprops [Keyword]
```

(19) To show how the shell resolve a current name, independent of whether a manual description is installed :
```
$ type [Command]
```

(20) To create, inspect, persist, bypass and remove command aliases ;
```
$ alias [Command] = [Replacement]
```
###Some Important shortcuts and syntax in `alias` command :

To remove an alias from current bash shell :
`unalias [Command]`

(21) To run a command while ignoring any shell function or alias that shares the same name :
```
$ \[Command]
command [Command]
```

(22) To leave current shell and choose the status it returns to its caller :
```
$ exit
```
###Some Important shortcuts and syntax in `exit` command :

To set the status returned to shell's caller :
`exit [Numeral]`

Note :

By convention :

0 --> success

Non-zero --> Failure or another conditional defined by the program

No argument --> Exits with the status of last command
