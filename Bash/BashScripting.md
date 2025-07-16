# Bash Shell Scripting

## What Is BASH

BASH -Bourn Again Shell  
Extenshion `.sh`

## File Basic

`#!/bin/bash` Should be the starting line of every bash file  
`#!` (shebang) Tells which interpreter should be used  
`/bin/bash` Is the path to the interpreter  
`bash filename.sh` To execute bash file
If as said above starting line is precent we can do `./filename.sh`  
 Don't forget to make the file executable with chmod

## Echo

Prints Message  
`Echo Hello` >> Hello

## Variables

Declared like `VARIABLE_NAME='somethig'`  
Called like `$VARIABLE_NAME`  
`echo $VARIABLE_NAME` >> somethig

## Read Values From User

`read FIRST_NAME` Promts for entering

## Piping `|`

`ls -l /user/bin | grep bash` Filters all files containing bash word in it ,grep is used for this filtering  
In piping forwards the output of Command after pipe symbol to the one behind

## Output redirection

Send Output of command to a file  
`>` Overwrites  
`>>` append's  
`echo Hello World > file.txt` >> Hello World will be stored in fil.txt  
To send output of a file to a command  
`wc -w < file.txt` Here `wc -w` is for getting word count output of file.txt will be passed to check for count  
`<<`  
`<<<`

## IF

```
if [condition]; then
    elif [condition]; then
    else
fi
```

## CASE

```
case 'a' in
        'a' | 'b')
        echo ''
        ;;
    'c')
        echo
        ;;
    *)
        echo
esac
```

## Array

arrayname=(i1 i2 i3) Syntax  
space is used for item seperations  
`MY_ARRAY=(1 2 3 4)`  
`echo ${MY_ARRAY}`>>Displays 1<sup>st</sup> element  
`echo ${MY_ARRAY[@]}`Display entire array  
`echo ${MY_ARRAY[1]}` >> 2 >> display item in 1 index

## For loop

for

## Test (Comparing Values)

[ hello = hello ]
