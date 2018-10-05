# PKGBUILDs for [Arch User Repository](https://aur.archlinux.org/)

Things I maintain, checked into git as subtrees for easier management or pull requests.

Powered by [aurpublish](https://www.archlinux.org/packages/community/any/aurpublish/) from [eli-schwartz](https://github.com/eli-schwartz)

## How it works

Commit PKGBUILDs in named subdirectories. Export them to the AUR with the `aurpublish` command, using the subtree push stratagem.
This preserves an independent history for third-party hosting, pull requests... ;)

## Commands

### `aurpublish setup`

Initialize a new repository with [githooks](#hooks).

### `aurpublish PACKAGE`

Push PACKAGE to the AUR. With "--speedup", merges the split history back in.

### `aurpublish -p PACKAGE`

Pull package from the AUR (if you adopted an existing package, or have a co-maintainer).

### `aurpublish log PACKAGE`

View the git log of a package subtree.

## Hooks

### pre-commit

Warn about whitespace errors, fail if checksums don't match, and auto-generate .SRCINFO for all changed PKGBUILDs.

### prepare-commit-msg

Prefill the commit message with a list of added/updated/deleted packages + versions (if any).

## License

[MIT](LICENSE)