## Pre-requisite: 
You have to know the  'sha' (Simple Hashing Algorithm)  for the  deleted branch using below command.
```
git reflog
```
Now you have two options, either checkout using sha  or HEAD
```
git checkout  -b <deleted branch> <sha> 

(OR)

git checkout HEAD@{18}
```
