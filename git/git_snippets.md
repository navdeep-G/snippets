## Remove all your local git branches but keep master

`git branch | grep -v "master" | xargs git branch -D` 

## Updating submodules
cd submodule
git checkout COMMIT
cd ..
git add submodule
git commit -m "Update submodule"
