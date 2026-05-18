# Guardian-Gate (ai-safety-layer)

**The AI Sandbox.**

Runtime safety and verification layer for AI agents. Use to enforce strict execution boundaries, audit all AI actions, and prevent the execution of destructive commands (e.g., recursive deletions on root, table drops). This reduces the cognitive burden of manual verification.

## Key Features
- **Deterministic Boundaries**: Regex-based blocking of dangerous commands.
- **Dry-Run Policy**: Validates commands before they are executed.
- **Audit Logging**: Every action (passed or blocked) is recorded with a timestamp.
- **CLI-Native**: Lightweight Python script for immediate verification.

## How it works
1. Pipe any AI-generated command or script through the `safety_check.py` tool.
2. The tool checks against a blacklist of destructive patterns.
3. If safe, the command is logged and allowed to proceed.
4. If dangerous, the command is blocked, and an alert is raised.

---
*Developed as part of the "Missing Tools" initiative for Developer Friction 2026.*
