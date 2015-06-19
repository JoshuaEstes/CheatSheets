Git Cheat Sheet
===============

## Subtree Example

### Add sub-project as remote

```bash
git remote add -f RemoteName RemoteUrl
```

### Run `git subtree` command

```bash
git subtree add --prefix Path/To/Put/Code NameOfRemote master --squash
```

#### Pull subtree as needed

```bash
git fetch NameOfRemote master
git subtree pull --prefix Path/To/Put/Code NameOfRemote master --squash
```

### Reference

* http://blogs.atlassian.com/2013/05/alternatives-to-git-submodule-git-subtree

## Create a branch without a parent

Very useful when you are updating a project that you are rewriting. For example,
say you are using semantic versioning and are wanting to start a new major
version.

```bash
git checkout --orphan BRANCH
```

## Delete All Branches that have been merged

Great for cleaning up local branches that aren't being used any more.

```bash
git checkout master
git branch --merged | grep -v "\*" | xargs -n 1 git branch -d
```

## Ignore changes to a file that is being tracked

### Ignore

```bash
git update-index --assume-unchanged [directory|file]
```

### Unignore

```bash
git update-index --no-assume-unchanged [directory|file]
```

## How to ignore dirty submodules

Edit your ``.git/config`` and add ``ignore = dirty``.

```text
[submodule "path/to/submodule"]
    path = path/to/submodule
    url = git://github.com/username/repo.git
    ignore = dirty
```

## Clone a repo and give name other than origin

```bash
git clone -o upstream https://repo.git
```

## Ignore Files for Repository without using `.gitignore`

Add the file `.git/info/exclude` and fill it with the contents you want to ignore. This will ONLY apply to the
repository and will not be tracked by git.

## Squash Commits

```bash
git log
```

Count the number of commits that you have made, let's say the previous 5 are your commits.

```bash
git rebase -i HEAD~5
```

The first commit leave as `pick` the rest will need to be changed to `squash`. After that you will be able to
leave a new commit message or just leave as is to keep the commit messages from all previous commits.

## Search for a specific line of code/file in the history

```bash
git log -S[search term]
```

Example:

```bash
git log -SThatOneFile.php
```

## Copy file from one branch to current branch

Copy a file from `branch` and put into staging.

```bash
git checkout BRANCH path/to/file.ext

# Real Life Examples
git checkout origin/featureBranch web/js/random.js
# Pulls into your current branch web/js/random.js from
# origin/featureBranch
```

## Git Grepping for fun and profit!

```shell
# Basic grep (case sensitive)
$ git grep 'search term'

# Case Insensitive search
$ git grep -i 'search term'

# Search within a directory
$ git grep 'search term' src/

# Search only files with `php` extension
$ git grep 'search term' -- '*.php'

# Grep in the 'src/` directory, only yml files
$ git grep 'search term' -- 'src/**.yml'
```
