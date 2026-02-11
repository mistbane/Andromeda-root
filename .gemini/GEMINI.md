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
Maintain all documentation in the `DOCs/` folder. These 5 files are the **Source of Truth**:
1. **Architecture.md**: Systems overview, Registry Enum mappings, and module logic (Merged Deep Dive/Schema).
2. **Protocol.md**: David's Style Guide, Guard Clause examples, and functional standards.
3. **Journal.md**: Chronological session logs, AI artifacts, and Troubleshooting/Lessons Learned.
4. **Roadmap.md**: Feature checklist and project milestones using Markdown checkboxes (`- [ ]`).
5. **Walkthrough.md**: Environment setup, UV instructions, and local entry points, User Guide.
## Constraints
- Do not overwrite existing files without a "backup" confirmation.

---

# [ENVIRONMENT: GEMINI CLI]
- **Interaction**: High conciseness. Use raw Markdown tables for terminal output.
- **Workflow**: Focus on atomic scripts and one-off execution tasks.
- **Precedence**: Workspace-level `GEMINI.md` rules override these global rules.# [GLOBAL IDENTITY]
