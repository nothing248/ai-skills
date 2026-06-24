# Project Custom Rules (AGENTS.md)

> [!IMPORTANT]
> This is a project-specific ruleset for AI Agents working on this codebase. All agents MUST strictly adhere to these instructions when modifying code, adding features, or proposing changes.

## 1. Business Logic & Constraints
- **Core Goals**: 为个人用户提供安全、快速的云端文件存储与分享服务（极简网盘系统）。
- **Key Entities & Workflows**:
  - 用户注册与登录。
  - 文件上传、下载与删除。
  - 提取码分享链接的生成。
- **Business Restrictions**:
  - 单个文件大小绝对不能超过 50MB。
  - 生成的分享链接必须设置过期时间（最长不能超过 7 天）。
  - 禁止存储任何违反法律法规的文件。

## 2. Tech Stack & Architecture Rules
- **Core Stack**: Next.js 14 (React 18), TypeScript, Tailwind CSS, Next.js API Routes, Supabase (PostgreSQL), Prisma ORM。
- **Directory Structure**:
  - 组件必须放在 `/components` 下。
  - 页面和路由使用 App Router 格式，必须放在 `/app` 下。
  - 工具类函数必须放在 `/utils` 下。
- **Technical Restrictions**:
  - 所有数据库操作必须使用 Prisma ORM。
  - API 接口设计必须符合 RESTful 风格。

## 3. Coding Standards & Conventions
- **Style & Naming**: 遵循 TypeScript 和 Next.js 的常规标准规范。
- **Error Handling & Logging**:
  - API Route 必须捕获所有可能发生的错误，并返回统一的 JSON 格式错误信息。
  - 禁止在生产环境中打印 `console.log`。
- **Specific Rules**: 暂无其他特殊规则。
