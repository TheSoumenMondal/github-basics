# Git Fundamentals

## Basic Git Commands and Concepts

### 1. Initializing a Repository
`git init` - Initializes a folder with Git by creating a `.git` directory that contains all the logic needed to track versions of your project.

### 2. Understanding Git Areas

#### Working Area
The working area contains files that are not currently tracked by Git. Changes in these files are not being managed by Git yet. When running `git status`, these appear as "untracked files."

#### Staging Area
The staging area (also called the index) contains files that will be part of the next commit. This is where Git tracks changes between the last version and the current version.

**Adding files to staging area:**
```bash
git add <filename>
```

**Removing files from staging area:**
```bash
git rm --cached <filename>
```

#### Repository Area
This area contains the complete history of your project including all previously committed versions. Git manages files in this area and knows their complete history.

### 3. Committing Changes

A commit captures a snapshot of the project's staged changes and creates a version record.

**Creating a commit with editor:**
```bash
git commit
```
This opens the default editor (usually Vim):
1. Press `i` to enter insert mode
2. Write your commit message
3. Press `Esc` followed by `:wq` and Enter to save and exit

**Creating a commit with inline message:**
```bash
git commit -m "commit message"
```

### 4. Viewing and Managing Changes

**View commit history:**
```bash
git log
```
Press `q` to exit the log view.

**Discard changes in working area:**
```bash
git restore <filename>
```
Removes all changes from a file, reverting it to the last committed version.

**Move file from staging area back to working area:**
```bash
git restore --staged <filename>
```

**Remove file from Git tracking:**
```bash
git rm <filename>
```
Removes the file from Git tracking and moves it to the working area.

**Compare commits:**
```bash
git diff <commitId1> <commitId2>
```
Shows differences between two specific commits.

### 5. Working with Remotes

**List remote connections:**
```bash
git remote
```

**Add a new remote connection:**
```bash
git remote add <remote-name> <remote-url>
```
Connects your local repository to a remote repository.

**Remove a remote connection:**
```bash
git remote rm <remote-name>
```

**Rename a remote connection:**
```bash
git remote rename <old-name> <new-name>
```

**Download changes from remote repository:**
```bash
git pull <remote-name> <branch-name>
```

### 6. Recommended Git Workflow

When collaborating on GitHub, follow this workflow:
1. Make your changes locally
2. Stage changes with `git add <file>`
3. Commit changes with `git commit -m "<message>"`
4. Pull latest changes from remote with `git pull`
5. Push your changes with `git push`

### 7. Merge Conflicts

Merge conflicts occur when multiple people make changes to the same parts of a file before collaborating. These conflicts must be resolved manually before changes can be committed.