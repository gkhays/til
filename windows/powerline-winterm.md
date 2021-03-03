# Set up Powerline in Windows Terminal

Update settings.json for Microsoft Terminal with `Ctrl+,`.

```json
"list":
[
  {
    // Make changes here to the powershell.exe profile.
    "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
    "name": "Windows PowerShell",
    "commandline": "powershell.exe",
    "fontFace": "Cascadia Code PL",
    "hidden": false
  },
  {
    "guid": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
    "hidden": false,
    "name": "PowerShell",
    "source": "Windows.Terminal.PowershellCore",
    "fontFace": "Cascadia Code PL"
  }
]
```

## References

1. [Tutorial: Set up Powerline in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup)
1. [How to make a pretty prompt in Windows Terminal with Powerline, Nerd Fonts, Cascadia Code, WSL, and oh-my-posh](https://www.hanselman.com/blog/how-to-make-a-pretty-prompt-in-windows-terminal-with-powerline-nerd-fonts-cascadia-code-wsl-and-ohmyposh)
1. [Cascadia Code](https://docs.microsoft.com/en-us/windows/terminal/cascadia-code)
1. [Cascadia Code](https://github.com/microsoft/cascadia-code) (GitHub)
1. [MEGATHREAD: Breaking settings changes in version 0.11! #5458](https://github.com/microsoft/terminal/issues/5458)
