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

- **Date (UTC):** 2026-08-15 00:41
- **Upstream:** [`d929643`](https://github.com/meshcore-dev/MeshCore/commit/d92964352441e53b93e8667b802e04f6e072b39e) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260815)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260815)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260815)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-08-15 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260815) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260815) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260815) |
| 2026-08-14 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260814) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260814) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260814) |
| 2026-08-13 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260813) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260813) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260813) |

<!-- END AUTO -->
