# Research Company · 公司调研与合作机会

输入公司名、官网或企业邮箱域名，先选择调研目的、产品重点和深度，再得到有来源的公司与合作机会报告。

[Skill 文件夹](../skills/research-company/) · [核心指令](../skills/research-company/SKILL.md)

## 功能

| 调研问题 | 报告内容 |
| --- | --- |
| 公司制造、集成还是销售？ | 主营业务、产品来源与多重供应链角色 |
| 哪款产品需要哪款我方产品？ | 具体客户型号、需求、接口约束与候选匹配 |
| 哪些是证据，哪些是推断？ | 事实/推断/待确认标签、逐项引用与证据台账 |
| 合作来自哪里？ | 现有采购、新品开发、项目扩展、分销或联合方案 |
| 第一封联系怎么写？ | 联系切入点、建议职能、一个核心问题和英文草稿 |
| 公司属于生态的哪里？ | 上游、交付环节、下游客户、设计和采购控制权 |

还可扩展近期动态、采购触发信号、同类公司与相邻市场、技术兼容性、商业优先级和证据置信度。

默认供应商目录为 Seeed，覆盖 LoRa 模组、开发板、气象站、传感器、采集器和网关。用户可以提供其他供应商目录。型号候选仅是检索入口，每次匹配都会重新核查相关公开规格。

## 交互

输入 `tinycontrol.pl` 后收集三个方向：

1. **目的，单选**：全面了解 / 产品合作与首次联系 / 同类公司与生态拓展。
2. **产品，多选**：LoRa 模组 / 开发板 / 气象站 / 传感器 / 采集器与网关 / 全部。
3. **深度，单选**：快速筛选 / 深入调研。

平台提供原生选择工具时使用真实控件。Claude Code 的 AskUserQuestion 支持多选时启用 multiSelect；其他平台按实际工具能力处理。控件数量有限时分组选择；只有单选或没有原生选择工具时保留编号多选。

文本模式可回复 `目的2；产品1,3,4；深度1`，也可说“默认”“全部产品，深入”。已经给出的方向不会重复询问。

## ChatGPT

在支持 Skills 的界面启用“公司调研与合作机会”，用 `@` 选择该 skill，输入公司名称或官网。当前创建者的 ChatGPT Work 已保存此 skill 后，可以在技能列表中找到它。

其他账号若提供 skill 文件导入入口，可下载本仓库，取出 `skills/research-company` 文件夹，压缩为 `research-company.zip` 后按界面指引导入。压缩包仅包含这个 skill，保持 `research-company/SKILL.md` 和 references 的相对路径。

若当前界面只有普通附件和聊天功能，可以附上 SKILL.md 与 references，明确要求按该流程调研，并启用搜索。这是手动使用流程，不代表已经安装原生 skill。

## Claude

下载本仓库，取出 `skills/research-company` 文件夹并压缩为 ZIP，在 **Customize → Skills → + → Create skill → Upload a skill** 中上传并启用。以实际账号可见入口为准。

Claude Code 用户可将完整文件夹复制到 `~/.claude/skills/research-company/`，然后调用：

```text
/research-company tinycontrol.pl
```

## Codex

将完整文件夹复制到用户技能目录 `~/.agents/skills/research-company/`，或项目目录 `.agents/skills/research-company/`，再调用：

```text
$research-company 调研 tinycontrol.pl
```

也可请当前 Codex 的 skill installer 从本仓库的 `skills/research-company` 路径安装。

## 示例

```text
使用公司调研与合作机会，调研 tinycontrol.pl。先让我选择方向。
```

```text
调研 Alpha-Omega Technology，全面了解，全部产品，快速筛选。
```

```text
调研这个企业邮箱所属公司：[企业邮箱]。重点找 LoRa 模组和气象站的合作机会，深入调研。
```

企业邮箱只用于提取公司域名，不将个人用户名提交到搜索。公共邮箱需要补充公司或官网。

## 运行条件与验证

使用平台已有的联网搜索和网页读取能力，沿用其账号权限与额度，无需 Gemini 密钥或本地网页服务。无联网工具时仅分析提供材料，报告注明覆盖范围。

Skill 格式、引用路径、JSON 示例和 OpenAI 界面元数据均通过本地检查。初次选择流程与已明确方向的联网调研流程经过独立试运行；这是流程验证，Claude 原生控件仍需在用户实际 Claude 环境验证。

## 官方适配资料

- [OpenAI Skills 构建](https://developers.openai.com/plugins/build/skills)
- [ChatGPT Skills 与插件](https://learn.chatgpt.com/docs/skills-and-plugins)
- [Codex 本地技能与使用](https://learn.chatgpt.com/docs/build-skills)
- [Claude 自定义技能](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- [Claude Code Skills](https://code.claude.com/docs/en/skills)
- [Anthropic 交互选择示例](https://github.com/anthropics/claude-code/blob/main/plugins/plugin-dev/skills/command-development/references/interactive-commands.md)

适配资料核查日期：2026-10-13。
