## for each directory<br>commands can be added prepended with an &&
`for d in ./*/ ; do (cd "$d" && echo "$d" && git status); done`

## for the current directory. <br>commands can be added  seperated by semicolon's

`d=${PWD##*/};echo ; echo $d;echo ;  git status $d;`

