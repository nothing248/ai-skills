---
name: agents-init
description: Generate or update the project's AGENTS.md configuration by analyzing key workspace markdown files, specifically prd.md (Product Requirements Document) and tech-stack.md (Tech Stack Design Document). Always use this skill when the user asks to initialize project rules, update agent guidelines, configure AGENTS.md, or align agent behaviors with design documents.
---

# Agents Init Skill

This skill allows Antigravity to automatically initialize or update the project's `AGENTS.md` (project-scoped custom rules) by extracting and synthesizing constraints and guidelines from `prd.md` (Product Requirements) and `tech-stack.md` (Tech Stack Design).

## Workflow

Follow these steps when this skill is triggered:

### 1. File Inspection
Check for the existence of `prd.md` and `tech-stack.md` in the project's root directory:
- If they exist, read both files.
- If one or both files are missing, search the workspace for files with similar names (e.g., `README.md`, `architecture.md`, `requirements.md`, `specification.md`).
- If no design or requirement documents are found, inform the user that `prd.md` and `tech-stack.md` are missing, and ask them to either provide the requirements/tech-stack details or point to the correct files.

### 2. Information Extraction
Extract the following information from the source markdown files:
- **From prd.md (Product Requirements)**:
  - Core business objectives and goals.
  - Critical business logic, workflows, and core entities.
  - Hard business constraints (e.g., "Must comply with GDPR", "Payments must only go through Stripe").
- **From tech-stack.md (Tech Stack Design)**:
  - Allowed programming languages, frameworks, libraries, and their specific versions.
  - Architectural patterns, folder/directory structure conventions.
  - Technical constraints (e.g., "Must use React hooks", "Do not use external CSS frameworks unless tailwind is requested").
  - Coding standards (naming conventions, error handling rules, logging conventions).

### 3. Synthesis & Compilation
Synthesize the extracted constraints into a clean, concise, and structured ruleset formatted as markdown.
Ensure the rules are framed as direct instructions for the AI Agent (e.g., "You MUST do X", "Do NOT use Y"). Avoid generic descriptions; focus on actionable rules.

### 4. Writing AGENTS.md
- Output the generated rules directly to the `.agents/AGENTS.md` file in the project workspace root.
- If the `.agents` folder does not exist, create it.
- Use the following standard layout for the `AGENTS.md`:

```markdown
# Project Custom Rules (AGENTS.md)

> [!IMPORTANT]
> This is a project-specific ruleset for AI Agents working on this codebase. All agents MUST strictly adhere to these instructions when modifying code, adding features, or proposing changes.

## 1. Business Logic & Constraints
- **Core Goals**: [Brief summary of what this project does]
- **Key Entities & Workflows**: [Definitions of key domain models or workflows]
- **Business Restrictions**: [Actions agents must never perform due to business requirements]

## 2. Tech Stack & Architecture Rules
- **Core Stack**: [Languages, frameworks, and tools with versions]
- **Directory Structure**: [Conventions on where to put specific code files]
- **Technical Restrictions**: [Forbidden tech choices, packages, or patterns]

## 3. Coding Standards & Conventions
- **Style & Naming**: [Conventions for variables, functions, files]
- **Error Handling & Logging**: [How errors should be caught and logged]
- **Specific Rules**: [Any unique instructions extracted from tech-stack.md]
```

### 5. Verification
After writing `.agents/AGENTS.md`, present the file contents to the user, highlight the key extracted rules, and explain how the generated ruleset aligns with the source documents (`prd.md` and `tech-stack.md`).
