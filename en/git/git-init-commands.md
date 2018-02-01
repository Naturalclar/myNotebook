# Git init

`git init` creates an empty Git repository or reinitialize an existing repository, so that it can keep track of modifications made in the repository.

## Commands

`-q --quiet` - Only prints error and warning messages upon initialization.

`--bare` - creates a bare repository. Bare repository is a repository where it is intended to be like a server where it can be shared with others (like github). A bare repository will not have a working tree as it is not intended to be edited in that folder directly.

`--template=<template_directory>` - speficy directory from which templates will be used.

`--separate-git-dir=<git dir>` - creates the `.git` file in the directory you speficy instead of the current directory.


## Reference: 

[git documentation](https://git-scm.com/docs/git-init)