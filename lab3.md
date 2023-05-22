# Lab Report 3

Researching Commands
I chose to look more into the `grep` command.
After researching this command I found it is useful to search texting patterns in files.
`r` (`recessive`) - Allows you to search for a pattern recursively in a directory and its subdirectories.
Here is example 1 
```
$ grep -r "pattern" ./technical
./technical/file1.txt:This is a pattern example.
./technical/subdir/file2.txt:Another pattern instance.
```
 The word "pattern" is searched in all files within the ./technical directory and its subdirectories.

Here is example 2
```
$ grep -r "error" ./technical/logs
./technical/logs/error.log:2023-05-10 12:34:56 Error: Connection timed out.
./technical/logs/subdir/debug.log:2023-05-10 13:45:21 Warning: Possible error in configuration.
```
The word "error" is searched in all files within the ./technical/logs directory and its subdirectories.

`i` (`--ignore-case`) - Allows you to perform a case-insensitive search.
Here is example 3
```
$ grep -i "pattern" ./technical/file1.txt
This is a PATTERN example.
Another line with pattern.
```
The word "pattern" is searched in ./technical/file1.txt without considering the case of the letters.

Here is example 4
```
$ grep -i "error" ./technical/logs/error.log
2023-05-10 12:34:56 ERROR: Connection timed out.
2023-05-10 13:45:21 Error: File not found.
```
The word "error" is searched in ./technical/logs/error.log without considering the case of the letters.

`-1` (`--files-with-matches`) - Outputs only the names of files containing the matching pattern.

Here is example 5
```
$ grep -l "pattern" ./technical/*
./technical/file1.txt
./technical/file3.txt
```
Lists the files in the ./technical directory that contain the word "pattern".

Here is example 6
```
$ grep -l "error" ./technical/logs/*
./technical/logs/error.log
./technical/logs/warnings.log
```
Lists the files in the ./technical/logs directory that contain the word "error".

`-A NUM` - Allows you to display NUM lines of trailing, leading, or both context around the matching lines.

Here is example 7
```
$ grep -A 1 "pattern" ./technical/file1.txt
This is a pattern example.
--The next line after the pattern.
```
The word "pattern" is searched in ./technical/file1.txt and displays one line of trailing context.

Here is example 8
```
$ grep -B 1 "error" ./technical/logs/error.log
--The line before the error.
2023-05-10 12:34:56 Error: Connection timed out.
```
The word "error" in ./technical/logs/error.log file and displays one line of leading context.

For each option I researched using this link [Link](https://www.gnu.org/software/grep/manual/grep.html) and chatGPT.
I only used chatGPT in understanding what the grep feature is overall to help me get a basic understanding before I looked deeper at in the link I provided. 
I'll list here what I asked it and what its output was.
Question: "in simple terms what does the grep command do".
Answer: "The grep command is a command-line utility in Unix and Unix-like operating systems that allows you to search text using patterns.
Here's the basic idea: grep stands for "global regular expression print".
It is used to search text for lines that match a certain pattern and then prints those lines to the screen.
The pattern that you provide can be simple text, or it could be a more complex regular expression."







