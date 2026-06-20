# 🧠 AI Skills Collection (AI 技能库)

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/LLM--Ready-Yes-blueviolt.svg" alt="LLM Ready">
  <img src="https://img.shields.io/badge/Obsidian--Ready-Yes-purple.svg" alt="Obsidian Ready">
</p>

> **这是一个专为 AI 编码助手（如 Gemini/Claude Code 等）设计的自定义技能库（Custom Skills Collection），用于辅助科学自学、结构化笔记大纲的定制生成以及 Obsidian 笔记的脱敏优化。**

---

## 📁 仓库结构

该仓库采用多 Skill 存储架构，目前包含以下两个核心技能：

```text
ai-skills/
├── README.md                                     # 仓库主文档（本文件）
└── skills/                                       # 技能存放目录
    ├── notes-create-template/                    # 技能 1: 笔记大纲生成器
    │   ├── README.md                             # 技能说明文档
    │   ├── SKILL.md                              # 技能行为规范文件
    │   └── resources/                            # 具体的笔记大纲模板
    │       ├── theory-template.md                # 理论概念大纲模板
    │       ├── tool-template.md                  # 工具框架大纲模板
    │       └── project-template.md               # 实战项目大纲模板
    └── notes-optimize/                           # 技能 2: 笔记优化与脱敏工具
        ├── README.md                             # 技能说明文档
        └── SKILL.md                              # 技能行为规范文件
```

---

## 🛠️ 技能介绍

### 1. [notes-create-template](skills/notes-create-template/README.md) (学习笔记与大纲架构师)
*   **核心功能**：根据具体的**学习事物**及**应用目标**，为用户量身定制纯净空白、高启发性的 Markdown 笔记大纲模板。
*   **内置方法**：深度融入了 SQ3R 提问法、康奈尔双栏笔记法、费曼测试以及蔡格尼克悬案箱，促进用户深度加工与主动学习，同时设计了双向代码路由以便后期维护。
*   **适用场景**：想要系统化学习某个新协议、新工具或手写核心项目时。

### 2. [notes-optimize](skills/notes-optimize/README.md) (Obsidian & RAG 笔记优化专家)
*   **核心功能**：将凌乱的技术草稿、日常随手记，一键转化为对大模型 RAG（检索增强生成）友好且安全脱敏的 Obsidian 笔记。
*   **内置方法**：自动识别并过滤隐私信息（IP地址、私钥、公司名、真实姓名等）为占位符；提取高信息密度的笔记摘要（summary）放入 YAML 中以提升向量数据库的检索召回精度。
*   **适用场景**：发布笔记前需要安全脱敏，或者想将笔记存入 Obsidian 并实现向量检索时。

---

## 🚀 安装与集成

### 1. gh skill 安装
如果你配置了 `gh skill` 扩展，可以直接在终端运行以下命令来安装对应的技能：

```bash
# 安装笔记大纲生成技能
gh skill install nothing248/ai-skills notes-create-template

# 或者一键集成此仓库内的所有技能
gh skill install nothing248/ai-skills
```

### 2. npx skills 安装
你也可以使用官方的 `npx skills` 工具从 GitHub 远程仓库或本地路径添加并管理技能：

```bash
# 远程安装：从 GitHub 仓库远程安装指定的单个技能
npx skills add nothing248/ai-skills --skill notes-create-template

# 或者一键集成此仓库内的所有技能
npx skills add nothing248/ai-skills --all
```

---

## 📄 许可证

本项目基于 [MIT License](LICENSE) 协议开源。
