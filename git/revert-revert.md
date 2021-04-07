# Revert a Revert

I attempted a simple `git push` so did a `git pull` to catch up and ended up with an unexpected, much larger merge. I chose to revert in order to try again.

```bash
git log --oneline
git revert -m 1 [commit-hash]
```

That worked but then it turned out the merge was correct and so now I found myself wanting to undo or revert the revert!

```bash
git revert [commit-hash]
```

## References

1. [Git undo merge](https://www.datree.io/resources/git-undo-merge)
1. [Re-doing a reverted merge in Git](https://stackoverflow.com/a/1078209/6146580)
1. [Revert a Faulty Merge](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/howto/revert-a-faulty-merge.txt)
