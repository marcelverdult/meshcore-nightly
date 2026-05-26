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

- **Date (UTC):** 2026-05-26 00:29
- **Upstream:** [`d2c2a6e`](https://github.com/meshcore-dev/MeshCore/commit/d2c2a6ef0b6b6e7323867c45cecbdae66179759a) on [`dev`](https://github.com/meshcore-dev/MeshCore/tree/dev)
- **Companion:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260526)
- **Repeater:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260526)
- **Room server:** [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260526)

## Recent builds

| Date | Companion | Repeater | Room server |
|------|-----------|----------|-------------|
| 2026-05-26 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260526) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260526) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260526) |
| 2026-05-25 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260525) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260525) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260525) |
| 2026-05-24 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260524) | failed | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260524) |
| 2026-05-23 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260523) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260523) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260523) |
| 2026-05-22 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260522) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260522) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260522) |
| 2026-05-21 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260521) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260521) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260521) |
| 2026-05-20 | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-companion-20260520) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-repeater-20260520) | [ok](https://github.com/marcelverdult/meshcore-nightly/releases/tag/nightly-room-server-20260520) |

## Configured PRs

- [#2553](https://github.com/meshcore-dev/MeshCore/pull/2553) Add exponential flood advert reduction based on hop count — merged
- [#1810](https://github.com/meshcore-dev/MeshCore/pull/1810) Allow direct message paths when denyf * is set — merged
- [#1727](https://github.com/meshcore-dev/MeshCore/pull/1727) Use hardware channel activity detection for checking interference — merged
- [#1954](https://github.com/meshcore-dev/MeshCore/pull/1954) Lora longer preamble — merged
- [#1687](https://github.com/meshcore-dev/MeshCore/pull/1687) Added PowerSaving for all ESP32-based repeaters — conflict
- [#2140](https://github.com/meshcore-dev/MeshCore/pull/2140) Add CLI control to LoRa's fem LNA. — conflict

<!-- END AUTO -->
