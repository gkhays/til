# Get the Commit Hash

Git log is your friend.

```bash
git log -1 --format=format:"%H"
```

Use `git-rev-parse` and retrieve the hash from the latest commit.

```bash
git rev-parse HEAD
```

## References

1. [How to Retrieve Hash for Commits in Git](https://www.w3docs.com/snippets/git/how-to-retrieve-hash-for-commits-in-git.html)
