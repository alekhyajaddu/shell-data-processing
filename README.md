# Shell Data Processing
## Basic Power shell commands
 
1. Open powershell here as administrator in windows, Create a new subfolder named shell-data-processing using
2. mkdir - Creates a new folder
 
mkdir shell-data-processing

3. Change directory into your sub folder.
4. ni - Creates a new item.
 powershell 
ni .gitignore
ni README.md

5. ls - lists the items 

## Git Bash Commands

## commands used to get the page text
 bash
 curl ""http://shakespeare.mit.edu/romeo_juliet/full.html"

## commands used to get the page text and output to a "data.txt" file

curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O "data.txt"

- The curl command will return the source for that URL - not the displayed page contents. 


## The command you used to find the most common words, sorted.
- tr transforms the file content - tr (bash) commands 
## Transform each space ' ' into a return character '\12' (aka ASCII line feed)

tr ' ' '\12' < returnedfile

## Pipe the output to sort (send the results of one command as input into another command)

tr ' ' '\12' < returnedfile | sort

## Pipe the sorted output to uniq -c to count

tr ' ' '\12' < returnedfile | sort | uniq -c

## Pipe the reduced output to sort with -nr flag

tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr

## Redirect the output to result.txt

tr ' ' '\12' < result.txt | sort | uniq -c | sort -nr > result.txt

## Important bash commands
- Bash redirect (>):  type ls > filelist.txt to redirect the contents of your directory into a file. 
- Bash redirect & append (>>): use two arrows to append rather than overwrite. 
- Type ls to list the contents of the default directory. Send the result to a new file called temp.txt (ls > temp.txt). 
- Use the cat command to display the contents of temp.txt. 
- Copy in Bash is not CTRL+C as in Windows, instead use CTRL+SHIFT+C.

## Bash preview:
- cat filename
- head -10 filename.fx
- tail -2 filename.fx

### PowerShell cat:
- Get-Content filename.fx
- gc one.txt -head 2
- gc one.txt -tail 2

## Data file
[data.txt](https://github.com/alekhyajaddu/shell-data-processing/blob/master/data.txt)

## Result file
[result.txt](https://github.com/alekhyajaddu/shell-data-processing/blob/master/result.txt)
