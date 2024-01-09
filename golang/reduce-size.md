# Reduce the Size of a Go Binary

Removing debug information from a Go binary can reduce its "footprint." This is accomplished by passing the `-s` amd `-w` `ldflags`. This can result in up to a 30% reduction in size.

```bash
go build -ldflags "-s -w" -o go-slim
```

To reduce the size even further requires compression. I use [upx](https://github.com/upx/upx), which is multi-platform and supports the Linux and Windows environments I frequently use. It yields an approximate 40% additonal reduction! The `upx` packer is also self-unpacking so no other dependencies are necessary.

```bash
$ ./contrib/upx go-slim
                       Ultimate Packer for eXecutables
                          Copyright (C) 1996 - 2024
UPX 4.2.2       Markus Oberhumer, Laszlo Molnar & John Reiser    Jan 3rd 2024

        File size         Ratio      Format      Name
   --------------------   ------   -----------   -----------
   7357440 ->   2682880   36.46%    win64/pe     go-slim

Packed 1 file.
```

## References

1. [Optimizing the size of the Go binary](https://prog.world/optimizing-the-size-of-the-go-binary/)
