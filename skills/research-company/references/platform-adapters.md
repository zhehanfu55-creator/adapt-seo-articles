# 平台适配

在执行前检查可用工具与实际参数。以下是能力映射，不是强制依赖。

| 能力 | Claude | ChatGPT / Codex |
| --- | --- | --- |
| 技能入口 | 支持 Agent Skills 的 Claude 环境读取 SKILL.md；Claude Code 可按安装后的命令调用 | Skills 环境读取 SKILL.md；Codex 可显式 `$research-company` |
| 搜索与读页 | 使用已提供的 web search / web fetch 或获授权的搜索工具 | 使用已提供的搜索与 open/fetch 工具 |
| 单选 | 存在 AskUserQuestion 时按其当前 schema 调用；否则使用宿主的选择功能或文本 | 存在 request_user_input 或其他选择工具时按当前 schema 调用；否则文本 |
| 多选 | AskUserQuestion 若支持 multiSelect，设 true；限制选项数量并按 intake.md 分组 | 仅在工具显式支持多选时使用；只有单选时保留编号多选 |
| 来源 | 使用实际检索结果的原生引用；可移植导出使用原始 URL | 使用实际检索结果的原生引用；可移植导出使用原始 URL |

## 可移植执行规则

1. 不强制依赖某个模型、Gemini、API 密钥、本地 Node 服务或付费搜索 API。
2. 读取工具文档再调用。不假定所有 Claude 界面都有 AskUserQuestion，也不假定所有 ChatGPT 界面都有弹窗或多选。
3. 原生工具缺失时显示简短文本问卷，用户用编号或自然语言作答。明确当前显示的是文本选项，不声称已弹窗。
4. 不把引用格式固定成某一家平台的特殊 token。浏览工具引用要匹配当前平台真实返回的来源编号。
5. 没有联网能力时接收用户提供的公开资料，标明“基于提供材料”；不要用训练记忆生成最新公司证据或虚构检索过程。
6. 保留 SKILL.md 的通用 frontmatter，仅 name 和 description。agents/openai.yaml 是 OpenAI 界面元数据，Claude 执行核心流程无需读取它。
7. 技能使用所在平台的正常额度与账号能力；不要宣称安装后获得无限或免费的额外搜索额度。
8. 在具有更高优先级工具限制、网络限制或保存规则的宿主中遵循它们；功能降级时具体说明受限的能力。

## 原生控件映射示例

仅在实际工具 schema 与示例字段一致时使用。例如 Claude Code 提供 AskUserQuestion 且允许四选项时，可以提交：

```json
{
  "questions": [{
    "question": "本次重点关注哪些产品？可多选，也可直接回复全部。",
    "header": "产品重点",
    "multiSelect": true,
    "options": [
      {"label": "LoRa模组", "description": "找无线通信器件的设计或采购切入点。"},
      {"label": "开发板", "description": "找原型验证、新品开发与教学机会。"},
      {"label": "气象站", "description": "找环境观测与项目扩展机会。"},
      {"label": "其他设备", "description": "继续选择传感器、采集器或网关。"}
    ]
  }]
}
```

当 ChatGPT 的 request_user_input 只允许单选与 2–3 个选项时，使用它处理目的/深度，另用文本保留产品多选。依据实际工具定义要求的 Recommended 后缀、header 长度、问题数量等约束生成参数，不将上例跨工具复制。

## 官方参考与维护

截至 2026-10-13 核查的官方文档：

- OpenAI 技能格式与构建：https://developers.openai.com/plugins/build/skills
- ChatGPT 技能与插件：https://learn.chatgpt.com/docs/skills-and-plugins
- Claude 自定义技能：https://support.claude.com/en/articles/12512180-use-skills-in-claude
- Claude Code 技能目录：https://code.claude.com/docs/en/skills
- Anthropic 原生问询示例：https://github.com/anthropics/claude-code/blob/main/plugins/plugin-dev/skills/command-development/references/interactive-commands.md

安装入口与工具权限可能因版本/账号变化，按实际界面和官方文档确认。不要将适配指南当作运行时工具注册。
