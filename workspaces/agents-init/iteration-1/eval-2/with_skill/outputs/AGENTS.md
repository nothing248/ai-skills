# Project Custom Rules (AGENTS.md)

> [!IMPORTANT]
> This is a project-specific ruleset for AI Agents working on this codebase. All agents MUST strictly adhere to these instructions when modifying code, adding features, or proposing changes.

## 1. Business Logic & Constraints
- **Core Goals**: 为个人用户提供安全、快速的云端文件存储与分享服务。
- **Key Entities & Workflows**: 
  - 用户注册与登录 (新增：支持微信扫码登录)
  - 文件上传、下载、删除
  - 提取码分享链接生成
  - 增值服务：付费扩容空间 (新增：微信支付接入)
- **Business Restrictions**: 
  - 单个文件限制 50MB。
  - 分享链接必须设置过期时间（最长 7 天）。
  - 微信支付回调必须进行签名验证以确保安全。

## 2. Tech Stack & Architecture Rules
- **Core Stack**: Next.js 14 (React 18), TypeScript, Tailwind CSS, Next.js API Routes, Supabase (PostgreSQL)。
- **Directory Structure**: 
  - 组件必须放在 `/components` 下
  - 页面和路由使用 App Router 放在 `/app` 下
  - 工具类函数放在 `/utils` 下
- **Technical Restrictions**: 
  - 所有数据库操作必须使用 Prisma ORM。
  - API 接口必须符合 RESTful 风格。

## 3. Coding Standards & Conventions
- **Style & Naming**: 遵循 TypeScript、Next.js 14 最佳实践，组件和页面结构符合 App Router 规范。
- **Error Handling & Logging**: 
  - API Route 必须捕获所有错误并返回统一的 JSON 格式错误信息。
  - 禁止在生产环境打印 `console.log`。
- **Specific Rules**: 无。
