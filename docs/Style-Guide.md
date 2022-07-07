# Style Guide

## Linters

### General

[Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### Markdown

[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

## Commit Messages

### [NIST Commit Styleguide](https://pages.nist.gov/dioptra/dev-guide/contributing-commit-styleguide.html)

#### Commit Message Format

```shell
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The header is mandatory and the scope of the header is optional. Both are written in camelCase.

#### Type

- **build**: Changes that affect the build system or external dependencies
- **ci**: Changes to our CI configuration files and scripts
- **chore**: Miscellaneous changes that do not fall under any of the other types, such as changes to meta information in the repo (owner files, editor config, etc) or licensing
- **docs**: Documentation only changes
- **examples**: Additions or changes to the examples provided in the project’s `examples/` folder
- **feat**: A new feature
- **fix**: A bug fix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **revert**: A change that reverses the change in earlier commit
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- **test**: Adding missing tests or correcting existing tests

#### Scope

Note that not all commits should have a scope. Cases where a commit should not specify a scope typically fall into one of two categories:

1. Changes impacting more than one scope: This is common with the examples, style, test, and refactor change types. Examples include restructuring the project layout or running a code beautifier across the entire codebase.
2. chore and build changes: There is a broad range of tools and libraries out there related to changes in the project’s configuration files and the build system (examples: conda, flake8, makefile, mypy, pre-commit, etc). The use of scopes for these kinds of changes is optional and it is generally recommended that you omit them in the interest of keeping the list of scopes simple.

#### Subject

The subject contains a succinct description of the change:

- Use the imperative, present tense: “change” not “changed” nor “changes”
- Don’t capitalize the first letter
- No dot (.) at the end
