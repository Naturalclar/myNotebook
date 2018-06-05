# Git commands to reset changes

Ways to remove unwanted changes and revert to a clean state.

- `git checkout .` - removes unstaged tracked file.
- `git clean -f` - removes unstaged untracked file.
- `git reset --hard` - removes both staged and unstaged tracked file.
- `git stash -u` - removes all changes