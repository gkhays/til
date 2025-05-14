# UV Python Package and Project Manager

`uv` is a responsive package and project manager for Python. It incorporates the features of the following tools:

- `pip`
- `pip-tools`
- `virtualenv`
- `pipenv`

### Key Features

It is very fast. Combining multiple tool functionality into a single CLI. With package management, environment management, and dependency resolution.

Support for [PEP 582](https://peps.python.org/pep-0582/).

Supports common formats with `pyproject.toml`.

## Installation

#### asdf
```bash
asdf plugin add uv
```

#### Homebrew
```bash
brew install uv
```

#### Scoop
```console
scoop install main/uv
```

#### WinGet
```console
winget install --id=astral-sh.uv -e
```

## Getting Started

```bash
uv python install
uv python list
```

```bash
uv init uv-demo
uv add requests
```

```bash
uv  sync
```

## References
- [uv: the unified packaging release](https://www.youtube.com/live/oj8yk0Y-Ky0?si=iPKMw_abYns0fAGv)
- [Unified Python packaging with uv](https://talkpython.fm/episodes/show/476/unified-python-packaging-with-uv)
- [uv | Introduction](https://docs.astral.sh/uv/)
- [uv: Unified Python packaging](https://astral.sh/blog/uv-unified-python-packaging)