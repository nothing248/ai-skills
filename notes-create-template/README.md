# 🧠 notes-create-template (学习笔记与大纲架构师)


> **基于自学科学理论与现代知识管理体系（PKM）设计的自学笔记大纲定制引擎。**

---

## 🎯 解决的核心痛点

在传统的自学过程中，我们常常面临以下三大难题：
1.  **“收藏即学会”的幻觉**：机械地复制文档、抄写代码，大脑处于被动的“低加工状态”，记完笔记很快就忘。
2.  **“笔记垃圾堆”的债务**：笔记写完就丢，无法在后续实践中持续迭代演进，最终成为死知识。
3.  **“代码与笔记脱节”**：看笔记时找不到当时跑通的 Demo，看代码时又想不起背后的原理，缺乏路由追踪。

`notes-create-template` 旨在利用 AI 代理，根据您具体的**学习主题**与**应用目标**，为您定制生成兼顾**“自学理解”**、**“传播分享”**以及**“生命周期维护”**的真空 Markdown 学习笔记大纲。

---

## 🗺️ 科学学习与维护架构图

本项目深度融合了学习心理学与软件工程中的版本管理思想，将笔记视为“活的软件”进行设计：

```mermaid
graph TD
    %% 阶段 1
    subgraph Phase0 [0. 带着问题出发]
        SQ3R[SQ3R 提问法] --> PreQ[前置疑问预留区]
        SQ3R --> CustomQ[智能定制3个硬核前置设问]
    end

    %% 阶段 2
    subgraph Phase1 [1. 深度认知加工]
        Cornell[康奈尔笔记] --> LeftCol[左栏：核心线索/启发提问]
        Cornell --> RightCol[右栏：代码骨架/空白笔记]
        Feynman[费曼技巧] --> PlainSummary[章节底部：新手大白话复盘]
    end

    %% 阶段 3
    subgraph Phase2 [2. 动态维护与分享]
        Router[代码-笔记双向路由] --> CodeRouter[绑定本地物理路径与Git Commit]
        Changelog[版本迭代日志] --> ReleaseLog[Changelog v1.0 -> v2.0 持续打版本]
        SpacedRep[艾宾浩斯复习] --> ReviewTable[1-3-7-30天打卡回看重点]
        PublishHub[分发中心] --> ShareBlog[支持 Notion/掘金/Github 一键分发]
    end

    PreQ --> LeftCol
    RightCol --> CodeRouter
    PlainSummary --> ReviewTable
```

---

## 🧠 融入的学术理论支柱

*   **SQ3R 学习法 (Questioning)**：在大纲首要位置设计「前置问题探索清单」，通过问题迫使大脑进行**“主动信息检索”**。
*   **康奈尔笔记法 (Cornell Notes)**：将正文任务里程碑（Milestones）拆分为 `[💡 核心线索/启发提问]` 与 `[📝 学习笔记与代码细节]` 的对照框架，促成概念深度绑定。
*   **费曼技巧 (Feynman Technique)**：每个核心里程碑后留有「白话教学输出栏」，用最简单、不带术语的语言解释给新手听，从而自我验证。
*   **蔡格尼克效应 (Zeigarnik Effect)**：增设 **「⏳ 蔡格尼克悬案箱」**，收集学习中途产生的临时盲区并挂牌，促进潜意识在日常中继续寻找答案。

---

## 📁 规范的技能结构

```text
notes-create-template/
├── README.md                                     # 本技能主文档
├── SKILL.md                                      # 核心 AI 技能行为规范文件
└── resources/                                    # 剥离的具体笔记大纲模板
    ├── theory-template.md
    ├── tool-template.md
    └── project-template.md
```

---

---

## 💻 运行与唤醒示例

启动您的 AI 代理，向其发送具体的目标描述指令，例如：

> **我输入**：
> 我想学习 `Docker`，我的具体学习目标是 `在生产环境中打包并安全部署一个 Node.js (Express) Web 应用，要求尽可能压缩镜像体积，并解决容器内应用崩溃无法自动重启的问题。`

> **AI 代理将依据 SKILL 规范为您输出**：
> 高度场景化定制的空白大纲笔记模板。输出的笔记大纲将实现全生命周期元数据管理、双向代码路由、调试避坑日志以及温故知新打卡等极致细节的空白模板。

---

## 📄 许可证

本项目基于 [MIT License](LICENSE) 协议开源。
