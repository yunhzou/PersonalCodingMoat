# Agent instructions

Before starting project work, clone or reuse [PersonalCodingMoat](https://github.com/yunhzou/PersonalCodingMoat.git) and read its [README.md](README.md) and this file in full. Apply these principles alongside the target project's instructions. Reload them for each new session or after context loss.

## 1. Explanation

Keep verbal explanations clear and concise. Keep niche technical details brief. Communication must be efficient and understandable to researchers.

## 2. Code structure

Code structure must coevolve with vibe coding. During a rapid proof of concept, it is okay to prototype quickly, even in a single file with hundreds of lines of code. Once the user confirms that a feature is useful, refactor it into a coherent, modular architecture.

Pay significant attention to high-level architectural design. Discuss the intended functionality, module boundaries, and responsibilities in depth with the developer. Think about the long-term structure: establish the key concepts and separable modules before focusing on niche functionality. Specify which parts of the code belong in each module and how the modules interact.

Organize modules around clear responsibilities and interfaces. Keep closely related functionality together, minimize dependencies between unrelated components, and separate reusable core logic from experiment-specific scripts. Modularity means meaningful separation of responsibilities, not simply dividing code into smaller files.

Follow the architectural principles and hierarchy previously approved by the user. Integrate new functionality into that structure, and identify when extending or revising the architecture is necessary. Avoid introducing competing structures or abstractions without a concrete need.

Revisit the architecture with the developer whenever refactoring reveals conflicting responsibilities, functionality is difficult to fit into the core modules, or features need refactoring before the necessary architectural changes have been agreed upon and completed. Resolve these design questions before proceeding with the affected refactoring.

You may provide architectural design choices, tradeoffs, and recommendations, but the user makes the final architectural decision. Once the design is agreed upon, document it in `design.md` and create architectural diagrams showing the module hierarchy, responsibilities, interfaces, and main interactions.

## 3. Cleaning

Code must never have fallback options. Duplicate functionality is unacceptable. After refactoring, remove the superseded code and options completely from the repository. Leave no obsolete code behind.

When you observe multiple fragmented pieces of code in the repository, treat this as a clear signal that it needs cleaning and refactoring. Follow principle 2.

For example, if several quickly written scripts exist in the repository and the user has confirmed that their functionality is useful, refactor that functionality into reusable core modules instead of leaving it in standalone scripts. Modularity and reusability must be enforced.

## 4. Version control

When the desired outcome is reached and the user confirms that a feature is good, immediately commit it to Git. Clearly document what experiment was performed, what was accepted, and whether refactoring and validation have been completed.

Version design principles as well as code. When the user explicitly specifies how the design should be structured, record those decisions and their reasoning in `design.md` and commit them.

Version control is not limited to preserving code. It must also support effective information exchange by documenting the reasoning and development process. Proper versioning also supports thorough cleaning.

## 5. Working on a cluster

Development often takes place locally and on a cluster. Whenever development spans multiple machines, always use Git to synchronize the work.

There must be a single source of truth for the project, and communication with the user must consistently refer to it. Each machine must have only one copy of the codebase. Enforce this, and use Git to reconcile changes whenever the copies become unsynchronized.
