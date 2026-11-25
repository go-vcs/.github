# .github

Shared defaults for the **go-vcs** organisation.

`profile/README.md` is the organisation's public page.

`default.json` is the Renovate preset every repository here extends with
`{"extends": ["github>go-vcs/.github"]}`, and `config.js` is the runner that
applies it to this organisation only (`.github/workflows/renovate.yml`, which
needs a `RENOVATE_TOKEN` secret).

Minor and patch Go dependency updates merge themselves once the tests pass.
**The Go toolchain does not.** `go1.27.0` miscompiles on loong64
([golang/go#81000](https://github.com/golang/go/issues/81000)), and a
repository without a loong64 lane sees nothing wrong with the bump. A library
that breaks is one library; a toolchain that breaks is every architecture at
once.
