## for each directory<br>commands can be added prepended with an &&
<pre>for d in ./*/ ; do (cd "$d" && echo "$d" && git status); done</pre>

## for the current directory. <br>commands can be added  seperated by semicolon's

<pre>d=${PWD##*/};echo ; echo $d;echo ;  git status $d;</pre>

## for each branch 

<pre>for BRANCH in `git branch --list| cut -c 3-`; do echo $BRANCH; done </pre>

## for each branch including all origin's origin 
<pre>git fetch --all; for BRANCH in `git branch --all| cut -c 18-`; do echo $BRANCH; done</pre>
## How I use it: (wipes all the work and gets it updated to origin.
<pre>git fetch --all; for BRANCH in `git branch --all| cut -c 18-`; do git checkout $BRANCH; git reset --hard origin/$BRANCH; done</pre>
