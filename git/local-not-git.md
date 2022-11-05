# Remove from Git but Keep Local File

This tip was in my [Git Cheat Sheet](https://github.com/gkhays/cheatsheets/blob/master/Git-CheatSheet.md#remove-a-file-from-a-git-repository-without-deleting-it-from-the-local) but since I used it recently, I decided it should be a `TIL` as well.

```
git rm --cached mylogfile.log
```

For a directory.

```
git rm --cached -r mydirectory
```

## References

1. [Remove a file from a Git repository without deleting it from the local filesystem](https://stackoverflow.com/a/1143800/6146580)
1. [git-rm - Remove files from the working tree and from the index](https://git-scm.com/docs/git-rm)
