# meshcore-nightly

Unofficial nightly firmware builds of [MeshCore](https://github.com/meshcore-dev/MeshCore) `dev` branch.

A scheduled GitHub Actions workflow runs every night at 00:00 UTC. It checks out upstream `dev`, optionally merges a list of upstream pull requests configured in [`nightly.yml`](nightly.yml), and publishes firmware releases for the three MeshCore roles: companion, repeater, room-server.

## Downloads

Pick the role you need from the [Releases](../../releases) page. Tags follow the pattern `nightly-<role>-YYYYMMDD`. The newest 10 nightlies per role are kept; older releases are pruned automatically.

## Configuration

Edit [`nightly.yml`](nightly.yml) on `main`:

- `extra_prs`: list of upstream PR numbers to merge on top of `dev` before each build. PRs that fail to merge cleanly are skipped and recorded under "Configured PRs" below.
- `retention`: number of nightly releases to retain per role.

## Suggesting upstream PRs

Want to see a specific upstream PR rolled into the next nightly? Open a PR against this repo that adds (or removes) a number in the `extra_prs` list of [`nightly.yml`](nightly.yml). A check workflow blocks PRs that touch any other file or any other config key, so PR review is mechanical: either the change is just a number in the PR list, or it isn't.

## Disclaimer

These builds track an active development branch. They may be unstable or fail to flash. The official releases live at [meshcore-dev/MeshCore](https://github.com/meshcore-dev/MeshCore/releases).

<!-- BEGIN AUTO -->

## Latest build

- **Date (UTC):** 2026-11-23 04:51
- **Upstream:** [`ae28381`](https://github.com/meshcore-dev/MeshCore/commit/ae283810e16b0231964c494aa954fb22ce75639e) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261123)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261123)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261123)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-11-23 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261123) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261123) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261123) |
| 2026-11-22 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261122) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261122) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261122) |
| 2026-11-21 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261121) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261121) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261121) |
| 2026-11-20 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261120) | failed | failed |
| 2026-11-19 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261119) | failed | failed |
| 2026-11-18 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261118) | failed | failed |
| 2026-11-17 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261117) | failed | failed |

<!-- END AUTO -->
