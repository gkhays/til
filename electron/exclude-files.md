# Exclude Files from an Electron Project

In `electron-builder.json`.

```js
{
  "files": [
    "**/*",
    "!.vscode/",
    "!README.md"
  ]
}
```

In the build section of `package.json`.

```js
{
    "name": "myApp",
    "version": "1.0.0",
    "description": "",

    "build": {
        "files": "!foo.json"
    }

}
```

A more elaborate build section (in `package.json`).

```js
"build": {
    "appId": "com.gettrici",
    "productName": "Trici",
    "mac": {
      "category": "public.app-category.developer-tools",
      "icon": "resources/images/trici_icon.icns",
      "target": "zip",
      "asar": false,
      "compression": "store",
      "files":["!builds/*","!patches/*","!packages/*"]
    }
  },
```

## References

1. [How to exclude file when build electron with electron-builder?](https://stackoverflow.com/a/59971102/6146580)
1. [Electron Builder Application Contents](https://www.electron.build/configuration/contents#files)
1. [How to use ignore files when packaging #383](https://github.com/electron-userland/electron-builder/issues/383)
1. [Unable to exclude files from app.asar #3446](https://github.com/electron-userland/electron-builder/issues/3446)
1. [electron-packager API - ignore](https://github.com/electron/electron-packager/blob/v13.0.1/docs/api.md#ignore)
1. [Allow excluding ignoring files/folders #673](https://github.com/electron-userland/electron-forge/issues/673)
1. [Exclude a directory while packaging #927](https://github.com/electron-userland/electron-builder/issues/927)
1. [Electron Packager](https://github.com/electron/electron-packager) (GitHub)
1. [Electron Packager](https://electron.github.io/electron-packager/master/)
