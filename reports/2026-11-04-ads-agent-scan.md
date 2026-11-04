# 广告投放 Agent / AI 项目日报：2026-11-04

> 整理时间：2026-11-04 13:49:44 UTC（纽约 2026-11-04 08:49:44 EST）。
> GitHub 元数据采集窗口：2026-11-04 13:27:45 — 2026-11-04 13:30:08 UTC；逐项时间见[数据快照](../sources/2026-11-04-github-snapshot.json)。
> 只收录直接服务广告投放的项目。主表门槛为 100 Stars，属于本日报的分层规则，不代表成熟度。

## 今日值得关注

- **本期首次收录 Claude Ads，关注度为 10,727 Stars。** [广告审计与规划 Skills](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L10-L46)直接面向付费广告数据、预算方案、素材与优化草稿；能力清单中 12 平台账户写入均禁用。它在本次样本中 Stars 最高，但不能据此认定具备自动账户执行或已验证的投放收益。
- **Google 官方 Ads MCP 已出现资产与标签写入。** [当前 README](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/README.md#L14-L36) 与选定源码新增广告资产创建、本地视频上传、标签/标签关联操作。本期应修订上期“仅核验读取工具”的适用范围；仍未证明支持预算、竞价等全部写入。
- **AdCraft 的关注度和默认分支均有变化。** 当前 595 Stars，较 11-02 快照 +33；[提交比较](https://github.com/GML-MMGroup/AdCraft/compare/0e6317d618a9d2065b3b6639c91b5119c1563e92...6e8cfdb7d958aca150b73979a82e6e928d135d1a)显示新增 70 个提交，涉及广告创意方法、脚本 Skills 与运行时。源码变化不能直接推导样片质量或 ROAS 提升。
- **Ryze 的高关注度需结合交付形式判断。** [托管服务接入仓库](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md) 为 6,952 Stars（较基线 +180）；固定提交的完整树共 24 个文件，未见服务端实现，不能按完整自托管服务器评估。
- **Synter 修订了平台覆盖表述。** [README](https://github.com/Synter-Media-AI/mcp-server/blob/73292595ea013e4de5025c9a8b73c53dc5919792/README.md#L168-L203) 区分托管服务“30+ 广告平台”的声明与本地包表列的 16 平台，部分平台的写入/创建有限。本文未验证这些平台的真实账户可用性。

本期主表 **18 项**，低热度专项观察 **4 项**，合计 **22 项**。本次新增收录 **3 个项目**（指本日报首次收录，不表示今天新发布）：[AgriciDaniel/claude-ads](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md)、[alimama-tech/AuctionNet](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md)、[DV0x/creative-ad-agent](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md)。

## 热度与比较口径

1. Stars、Forks 为本次 GitHub API 观察值；两张表分别按 Stars 降序。热度不等于真实用户、广告支出、生产可用性或投放收益。
2. “Stars 较 11-02”来自[上期固定提交的数据快照](https://github.com/duanyuanzhe/adsWithAi/blob/20b44d926179cb316fc97b3e67e3682e653c48a2/sources/2026-11-02-github-snapshot.json)，覆盖约 60 小时；**不是今日或近 24 小时增长**。新增项没有相同基线，不补造增量。Forks 变化和精确采集时间也保留在 JSON 中。
3. 最近推送采用 `pushed_at`，可能来自其他分支；功能变化另用固定提交之间的 compare 核对，不把更新时间当作发布或上线时间。
4. 上期 [PR #1](https://github.com/duanyuanzhe/adsWithAi/pull/1) 在本次整理时仍为 OPEN。本期从当前 `main` 建独立分支，不将待合并的上期报告重复打包；上期比较链接固定到实际提交。

## 100 Stars 以上的广告相关项目

| 项目 | Stars / Forks | Stars 较 11-02 | 最近推送 UTC | 直接广告能力与证据 | 投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [AgriciDaniel/claude-ads](https://github.com/AgriciDaniel/claude-ads) | 10,727 / 1,563 | 首次收录 | 2026-11-01 | 广告专用审计与优化 Skills：12 平台广告数据/导出分析、预算与渠道方案、投放节奏监测、广告素材 Brief、草稿优化。 [证据](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L10-L12) | 用于投放诊断与变更前审阅。清单内 12 平台账户写入均禁用；Amazon 原生导出标准化与账户健康评分也禁用。仅 Claude Code 获项目方运行验证，本文未复测。 |
| [irinabuht12-oss/google-ads-meta-ads-mcp](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp) | 6,952 / 373 | +180 | 2026-10-27 | 托管 Google/Meta 广告账户、Campaign、预算、受众、素材与效果分析入口；功能范围为 README 声明。 [证据](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md#L117-L145) | 仓库树 24 个文件中未见服务端实现；6,952 Stars 是公开关注度，不代表可自行部署或真实投放效果。 |
| [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp) | 1,350 / 282 | +6 | 2026-10-20 | Meta Campaign/Ad Set/Ad 管理、预算、定向、素材上传和效果分析。 [证据](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md#L175-L188) | 适合 Meta 执行连接器。仓库含 Python 实现；托管服务的五平台与工具总数不能直接算作本仓库覆盖。 |
| [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) | 1,117 / 350 | +13 | 2026-11-02 | GAQL 账户读取、广告资产创建、本地视频上传、标签和标签关联管理；写入采用 Propose & Confirm。 [证据](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/README.md#L14-L36) | 本次新增资产/标签写入证据，不能推断已支持预算或竞价修改。远程图片用 base64；视频上传仅本地 stdio。文档要求人工确认，checksum 校验本身不是独立审批凭证。 |
| [realkimbarrett/advertising-skills](https://github.com/realkimbarrett/advertising-skills) | 772 / 68 | +3 | 2026-03-26 | 仅收录广告创意组件：前三秒 Hook/画面/脚本构思，以及广告角度与 Hook 变体生成。 [证据](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/README.md#L42-L51) | 广告素材提示词资产；不推荐其中的邮件、落地页等泛营销部分。没有广告账户执行能力。 |
| [cohnen/mcp-google-ads](https://github.com/cohnen/mcp-google-ads) | 718 / 158 | +1 | 2025-10-16 | 通过 MCP 分析 Google Ads Campaign、广告、关键词、预算消耗与竞价策略数据。 [证据](https://github.com/cohnen/mcp-google-ads/blob/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a/README.md#L7-L35) | 适合只读分析接入比较；最近推送为 2025-10-16，采纳前需核对当前依赖与 API 兼容性。 |
| [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft) | 595 / 74 | +33 | 2026-11-04 | 面向广告视频的 Agent 工作流：创意、脚本、产品视觉、分镜、视频与最终合成。 [证据](https://github.com/GML-MMGroup/AdCraft/blob/6e8cfdb7d958aca150b73979a82e6e928d135d1a/README.md#L71-L113) | 广告视频生产方向。默认分支新增 70 个提交，涉及创意方法、脚本 Skill 与运行时；本次只做文档/选定源码核验，未生成或评估广告样片。 |
| [poseljacob/agentic-video-editor](https://github.com/poseljacob/agentic-video-editor) | 507 / 62 | +0 | 2026-04-14 | 以原始素材与创意 Brief 生成广告剪辑；包含 UGC 广告管线、DTC 风格及导演/剪辑/审片反馈循环。 [证据](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md#L104-L130) | 适合短视频广告素材迭代。CLI 是文档推荐路径，Web UI 标明 pre-alpha；不负责账户投放。 |
| [mathiaschu/meta-ads-analyzer](https://github.com/mathiaschu/meta-ads-analyzer) | 466 / 63 | +2 | 2026-02-26 | 分析 Meta Campaign/Ad Set/Ad 表现，诊断 Breakdown Effect、学习阶段、重叠、节奏与素材疲劳。 [证据](https://github.com/mathiaschu/meta-ads-analyzer/blob/9088472ddacdb89f3c5943c3db6be7b8ee25c922/README.md#L3-L14) | 广告分析 Skill；可用广告导出数据，也可配置外部 MCP 取实时数据，不能当作独立全功能执行服务器。 |
| [gomarble-ai/facebook-ads-mcp-server](https://github.com/gomarble-ai/facebook-ads-mcp-server) | 368 / 111 | +2 | 2026-08-05 | 读取 Meta 广告账户、Campaign、Ad Set、Ad、Creative 和 Insights，给 AI 提供广告数据。 [证据](https://github.com/gomarble-ai/facebook-ads-mcp-server/blob/a3b555a12dff5b888b172ef9113dd1f36d69e525/readme.md#L99-L133) | 适合广告效果分析连接器。本文不据这些读取工具推定支持创建或修改投放。 |
| [TheMattBerman/meta-ads-kit](https://github.com/TheMattBerman/meta-ads-kit) | 350 / 68 | +2 | 2026-06-10 | Meta 广告日报、素材疲劳、预算建议、广告文案、暂停/恢复及 Pixel/CAPI 检查。 [证据](https://github.com/TheMattBerman/meta-ads-kit/blob/dffa0daf6ed1e278481e9408af3be6aaf9709b28/README.md#L12-L25) | OpenClaw 广告专用工作流；上传采用 CLI-first、PAUSED/dry-run 约束，具体上传范围仍受 CLI 支持限制。 |
| [zubair-trabzada/ai-ads-claude](https://github.com/zubair-trabzada/ai-ads-claude) | 285 / 99 | +2 | 2026-04-08 | 广告专用 Claude Code Skills：平台格式广告文案、视频广告脚本、关键词及预算方案。 [证据](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/README.md#L74-L103) | 优先关注 ads-copy/ads-video 素材组件；策略评分和预算预测是模型建议，没有证明可自动修改账户。 |
| [alimama-tech/AuctionNet](https://github.com/alimama-tech/AuctionNet) | 257 / 41 | 首次收录 | 2025-04-25 | 广告拍卖与自动竞价 Agent 基准：仿真环境、数据轨迹、强化学习、在线线性规划及 Decision Transformer 策略。 [证据](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md#L14-L20) | 适合预算/CPA 约束下的离线竞价策略比较。属于仿真和训练，不能直接执行广告账户投放；Diffbid 待实现，最近推送为 2025-04-25。 |
| [TheMattBerman/google-ads-copilot](https://github.com/TheMattBerman/google-ads-copilot) | 241 / 47 | +0 | 2026-06-10 | 读取账户或 CSV，形成可审核草稿；文档列出否定关键词、暂停关键词/广告组、日预算调整的受控 Apply。 [证据](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md#L19-L29) | 适合 Read → Draft → Apply 设计；应以列明的写入范围评估，不能推定覆盖全部 Google Ads 操作。 |
| [brijr/meta-mcp](https://github.com/brijr/meta-mcp) | 201 / 75 | +0 | 2026-05-28 | Cloudflare Workers 上的 Meta 广告账户设置、Campaign、Ad Set、素材、受众与报表工具。 [证据](https://github.com/brijr/meta-mcp/blob/664b20617a6aee529ff31f8093e85fca7db4b7be/README.md#L73-L82) | 适合 Meta OAuth、工具组织和部署模型比较；与 Pipeboard 是不同实现。 |
| [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) | 146 / 47 | +0 | 2026-08-05 | Google Ads OAuth、GAQL 广告数据查询与关键词研究，供 AI 客户端调用。 [证据](https://github.com/gomarble-ai/google-ads-mcp-server/blob/4f922abc8f9932a5080052a222a5edb86d7a3697/README.md#L27-L35) | 适合 Google Ads 数据接入备选；文档的 account management 不足以证明全部 Campaign 写入。 |
| [DV0x/creative-ad-agent](https://github.com/DV0x/creative-ad-agent) | 127 / 28 | 首次收录 | 2026-09-06 | 广告专用素材 Agent：品牌网页事实研究 → Hook → 视觉提示 → AI 图片，输出多广告概念与素材变体。 [证据](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md#L1-L3) | 适合为投放测试准备图片素材。依赖外部模型/图片服务；未证明发布广告、控制预算或读取真实 A/B 结果，也未验证转化提升。 |
| [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent) | 117 / 24 | +1 | 2026-11-01 | 跨渠道广告消耗、转化、CPL、预算节奏分析及报告，准备带原因和检查计划的 Campaign 变更。 [证据](https://github.com/langchain-ai/paid-media-agent/blob/c81f9950cd56449a770a9a9e5e9e0a3fad54c382/README.md#L27-L54) | 适合投放分析到审核的业务闭环。真实账户变更默认关闭，需写入策略、发布检查与授权审核。 |

## 低热度专项观察

以下项目均有直接广告业务证据，但低于主表门槛；保留为协议、参考架构或控制流程观察，**不称作热门项目**。

| 项目 | Stars / Forks | Stars 较 11-02 | 最近推送 UTC | 直接广告能力与证据 | 投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [prebid/salesagent](https://github.com/prebid/salesagent) | 39 / 60 | +0 | 2026-11-04 | 通过 MCP/A2A 暴露广告库存，支持媒体购买与 Google Ad Manager 等广告服务器对接。 [证据](https://github.com/prebid/salesagent/blob/960f506bdd17ed71ab606667909c7b2ec0af9b50/README.md#L3-L20) | 媒体交易与供给侧参考；README 明确为 alpha，不能以协议或示例等同于生产投放验证。 |
| [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws) | 22 / 8 | +0 | 2026-11-02 | 基于 Bedrock AgentCore 的广告多 Agent 方案，覆盖媒体规划、受众、竞价优化与发布商变现。 [证据](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8/README.md#L82-L95) | 广告专用参考架构。含演示数据与演示 UI，不是已验证的真实账户优化服务。 |
| [Synter-Media-AI/mcp-server](https://github.com/Synter-Media-AI/mcp-server) | 21 / 4 | +0 | 2026-11-03 | 广告报表、账户/Campaign 操作、预算和写后读回；README 区分托管 30+ 平台声明与本地表列 16 平台。 [证据](https://github.com/Synter-Media-AI/mcp-server/blob/73292595ea013e4de5025c9a8b73c53dc5919792/README.md#L168-L203) | 平台覆盖和 Verified 字样均为项目方声明；各平台写入深度不同。写入默认开启，可选只读，客户端确认取决于配置。 |
| [ynnickw/adport](https://github.com/ynnickw/adport) | 15 / 8 | +0 | 2026-11-04 | 11 个广告 Provider 的 CLI/MCP 控制面，含效果报表、审计及先预览后批准的写入。 [证据](https://github.com/ynnickw/adport/blob/cf5b8586568393e036cc0e4a31021cdb3b5f7dd9/README.md#L62-L93) | 统一广告模型与策略约束参考。README 自述实现/合同测试不证明各平台全部操作已获批并真实执行。 |

## 本次新增收录的广告能力

**Claude Ads：广告账户诊断与优化草稿。** [命令表](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L41-L46)提供审计、渠道/预算规划、素材、监测和草稿优化；[能力清单](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/control-plane/manifests/capability-manifest.json)默认只读，12 个平台的 `account-mutation` 均为 disabled。Amazon 原生导出标准化和账户健康评分也未启用，不能把平台名称清单解释为全部能力均已实现。适合把广告证据、诊断、未检查项和变更草稿一起交给投放运营审阅。项目方标注只有 Claude Code 经运行验证，本文未复测。

**AuctionNet：广告竞价策略研究。** [广告拍卖基准介绍](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md#L14-L20)明确面向广告竞价；[策略对象](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/simul_bidding_env/strategy/base_bidding_strategy.py#L9-L21)包含预算和 CPA 约束，[IQL 策略](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/simul_bidding_env/strategy/iql_bidding_strategy.py#L99-L104)将模型结果转换为竞价。对 adsWithAi 的价值是比较和训练预算约束下的出价策略；它属于仿真基础设施，[测试入口](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/run/run_test.py#L103-L108)运行的是竞价模拟，不能视为真实 DSP 或广告平台连接器。README 的 Diffbid 标为待实现，最近推送为 2025-04-25。

**Creative Ad Agent：供投放测试的广告图片。** [广告工作流](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md#L38-L43)从品牌网页研究进入 Hook、视觉提示和图片生成；[图片工具](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/server/lib/nano-banana-mcp.ts#L100-L112)有具体的广告图片生成接口。适合批量准备概念与素材变体，但返回图片不等于发布广告或完成线上 A/B 测试。源码依赖外部模型与 fal.ai，本文未验证运行时兼容性，也不采信未独立验证的转化提升宣传。

## 本期变化的具体含义

### Google Ads MCP：读取之外，新增资产与标签操作

[README](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/README.md#L14-L36) 列出 `create_asset`、`upload_video_asset`、`manage_labels` 和 `manage_label_associations`。相对上期固定提交的 [10 个新增提交](https://github.com/googleads/google-ads-mcp/compare/9a78cbdceebae71a6bc8483bdec333695834ef9c...7452a9d49e3d350403f2610cd7125c60f6d05264)包含这些工具和两阶段调用辅助函数；本文同时阅读了实现文件。

- [资产创建实现](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/ads_mcp/tools/create_asset.py#L241-L314)支持文字、图片、YouTube 视频引用、附加链接等资产；图片本地路径仅适用于 stdio，远程 HTTP 使用 base64。创建资产不等于已将它投放到 Campaign。
- [视频上传实现](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/ads_mcp/tools/upload_video.py#L53-L99)采用后台任务，当前限本地 stdio；广告平台权限、格式和处理结果仍需独立验证。
- 默认调用 `validate_only=True`，返回 `change_items` 与绑定客户/参数的 checksum；确认时使用相同参数和 checksum。[校验与执行代码](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/ads_mcp/propose_and_confirm.py#L265-L325)体现了参数绑定，文档另要求用户明示批准。**checksum 本身并不构成独立的人工审批凭证**，集成方仍需落实审批动作。
- [默认工具配置](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/ads_mcp/tools_config.yaml)开启 assets/labels；严格只读部署需按 README 关闭两类工具。不能继续笼统地把当前默认分支称为“纯只读”，也不能外推为支持全部预算或竞价操作。

对 adsWithAi 的价值是把“素材准备 → 审核 → 广告平台资产入库”接起来，并用标签追踪素材版本。以上是可参考的集成设计，不是本仓库已实现或已测试的业务功能。

### AdCraft：聚焦广告脚本和创意方法的迭代

[当前脚本 Skill](https://github.com/GML-MMGroup/AdCraft/blob/6e8cfdb7d958aca150b73979a82e6e928d135d1a/apps/api/agent/skills/video_agent_script_authoring/SKILL.md#L1-L15)明确要求按已批准的广告构思保留产品角色、时长和文案，并避免编造产品主张；[创意策略 Skill](https://github.com/GML-MMGroup/AdCraft/blob/6e8cfdb7d958aca150b73979a82e6e928d135d1a/apps/api/agent/skills/brand_agent_creative_strategy/SKILL.md#L7-L48)约束了从方法目录提出候选、推荐与用户确认的职责。与上期的 [固定提交差异](https://github.com/GML-MMGroup/AdCraft/compare/0e6317d618a9d2065b3b6639c91b5119c1563e92...6e8cfdb7d958aca150b73979a82e6e928d135d1a)可核对这些文件的修改。适合借鉴广告素材批次和版本设计；本次未生成样片，不能把提示词调整解释为已经改善 CTR、CVR 或转化。

### 低热度项目：区分产品声明与已核验变化

- **Synter：** [本期 1 个提交](https://github.com/Synter-Media-AI/mcp-server/compare/6ed95d885030a218d675e3177b6e1f7732f124d2...73292595ea013e4de5025c9a8b73c53dc5919792)主要修改 README、发现元数据与客户端接入文件。托管“30+”与本地枚举表列 16 平台是不同范围，不能据此次文案变化声称新增了等量连接器实现。写入默认开启，只读为可选模式；人工确认行为由客户端配置决定。
- **Prebid：** [本期 2 个提交](https://github.com/prebid/salesagent/compare/1c202df28c6715bd00fb638197fe5bc08fb163d3...960f506bdd17ed71ab606667909c7b2ec0af9b50)涉及依赖更新与测试日期维护；[广告库存购买定位和 alpha 状态](https://github.com/prebid/salesagent/blob/960f506bdd17ed71ab606667909c7b2ec0af9b50/README.md#L3-L21)仍是其直接广告证据。此次没有依据宣称新增广告交易能力。
- **AWS Guidance：** [本期 3 个提交](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/compare/13239f178ad8ea749fbdc258300f7141ef9ec306...e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8)包含模型配置调整和合成品牌安全数据；[方案介绍](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8/README.md#L80-L101)覆盖媒体规划、受众与竞价工作流。它仍应作为参考架构和演示评估。
- **Adport：** [本期 27 个提交](https://github.com/ynnickw/adport/compare/f6515a3ac94b185941ef9bb31e32d59f563bef11...cf5b8586568393e036cc0e4a31021cdb3b5f7dd9)包含组织/项目授权、受控操作审阅与素材预览相关改动。README 的[先预览再确认规则](https://github.com/ynnickw/adport/blob/cf5b8586568393e036cc0e4a31021cdb3b5f7dd9/README.md#L81-L93)仍有效；只阅读选定静态文件，未验证 Cloud 或任一真实广告平台的写入。比较 API 返回的文件清单达 300 条上限，不据此声称审阅了全部改动。

## 检索与验证边界

- 本次刷新上期 19 个入选项目，并使用 GitHub 公开搜索补充候选；入选均回到项目方 README、具体组件或广告工具实现核验。搜索条件及结果数量保留在[快照](../sources/2026-11-04-github-snapshot.json)，不发布无关项目列表。
- 通用网页搜索也已尝试，但返回噪声、JavaScript 中间页或验证码，未采用其摘要作为证据；有效研究范围主要是 GitHub 公开 API、项目方仓库与官方站点交叉核对，不声称穷尽全网。
- 所有功能证据固定到本次观察的默认分支提交，并保留文件 Git blob SHA 与 SHA-256。同时包含泛营销能力的 Skills 仓库只按明确的广告专用组件收录，其泛营销部分不在推荐范围内。
- 没有安装或运行候选项目，没有授权广告账户、创建 Campaign、修改预算或执行真实投放。文档声明、选定源码核验与真实账户验证是不同证据层级；兼容性、输出质量和投放收益未验证。
- 若后续无合适项目，应明确记录无合适项目，不用通用 Agent、普通 AI 工具或没有广告能力的泛营销项目补足数量。
