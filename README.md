# PersonalCodingMoat

Shared coding principles for agents working on my projects.

Before starting work, read and follow [AGENTS.md](AGENTS.md).

Place this `AGENTS.md` in the root of your working repository, or merge it into the existing file while preserving project-specific instructions.

- **Codex** loads `AGENTS.md` automatically. An `AGENTS.override.md` in the same directory takes precedence. [Official documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md).
- **Claude Code** (v2.1.277+) loads `AGENTS.md` by default when no project `CLAUDE.md`, `.claude/CLAUDE.md`, or `CLAUDE.local.md` exists in the working directory or its parents. If those instructions exist, or direct loading is unavailable, add `@AGENTS.md` on its own line in the repository-root `CLAUDE.md`, preserving existing content. [Official documentation](https://code.claude.com/docs/en/memory#agentsmd).

Start a new session in the working repository after setup.
