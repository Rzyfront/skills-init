# AI Skill Init

> **Rapid Context Architecture Generator for AI Agents**

Automatically generates enterprise-grade skill/context systems for AI assistants (Claude, Gemini, Copilot, OpenCode) in any repository.

## 🚀 Quick Start

1.  **Download** or **clone** this repository into your target project:
    ```bash
    cp -r skill-init /path/to/your/project/
    ```

2.  **Run the Wizard**:
    ```bash
    cd /path/to/your/project/skill-init
    ./bin/skill-init
    ```

3.  **Follow the Prompts**:
    *   Select your project stack (Frontend, Backend, etc.).
    *   Choose AI tools to support (Claude, Gemini, Copilot, etc.).
    *   Enable **Skill Creator** and **Skill Sync** (Recommended).
    *   Define dense module contexts (e.g., `apps/api`, `packages/ui`).

## 🌟 Key Features

### 1. Multi-Provider Synchronization
Automatically configures your project for multiple AI assistants using a "Single Source of Truth":

| AI Provider | Configuration Path | Sync Method |
| :--- | :--- | :--- |
| **OpenCode** | `.opencode/skills/` | Symlink / Content Sync |
| **Claude Code** | `.claude/skills/` | Symlink |
| **Gemini** | `.agent/skills/` | Symlink |
| **GitHub Copilot** | `.github/copilot-instructions.md` | Content Embedding |

### 2. Meta-Skills Included
*   **`skill-creator`**: Teaches the AI how to create *new* skills for you, adhering to project standards.
*   **`skill-sync`**: Automates the maintenance of `AGENTS.md`, updating trigger tables and context links.

### 3. Modular Context Architecture
For large monorepos, `skill-init` generates:
*   **Root Context**: High-level rules and "Core" skills.
*   **Module Contexts**: Specific `AGENT.md` files for subdirectories (e.g., `apps/backend/AGENT.md`) to keep context dense and relevant.

### 4. Language Adaptability
Enforces a protocol where the AI **automatically detects and responds in the user's language** (English, Spanish, French, etc.), while keeping the underlying system instructions standardized in English.

## 📂 Generated Structure

```text
your-project/
├── AGENTS.md              # Single Source of Truth (Root)
├── CLAUDE.md              # Entry point for Claude
├── GEMINI.md              # Entry point for Gemini
├── opencode.json          # Entry point for OpenCode
├── .github/
│   └── copilot-instructions.md
├── skills/                # The brain of your project
│   ├── setup.sh           # The synchronizer script
│   ├── skill-creator/     # Meta-skill for creating skills
│   ├── skill-sync/        # Meta-skill for syncing metadata
│   └── your-project-core/ # Core rules (generated)
└── apps/
    └── api/
        └── AGENT.md       # Modular context (optional)
```

## 🛠 Usage Commands

After initialization, you manage your AI context with:

```bash
# Sync all skills to AI providers (Run after adding new skills)
./skills/setup.sh --sync

# Regenerate configuration for a specific tool
./skills/setup.sh --claude
./skills/setup.sh --copilot
```

## 🤝 Contributing

This project is self-hosted! It uses its own `skill-init` architecture.
Check `AGENTS.md` and `skills/` to see how it works internally.

## 📄 License

Apache 2.0
