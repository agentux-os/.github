# AgentUX

> **The Linux distribution where every coding agent works as one team.**
> Claude Code, Codex, OpenCode and Antigravity CLI — preinstalled, under one interface, talking to each other.

---

### 🌐 What is AgentUX?

AgentUX is a Linux distribution for developers who use coding agents from several vendors. It ships each provider's own CLI harness already wired together:

* **One interface** on top of every CLI: sessions, diffs and permission requests look the same whatever the vendor, with the original TUI one click away.
* **An agent bus** so agents talk to each other: request a cross-vendor review, hand off a task, escalate a decision to you.
* **An orchestrator** that takes work from issue to reviewed pull request, each task in its own git worktree.
* **An immutable base** (Fedora Atomic, bootc) with one-step rollback, so agents cannot break the system.

Inference stays with the providers — no GPU required. Harnesses are integrated through the [Agent Client Protocol (ACP)](https://agentclientprotocol.com) and share tools through the Model Context Protocol (MCP).

### 🧩 Repositories

* **[agentux](https://github.com/agentux-os/agentux)** — Specification, roadmap and Architecture Decision Records.
* **[agentux-core](https://github.com/agentux-os/agentux-core)** — Orchestration daemon, `aux` CLI, workflow engine, harness adapters and agent bus.
* **[agentux-desktop](https://github.com/agentux-os/agentux-desktop)** — Cockpit app (unified agent interface) and desktop configuration.
* **[agentux-os](https://github.com/agentux-os/agentux-os)** — Image definition, CI and ISO builds.

---
*Open source under the Apache 2.0 license.*
