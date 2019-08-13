Useful script tidbits
=====================

## Bash Scripts ##

### Find files with extension and run a command against those files ###
`find . -name "*.txt" -type f -exec head -n2 {} \;`

For example, find all files in a directory tree where the name matches a pattern and grep them:

`find . -name \*.txt -exec grep pattern {} +`

### Sorting some output and getting the first and last values (lines) ###

`<some command generating output> | sort | sed -n '1p;$p'`

`<some command generating output> | sort | tee >(head -n 1) >(tail -n 1) >/dev/null`

### Extract lines beginning with a pattern ###
`sed -n -e '/^{"pattern"/p' infile.txt` 

### Remove space between first and second column of a text file: ###
`sed -r 's/[[:blank:]]+//1' infile.txt`
replace the 1 with another number to do other columns

### Find the number of files in a dir ###
`find DIR_NAME -type f | wc -l`
replace DIR_NAME with the directory

### Kill all processes matching a pattern ###
`ps aux |grep pattern_of_process |awk '{print $2}' |xargs kill`
