repos
=====

Small script to perform some Git commands to multiple repositories in a single directory

Usage:

1. Put "repos" into ~/bin
2. Create symlinks
```
ln -s repos status
ln -s repos fetch
ln -s repos pull
ln -s repos checkout
```

3. Go to a directory with mani Git repositories, and say ```status``` to get ```git status``` listing from all of the repos
4. If you don't want some repositories to appear in the listing, filter them out by adding ```~/.repos/config``` file:
```
[main]
hidden=directory,names,separated,by,commas
```