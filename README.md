# Overview
We have some simple directory structure with binaries (bin) and sources with subdirectories (src). 
We have three commits with one source file changed. The commits are marked with tags v1.0 and v1.1.
We want the only changed file checked out with all the subfolders recursively created.

## Directories
bin - dummy binary files
src - dummy source files (tree)

## Tags
v1.0 (bound to revision 31842e8bf79a3688807ebc3ace3438ef6240c5ff)
v1.1 (bound to revision f2236ce8e9feb0f09d0b8127ed2df68edea70c95)

## Files changed between v1.0 and v1.1
src/a/source_001.txt

# How to checkout only changed files
```
# inits git repo
git init .

# binds remote repository
git remote add origin https://github.com/ki11roy/overrides.git

# fetching whole repo here into .git folder... ;(
git fetch

# checking out only needed files
git checkout origin/master -- `git diff --name-only v1.0 v1.1`
```
