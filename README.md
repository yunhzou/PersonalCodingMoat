# PersonalCodingMoat

The central repository for the coding practices every agent working on my projects must follow.

Before starting project work, an agent must clone or reuse this repository and complete the setup in [AGENTS.md](AGENTS.md). This includes planning, investigation, implementation, and review. Reading instructions and fetching the setup materials are the bootstrap steps that come first.

## First-time setup

1. Clone this repository into a persistent location accessible to the agent:

   ```sh
   git clone https://github.com/yunhzou/PersonalCodingMoat.git "$HOME/PersonalCodingMoat"
   ```

   A different location is fine. If it is already cloned, reuse that checkout. Confirm that its `origin` points to this repository. At the start of a new session, update a clean checkout on its default branch with `git pull --ff-only`. Preserve local changes; do not reset or overwrite them to update.

2. Read this README and [AGENTS.md](AGENTS.md) in full.
3. Follow the five principles in AGENTS.md throughout the requested project work.

Repeat the instruction-loading steps for each new agent session. After a context reset or handoff, reload them if they are no longer available in context.

## Connect another project or agent

Cloning this repository alone does not make agents in other projects discover it. Add the following instruction to each agent's persistent instructions or the target project's agent instruction file, preserving any existing content:

```text
Before starting any project work, clone or reuse
https://github.com/yunhzou/PersonalCodingMoat.git in a persistent local location.
Read its README.md and AGENTS.md in full and follow the five principles
alongside the target project's instructions.
Do this for every new session; reload after context loss or handoff.
If required setup materials cannot be loaded, report the blocker before
starting project work. Do not claim setup is complete without reading them.
```

Use the same bootstrap instruction when handing work to another agent. Each agent needs access to the checkout and the instructions, even when another agent has already completed setup.

## Evolving these practices

Keep the owner's shared requirements in AGENTS.md and setup instructions here. Update these practices as the owner specifies them.
