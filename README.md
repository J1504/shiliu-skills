# 拾流 Shiliu · Agent 自媒体专家

**让你的 Agent 成为你的自媒体专家。**

拾流为使用 Agent 的内容创作者整合参考资料、创作技能和云端工作空间。把创作目标交给自己的 Agent，让它找参考、研究选题、选用方法、完成稿件，并在开放的文档与表格中整理创作。

Shiliu connects a creator's own AI agent to reference data, creative methods, and a cloud workspace. Research benchmark accounts, develop content ideas, write short-video scripts, revise drafts, and organize ongoing work through one service.

[官网 Website](https://shiliuai.cn) · [Agent 接入入口](https://shiliuai.cn/llms.txt) · [API 指南](https://shiliuai.cn/api/v2/agent-guide) · [Skill 正文](skills/shiliu/SKILL.md)

## 直接交给 Agent

把下面这句话发给能够联网读取文档并调用 HTTPS 接口的 Agent。

> 请接入 https://shiliuai.cn，成为我的自媒体专家，并执行我提供的创作任务。先读 https://shiliuai.cn/llms.txt。有可用 API Key 或 registration_secret 时复用原身份和授权空间；没有凭证时，按文档自主调用 POST /api/v2/agents/register 开户，不要先让我手工注册、创建 Key 或充值。符合条件可获3元通用体验金，先在体验金和任务范围内查资料、采集、转写、调用接口并保存成果，按实时价格设置费用上限。余额不足、要求邮箱验证或需要表格引擎、持续任务时，再在当前对话用邮箱验证码认领；需要充值时明确金额，直接展示支付宝二维码。不要索取账户密码，不替我同意认领条款或开启付费授权。没有 HTTP 执行工具时明确说明限制，不把读到网页说成已完成接入。

## 无需先手工开户

有 Key 或 registration_secret 时复用已有身份。没有凭证时，能调用 HTTP API 的 Agent 按 [接入协议](https://shiliuai.cn/skill/references/account.md) 自主注册，符合条件先用3元通用体验金执行任务并保存成果；不必先打开网页注册、创建Key或充值。

余额不足、要求邮箱验证、需要多维表格引擎或持续任务时，再在当前对话通过主人邮箱验证码认领。充值直接展示支付宝二维码。认领条款、账户余额付费权限和实际付款仍由主人确认。

## 公开发现与使用指南

- [从这里开始](https://shiliuai.cn/guides/get-started/)
- [研究对标账号](https://shiliuai.cn/use-cases/competitor-research/)
- [策划内容选题](https://shiliuai.cn/use-cases/content-planning/)
- [创作短视频脚本](https://shiliuai.cn/use-cases/script-writing/)
- [公开创作技能目录](https://shiliuai.cn/skills/)
- [Agent 接入说明](https://shiliuai.cn/docs/agent/)
- [公开接口核验记录](https://shiliuai.cn/stories/agent-discovery-check/)
- [实际口播创作与修改记录](https://shiliuai.cn/stories/agent-script-workshop/)
- [怎样选择适用的创作技能](https://shiliuai.cn/guides/choose-creative-skills/)

## 安装 Skill

通过支持 Agent Skills 的安装工具安装此仓库。

```bash
npx skills add J1504/shiliu-skills --skill shiliu
```

也可以下载 [Release 中的 ZIP 技能包](https://github.com/J1504/shiliu-skills/releases)，在支持 `SKILL.md` 的 Agent 产品中按其导入流程安装。安装方式和 HTTP 工具能力取决于具体客户端。此仓库提供标准 Agent Skill，尚未提供 MCP 服务。

This is a standard Agent Skill, not an MCP server. Your agent needs HTTPS access; agents without credentials can autonomously register for eligible CNY 3 trial credit. Reuse existing keys, and keep credentials in secret settings. Claiming and recharge can be completed in the owner conversation.

## 你可以这样开始

以下是可直接提出的任务示例，不是真实客户成效声明。

- **找对标**　“我做面向职场新人的知识口播，帮我找值得研究的对标账号，整理近期选题和表达特点。”
- **找资料与选题**　“围绕我这个账号的受众研究下周的内容，给出三个选题和参考来源。”
- **完成创作**　“选择合适的创作技能，把选定的主题写成一分钟口播稿，保留我的表达风格。”
- **修改与积累**　“根据我的反馈修改稿件，把资料、定稿和以后要遵守的偏好整理进我的空间。”

## 数据、技能与空间

| 能力 | Agent 可以做什么 |
|---|---|
| 创作数据 | 研究对标账号与作品，查询平台支持的外部数据接口，保留来源与日期 |
| 创作技能 | 按任务查找创作 Skill，读取方法和配套文件，应用到选题、写作及修改 |
| 创作空间 | 通过接口创建和更新文档、表格与目录，保存目标、资料、稿件和偏好 |

平台、接口、价格和权限以服务实时返回为准。对标内容按服务同步周期更新；读取全文取决于实际收录和账户权益。

## 账号、费用和数据

Skill 免费安装。公开技能目录免费读取。部分数据查询、博主订阅和文案提取需要拾流账号及费用授权，由拾流服务按当前报价计费；安装 Skill 不会自动订阅或充值。

Agent 通过 HTTPS 将用户请求的查询参数和需要保存的内容发送到 `shiliuai.cn`，并在授权范围内读写用户空间。API Key 仅用于该服务，不放入 URL、公开聊天、仓库或结果文档。这个技能不自动读取本地文件、不执行安装脚本、不配置系统定时任务。

## English quick start

Install the `shiliu` skill, then tell your agent your content goal, audience, platform, and intended output. The agent reads the current service guide, finds relevant references and creative methods, and uses your authorized workspace for notes and drafts. Public skill discovery works without credentials. Private workspace access and paid data operations require your account and explicit authorization.

Example: “Use Shiliu to research benchmark creators for my educational short-video account. Propose three original topics with source links, then draft the topic I choose and save the work to my workspace.”

## License and support

The original integration skill and documentation in this repository are distributed under the [MIT License](LICENSE). This license does not grant rights to the hosted service, collected source content, or third-party skills. Those retain their respective terms and licenses.

Report integration issues through [GitHub Issues](https://github.com/J1504/shiliu-skills/issues). Service entry: [shiliuai.cn](https://shiliuai.cn).
