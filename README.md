repos
=====

Small script to perform some Git commands to multiple repositories in a single directory

Usage (symlink style):

1. Put "repos" into ~/bin
2. Create symlinks

        ln -s repos status
        ln -s repos fetch
        ln -s repos pull
        ln -s repos checkout
        ln -s repos branch

        # "branch" lists out branches in all repos,
        # Given a branch name as an argument, shows repos that have that branch

3. Go to a directory with many Git repositories, and say ```status``` to get ```git status``` listing from all of the repositories

```repos``` accepts parameters too, if you don't want to use symlink style (like on Windows).

    -s -> git status
    -f -> git fetch
    -p -> git pull
    -c <branch> -> git checkout <branch>
    -b [branch name]

If you don't want some repositories to appear in the listing, filter them out by adding ```~/.repos/config``` file:

        [main]
        hidden=directory,names,separated,by,commas
