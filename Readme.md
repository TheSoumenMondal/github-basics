1. `git init` : Powers your folder with git and create a .git folder into the current directory and it includes all the logic to track the version of your project.


2. `working area` :  There can be a bunch of files that are not currently tracked by git.This means the changes done or to be done in those files are not being managed by the git.A file which is in working area is considered to be not in  the staging area.When we do 'git status' and we see bunch of 'untracked files' then these are actually called to be in the working area.


3. `Staging area area` : What all files are going to be the part of next version.This is the area where git understands what are the changes from the last version and current version.

Here is the command to add any file to staging area
```
git add <filename>
```

Now how can we remove any file from staging are and bring it back to the working area ?

```
git rm --cached <filename>
```

4. `Repository area` : The area contains all the details about all of your previous registered versions.And the files in this area , git already managing them and know their history.

5. `Commit` : Commit is a particular version of your project. It captures a snapshot of the project's stage changes and create a version out of it.

```
git commit -m "<Your commit message>"
```

