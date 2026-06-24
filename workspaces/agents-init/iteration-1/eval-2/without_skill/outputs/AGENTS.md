# Project Custom Rules (AGENTS.md)

## 1. Business Logic & Constraints
- **Core Goals**: 提供安全、快速的云端文件存储与分享服务。
- **Key Entities & Workflows**:
  - 用户注册与登录：支持微信扫码登录。
  - 文件管理：文件上传、下载、删除。
  - 提取码分享：生成提取码分享链接。
  - 增值服务：付费扩容空间，接入微信支付。
- **Business Restrictions**:
  - 单个文件大小不能超过 50MB。
  - 分享链接必须设置过期时间，最长 7 天。
  - 微信支付回调必须进行签名验证以确保安全。

## 2. Tech Stack & Architecture Rules
- **Core Stack**: Next.js 14 (React 18), TypeScript, Tailwind CSS, Supabase (PostgreSQL).
- **Directory Structure**:
  - 组件必须放在 `/components` 下。
  - 页面和路由使用 App Router 放在 `/app` 下。
  - 工具类函数放在 `/utils` 下。
- **Technical Restrictions**:
  - 所有数据库操作必须使用 Prisma ORM。
  - API 接口必须符合 RESTful 风格.
  - 错误处理：API Route 必须捕获所有错误并返回统一的 JSON 格式错误信息。
  - 生产环境禁止打印 `console.log`。
