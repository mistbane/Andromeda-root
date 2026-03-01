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
2. **Modular Threshold**: Any single file exceeding 300 lines or containing >3 primary responsibilities must be refactored into a package with a [__init__.py](cci:7://file:///d:/wrk/python/practice/tag-lab/tagger/__init__.py:0:0-0:0) facade.
3. **Guard Clause Architecture**: Flatten code by handling edge cases/errors first. Indentation must not exceed 2 levels in core logic.
4. **Functional Purity**: Core business logic must be deterministic and modular. Separate I/O (CLI, API, DB) from logic.
5. **Schema-First Config**: Validate all external configurations (YAML/JSON) using Pydantic or Dataclasses during load. Fail-fast on schema mismatch.
6. **Robustness**: Default to UTF-8. For local data files, attempt `Big5` or `GBK` if UTF-8 parsing fails.
7. **Type Safety**: Implement comprehensive Python 3.12+ type hints across all modules.
8. **Tooling**: Use `uv run` for execution and `uv pip` for management. Use `python-dotenv` for all secrets.

# [DOCUMENTATION ARCHITECTURE]
Maintain all documentation in the `DOCs/` folder. These are the Core Source of Truth:
1. **Roadmap.md**, **Journal.md**, **Architecture.md**, **Protocol.md**, **Walkthrough.md**.
2. **Gotchas.md**: (NEW CORE) Mandatory log of traps, bugs, and non-obvious lessons learned.

## [PROJECT-SPECIFIC EXTENSIONS]
If the project involves these domains, the following files are REQUIRED:
- **Prompts.md**: For AI-integrated apps. Stores personas, few-shot examples, and model logic.
- **API.md**: For Web apps. Maps HTMX endpoints to their logic and HTML partials.
- **Notes.md**: For unique business logic (e.g., Mapping Protocols, Math formulas).

# [GEMINI CLI INTERACTION]
- **Interaction**: High conciseness. Use raw Markdown tables for terminal output.
- **Workflow**: Focus on atomic scripts and one-off execution tasks.