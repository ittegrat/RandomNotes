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

## abort merge
git merge --abort
git reset --hard HEAD

## delete remote tag
git tag -d 12345
git push origin :refs/tags/12345

## reset old author
git rebase -i <parent-commit>
 1. mark commits with e
 2. git commit --amend --author="Author Name <email@address.com>"
 3. git rebase --continue
 4. if diverged push -f

=============================================

git branch -m new-name  
git branch -m old-name new-name  
git push origin :old-name new-name  
git push origin -u new-name  

=============================================
Copy commit somewhere

Go to the stable branch:
git checkout stable

Copy the desired commit to the current branch.
git cherry-pick e87568fa

You can now return to dev:
git checkout dev

=============================================
http://sethrobertson.github.io/GitFixUm/fixup.html
