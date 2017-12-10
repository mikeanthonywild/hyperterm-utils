## How to Contribute to Hyperterm

A good first step is to read the [contributing guide](https://github.com/mikeanthonywild/hyperterm-hardware/blob/master/CONTRIBUTING.md) on the main Hyperterm project. This details many general aspects to contributing to the Hyperterm project. The guidelines which follow are Python-specific.

### Writing and Running Tests

All PRs must pass the CI tests. You *should* run the test suite before submitting a PR. To do this simply run `tox`, which will build the package and install it into a virtualenv before running the test suite. It will also build the documentation.

### Dependency Pinning

To ensure reproducible builds, all dependencies should be pinned in the `requirements.txt` file. To aid in this, the `pip-compile` command can be used (part of `pip-tools`) to resolve the dependencies listed in `setup.py` and freeze them to pinned versions. The subsequent `requirements.txt` should be used by Tox during testing to ensure the results are reproducible.

### Release Process

As detailed in the general contributing guide (read this first if you haven't done so), the Hyperterm development process is done using the GitHub flow using forks and PRs into `master`. Once ready for a new release, a new commit should be made to `master` which bumps the version number (see [below](#versioning) for details on version numbers) and adds an entry to `CHANGELOG.md` (see http://keepachangelog.com).

* Releases are created using [GitHub Releases](https://help.github.com/articles/about-releases/).
* A release should contain a copy of the relevant change notes as well as a copy of the source (added automatically).
* No build products should be uploaded - this is handled by the CI platform and only uploaded to PyPI to prevent confusion.

### Versioning

The `hyperterm-utils` project uses [Semantic Versioning](https://semver.org) to encode information about API changes in the version string. The *API* is defined as that which is documented at https://mikeanthonywild.github.io/hyperterm-utils/.

