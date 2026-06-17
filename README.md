# 🧠 notes-structure-skill (学习笔记与大纲架构师)

> 运用认知心理学与现代个人知识管理（PKM）系统（如 Obsidian、Notion）设计的自学笔记结构定制引擎。

这是一个专为自学者和内容分享者打造的 AI Agent 技能（Skill）。它能够根据您具体的 **学习事物**（理论、工具或项目）与 **学习目标**，运用成熟的科学自学法（SQ3R、费曼技巧、康奈尔笔记、蔡格尼克效应）和版本维护逻辑，动态定制生成一套**空白的、带启发式提问的 Markdown 自学笔记大纲与管理模板**。

---

## 🎨 核心设计理念

### 1. 融入的学习科学理论 (Active Learning)
*   **SQ3R 主动检索 (Questioning)**：首创前置自我探索问答，除留空让您在自学前罗列个人疑问外，技能会结合目标为您智能定制 3 个最核心、非直觉的“硬核前置问题”，强迫大脑带着疑问去检索答案。
*   **康奈尔笔记法 (Cornell Notes)**：正文结构采用 **「💡 核心线索/启发提问」** 与 **「📝 我的学习笔记与代码细节」** 的左线索右笔记对照结构，拒绝机械性地“读完即复制”，提升知识的加工深度。
*   **费曼技巧 (Feynman Technique)**：在章节底部留出白话教学输出栏，引导您尝试用最简单、不带任何术语的语言解释给新手听，从而验证自己是否真正掌握。
*   **蔡格尼克效应 (Zeigarnik Effect)**：增设 **「⏳ 蔡格尼克悬案箱」**，收集学习中途产生的临时盲区并挂牌，促进潜意识在日常中继续寻找答案。

### 2. 笔记生命周期与知识图谱管理 (PKM Lifecycle)
为了避免“记完即弃”的技术债务，使这篇笔记成为“可维护、可演进的知识软件”：
*   **标准 YAML Frontmatter 看板**：支持 Obsidian、Logseq、Notion 等知识库直接解析，提供状态标记（🔴 未开始 -> 🟡 进行中 -> 🟢 已掌握 -> 🔵 复习中）和掌握度评分。
*   **物理与代码物理路由 (`code_router`)**：支持绑定本地代码物理绝对路径、分支及 Git 仓库，实现代码和笔记的双向一键直达。
*   **分享发布中心 (`publishing`)**：集中记录与跟踪当前文章分发到掘金、Notion、个人博客、GitHub Wiki 等平台的状态与链接。
*   **笔记版本迭代日志 (Release Changelog)**：每一次由于新技术版本变更、或者是重温避坑重新修改笔记时，在此留下一行 Changelog 记录（如 `v1.0 搭建骨架` -> `v1.1 修复 node 22 版本下 alpine 镜像编译 node-sass 报错日志`）。
*   **艾宾浩斯间隔复习打卡表**：为这篇笔记量身制定 1天-3天-7天-30天 复习任务与回看重点，抗遗忘必备。

---

## 📂 项目结构

```text
notes-structure-skill/
├── .gitignore
├── LICENSE
├── README.md
├── .agents/
│   └── skills/
│       └── agency-learning-notebook-architect/
│           └── SKILL.md                          # 核心 AI 技能行为规范文件
└── examples/
    └── docker_nodejs_example.md                  # 模拟生成的空白大纲示例文件
```

---

## 🚀 安装与使用

### 1. 手动集成到您的 Agent 项目中
直接将本项目下的 `.agents/skills/agency-learning-notebook-architect` 文件夹拷贝到您自己的项目的 `.agents/skills/` 目录下即可激活：

```bash
# 假设您的项目根目录为 your-agent-project
cp -r .agents/skills/agency-learning-notebook-architect /path/to/your-agent-project/.agents/skills/
```

### 2. 运行与唤醒
启动您的 AI 代理对话，向支持 Skills Router 的 Agent 发送类似以下指令：

```text
我想学习：[Docker]
我的具体学习目标是：[在生产环境中打包并安全部署一个 Node.js (Express) Web 应用，要求尽可能压缩镜像体积，并解决容器内应用崩溃无法自动重启的问题。]
```

Agent 将自动识别该技能，并根据您的具体目标为您生成一套场景化定制、空白的 Markdown 自学笔记大纲模板。

---

## 📄 示例大纲展示

您可以访问 [examples/docker_nodejs_example.md](examples/docker_nodejs_example.md) 查看技能根据具体目标量身定做的 Docker + Node.js 镜像打包空白笔记大纲。

---

## 📄 许可证

本项目基于 [MIT License](LICENSE) 协议开源。
