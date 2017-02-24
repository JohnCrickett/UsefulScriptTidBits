Useful script tidbits
=====================


### Remove space between first and second column of a text file: ###
`sed -r 's/[[:blank:]]+//1' infile.txt`
replace the 1 with another number to do other columns