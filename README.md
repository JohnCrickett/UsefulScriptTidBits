Useful script tidbits
=====================

## Bash Scripts ##

### Find files with extension and run a command against those files ###
`find . -name "*.txt" -type f -exec head -n2 {} \;`

### Remove space between first and second column of a text file: ###
`sed -r 's/[[:blank:]]+//1' infile.txt`
replace the 1 with another number to do other columns

### Find the number of files in a dir ###
`find DIR_NAME -type f | wc -l`
replace DIR_NAME with the directory
