# 技术栈设计: 极简网盘系统

## 1. 核心技术栈
- 前端：Next.js 14 (React 18), TypeScript, Tailwind CSS
- 后端：Next.js API Routes
- 数据库：Supabase (PostgreSQL)

## 2. 目录规范
- 组件必须放在 `/components` 下
- 页面和路由使用 App Router 放在 `/app` 下
- 工具类函数放在 `/utils` 下

## 3. 开发规范与约束
- 所有数据库操作必须使用 Prisma ORM
- API 接口必须符合 RESTful 风格
- 错误处理：API Route 必须捕获所有错误并返回统一 of JSON 格式错误信息，禁止在生产环境打印 `console.log`。
