## Remove all your local git branches but keep master

git branch | grep -v "master" | xargs git branch -D 
