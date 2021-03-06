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

### Abort merge
git merge --abort<br>
git reset --hard HEAD

### Delete remote tag
git tag -d 12345<br>
git push origin :refs/tags/12345

### Reset old author
`git rebase -i <parent-commit>`
 1. mark commits with e
 2. `git commit --amend --author="Author Name <email@address.com>"`
 3. `git rebase --continue`
 4. if diverged push -f

### Mirroring a repository
1. `git clone --bare https://github.com/exampleuser/old-repository.git`
2. `cd old-repository.git`
3. `git push --mirror https://github.com/exampleuser/new-repository.git`

### Rename a local and remote branch
1. Rename the local one: `git branch -m new-name / git branch -m old-name new-name`
2. Delete the remote one: `git push origin :old-name new-name`
3. Push the new-name local branch: `git push origin -u new-name`

### cherry-pick
1. Checkout the receiving branch: `git checkout stable`
2. Copy the desired commit to the current branch: `git cherry-pick e87568fa`

### Move the most recent commit(s) to a new branch
Note: Any changes not committed will be lost.
1. Create a new branch, saving the desired commits: `git branch newbranch`
2. Move current branch back by 3 commits: `git reset --hard HEAD~3`
3. Go to the new branch that still has the desired commits: `git checkout newbranch`

=============================================<br>

git config sendpack.sideband false

=============================================<br>
http://sethrobertson.github.io/GitFixUm/fixup.html

### SSL Problems
`GIT_SSL_NO_VERIFY=true git ...`<br>
`git config [–local] http.sslVerify false`
