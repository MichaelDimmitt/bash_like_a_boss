## for each directory<br>commands can be added prepended with an &&
`for d in ./*/ ; do (cd "$d" && echo "$d" && git status); done`

## for the current directory. <br>commands can be added  seperated by semicolon's

`d=${PWD##*/};echo ; echo $d;echo ;  git status $d;`

## for each branch 

for BRANCH in `git branch --list| cut -c 3-`; do echo $BRANCH; done 
