# [GLOBAL IDENTITY]
- **User**: David (Taiwan-based)
- **Primary Stack**: Python 3.12+, UV (Dependency Manager), Dotenv (Secrets Management).
- **Core Philosophy**: Functional Programming (FP), Modular architecture, and Registry-driven dispatch.

# [CORE STANDARDS: SHARED]
## 🛡️ Safety & Git Protocols
1. **Initial Sync**: Always run `git status` before starting any multi-file task.
2. **Commit Gate**: If uncommitted changes exist, pause and ask David for a "Commit or Stash" decision.
3. **Automated Backups**: Create a temporary backup commit for changes involving >3 files: `git commit -m "AG_BACKUP: [task description]" --no-verify`.
4. **Environment Security**: 
   - **Hard Block**: Never create, edit, or commit [.env](cci:7://file:///d:/wrk/python/practice/tag-lab/.env:0:0-0:0), `.env.example`, or credential-related files ([.json](cci:7://file:///d:/wrk/python/practice/tag-lab/client_secret.json:0:0-0:0) keys, `token.json`, etc.).
   - Ensure [.gitignore](cci:7://file:///d:/wrk/python/practice/tag-lab/.gitignore:0:0-0:0) is present and strictly covers all secrets immediately.

## 🛠️ Technical Architecture (The "David" Standard)
1. **Registry Pattern**: Use Enums or Registry Maps for command dispatch and strategy selection. Avoid magic strings.
2. **Modular Threshold**: Any single file exceeding 300 lines or containing >3 primary responsibilities must be refactored into a package with a `__init__.py` facade.
3. **Guard Clause Architecture**: Flatten code by handling edge cases/errors first. Indentation must not exceed 2 levels in core logic.
4. **Functional Purity**: Core business logic must be deterministic and modular. Separate I/O (CLI, API, DB) from logic.
5. **Schema-First Config**: Validate all external configurations (YAML/JSON) using Pydantic or Dataclasses during load. Fail-fast on schema mismatch.
6. **Robustness**: Default to UTF-8. For local data files, attempt `Big5` or `GBK` if UTF-8 parsing fails.
7. **Type Safety**: Implement comprehensive Python 3.12+ type hints across all modules.
8. **Tooling**: Use `uv run` for execution and `uv pip` for management. Use `python-dotenv` for all secrets.

# [DOCUMENTATION ARCHITECTURE]
Maintain all documentation in the `DOCs/` folder. These 5 files are the Source of Truth:
1. **Roadmap.md**, **Journal.md**, **Architecture.md**, **Protocol.md**, **Walkthrough.md**.

# [GEMINI CLI INTERACTION]
- **Interaction**: High conciseness. Use raw Markdown tables for terminal output.
- **Workflow**: Focus on atomic scripts and one-off execution tasks.

<!-- # [GLOBAL IDENTITY]
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
   - Ensure `.token.json`, `client_secret.json` is in `.gitignore` immediately.
   - **Hard Block**: Never create, edit, or commit `.env` or `.env.example` files to the repository.
   - **Hard Block**: Never `git add` or commit credential-related files (`.json` keys, `token.json`, `client_secret.json`, `cookies.txt`, etc.).

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
Maintain all documentation in the `DOCs/` folder. These 5 files are the **Source of Truth**:
1. **Roadmap.md**: Feature checklist and project milestones using Markdown checkboxes (`- [ ]`).
## Constraints
- Do not overwrite existing files without a "backup" confirmation.
## None Vital, only when asked, update these:
1. **Architecture.md**: Systems overview, Registry Enum mappings, and module logic (Merged Deep Dive/Schema).
2. **Protocol.md**: David's Style Guide, Guard Clause examples, and functional standards.
3. **Journal.md**: Chronological session logs, AI artifacts, and Troubleshooting/Lessons Learned.
4. **Walkthrough.md**: Environment setup, UV instructions, and local entry points, User Guide.
---

# [ENVIRONMENT: GEMINI CLI]
- **Interaction**: High conciseness. Use raw Markdown tables for terminal output.
- **Workflow**: Focus on atomic scripts and one-off execution tasks.
- **Precedence**: Workspace-level `GEMINI.md` rules override these global rules.# [GLOBAL IDENTITY] -->
