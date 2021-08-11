# Remove Unused Branches

First locate branches that have already been merged.

```bash
git branch --merged
```

Then remove them.

```bash
git branch --merged | grep fix | xargs git branch -d
```

## References

1. [Clean up unused git branches](https://ardalis.com/clean-up-unused-git-branches/)
1. [Delete unused local branches](https://gist.github.com/leodutra/9e7bb9f9a27201db47f9ed0786b5e38b)
1. [Delete all local git branches](https://stackoverflow.com/a/10610669/6146580)
