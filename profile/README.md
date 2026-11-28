<p align="center"><img src="https://raw.githubusercontent.com/go-vcs/brand/main/social/go-vcs.png" alt="go-vcs" width="640"></p>

<h1 align="center">go-vcs</h1>
<p align="center">Light, secure Git forge for people and agents, written in Go.</p>
<p align="center">
  <img src="https://img.shields.io/badge/Go-1.27-00ADD8?style=flat-square&logo=go&logoColor=white">
  <img src="https://img.shields.io/badge/license-BSD--3--Clause-0A6E96?style=flat-square">
  <img src="https://img.shields.io/badge/stage-early-0079A8?style=flat-square">
</p>

---

## What this is

A Git forge small enough to read and strict enough to trust: repository
hosting, a web UI, an administration API over gRPC with FIDO2 on the
privileged operations, and Actions runners scheduled through GARM.

**It is early.** The admin gRPC API and its CLI, read-only clone and fetch over
SSH and smart HTTP, OIDC sign-in and a read-only web UI are implemented; push is
still design only. The design is written down in
[`forge/docs/design.md`](https://github.com/go-vcs/forge/blob/main/docs/design.md);
what is not built yet is not described here as if it were.

## Repos

| | Repo | |
|---|---|---|
| <img src="https://raw.githubusercontent.com/go-vcs/brand/main/avatar/go-vcs-forge.png" width="36"> | [`forge`](https://github.com/go-vcs/forge) | Light, secure Git forge: hosting, web UI, admin gRPC, Actions runners via GARM. |
| <img src="https://raw.githubusercontent.com/go-vcs/brand/main/avatar/go-vcs-gitproto.png" width="36"> | [`gitproto`](https://github.com/go-vcs/gitproto) | Git wire protocol v2 (fetch side), v0.1.0: fuzzed, and 0.93 to 0.96 of the time of `git upload-pack` on a full clone. |
| <img src="https://raw.githubusercontent.com/go-vcs/brand/main/avatar/go-vcs-actions.png" width="36"> | [`actions`](https://github.com/go-vcs/actions) | GitHub Actions workflow engine and gitea-runner protocol server. |
| <img src="https://raw.githubusercontent.com/go-vcs/brand/main/avatar/go-vcs-agentd.png" width="36"> | [`agentd`](https://github.com/go-vcs/agentd) | Local daemon between many agent sessions and GitHub, v0.4.1: one poller per commit, no token in an agent, an object cache, `Materialize` and an event stream. |

## Links

- Landing page: <https://go-vcs.github.io>
- Documentation: <https://go-vcs.github.io/docs/>
- Brand assets: <https://github.com/go-vcs/brand>
