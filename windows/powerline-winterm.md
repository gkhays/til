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

## WSL

```bash
wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
chmod +x /usr/local/bin/oh-my-posh
```

```bash
mkdir ~/.poshthemes
wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
chmod u+rw ~/.poshthemes/*.json
rm ~/.poshthemes/themes.zip
```

## Troublehooting

> JanDeDobbeleer commented 10 days ago
> Set-Theme is a V2 cmdlet. This got renamed to Set-PoshPrompt for V3. See here for more info.

## References

1. [Tutorial: Set up Powerline in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup)
1. [How to make a pretty prompt in Windows Terminal with Powerline, Nerd Fonts, Cascadia Code, WSL, and oh-my-posh](https://www.hanselman.com/blog/how-to-make-a-pretty-prompt-in-windows-terminal-with-powerline-nerd-fonts-cascadia-code-wsl-and-ohmyposh)
1. [Setting Up Powerline Shell on Windows Subsystem for Linux](http://iamnotmyself.com/2017/04/15/setting-up-powerline-shell-on-windows-subsystem-for-linux/)
1. [Cascadia Code](https://docs.microsoft.com/en-us/windows/terminal/cascadia-code)
1. [Cascadia Code](https://github.com/microsoft/cascadia-code) (GitHub)
1. [MEGATHREAD: Breaking settings changes in version 0.11! #5458](https://github.com/microsoft/terminal/issues/5458)
1. [Oh my Posh](https://ohmyposh.dev/)
1. [Windows Terminal - PowerShell customization via oh-my-posh/posh-git Set-Theme error? #441](https://github.com/JanDeDobbeleer/oh-my-posh/issues/441)
1. [How to Make Windows Terminal Transparent](https://allthings.how/how-to-make-windows-terminal-transparent/)
