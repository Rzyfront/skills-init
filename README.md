
## 🔧 TODO

- [x] Implement `interactive_wizard()` in `bin/skill-init`
- [x] Add more stack detectors
- [ ] Generate pre-configured skills by stack
- [x] Support for Gemini and OpenCode
- [ ] Support for Windsurf, Cursor, etc.
- [ ] Setup.sh tests

## 📚 Based On

This generator is based on the [Gentleman.Dots](https://github.com/gentleman-programming/Gentleman.Dots) skill system.


## 📋 Features

| Feature | Description |
|---------|-------------|
| **Auto-detection** | Automatically analyzes your tech stack |
| **Template Generation** | Creates structured `AGENTS.md` and `SKILL.md` |
| **Universal Setup** | `setup.sh` script adaptable to any repo |
| **Multi-tool Sync** | Claude, Copilot, Gemini, OpenCode, etc. |
| **Interactive CLI** | Step-by-step guided wizard |

## 🎯 Usage

```bash
# Interactive Menu
./bin/skill-init

# Auto-detect Stack
./bin/skill-init --auto

# View Help
./bin/skill-init --help
```

## 📁 Generated Structure

```
your-project/
├── AGENTS.md              # Single Source of Truth
├── CLAUDE.md              # Claude Code instructions
├── GEMINI.md              # Gemini CLI instructions
├── opencode.json          # OpenCode configuration
├── .github/
│   └── copilot-instructions.md
├── skills/                # Repository-specific skills
│   ├── your-project-core/
│   │   └── SKILL.md
│   └── setup.sh
└── .skill-config          # Local config
```
