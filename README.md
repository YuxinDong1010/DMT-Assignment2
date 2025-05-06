# Data Mining Techniques - Assignment 2

## Getting started

This repository uses _uv_ to manage Python and its dependencies, and _pre-commit_ to run
automatic code linting & formatting, and Jupyter notebook cleanup prior to git commits. More about UV [here](https://docs.astral.sh/uv/guides/projects/). It is not necessary to use _uv_ to be able to use and run the code, but it is highly recommended in case you would like to contribute to the project. In that case, you can follow the steps below.

1. Install [uv](https://github.com/astral-sh/uv)

2. Install the project Python dependencies (you might need to open a new terminal window):

```zsh
uv sync
```

3. Install pre-commit:

```zsh
# We can use uv to install pre-commit!
uv tool install pre-commit --with pre-commit-uv --force-reinstall

# Check that pre-commit installed alright (should say 3.8.0 or similar)
pre-commit --version

# After installing pre-commit, you'll need to initialise it.
# This installs all pre-commit hooks, the scripts which run before a commit.
pre-commit install

# It's a good idea to run pre-commit now on all files.
pre-commit run --all-files
```

4. Start Jupyter

```zsh
# Jupyter lab
uv run jupyter lab

# Or Jupyter notebook (classic)
uv run jupyter notebook
```

## Best practices for working on this repository

1. Always create a new branch and pull request, do not push directly to the main branch
2. For each task, create a new branch and label it with the name of the task, e.g. "adding_of_age_parameter". Do not use your name as a branch name.
3. Try to work on one or two tasks at the same time maximum and break bigger tasks into smaller sub-tasks
4. Merge new bits of code as soon as possible (and properly tested)
5. After task is done and a branch is merged, delete the branch. Refrain from re-using the same branch name for another branch.
6. Each pull request needs to be checked by at least one person
7. All functions has to have at least one-line docstring before merging to main
8. Do as many commits as possible
9. Do not leave large chunks of commented code in the code (or at least remove it before merging to main), we can always find the removed code and reverse to an older version if needed

## Cheatsheet on how to use git

1. Before you start working on a task, pull the newest version of the code and create a new branch

```zsh
# Make sure you are on the main branch
git checkout main

git pull

# Create new branch
git checkout -b "my_new_task"
```

2. Whenever you finish any small piece of code, commit it. Try to be short but descriptive in the commit, but it is also fine, to do small intermediate commits with bad commit messages than not to commit at all.

```zsh
# If you want to commit all the file
git add .

# or if you want to just commit a specific file
git add /path/to/my/file_to_commit

# Add a commit message
git commit -m "This is my great commit message"

# Push your changes
git push
```

3. Once you are done, try to test and check the code once more to make sure it is nice and clean. Commit all your changes (see above) and push. Then navigate to Github and create a pull request. Tag at least one person as a reviewer.

4. Once the pull request is reviewed, it can be merged and the branch can be deleted. Also make sure you delete the branch on you computer (just to prevent mess).


```zsh
# Checkout to main branch
git checkout main

git pull

# Delete your branch
git branch -d "my_new_task"
```
