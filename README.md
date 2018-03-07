# hyperterm-utils [![Build Status](https://travis-ci.org/mikeanthonywild/hyperterm-utils.svg?branch=master)](https://travis-ci.org/mikeanthonywild/hyperterm-utils)

An open-source laptop with maintainability and sustainability in mind. This repo contains Python build tools and utilities for [Hyperterm](https://github.com/mikeanthonywild/hyperterm-hardware).

## Package Contents

* `eeschema` - Python API and CLI for Eeschema

## Quickstart

If you just want to use the tools provided by `hyperterm-utils`, simply run:

```
$ pip install --user hyperterm-utils
```

For development, you'll want to clone the `hyperterm-utils` repo and set up a development environment with [Pipenv](https://pipenv.org/):

```
$ git clone git@github.com:mikeanthonywild/hyperterm-utils.git
$ pip install --user pipenv
$ cd hyperterm-utils
$ pipenv install --dev
```

> If multiple versions of Python are installed, be sure to create a Python 3 development environment with `pipenv install --dev --three`.

## Resources

* [Main Hyperterm project](https://github.com/mikeanthonywild/hyperterm-hardware)
* [Contributing](CONTRIBUTING.md)
* [Documentation](https://mikeanthonywild.github.io/hyperterm-utils/)
