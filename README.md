# TIL

> Today I Learned

My "Today I Learned" (TIL) snippets, inspired by [jbranchaud/til](https://github.com/jbranchaud/til). I'd also like to point out [simonw/til](https://github.com/simonw/til).

---

### Categories

-   [Ansible](#ansible)
-   [Authentication](#authentication)
-   [AWS](#aws)
-   [Bash](#bash)
-   [Chrome](#chrome)
-   [Docker](#docker)
-   [Dropwizard](#dropwizard)
-   [Electron](#electron)
-   [Git](#git)
-   [GitHub](#github)
-   [H2](#h2)
-   [HTML](#html)
-   [HTTP](#http)
-   [Java](#java)
-   [JavaScript](#javascript)
-   [Kubernetes](#k8s)
-   [Linux](#linux)
-   [Markdown](#markdown)
-   [Maven](#maven)
-   [Microsoft Teams](#microsoft-teams)
-   [Obsidian](#obsidian)
-   [PostgreSQL](#postgresql)
-   [Postman](#postman)
-   [PowerShell](#powershell)
-   [Raspberry Pi](#raspberry-pi)
-   [RDP](#rdp)
-   [React](#react)
-   [Rust](#rust)
-   [SSH](#ssh)
-   [Terraform](#terraform)
-   [Terragrunt](#terragrunt)
-   [Ubuntu](#ubuntu)
-   [VIM](#vim)
-   [VMware](#vmware)
-   [VSCode](#vscode)
-   [Wget](#wget)
-   [Windows](#windows)
-   [WSL](#wsl)

---

### Ansible

-   [Ansible configuration directory should not be world writable](ansible/ansible-cfg.md)

### Authentication

-   [JSON Web Token (JWT) debugger](authentication/jwt-io.md)

### AWS

-   [List MFA Devices](aws/list-mfa.md)
-   [List CIDR Blocks in Use](aws/list-cidr.md)
-   [List EC2 Instances Filtered by AMI](aws/ec2-by-ami.md)
-   [List RDS Cluster Snapshots](aws/list-snapshots.md)
-   [Exit Assumed IAM Role](aws/exit-assumed.md)

### Bash

-   [Get Multiple Values from a Bash Function](bash/multiple-return-values.md)
-   [Move Multiple Files](bash/move-multiple-files.md)
-   [Expand Parameters](bash/expand-variables.md)

### Chrome

-   [Chrome Proxy](chrome/proxy.md)
-   [How to Obtain a HAR Capture](chrome/har-capture.md)

### Docker

-   [Compose, Build, and Tag](docker/compose-build.md)
-   [Docker container statistics](docker/stats.md)
-   [The difference between CMD and ENTRYPOINT](docker/cmd-entrypoint.md)
-   [Docker Compose Restart Policy](docker/docker-compose-restart.md)
-   [Docker Health Check](docker/health-check.md)
-   [Format Docker Inspect with jq](docker/format-jq.md)
-   [Override the Entry Point](docker/entrypoint.md)
-   [Volume Mounts on Windows](docker/windows-volume.md)
-   [Docker Import](docker/import.md)
-   [Extract File from Docker Image](docker/extract-file.md)

### Dropwizard

-   [Set the root path](dropwizard/root-path.md)
-   [Shutdown options for Dropwizard](dropwizard/shutdown.md)
-   [Database transactions in non-Jersey resources](dropwizard/unitofwork-proxy.md)
-   [Environment variables](dropwizard/env-var.md)
-   [Add Swagger Documentation to Dropwizard](dropwizard/swagger.md)
-   [Change Log Level Using Admin Task](dropwizard/log-level.md)
-   [Run a Background Process in Dropwizard](dropwizard/background-process.md)
-   [Update Deprecated API Reference](dropwizard/deprecated-hibernate.md)

### Electron

-   [Exclude Files from an Electron Project](electron/exclude-files.md)

### Git

-   [Recover Deleted Branch](git/recover-deleted.md)
-   [Bypass Git Hooks](git/skip-hooks.md)
-   [Use Credential Manager Under WSL](git/cred-wsl.md)
-   [Merge Individual Files](git/merge-single-file.md)
-   [Checkout a Tag](git/checkout-tag.md)
-   [Remove a Tag](git/remove-tag.md)
-   [Modify Commit Message](git/modify-msg.md)
-   [Rename a Tag](git/rename-tag.md)
-   [Change Commit for Tag](git/change-tag.md)
-   [Revert a Revert](git/revert-revert.md)
-   [Find Commit by Git Hash](git/commit-hays.md)
-   [Get the Commit Hash](git/retrieve-hash.md)
-   [Locate Branches the Commit is On](git/commit-branch.md)
-   [Signing Commits](git/commit-sig.md)
-   [Remove Unused Branches](git/remove-unused-branches.md)
-   [Remove from Git but Keep Local File](git/local-not-git.md)

### GitHub

-   [Create Empty Folder with Online Editor](github/empty-dir.md)
-   [GitHub CLI](github/gh-cli.md)
-   [Add an Image to a Wiki](github/wiki-img.md)
-   [Filter API Results with JQ](github/api-jq.md)
-   [GitHub Statistics in Your README](github-stats.md)

### Golang

-   [Repeat a String in Go](golang/repeat-string.md)
-   [Reduce the Size of a Go Binary](golang/reduce-size.md)

### H2

-   [Import Data to H2 From PostgreSQL](h2/import-postgres.md)

### HTML

-   [Open a New Tab or Window from Form](new-tab.md)
-   [Disable Autocomplete](disable-autocomplete.md)
-   [Remove Indent from Lists](remove-indent.md)
-   [HTML 5 Details Tag](html/html5-details.md)

### HTTP

-   [A simple HTTP Request & Response Service](http/httpbin.md)

### Java

-   [Execute a Java Class with JShell](java/jshell-run-class.md)
-   [Use Jackson to deserialize an array of objects](java/jackson-deserialize-array.md)
-   [Ignore null values with Jackson](java/jackson-ignore-null.md)
-   [Add Classpath to Shaded JAR](java/shaded-classpath.md)
-   [Import External Library in JShell](java/jshell-import-jar.md)
-   [Hide Password in Command Line Argument using Argparse4j](java/noshow-pass.md)
-   [Convert Hex to Base64](java/hex-to-base64.md)
-   [Get URI information](java/uri-info.md)
-   [Shebang! Run Single File Java as Script](java/java-shebang.md)
-   [Display Contents of JAR Manifest](java/jar-manifest.md)
-   [Check Certificates in a Keystore](java/keystore-certs.md)
-   [Update Manifest inside JAR](java/update-manifest.md)
-   [Java Console Application Spinner](java/console-spinner.md)
-   [Java Simple Web Server](java/java-simple-webserver.md)

### JavaScript

-   [Reload a Page](javascript/reload-page.md)
-   [Set JavaScript Console Log Level](javascript/console-log-level.md)

### Kubernetes

-   [Switch Context](k8s/context.md)
-   [Copy Files from a Pod](k8s/kubectl-cp.md)
-   [Obtain Previous Container's Crash Log](k8s/crash-log.md)
-   [List Recently Deleted Pods](k8s/deleted-pods.md)

### Linux

-   [Type List Backwards](linux/list-backwards.md)
-   [Get Version and Details of Package Using Zypper](linux/zypper-details.md)
-   [TCP Command-Line Tool](linux/tcpserver.md)

### Markdown

-   [List in Markdown Table Cell](markdown/list-in-table.md)
-   [Internal, Relative Links](markdown/internal-links.md)
-   [Note and Warning Emphasis](markdown/note-warning.md)

### Maven

-   [Maven Parallel Build](maven/parallel-build.md)
-   [Special Characters in Maven Settings](maven/settings-special-char.md)
-   [Set Execute Permission in Maven](maven/set-execute-permission.md)

### Microsoft Teams

-   [Navigate from the keyboard](msteams/navigate.md)
-   [Export Wiki as PDF Document](msteams/export-wiki.md)

### Obsidian

-  [Callouts](obsidian/callouts.md)
-  [Change Location of Images](obsidian/image-location.md)
-  [How to Embed YouTube Videos](obsidian/youtube-videos.md)

### PostgreSQL

-   [Export tables to CSV](postgres/export-csv.md)
-   [Change password](postgres/change-password.md)
-   [Dump a Database from a Docker Container](postgres/dump-container.md)
-   [PostgreSQL Is Ready Utility](postgres/pg-isready.md)
-   [Analyze a PostgreSQL Database from the Command Line](postgres/analyze-db.md)

### Postman

-   [Load payload from file](postman/file-payload.md)
-   [Show Request Headers](postman/request-headers.md)

### PowerShell

-   [Get Windows Capability](powershell/get-capability.md)
-   [Scoop](powershell/scoop.md)
-   [Equivalent of Which in PowerShell](powershell/which.md)
-   [How to Dot Source in PowerShell](powershell/source.md)
-   [Generate a GUID](powershell/guid.md)

### Python

-   [UV Python Package and Project Manager](python/uv.md)

### Raspberry Pi

-   [Play Sound from Unattended Session](pi/headless-sound.md)

### RDP

-   [Multiple Monitors with Remote Desktop Session](rdp/multi-monitor.md)

### React

-   [How to Use Comments in React](react/comments.md)

### Rust

-   [Isolating a Rust Application in a Docker Container](rust/rust-in-docker.md)

### SSH

-   [sshpass](ssh/sshpass.md)
-   [ssh-copy-id](ssh/ssh-copy-id)
-   [Show SSH Key Hashes](ssh/ssh-hash.md)
-   [Remove Passphrase from SSH Key](ssh/remove-passphrase.md)

### Terraform

-   [Create a graph of Terraform resources](terraform/tform-graph.md)

### Terragrunt

-   [Fix empty tuple error](terragrunt/fix-empty-tuple.md)

### Ubuntu

-   [Recover root password on Ubuntu 18.04](ubuntu/recover-passwd.md)
-   [Disable ipv6 in Ubuntu](ubuntu/disable-ipv6.md)
-   [Troubleshoot reverse lookups on Ubuntu 18.04](ubuntu/dhcp-reverse.md)
-   [Set Default Java Version](ubuntu/default-java.md)

### Vim

-   [Alternative to Escape Key](vim/esc-alt.md)

### VMware

-   [Force BIOS Setup](vmware/force-bios.md)

## VSCode

-   [Change VSCode Terminal Font](vscode/terminal-font.md)
-   [Attach a Source JAR](vscode/source-jar.md)
-   [Search and Replace Tabs in VSCode](vscode/replace-tabs.md)

### Wget

-   [Output JSON Response to Stdout](wget/get-stdout.md)

### Windows

-   [Retrieve Windows product key](windows/productkey.md)
-   [Look up RGB codes with Microsoft Paint](windows/paint-dropper-tool.md)
-   [Command Line Interface to Windows Credential Manager](windows/cred-cli.md)
-   [Decode Base64 on the Command Line](windows/base64-decode.md)
-   [Set up Powerline in Windows Terminal](windows/powerline-winterm.md)
-   [Add Cmder to Windows Terminal](windows/cmder-winterm.md)
-   [Applications Virtual Folder Shortcut](windows/apps-shortcut.md)
-   [Using Windows 10 Snip & Sketch](windows/snip-sketch.md)
-   [Add Git Bash to Windows Terminal](windows/gitbash-winterm.md)

### WSL

-   [Map WSL Disk as Network Drive](wsl/map-wsl-disk.md)
-   [Browse WSL Files from Windows Explorer](wsl/browse-explorer.md)
-   [Set Terminal Starting Directory to WSL Home](wsl/wsl-starting-dir.md)
-   [Limit WSL 2 Memory](wsl/limit-memory.md)

## Acknowledgements

I "borrowed" this idea from [jbranchaud/til](https://github.com/jbranchaud/til).

## License

&copy; 2020 Garve Hays

This repository is licensed under the MIT license. See `LICENSE` for details.
