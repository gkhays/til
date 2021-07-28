# Alternative to Escape Key

I'm definitely a fan of modal operations in Vim but the Escape key is too far away to hit without taking my fingers off the home row.

I first got the idea of mapping `jj` to `<ESC>` from [ThePrimeagen](https://www.youtube.com/channel/UC8ENHE5xdFSwx71u3fDH5Xw). But followed up with some addtional articles; see below.

While in normal mode use `:inoremap jj <Esc>`. I added it to my `.vimrc`.

```vim
" Ctrl-[ is an alternative to <ESC>
inoremap jj <ESC>
```

## References

1. [Your first VimRC: How to setup your vim's vimrc](https://www.youtube.com/watch?v=n9k9scbTuvQ)
1. [VimRC 2021 (Jan): How to setup your Vim RC](https://www.youtube.com/watch?v=DogKdiRx7ls)
1. [Escape key alternatives in Vim](https://www.bautista.dev/escape-key-alternatives-in-vim/)
1. [Other ways to exit Insert mode besides Escape](https://vi.stackexchange.com/a/301)
1. [Avoid the escape key](https://vim.fandom.com/wiki/Avoid_the_escape_key)
1. [Alternative to the escape key in Vim](https://til.hashrocket.com/posts/dqeahsdoaf-alternative-to-the-escape-key-in-vim) <-- TIL! 😃
