# Remove a Tag

## Local

```bash
git tag --delete tagname
```

## Remote

```bash
git push origin :tagname
```

Or

```bash
git push --delete origin tagname
```

Remove a tag but not a branch with the same name.

```bash
git push origin :refs/tags/tagname
```

## References

1. [How to delete a remote tag?](https://stackoverflow.com/a/5480292/6146580)
