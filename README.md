Useful R development practices and workflows
================
Philipp Baumann
11/8/2019

# Syncing a github fork repository with upstream version

This is a short version derived from the official github help package
[here](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork)
and
[here](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork).

Create a fork of an upstream repository on github.com, clone the fork
with git, and then specify the upstream repository from which you forked
on the local git
with

``` bash
git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
# Check if it upstream fetch and push URLs have been added
git remote -v
```

To feed the newest commits from the upstream repository into the local
branch `upstream/master`:

``` bash
git fetch upstream
```

To merge the changes from the `upstream/master` branch into the local
`master` branch, execute

``` bash
# Switch to master branch
git checkout master
git merge upstream/master
```
