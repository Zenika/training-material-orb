# Orb Project Template

[![CircleCI Build Status](https://circleci.com/gh/Zenika/training-material-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/Zenika/training-material-orb) [![CircleCI Orb Version](https://badges.circleci.com/orbs/zenika/training-material)](https://circleci.com/orbs/registry/orb/zenika/training-material) [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/Zenika/training-material-orb/master/LICENSE)

Build Zenika training materials with [sensei](https://github.com/Zenika/sensei) and publish them.

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/zenika/training-material) - The official registry page of this orb for all versions, executors, commands, and jobs described.

### How to Contribute

We welcome [issues](https://github.com/Zenika/training-material-orb/issues) to and [pull requests](https://github.com/Zenika/training-material-orb/pulls) against this repository!

### How to Publish

* Create and push a branch with your new features.
* When ready to publish a new production version, create a Pull Request from _feature branch_ to `master`.
* The title of the pull request must contain a special semver tag: `[semver:<segement>]` where `<segment>` is replaced by one of the following values.

| Increment | Description|
| ----------| -----------|
| major     | Issue a 1.0.0 incremented release|
| minor     | Issue a x.1.0 incremented release|
| patch     | Issue a x.x.1 incremented release|
| skip      | Do not issue a release|

Example: `[semver:major]`

* Squash and merge. Ensure the semver tag is preserved and entered as a part of the commit message.
* On merge, after manual approval, the orb will automatically be published to the Orb Registry.
