# 🧠 AI Skills Collection (AI 技能库)

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/LLM--Ready-Yes-blueviolt.svg" alt="LLM Ready">
  <img src="https://img.shields.io/badge/Obsidian--Ready-Yes-purple.svg" alt="Obsidian Ready">
</p>

> **这是一个专为 AI 编码助手（如 Gemini/Claude Code 等）设计的自定义技能库（Custom Skills Collection），用于辅助科学自学、结构化笔记大纲的定制生成以及 Obsidian 笔记的脱敏优化。**

---

## 📁 仓库结构

该仓库采用多 Skill 存储架构，目前包含以下核心技能及开发测试工作区：

```text
ai-skills/
├── README.md                                     # 仓库主文档（本文件）
├── skills/                                       # 技能存放目录
│   ├── agents-init/                              # 技能 1: 项目级 Agent 规则初始化工具
│   │   ├── README.md                             # 技能说明文档
│   │   ├── SKILL.md                              # 技能行为规范文件
│   │   └── evals/                                # 自动化评测用例
│   │       └── evals.json
│   ├── notes-create-template/                    # 技能 2: 笔记大纲生成器
│   │   ├── README.md                             # 技能说明文档
│   │   ├── SKILL.md                              # 技能行为规范文件
│   │   └── resources/                            # 具体的笔记大纲模板
│   │       ├── theory-template.md                # 理论概念大纲模板
│   │       ├── tool-template.md                  # 工具框架大纲模板
│   │       └── project-template.md               # 实战项目大纲模板
│   └── notes-optimize/                           # 技能 3: 笔记优化与脱敏工具
│       ├── README.md                             # 技能说明文档
│       └── SKILL.md                              # 技能行为规范文件
└── workspaces/                                   # 技能开发与测试工作区
    └── agents-init/                              # agents-init 技能评测工作目录与历史归档
```

---

## 🛠️ 技能介绍

### 1. [agents-init](skills/agents-init/README.md) (项目级 Agent 规则初始化)
*   **核心功能**：通过自动分析和提取项目中的 `prd.md`（产品需求）和 `tech-stack.md`（技术架构），整合并生成一套专门约束和引导后续开发 Agent 的行为守则及项目规范（写在 `.agents/AGENTS.md` 中）。
*   **内置方法**：自动识别核心业务逻辑实体限制（如文件大小限制、过期时间限制）以及硬性技术规范（如数据库框架选用、错误返回及日志打印限制），并格式化为标准规则模块。
*   **适用场景**：新项目初始化时需要划定 Agent 行为准则，或需求设计文档变动后需要一键同步规则给后续 Agent 时。

### 2. [notes-create-template](skills/notes-create-template/README.md) (学习笔记与大纲架构师)
*   **核心功能**：根据具体的**学习事物**及**应用目标**，为用户量身定制纯净空白、高启发性的 Markdown 笔记大纲模板。
*   **内置方法**：深度融入了 SQ3R 提问法、康奈尔双栏笔记法、费曼测试以及蔡格尼克悬案箱，促进用户深度加工与主动学习，同时设计了双向代码路由以便后期维护。
*   **适用场景**：想要系统化学习某个新协议、新工具或手写核心项目时。

### 3. [notes-optimize](skills/notes-optimize/README.md) (Obsidian & RAG 笔记优化专家)
*   **核心功能**：将凌乱的技术草稿、日常随手记，一键转化为对大模型 RAG（检索增强生成）友好且安全脱敏的 Obsidian 笔记。
*   **内置方法**：自动识别并过滤隐私信息（IP地址、私钥、公司名、真实姓名等）为占位符；提取高信息密度的笔记摘要（summary）放入 YAML 中以提升向量数据库的检索召回精度。
*   **适用场景**：发布笔记前需要安全脱敏，或者想将笔记存入 Obsidian 并实现向量检索时。

---

## 🚀 安装与集成

### 1. gh skill 安装
如果你配置了 `gh skill` 扩展，可以直接在终端运行以下命令来安装对应的技能：

```bash
# 安装项目规则初始化技能
gh skill install nothing248/ai-skills agents-init

# 或者一键集成此仓库内的所有技能
gh skill install nothing248/ai-skills
```

### 2. npx skills 安装
你也可以使用官方的 `npx skills` 工具从 GitHub 远程仓库或本地路径添加并管理技能：

```bash
# 远程安装：从 GitHub 仓库远程安装指定的单个技能
npx skills add nothing248/ai-skills --skill agents-init

# 或者一键集成此仓库内的所有技能
npx skills add nothing248/ai-skills --all
```

---

## 📄 许可证

本项目基于 [MIT License](LICENSE) 协议开源。
