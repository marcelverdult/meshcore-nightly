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

- **Date (UTC):** 2026-05-14 00:30
- **Upstream:** [`5557457`](https://github.com/meshcore-dev/MeshCore/commit/555745700e48e0bd0403ebe90ef847ed2bcaf427) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260514)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260514)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260514)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-05-14 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260514) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260514) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260514) |
| 2026-05-13 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260513) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260513) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260513) |
| 2026-05-12 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260512) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260512) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260512) |
| 2026-05-11 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260511) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260511) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260511) |
| 2026-05-10 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260510) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260510) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260510) |
| 2026-05-09 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260509) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260509) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260509) |

## Configured PRs

- [#1338](https://github.com/meshcore-dev/MeshCore/pull/1338) Limit flood advert packet forwarding — conflict
- [#1810](https://github.com/meshcore-dev/MeshCore/pull/1810) Allow direct message paths when denyf * is set — merged
- [#1727](https://github.com/meshcore-dev/MeshCore/pull/1727) Use hardware channel activity detection for checking interference — merged
- [#1954](https://github.com/meshcore-dev/MeshCore/pull/1954) Lora longer preamble — merged
- [#1687](https://github.com/meshcore-dev/MeshCore/pull/1687) Added PowerSaving for all ESP32-based repeaters — merged

<!-- END AUTO -->
