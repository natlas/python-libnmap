# natlas-libnmap

## Code status

[![Release](https://img.shields.io/github/release/natlas/natlas-libnmap.svg)](https://github.com/natlas/natlas-libnmap/releases/latest)
![Last Commit](https://img.shields.io/github/last-commit/natlas/natlas-libnmap.svg)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/natlas-libnmap)](https://pypi.org/project/natlas-libnmap/0.7.1/)
![Code Size](https://img.shields.io/github/languages/code-size/natlas/natlas-libnmap.svg)
[![Contributors](https://img.shields.io/github/contributors/natlas/natlas-libnmap.svg)](https://github.com/natlas/natlas-libnmap/graphs/contributors)

[![Maintainability](https://api.codeclimate.com/v1/badges/660913964e02d6d90e1c/maintainability)](https://codeclimate.com/github/natlas/natlas-libnmap/maintainability)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/natlas/natlas-libnmap.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/natlas/natlas-libnmap/alerts/)

## Summary

This repo originated as a fork of [python-libnmap] after several months of unresponsiveness regarding fixing an XML parsing vulnerability. It has been simplified to focus purely on parsing nmap results and doing diffs on pairs of scans. The backend functionality has been removed, as has the nmap process management functionality. By removing this extraneous functionality, we can focus on making the parsing functionality the best at what it does without worrying about updating support for various backends.

## Use cases

libnmap is a python library enabling python developers to manipulate nmap data.

libnmap is what you were looking for if you need to implement the following:

* manipulate nmap scans results to do reporting
* compare and diff nmap scans to generate graphs
* batch process scan reports

The above uses cases will be easy to implement with the help of the libnmap modules.

## libnmap modules

The lib currently offers the following modules:

* **parse**: enables you to parse nmap XML reports from a file, a string,...
* **report**: enables you to manipulate a parsed scan result and de/serialize scan results in a json format
* **diff**: enables you to see what changed between two scans
* **common**: contains basic nmap objects like NmapHost and NmapService. It is to note that each object can be "diff()ed" with another similar object.

## Documentation

All the documentation is available on [read the docs]. This documentation contains small code samples that you directly reuse.

## Dependencies

libnmap dependencies are captured in [Pipfile](Pipfile).

## Python Support

The old version of libnmap supported many versions of python going back to 2.7. Since python 2.7 is no longer supported, this library will only support Python >= 3.6.

* Python 3.6
* Python 3.7
* Python 3.8

## Install

```bash
pipenv install natlas-libnmap
```

or via git:

```bash
git clone https://github.com/natlas/natlas-libnmap.git
cd natlas-libnmap
python setup.py install
```

## Examples

Some codes samples are available in the examples directory or in the [documentation].

## Contributors

Ronald "[savon-noir]" Bister for the original work on python-libnmap.

[savon-noir]: https://github.com/savon-noir
[python-libnmap]: https://github.com/savon-noir/python-libnmap
[read the docs]: https://libnmap.readthedocs.org
[documentation]: https://libnmap.readthedocs.org
