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

- **Date (UTC):** 2026-10-23 02:38
- **Upstream:** [`02c9922`](https://github.com/meshcore-dev/MeshCore/commit/02c99229541fb5954d444a1a994b18f0f1747b8b) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261023)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261023)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261023)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-10-23 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261023) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261023) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261023) |
| 2026-10-22 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261022) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261022) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261022) |
| 2026-10-21 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261021) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20261021) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20261021) |
| 2026-10-20 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261020) | failed | failed |
| 2026-10-19 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261019) | failed | failed |
| 2026-10-18 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261018) | failed | failed |
| 2026-10-15 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20261015) | failed | failed |

<!-- END AUTO -->
