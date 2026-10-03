# AgentUX

> **One control plane for every coding agent you already use.**
> Orchestrate Claude Code, Codex, OpenCode, Antigravity and other harnesses across multiple projects — from issue to reviewed pull request.

---

### 🌐 What is AgentUX?

AgentUX coordinates coding agents from different vendors so they work together instead of side by side. Each task runs in its own git worktree, one agent implements, another vendor's agent reviews, tests gate every step, and you only step in when a decision is yours to make.

Inference stays with the providers; AgentUX is the orchestration layer. It integrates harnesses through the [Agent Client Protocol (ACP)](https://agentclientprotocol.com) and their native headless modes, and gives them shared tools through the Model Context Protocol (MCP).

### 🧩 Repositories

* **[agentux](https://github.com/agentux-os/agentux)** — Specification, roadmap and Architecture Decision Records.
* **[agentux-core](https://github.com/agentux-os/agentux-core)** — Orchestration daemon, workflow engine and harness adapters.
* **[agentux-desktop](https://github.com/agentux-os/agentux-desktop)** — Cockpit UI: live agent status, diffs, approvals and token spend.
* **[agentux-os](https://github.com/agentux-os/agentux-os)** — Optional Linux flavor with AgentUX and a modern dev toolchain preinstalled (planned).

---
*Open source under the Apache 2.0 license.*
