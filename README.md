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

- **Date (UTC):** 2026-09-28 02:41
- **Upstream:** [`b9f519e`](https://github.com/meshcore-dev/MeshCore/commit/b9f519ef5a13da72d7efca1bfb2e16501541fe0a) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260928)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260928)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260928)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-09-28 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260928) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260928) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260928) |
| 2026-09-27 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260927) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260927) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260927) |
| 2026-09-26 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260926) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260926) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260926) |

<!-- END AUTO -->
