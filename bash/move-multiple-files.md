# Move Multiple Files

I accidently unzipped several files into the wrong directory. I started moving them one at a time but "laziness" quickly kicked in!

```bash
mv -t target file1 file2 file3
```

What does it say that I first `googled` instead of using the built-in help?

```bash
  -t, --target-directory=DIRECTORY  move all SOURCE arguments into DIRECTORY
```

### List Files

A follow-up problem is how to generate a list of all the files to move? I couldn't figure out how to pass multiple whitespace delimiters to `cut` so I preprocessed with `tr`.

```bash
unzip -l -qq pocorgtfo18.pdf | tr -s " " | cut -d " " -f5
```

Putting it all together.

```bash
mv -t pocorgtfo18 $(unzip -l -qq pocorgtfo18.pdf | tr -s " " | cut -d " " -f5 | xargs)
```

Had I been aware of `zipinfo` I could have reduced the number of steps.

```bash
zipinfo -1 pocorgtfo18.pdf
index.txt
manwholostthesea.txt
heijningen-thesis.pdf
automatedwhiteboxfuzzing.pdf
stp.pdf
...
```

Yes, I've made my `TIL` into somewhat of a polyglot by unzipping a [polyglot file](https://github.com/angea/pocorgtfo/blob/master/releases/pocorgtfo18.pdf)! 😭

### ChatGPT

But did you ask ChatGPT? Fine. Just to be thorough.

```console
zip_file="example.zip"; destination_directory="new_directory"; unzip -l "$zip_file" | awk '{print $4}' | xargs -I {} mv {} "$destination_directory"
```

## References

1. [How to move multiple files at once to a specific destination directory?](https://askubuntu.com/a/217067)
1. [How do I use cut to separate by multiple whitespace?](https://unix.stackexchange.com/a/340069)
1. [Extract list of file names in a zip archive when `unzip -l`](https://stackoverflow.com/a/13619930)
