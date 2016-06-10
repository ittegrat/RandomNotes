git config user.name ittegrat
git config user.email ittegrat@users.noreply.github.com

git commit --amend --reset-author

git config --local push.default matching

git fetch upstream master + git merge upstream/master ( ? git pull ? )
git push origin

mkdir /path/to/somewhere
git archive branch-of-interest | tar -xC /path/to/somewhere

ALTERNATIVE:
 git --work-tree=/path/to/somewhere checkout branch-of-interest -- .

git merge --no-commit --no-ff master

git diff branch1 branch2 -- path/to/file
git difftool -x C:/Programs/WinMerge/WinMergeU.exe branch1 branch2 -- path/to/file

# abort merge
git reset --hard HEAD

