<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/agentux-os/.github/raw/main/profile/assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/agentux-os/.github/raw/main/profile/assets/banner-light.svg">
  <img alt="AgentUX: the Linux distribution where every coding agent works as one team" src="https://github.com/agentux-os/.github/raw/main/profile/assets/banner-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://agentuxos.org"><img alt="Website" src="https://img.shields.io/badge/website-agentuxos.org-c6f36b?labelColor=0b0d10"></a>
  <a href="https://download.agentuxos.org"><img alt="Download" src="https://img.shields.io/badge/download-ISO-c6f36b?labelColor=0b0d10"></a>
  <a href="https://github.com/agentux-os/agentux-os/actions/workflows/build.yml"><img alt="Image build" src="https://img.shields.io/github/actions/workflow/status/agentux-os/agentux-os/build.yml?branch=main&label=image&logo=github&labelColor=0b0d10"></a>
  <a href="https://github.com/agentux-os/agentux-core/releases"><img alt="agentux-core release" src="https://img.shields.io/github/v/release/agentux-os/agentux-core?include_prereleases&label=agentux-core&labelColor=0b0d10&color=4f7d0b"></a>
  <a href="https://github.com/agentux-os/agentux-desktop/releases"><img alt="agentux-desktop release" src="https://img.shields.io/github/v/release/agentux-os/agentux-desktop?include_prereleases&label=agentux-desktop&labelColor=0b0d10&color=4f7d0b"></a>
  <a href="https://github.com/agentux-os/agentux-core/actions/workflows/ci.yml"><img alt="agentux-core CI" src="https://img.shields.io/github/actions/workflow/status/agentux-os/agentux-core/ci.yml?branch=main&label=core%20ci&labelColor=0b0d10"></a>
  <a href="https://github.com/agentux-os/agentux-desktop/actions/workflows/ci.yml"><img alt="agentux-desktop CI" src="https://img.shields.io/github/actions/workflow/status/agentux-os/agentux-desktop/ci.yml?branch=main&label=desktop%20ci&labelColor=0b0d10"></a>
  <a href="https://fedoraproject.org/atomic-desktops/kinoite/"><img alt="Base: Fedora Kinoite 44" src="https://img.shields.io/badge/base-Fedora%20Kinoite%2044%20%C2%B7%20bootc-4f7d0b?logo=fedora&logoColor=white&labelColor=0b0d10"></a>
  <a href="https://github.com/agentux-os/agentux/blob/main/LICENSE"><img alt="License: Apache 2.0" src="https://img.shields.io/badge/license-Apache%202.0-4f7d0b?labelColor=0b0d10"></a>
</p>

<p align="center">
  <a href="https://agentuxos.org"><b>Website</b></a> ·
  <a href="https://download.agentuxos.org"><b>Download</b></a> ·
  <a href="https://github.com/agentux-os/agentux/tree/main/docs"><b>Docs</b></a> ·
  <a href="https://github.com/agentux-os/agentux/blob/main/docs/getting-started.md"><b>Getting started</b></a> ·
  <a href="https://github.com/agentux-os/agentux-os/releases"><b>Releases</b></a>
</p>

AgentUX is a Linux distribution for developers who use coding agents from several vendors. Claude Code, Codex, OpenCode and Antigravity CLI come preinstalled and wired together:

- **One interface** on top of every CLI: sessions, diffs and permission requests look the same whatever the vendor, with the original TUI one click away.
- **An agent bus** so agents talk to each other: ask a reviewer from another vendor to check a diff, hand off a task, escalate a decision to you.
- **An orchestrator** that takes work from issue to reviewed pull request, each task in its own git worktree.
- **An immutable base** (Fedora Kinoite, bootc) with one-step rollback, so agents cannot break the system.

Inference stays with the providers, on your own logins and API keys; no GPU required. Harnesses are driven through the [Agent Client Protocol](https://agentclientprotocol.com) and share tools over the Model Context Protocol.

<p align="center">
  <a href="https://github.com/agentux-os/agentux"><img alt="The AgentUX cockpit: two runs, one waiting for plan approval" src="https://raw.githubusercontent.com/agentux-os/agentux/main/docs/screenshots/cockpit-plan-approval.png" width="760"></a>
</p>

### Try it

AgentUX is pre-release: the first image release (v0.5.x) is being published now, for x86_64 and aarch64, in a KDE Plasma and a Hyprland variant.

- **Without installing:** boot the [live ISO](https://download.agentuxos.org/iso/stable/agentux-live-x86_64.iso) from a USB stick or a VM. It runs the real desktop with a demo of fake agents, and installs when you want to keep it ([how](https://github.com/agentux-os/agentux-os#try-it-live)).
- **Install:** the [installer ISO](https://download.agentuxos.org/iso/stable/agentux-x86_64.iso), or switch an existing Fedora Atomic / bootc system:

  ```sh
  sudo bootc switch ghcr.io/agentux-os/agentux:stable
  systemctl reboot
  ```

- **Then:** follow [Getting started](https://github.com/agentux-os/agentux/blob/main/docs/getting-started.md) to log in to the vendor CLIs and start a first run.

Every image is signed with cosign and installed systems refuse unsigned updates ([verifying](https://github.com/agentux-os/agentux-os#verifying-the-image)). All downloads, with checksums and signatures: [download.agentuxos.org](https://download.agentuxos.org) · [Install guide](https://github.com/agentux-os/agentux-os#install)

### Repositories

| Repository | What it holds |
|---|---|
| [agentux](https://github.com/agentux-os/agentux) | Specification, roadmap, architecture decision records, brand |
| [agentux-core](https://github.com/agentux-os/agentux-core) | `agentuxd` daemon, `aux` CLI, workflow engine, harness adapters, agent bus |
| [agentux-desktop](https://github.com/agentux-os/agentux-desktop) | Cockpit app (one interface over every agent) and the KDE Plasma defaults |
| [agentux-os](https://github.com/agentux-os/agentux-os) | Image definition (`Containerfile`), image CI, signing and ISO builds |

<sub>Open source under the Apache 2.0 license.</sub>
