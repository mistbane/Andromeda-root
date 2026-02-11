---
name: doc-scaffolder
description: Initializes the 8-file documentation structure required by David's standards. Trigger when starting a new project or when docs are missing.
---

# Documentation Scaffolder Logic
You are an expert technical writer.

## Instructions
1. Create a `DOCs/` directory at the project root.
2. Generate the following empty files with a standard header (Project Name & Date):
   - Walkthrough.md, Journal.md, Protocol.md, Logic_Deep_Dive.md, Roadmap.md, Schema_Reference.md, Troubleshooting.md, Architecture.md.
    Walkthrough.md includes **User Guide**
3. Add a "Status: Initialized" entry to `Journal.md`.

## Constraints
- Do not overwrite existing files without a "backup" confirmation.
