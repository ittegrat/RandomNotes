### BASIC UPDATE CYCLE ###
1. git checkout master
1. git pull upstream master
1. git checkout ittegrat
1. git merge --no-commit --no-ff master
1. ... compile and check ...
1. git commit -m 'Merge Uzer/Repo@SHA10 into ittegrat'
1. git push origin
