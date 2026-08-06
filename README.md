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

- **Date (UTC):** 2026-08-06 01:45
- **Upstream:** [`84e3a67`](https://github.com/meshcore-dev/MeshCore/commit/84e3a67bd7595ba7b37d69c09be8a42d94d1ee6d) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260806)
- **Repeater:** failed
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260806)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-08-06 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260806) | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260806) |
| 2026-08-05 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260805) | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260805) |
| 2026-08-04 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260804) | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260804) |
| 2026-07-20 | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260720) | failed |
| 2026-07-19 | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260719) | failed |
| 2026-07-18 | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260718) | failed |

<!-- END AUTO -->
