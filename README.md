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

- **Date (UTC):** 2026-11-05 04:21
- **Upstream:** [`77e27e5`](https://github.com/meshcore-dev/MeshCore/commit/77e27e5634861cc80d91b69d754d40d548a6684d) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261105)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261105)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261105)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-11-05 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261105) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261105) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261105) |
| 2026-11-04 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261104) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261104) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261104) |
| 2026-11-03 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261103) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261103) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261103) |
| 2026-11-02 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261102) | failed | failed |
| 2026-11-01 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261101) | failed | failed |
| 2026-10-31 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261031) | failed | failed |
| 2026-10-30 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261030) | failed | failed |

<!-- END AUTO -->
