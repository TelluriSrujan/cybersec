# Linux Commands

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
