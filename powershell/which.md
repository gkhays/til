# Equivalent of Which in PowerShell

In PowerShell, use `Get-Command` or set an alias.

```pwsh
New-Alias which get-command
```

Add to profile.

```pwsh
"`nNew-Alias which get-command" | add-content $profile
```

## References

1. [Equivalent of \*Nix 'which' command in PowerShell?](https://stackoverflow.com/a/65148/6146580)
1. [Windows: `Which` Equivalent – CMD & PowerShell](https://www.shellhacks.com/windows-which-equivalent-cmd-powershell/)

Related: [Windows: `Grep` Equivalent – CMD & PowerShell](https://www.shellhacks.com/windows-grep-equivalent-cmd-powershell/)
