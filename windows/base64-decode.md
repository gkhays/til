# Decode Base64 on the Command Line

```console
certutil -decode in.b64 out.txt
```

Alternatively, in PowerShell.

```pwsh
$MYTEXT = 'This is my secret text'
$ENCODED = [Convert]::ToBase64String([Text.Encoding]::Unicode.GetBytes($MYTEXT))
Write-Output $ENCODED
```

```
$file = "C:\input.txt"
$data = Get-Content $file
[System.Text.Encoding]::ASCII.GetString([System.Convert]::FromBase64String($data)) | Out-File -Encoding "ASCII" out.html
```

Related

```console
type out.txt | keybase pgp decrypt
```

## References

1. [Decoding base64 in batch](https://stackoverflow.com/a/16946681/6146580)
