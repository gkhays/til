# Generate a GUID

```ps1
❯ [guid]::NewGuid()

Guid
----
bc4f4084-dc69-4aa4-bab5-7d2bd07578a0
```

Alternatively, to use the Windows Registry format:

```ps1
'{'+[guid]::NewGuid().ToString()+'}'
```

## References

1. [To Generate a GUID in Windows 10 with PowerShell](https://winaero.com/generate-new-guid-in-windows-10/)
