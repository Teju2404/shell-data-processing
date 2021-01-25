# shell-data-processing

## steps to the powershell:

1. Open windows here as administrator in windows.
2. Create a new subfolder shell-data-processing.Using mkdir which used to create a subfolder.
``` 
mkdir shell-data-processing
```
3. To change the directory into subfolder use cd command.
4. Creates a new empty item using ni.
``` powershell 
ni .gitignore
ni README.md
```
5. ls- Used for Listing the contents which are created using above commands.

## Commands url used to return the pagetext from an url and copies the file in output:
### Command Url:
``` bash
curl ""http://shakespeare.mit.edu/romeo_juliet/full.html" -O
```
### Command url to copy the file in "data.txt" which is an output file.
```
curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O "data.txt"
```
### Note: The curl command will return the source for that URL - not the displayed page contents. 

### To request content from an HTTPS url, you may need to use the following command:

```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
```
### If using PowerShell, close the window by hitting ALT SPACE C. 

# GitBash Commands

## To Process Text Data

- tr ' ' '\12' < returnedfile is used to Transform each space ' ' into a return character '\12'
```
tr ' ' '\12' < returnedfile
```

## Pipe the output to sort which mean sending  the results of one command as input into another command
```
tr ' ' '\12' < returnedfile | sort
```
## Pipe the sorted output to uniq -c to count
```
tr ' ' '\12' < returnedfile | sort | uniq -c
```
## Pipe the reduced output to sort with -nr flag
```
tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr
```
## Redirect the output to result.txt
```
tr ' ' '\12' < result.txt | sort | uniq -c | sort -nr > result.txt
```
## Important bash commands
- Bash redirect (>):  type ls > filelist.txt to redirect the contents of your directory into a file. 
- Bash redirect & append (>>): use two arrows to append rather than overwrite. 
- Type ls to list the contents of the default directory. Send the result to a new file called temp.txt (ls > temp.txt). 
- Use the cat command to display the contents of temp.txt. 
- Copy in Bash is not CTRL+C as in Windows, instead use CTRL+SHIFT+C.

## Bash preview:
- cat filename
- head -5 filename.fx
- tail -2 filename.fx

### PowerShell cat:
- Get-Content filename.fx
- gc one.txt -head 2
- gc one.txt -tail 2
