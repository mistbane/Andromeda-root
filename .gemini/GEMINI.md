# [GLOBAL IDENTITY]
- **User**: David (Taiwan-based)
- **Primary Stack**: Python 3.12+, UV (Dependency Manager), Dotenv (Secrets Management).
- **Core Philosophy**: Functional Programming (FP), modular architecture, and Registry-driven dispatch.

---

# [CORE STANDARDS: SHARED]
## 🛡️ Safety & Git Protocols
1. **Git Status Check**: Always run `git status` before starting any multi-file task.
2. **Commit Gate**: If uncommitted changes exist, pause and ask David for a "Commit or Stash" decision.
3. **Automated Backups**: For changes involving >3 files, create a temporary backup commit: `git commit -m "AG_BACKUP: [task description]" --no-verify`.
4. **Environment Security**: 
   - Ensure `.env` is in `.gitignore` immediately.
   - **Hard Block**: Never create, edit, or commit `.env` or `.env.example` files to the repository.

## 🛠️ Technical Architecture (The "David" Standard)
1. **Registry Pattern**: Use Enums to drive command dispatch and source processing. Avoid conditional strings.
2. **Guard Clauses**: Flatten code by handling edge cases/errors first. Indentation must not exceed 2 levels.
3. **Functional Purity**: Core logic must be deterministic and modular. Separate CLI, UI, Config, and API utilities.
4. **Type Safety**: Implement comprehensive type hints (Python 3.12+ syntax) across all modules.
5. **Robustness**: Default to UTF-8. For local data files, attempt `Big5` or `GBK` if UTF-8 parsing fails.
6. **Tooling**: Use `uv run` for execution and `uv pip` for management. Use `python-dotenv` for all secrets.

---

# [ENVIRONMENT: ANTIGRAVITY IDE]
## Documentation Architecture (Professional 5)
Maintain all documentation in the `DOCumentations/` folder. These 5 files are the **Source of Truth**:
1. **Architecture.md**: Systems overview, Registry Enum mappings, and module logic (Merged Deep Dive/Schema).
2. **Protocol.md**: David's Style Guide, Guard Clause examples, and functional standards.
3. **Journal.md**: Chronological session logs, AI artifacts, and Troubleshooting/Lessons Learned.
4. **Roadmap.md**: Feature checklist and project milestones using Markdown checkboxes (`- [ ]`).
5. **Walkthrough.md**: Environment setup, UV instructions, and local entry points.

---

# [ENVIRONMENT: GEMINI CLI]
- **Interaction**: High conciseness. Use raw Markdown tables for terminal output.
- **Workflow**: Focus on atomic scripts and one-off execution tasks.
- **Precedence**: Workspace-level `GEMINI.md` rules override these global rules.# [GLOBAL IDENTITY]

<!--
- User: David (Taiwan-based)
- Core Stack: Python 3.12+, UV, Dotenv.
- Communication: Direct, technical, and grounded.

---

# [CORE STANDARDS: SHARED]
## Safety Protocols
1. **Git First**: Always check `git status` before any complex task. 
2. **Commit Gate**: If uncommitted changes exist, pause and ask for a commit.
3. **Backup Mode**: If modifying >3 files, create a temporary backup commit: `git commit -m "AG_BACKUP: [task name]" --no-verify`.

## Technical Standards (The "David" Pattern)
1. **Registry Pattern**: Use Enums to drive command dispatch and source processing.
2. **Clean Logic**: No nested `if/else` or `for` loops. Use guard clauses and helper functions.
3. **Modular Architecture**: Strict separation of CLI, UI, Config, and API Utilities.
4. **Type Safety & FP**: Use comprehensive type hints and functional programming patterns for core logic.
5. **Robustness**: Default to UTF-8 for all configs. For data files, attempt Big5/GBK if UTF-8 fails.
## Tools
1. Use `uv` for all dependency/execution tasks. 
2. Use `python-dotenv` for secrets.

## Security
- Always ensure `.env` is in `.gitignore`.
- **Hard Block**: Never create `.env` or `.env.example` in the repo.

---

# [ENVIRONMENT: ANTIGRAVITY IDE]
## Documentation Architecture
- All documentation MUST reside in the `DOCumentations/` folder.
- Maintain these 8 specific files: `Walkthrough.md`, `Journal.md`, `Protocol.md`, `Logic_Deep_Dive.md`, `Roadmap.md`, `Schema_Reference.md`, `Troubleshooting.md`, `Architecture.md`.
- Sync AG "Task Artifacts" into the `Journal.md` or `Roadmap.md` after completion.

---

# [ENVIRONMENT: GEMINI CLI]
- **Formatting**: Use terminal-optimized tables.
- **Conciseness**: Avoid conversational filler; output code or status directly.## Safety Protocols
1. Always check git status before starting a complex task.
2. If there are uncommitted changes, ask the user if they want to commit them first.
3. If the task involves modifying more than 3 files, create a temporary backup commit automatically.

## Technical Standards
1.  **Registry Pattern**: Use Enums to drive command dispatch and source processing.
2.  **No Nested Logic**: Avoid nested `if/else` and `for` loops; use guard clauses and helper functions.
3.  **Modular Architecture**: Separate CLI, UI, Config Management, and API Utilities into distinct modules.
4.  **Type Safety**: Implement comprehensive type hints across the entire codebase.
5.  **Robustness**: Explicitly handle UTF-8 encoding for configuration files to support international characters.
6. **function programming**: Use function programming to implement the core logic of the application.
7. Use UV to manage dependencies.
8. Use dotenv to manage environment variables.

## Other Requirements
1. Add .env into .gitignore
2. Do not put any .env file in the repository.
3. Do not put any .env.example file in the repository.

## Documentation:
1. Save all *.md file under local DOCumentations
2. Walkthrough.md
3. Journal.md
4. Protocol.md
5. Logic_Deep_Dive.md
6. Roadmap.md
7. Schema_Reference.md
8. Troubleshooting.md
-->
 