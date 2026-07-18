# Stremio Stream Engine for Home Assistant

Home Assistant app repository for running the open-source [`perpetus/stream-server`](https://github.com/perpetus/stream-server) engine locally on Home Assistant OS or Supervised installations.

The app exposes a Stremio-compatible HTTP API on port `11470` for use with the separate [`Stremio Stream Bridge`](https://github.com/diegocesaretti/stream-server-ha) custom integration.

## Installation

Add this repository in the Home Assistant app store:

```text
https://github.com/diegocesaretti/stremio-stream-engine-ha
```

Then install **Stremio Stream Engine**, start it, and configure Stremio Stream Bridge to use:

```text
http://HOME_ASSISTANT_IP:11470
```

Use the Raspberry Pi or Home Assistant host LAN address rather than `localhost`, because Cast receivers must reach the stream URL directly.

## Supported architectures

- `aarch64` — Raspberry Pi 5 and other 64-bit ARM hosts
- `amd64` — x86-64 hosts

## Upstream

The container builds the pinned `perpetus/stream-server` v0.1.8 release with the upstream-supported `libtorrent` backend.
