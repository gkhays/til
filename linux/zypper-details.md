# Get Version and Details of Package Using Zypper

My goal was to retrieve the version number of a recent `yq` package under SUSE. Short of installing it and observing the version, I wanted to see what is available. It turns out that `zypper` supports a search function, `zypper se` for short.

```console
# zypper se --match-exact --details yq
Loading repository data...
Reading installed packages...
S | Name | Type    | Version           | Arch   | Repository
--+------+---------+-------------------+--------+----------------
  | yq   | package | 4.18.1-bp154.1.17 | x86_64 | Main Repository
```

If you don't use the matching and details switches, you may get more than you bargained for! 😀

```console
# zypper se yq
Retrieving repository 'Update repository of openSUSE Backports' metadata .........................................[done]
Loading repository data...
Reading installed packages...
S | Name                                  | Summary                                                     | Type
--+---------------------------------------+-------------------------------------------------------------+-----------
  | python-pyqt-rpm-macros                | RPM macros for building PyQt packages                       | package
  | python3-AnyQt                         | PyQt4/PyQt5 compatibility layer                             | package
  | python3-PyQRCode                      | Python 3 module to generate QR Codes                        | package
  | python3-pyqt-builder                  | The PEP 517 compliant PyQt build system                     | package
  | python3-pyqt-builder                  | The PEP 517 compliant PyQt build system                     | srcpackage
  | python3-PyQt6                         | Python bindings for Qt 6                                    | package
  | python3-PyQt6-3D                      | Python bindings for the Qt 3D framework                     | package
  | python3-PyQt6-3D-devel                | Devel files for python3-PyQt6-3D                            | package
  | python3-PyQt6-Charts                  | Python bindings for the Qt Charts library                   | package
  | python3-PyQt6-Charts-devel            | Devel files for python3-PyQt6-Charts                        | package
  | python3-PyQt6-DataVisualization       | Python bindings for the Qt Data Visualization library       | package
  | python3-PyQt6-DataVisualization-devel | Devel files for python3-PyQt6-DataVisualization             | package
  | python3-PyQt6-devel                   | PyQt - devel part of python bindings for Qt 6               | package
  | python3-PyQt6-doc                     | Examples for python3-PyQt6                                  | package
  | python3-PyQt6-NetworkAuth             | Python bindings for the Qt Network Authorization library    | package
  | python3-PyQt6-NetworkAuth-devel       | Devel files for python3-PyQt6-NetworkAuth                   | package
  | python3-PyQt6-QScintilla              | Python bindings for QScintilla for PyQt6                    | package
  | python3-PyQt6-sip                     | The sip module support for PyQt6                            | package
  | python3-PyQt6-WebEngine               | Python bindings for the Qt WebEngine framework              | package
  | python3-PyQt6-WebEngine-devel         | Devel files for python3-PyQt6-WebEngine                     | package
  | python3-pyqtgraph                     | Scientific Graphics and GUI Library for Python              | package
  | python3-pyquery                       | A jQuery-like library for python                            | package
  | python3-yq                            | Command-line YAML processor - jq wrapper for YAML documents | package
  | texlive-yquant                        | Typesetting quantum circuits in a human-readable language   | package
  | texlive-yquant-doc                    | Documentation for texlive-yquant                            | package
  | yq                                    | A portable command-line YAML processor                      | package
  | yq-bash-completion                    | Bash Completion for yq                                      | package
  | yq-fish-completion                    | Fish Completion for yq                                      | package
  | yq-zsh-completion                     | Zsh Completion for yq                                       | package
```
