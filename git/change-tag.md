# Change Commit for Tag

```bash
git tag -d fix123                # delete the old local tag
git push github :fix123          # delete the old remote tag (use for each affected remote)
git tag fix123 790a621265        # create a new local tag
git push github fix123           # push new tag to remote    (use for each affected remote)
```

## References

1. [How can I move a tag on a git branch to a different commit?](https://stackoverflow.com/a/8044605/6146580)
1. [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
