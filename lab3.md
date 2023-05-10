# Lab Report 3

Researching Commands
I chose to look more into the `grep` command.
After researching this command I found it is useful to search texting patterns in files.
`r` (`recessive`) - Allows you to search for a pattern recursively in a directory and its subdirectories.
Here is example 1 

`$ grep -r "pattern" ./technical
./technical/file1.txt:This is a pattern example.
./technical/subdir/file2.txt:Another pattern instance.`

 The word "pattern" is searched in all files within the ./technical directory and its subdirectories.

Here is example 2

`$ grep -r "error" ./technical/logs`
`./technical/logs/error.log:2023-05-10 12:34:56 Error: Connection timed out.`
`./technical/logs/subdir/debug.log:2023-05-10 13:45:21 Warning: Possible error in configuration.`

The word "error" is searched in all files within the ./technical/logs directory and its subdirectories.




