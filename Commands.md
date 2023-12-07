
### cp (Copy)

-   **Usage**: Copy files and directories.
-   **Common Flags**: `-r` (recursive), `-v` (verbose).
-   **Example**: Copy a file to another directory.
  
    `cp source.txt /destination/directory/` 
    

### mv (Move)

-   **Usage**: Move or rename files and directories.
-   **Common Flags**: `-v` (verbose).
-   **Example**: Rename a file.
   
    
    `mv oldname.txt newname.txt` 
    

### ls (List)

-   **Usage**: List directory contents.
-   **Common Flags**: `-l` (long listing), `-a` (all files), `-h` (human-readable sizes), `-S` (sort by file size).
-   **Example**: List files sorted by size.
    
    `ls -lhS` 
    

### du (Disk Usage)

-   **Usage**: Estimate file space usage.
-   **Common Flags**: `-h` (human-readable), `-s` (summarize).
- `-d=N`: Analyze up to `N` levels of directories deep.
-   **Example**: Display disk usage of a directory.
    
    `du -sh -d 1 /path/to/directory` 
    

### df (Disk Free)

-   **Usage**: Report file system disk space usage.
-   **Common Flags**: `-h` (human-readable).
-   **Example**: Display disk space of file systems.
    
    bashCopy code
    
    `df -h` 
    

### sed (Stream Editor)

-   **Usage**: Stream editor for filtering and transforming text.
-   **Example**: Replace 'old' with 'new' in a file.
    `sed 's/old/new/' file.txt` 
  -  **Example**: Replace all occurrences of 'apple' with 'orange' in a file.
  `sed 's/apple/orange/g' file.txt`

    

### tr (Translate)

-   **Usage**: Translate or delete characters.
-     Works only on streams (like those from a pipe or standard input).
-   **Example**: Replace lowercase with uppercase.
    
    `echo "Hello World" | tr 'a-z' 'A-Z'` 
    

### time

-   **Usage**: Measure program resource use.
-   **Example**: Time a program's execution.
    `time ./script.sh` 
    

### grep (Global Regular Expression Print)

-   **Usage**: Search for patterns in text.
-   **Common Flags**: `-i` (ignore case), `-r` (recursive).
`-w` flag in the `grep` command is used to match whole words in the tex
-   **Example**: Search for 'text' in all files recursively.
    
    `grep -ri "text" /path/to/directory` 
    

### zip

-   **Usage**: Package and compress (archive) files.
-   **Example**: Zip a directory.
   
    
    `zip -r archive_name.zip /path/to/directory` 
    

### unzip

-   **Usage**: Extract files from a ZIP archive.
-   **Example**: Unzip an archive.
       
    `unzip archive_name.zip` 
    

### cat (Concatenate)

-   **Usage**: Read, concatenate, and write files.
-   **Example**: Display the content of a file.
    
    `cat file.txt` 
    
- Displays content of multiple files
    `cat file1.txt file2.txt`
    
- Write to a file
`cat file1.txt > newfile.txt`

- Append to a file
-  `cat file1.txt >> existingfile.txt`

    

### echo

-   **Usage**: Display a line of text.
-   **Example**: Print text to the console.
   
    `echo "Hello, World!"` 
    

### wc (Word Count)

-   **Usage**: Print newline, word, and byte counts for files.
-   **Common Flags**: `-l` (lines), `-w` (words), `-c` (bytes).
-   **Example**: Count words in a file.
    
    `wc -w file.txt` 
    

### sort

-   **Usage**: Sort lines of text files.
-   **Common Flags**: `-n` (numeric sort), `-r` (reverse sort).
-   **Example**: Sort a file numerically.
    
    `sort -n file.txt`

### awk
The `awk` command in Linux is a powerful text processing tool, commonly used for data extraction and reporting. Here is a basic usage format

`awk [options] 'pattern {action}' file`

- `awk` to print the first and third columns of a file Default separator whitespace:
`awk '{print $1, $3}' filename`

- print the first and third fields of a file where fields are separated by commas:
`awk -F',' '{print $1, $3}' filename`

- let's say you want to print the first field of each line where the second field is equal to a specific value, for instance, "XYZ".
`awk -F',' '$2 == "XYZ" {print $1}' data.txt`

