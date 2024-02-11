# Changes

## [2.1.0](https://github.com/prantlf/bump-version-action/compare/v2.0.1...v2.1.0) (2024-02-11)

### Features

* Add no-vlang, no-node and no-rust input parameters ([cd861a2](https://github.com/prantlf/bump-version-action/commit/cd861a2842a56e557d8b303a36443cc70d3c52ec))

## [2.0.1](https://github.com/prantlf/bump-version-action/compare/v2.0.0...v2.0.1) (2023-10-24)

### Bug Fixes

* Remove quotes from bump-files ([7ebaf8e](https://github.com/prantlf/bump-version-action/commit/7ebaf8e624cbcb86ff4351b976a3a473a663287e))

## [2.0.0](https://github.com/prantlf/bump-version-action/compare/v1.4.0...v2.0.0) (2023-10-24)

### Features

* Allow specifying extra files in which to bump the version number ([f76d27f](https://github.com/prantlf/bump-version-action/commit/f76d27f72b2d7acf9b6aad178aafe1755af411c3))

### Bug Fixes

* Detect the changed files using git ([bc21fc2](https://github.com/prantlf/bump-version-action/commit/bc21fc25abf989f8889add122cd7c567e0a8a361))

### BREAKING CHANGES

Instead of adding changelog and package descriptor to the changed files, git is used to detect the changed files. Although there probably are not other changed files in the local repo after running this action, there might be in some build configurations. In such case, this action should be run as the first one, to collect only changes made by the version number bumping.

## [1.4.0](https://github.com/prantlf/bump-version-action/compare/v1.3.2...v1.4.0) (2023-10-23)

### Features

* Implement dry-run ([b9c8d18](https://github.com/prantlf/bump-version-action/commit/b9c8d185ab06dccacace444005e086a4eb66b5c4))

## [1.3.2](https://github.com/prantlf/bump-version-action/compare/v1.3.1...v1.3.2) (2023-10-23)

### Bug Fixes

* Correct multivalue action parameters ([7c1d58a](https://github.com/prantlf/bump-version-action/commit/7c1d58af86694e898a0c7fb082a71935fa6ddd6c))

## [1.3.1](https://github.com/prantlf/bump-version-action/compare/v1.3.0...v1.3.1) (2023-10-23)

### Bug Fixes

* Log the executed command ([ab4a338](https://github.com/prantlf/bump-version-action/commit/ab4a338cdee4f4f6464d57297d10591c899bb719))

## [1.3.0](https://github.com/prantlf/bump-version-action/compare/v1.2.0...v1.3.0) (2023-10-23)

### Features

* Implement dry-run ([32ff0ee](https://github.com/prantlf/bump-version-action/commit/32ff0ee01050927017eb7ec2ff3a44dbd6a95ce1))

## [1.2.0](https://github.com/prantlf/bump-version-action/compare/v1.1.0...v1.2.0) (2023-10-23)

### Features

* Add input "enable" ([2dca931](https://github.com/prantlf/bump-version-action/commit/2dca93102c9668d0adad872b4fc1949bc964554d))

## [1.1.0](https://github.com/prantlf/bump-version-action/compare/v1.0.0...v1.1.0) (2023-10-23)

### Features

* Add output changed-files ([458297e](https://github.com/prantlf/bump-version-action/commit/458297e67ecdef6a5e8ac81892cf2920298b14b3))

## 1.0.0 (2023-10-22)

Testing commit
