# Update Changelog and Bump Version

GitHub action for updating changelog and bumping the project version using git commit messages formatted according to [Conventional Commits] and [Semantic Versioning].

Uses tools [newchanges] and [vp]. Uses git to detect changed files. Only platforms Linux, macOS, Windows on the architecture X64 are supported.

## Usage

Update the change log and write the new version ot the project source files:

```yml
- uses: prantlf/bump-version-action@v1
```

Work only in specific release branches:

```yml
jobs:
  build:
    steps:
    - uses: actions/checkout@v4
    - uses: prantlf/setup-v-action@v2
    - run: ...
    - uses prantlf/bump-version-action@v1
      with:
        branches: master v1.x
```

**Attantion**: This action can be used only to update an already published project. The first publishing has to happen manually:

1. Changelog with the first version has to be added, for example, a file `CHANGELOG.md`:

```
# Changes

# 1.0.0 (2023-10-22)

Initial release
```

2. Commit releasing the first version has to be correspondingly tagged, for example with `v1.0.0`.

Then this action can be added to a GitHub workflow.

## Inputs

The following parameters can be specified using the `with` object:

### branches

Type: `String`<br>
Default: `'main master'`

Branches which this action should run for, which are used to publishing releases. Use whitespace for separating the branch names. If you want to use multiple lines in YAML, introduce them with ">-". If you want to allow all branches, set the value to "*".

### enable

Type: `Boolean`<br>
Default: `true`

Can be set to `false` to prevent this action from running. It's helpful in the pipeline, which will not continue releasing, but only building and testing, and that will be decided in the middle of a job execution.

### dry-run

Type: `Boolean`<br>
Default: `false`

Can be set to `true` to only print what would be done without actually doing it.

### debug

Type: `Boolean`<br>
Default: `false`

Can be set to `true` to enable debug logging of the supporting tools. Debug logging will be enabled also if it's enabled on the runner.

## Outputs

The following parameters can be accessed by the `github` context:

### bumped

Type: `String`<br>

Set to `true` if the changelog was updated and the new version set.

### new-version

Type: `String`<br>

The new version written to the changelog and to the project source files.

### changed-files

Type: `String`<br>

Files modified by this action, separated by spaces.

## License

Copyright (C) 2023 Ferdinand Prantl

Licensed under the [MIT License].

[MIT License]: http://en.wikipedia.org/wiki/MIT_License
[Conventional Commits]: https://www.conventionalcommits.org/
[Semantic Versioning]: https://semver.org/
[newchanges]: https://github.com/prantlf/v-newchanges
[vp]: https://github.com/prantlf/vp
