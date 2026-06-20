# 🧠 notes-optimize (Obsidian & RAG 笔记优化专家)

> **专为 Obsidian 笔记生态与 RAG（检索增强生成）向量检索设计的高品质 Markdown 格式化与脱敏处理技能。**

---

## 🎯 解决的核心痛点

在管理个人知识库（PKM）以及将知识库对接大模型进行 RAG 检索时，我们常遇到以下问题：
1.  **敏感信息泄露**：笔记中夹杂着个人账号、真实姓名、公司内网 IP 或私密密钥，在推送到云端或输入公开大模型时存在极高的泄露风险。
2.  **检索效率低下（RAG 噪音）**：无规整的草稿缺乏语义概述，且含有大量无实际价值的废话（如“本文讲了...”），降低了向量检索（Vector Search）的精度。
3.  **Obsidian 属性缺失**：笔记无 YAML Front Matter 或是缺少 `tags`、`aliases`，导致在 Obsidian 内难以建立关联图谱。

`notes-optimize` 能自动提取草稿核心要点生成高信息密度的 `description`，自动去除并用占位符替换所有隐私敏感词，同时注入标准的 Obsidian YAML 头部及排版样式。

---

## 📁 规范的技能结构

```text
notes-optimize/
├── README.md                                     # 本技能主说明文档
└── SKILL.md                                      # 核心 AI 技能行为规范文件
```

---

---

## 💻 运行与唤醒示例

启动您的 AI 代理，对其发送草稿优化请求：
> **我输入**：
> 帮我把刚才随手写的排版一下，记得去掉里面的敏感 IP 和公司名字，保存到 `my-obsidian-notes/` 下面。

> **AI 代理将依据 SKILL 规范为您输出**：
> 自动在元数据中标记为 `status: completed` 并填充标准属性（包括过滤为 `[IP已隐藏]` 的网络记录），同时生成符合 Kebab-case 的英文文件名，最终保存至对应的 `.md` 文件。

---

## 📄 许可证

本项目基于 [MIT License](LICENSE) 协议开源。
