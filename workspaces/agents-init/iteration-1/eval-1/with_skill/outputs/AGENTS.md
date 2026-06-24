# Project Custom Rules (AGENTS.md)

> [!IMPORTANT]
> This is a project-specific ruleset for AI Agents working on this codebase. All agents MUST strictly adhere to these instructions when modifying code, adding features, or proposing changes.

## 1. Business Logic & Constraints
- **Core Goals**: A simple serverless memo application built with React and LocalStorage.
- **Key Entities & Workflows**: Memo items, saved and retrieved locally.
- **Business Restrictions**: Serverless data persistence using browser's LocalStorage only.

## 2. Tech Stack & Architecture Rules
- **Core Stack**: React, LocalStorage, Vite, Vanilla CSS.
- **Directory Structure**: Standard Vite-React project structure.
- **Technical Restrictions**:
  - You MUST use React Hooks for state management.
  - You MUST keep all styles in raw CSS files.
  - Do NOT use any CSS framework.
  - The application server MUST run on port 3000.

## 3. Coding Standards & Conventions
- **Style & Naming**: Standard React component naming (PascalCase) and functional component guidelines.
- **Error Handling & Logging**: Safely handle LocalStorage read/write exceptions.
- **Specific Rules**: Ensure Vite config is locked to port 3000.
