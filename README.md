# 朋友圈文案主理人 | WeChat Moments Polisher

> **一句话介绍：** 面向希望经营微信私域的中文创作者、独立顾问和专业服务者，这个 Agent Skill 会结合个人背景与最多 20 条历史朋友圈，把图片、草稿或零散想法整理成自然、可信、贴近本人风格的可发布文案。

**核心价值不是“多写几条”，而是让 AI 写得更像你，少一点 AI 腔，也不为凑内容硬拔高。**

English: A reusable Agent Skill that turns images, drafts, and rough notes into natural Chinese WeChat Moments posts in the user's own voice, guided by personal context and up to 20 writing samples.

## 适合谁

- 需要长期经营微信私域的内容创作者、顾问、教练和知识服务者；
- 有想法、有素材，但不想每次从头写朋友圈的人；
- 希望 AI 保留自己的表达习惯，而不是生成标准化营销文案的人。

## 它能做什么

- 只发图片时，直接输出一条可发布文案，不要求用户再次解释图片；
- 润色完整草稿时，优先轻改，保留原意和个人判断；
- 处理零散想法时，帮助整理逻辑与表达，不虚构经历、数据或案例；
- 可以从本地样本读取最多 20 条历史朋友圈，也可在已连接且获授权时使用指定飞书多维表格；
- 只有素材确实缺乏可表达价值时，才提醒用户暂时不适合发，不为了完成任务硬凑。

## 演示

建议在首次发布前，补充一段 20～30 秒的真实使用 GIF 或短视频，展示 **原始输入 → Skill 实际返回的结果**。不要只放架构图，也不要把人工改过的结果伪装成 Agent 原始输出。

演示案例记录模板见 [`examples/真实案例展示模板.md`](examples/真实案例展示模板.md)，录制方法见 [`docs/30秒演示视频脚本.md`](docs/30秒演示视频脚本.md)。

## 快速安装

### Tencent WorkBuddy

1. 下载仓库中的 `dist/wechat-moments-polisher-workbuddy.zip`；
2. 打开 WorkBuddy 的「技能」页面，选择添加/上传本地技能包；
3. 安装后，在对话中发送图片、草稿或零散想法进行测试。

本包按 WorkBuddy 官方文档提供的技能目录与元数据格式准备。首次安装后仍需在你的 WorkBuddy 版本中实际验证。若要读取飞书数据，还需另行连接飞书工具并授予指定多维表格的读取权限。

### Codex

把整个 Skill 文件夹放在用户级目录 `~/.agents/skills/wechat-moments-polisher/`，或放进项目的 `.agents/skills/wechat-moments-polisher/`。目录中需要保留 `SKILL.md` 和 `references/`。Codex 的本地 Skill 发现路径以官方文档为准。

### Claude Code

把整个 Skill 文件夹放在 `~/.claude/skills/wechat-moments-polisher/`（个人级）或项目中的 `.claude/skills/wechat-moments-polisher/`。Claude Code 会发现目录里的 `SKILL.md`。

> 兼容说明：Codex 与 Claude Code 原生支持自定义 Agent Skills；WorkBuddy 使用对应的技能包格式。本仓库包含相应的 WorkBuddy 导入 ZIP。不同客户端对附加元数据、目录位置和工具连接的要求可能不同，请按各自官方文档安装，并以实际测试为准。此 Skill 本身不会自动获得飞书权限。

## 配置个人风格

1. 复制 `references/个人背景与内容策略模板.md` 为 `references/我的个人背景与内容策略.md`；
2. 复制 `references/个人风格样本模板.md` 为 `references/我的个人风格样本.md`，填入最多 20 条本人真实发布过的朋友圈；
3. 如需从飞书读取历史文案，复制 `references/数据源配置模板.md` 为 `references/我的数据源配置.md`，填写目标表与字段信息；
4. 确认 Agent 能访问这些文件，且已经配置所需的连接器和权限。

建议样本覆盖：求职市场观察、产品思考、高价值观点、日常生活。不要把客户资料、私人聊天、访问令牌或其他敏感信息提交到公开仓库。

## 项目结构

```text
wechat-moments-polisher/
├── SKILL.md
├── README.md
├── LICENSE
├── references/
│   ├── 个人背景与内容策略模板.md
│   ├── 个人风格样本模板.md
│   └── 数据源配置模板.md
├── examples/
│   └── 真实案例展示模板.md
├── docs/
│   ├── 30秒演示视频脚本.md
│   └── GitHub发布操作指南.md
└── dist/
    └── wechat-moments-polisher-workbuddy.zip
```

## 隐私与安全

- 公开仓库只放通用规则、空白模板和已脱敏的示例；
- 不要上传真实私人朋友圈样本、客户简历、聊天记录、私有飞书链接或凭据；
- Skill 会根据可访问的信息工作，不会绕过权限；读取失败时不应声称读取成功；
- 安装任何第三方 Skill 前，先检查其中的指令、脚本和外部连接能力。

## 反馈与迭代

欢迎提交 Issue，反馈安装问题、生成结果偏差和兼容性情况。最有帮助的反馈包含：输入类型、预期结果、实际结果，以及可以公开分享的脱敏案例。

## License

本项目采用 MIT License，详见 [`LICENSE`](LICENSE)。
