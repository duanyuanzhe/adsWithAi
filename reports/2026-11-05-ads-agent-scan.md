# 广告投放 Agent / AI 项目日报：2026-11-05

> 整理时间：2026-11-05 12:38:30（Asia/Shanghai）。
> GitHub 元数据采集窗口：2026-11-05 10:13:13 — 2026-11-05 12:31:31（Asia/Shanghai）；逐项 UTC 时间及固定提交见[数据快照](../sources/2026-11-05-github-snapshot.json)。
> 严格限定直接服务广告投放的项目；主表门槛为 100 Stars，是本日报的分层规则，不代表行业标准或生产成熟度。

## 本期结果

本期主表 **22 项**、低热度专项观察 **4 项**，合计 **26 项**。刷新上期全部 22 项，首次收录 **4 项**：Soku CLI、SMB AdTech Platform、Amazon Ads 搜索词分析组件和 Adspirer Ads MCP。“首次收录”不表示今天发布；只按直接广告能力纳入，不推送同仓库的非广告部分。

- **关注度最高的已收录项仍是 Claude Ads。** [广告审计 Skills](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L10-L46)为 10,749 Stars，较上期 +22；当前默认分支和 README 均未变化，其账户写入禁用边界仍成立。
- **本次新增项补充业务环节。** Soku CLI（301 Stars）提供广告报表与待审批操作的客户端；Amazon Skills（249 Stars）只推荐其广告搜索词报告分析；Adspirer（106 Stars）为托管多平台广告 MCP 接入。SMB 原型（471 Stars）可作竞价/归因学习材料，需明确未训练模型的降级行为。
- **AdCraft 与 Adport 有可核对的提交变化。** AdCraft 当前 601 Stars（+6），[42 个新增提交](https://github.com/GML-MMGroup/AdCraft/compare/6e8cfdb7d958aca150b73979a82e6e928d135d1a...1f7acdb170d773607a7912568bd2185f00191e42)涉及字幕、分镜进度和提示版本；Adport 当前 16 Stars（+1），[2 个新增提交](https://github.com/ynnickw/adport/compare/cf5b8586568393e036cc0e4a31021cdb3b5f7dd9...84a27097b28172005cca4a09a10d324a2970fa61)涉及按日报表与紧凑组件。本文只核验选定源码，未验证界面或真实投放效果。
- **推送时间不代表新增功能。** Paid Media Agent 的 `pushed_at` 变为 2026-11-04 23:29:19 UTC，但默认分支仍是上期同一提交，因此不把它写成一次已发布的功能升级。

## 热度和比较口径

1. Stars / Forks 是本次 GitHub API 观察值，两张表内分别按 Stars 降序；不等同于用户数、广告花费、生产可用性、ROAS 或今日增长率。
2. “Stars 较上期”以[11 月 4 日固定提交快照](https://github.com/duanyuanzhe/adsWithAi/blob/5acf65cadcc032cb63af839e24dd10cb6787f958/sources/2026-11-04-github-snapshot.json)逐项相减，对已跟踪项目的观察间隔约 **12.7–12.8 小时**，**不是完整 24 小时增长**。首次收录项没有相同基线，不补造增量。Forks 变化也保留在 JSON 中。
3. `pushed_at` 可以来自其他分支。默认分支有无变化使用提交 SHA 判断，变化说明另链接对应 compare；比较所得提交数量不代表新功能数量。
4. 上期 [PR #2](https://github.com/duanyuanzhe/adsWithAi/pull/2) 及更早 [PR #1](https://github.com/duanyuanzhe/adsWithAi/pull/1) 在本期检查时仍为 OPEN。本期从 `main` 独立创建，不重复打包待合并的旧报告；比较引用固定提交。

## 100 Stars 以上的广告相关项目

| 项目 | Stars / Forks | Stars 较上期 | 最近推送 UTC | 直接广告能力与证据 | 广告投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [AgriciDaniel/claude-ads](https://github.com/AgriciDaniel/claude-ads) | 10,749 / 1,563 | +22 | 2026-11-01 | 广告专用审计与优化 Skills：12 平台广告数据/导出分析、预算与渠道方案、投放节奏监测、广告素材 Brief、草稿优化。 [证据](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L10-L12) | 用于投放诊断与变更前审阅。清单内 12 平台账户写入均禁用；Amazon 原生导出标准化与账户健康评分也禁用。仅 Claude Code 获项目方运行验证，本文未复测。 |
| [irinabuht12-oss/google-ads-meta-ads-mcp](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp) | 6,983 / 373 | +31 | 2026-10-27 | 托管 Google/Meta 广告账户、Campaign、预算、受众、素材与效果分析入口；功能范围为 README 声明。 [证据](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md#L117-L145) | 托管服务接入仓库。当前完整树 24 个文件中未见服务端实现；Stars 反映公开关注度，不能视为完整自托管代码或服务效果。 |
| [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp) | 1,350 / 282 | +0 | 2026-10-20 | Meta Campaign/Ad Set/Ad 管理、预算、定向、素材上传和效果分析。 [证据](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md#L175-L188) | 适合 Meta 执行连接器。仓库含 Python 实现；托管服务的五平台与工具总数不能直接算作本仓库覆盖。 |
| [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) | 1,118 / 350 | +1 | 2026-11-02 | GAQL 账户读取、广告资产创建、本地视频上传、标签和标签关联管理；写入采用 Propose & Confirm。 [证据](https://github.com/googleads/google-ads-mcp/blob/7452a9d49e3d350403f2610cd7125c60f6d05264/README.md#L14-L36) | 资产/标签写入已在上期记录，不能推断已支持预算或竞价修改。远程图片用 base64；视频上传仅本地 stdio。文档要求人工确认，checksum 校验本身不是独立审批凭证。 |
| [realkimbarrett/advertising-skills](https://github.com/realkimbarrett/advertising-skills) | 772 / 68 | +0 | 2026-03-26 | 仅收录广告创意组件：前三秒 Hook/画面/脚本构思，以及广告角度与 Hook 变体生成。 [证据](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/README.md#L42-L51) | 广告素材提示词资产；不推荐其中的邮件、落地页等泛营销部分。没有广告账户执行能力。 |
| [cohnen/mcp-google-ads](https://github.com/cohnen/mcp-google-ads) | 718 / 158 | +0 | 2025-10-16 | 通过 MCP 分析 Google Ads Campaign、广告、关键词、预算消耗与竞价策略数据。 [证据](https://github.com/cohnen/mcp-google-ads/blob/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a/README.md#L7-L35) | 适合只读分析接入比较；最近推送为 2025-10-16，采纳前需核对当前依赖与 API 兼容性。 |
| [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft) | 601 / 75 | +6 | 2026-11-04 | 面向广告视频的 Agent 工作流：创意、脚本、产品视觉、分镜、视频与最终合成。 [证据](https://github.com/GML-MMGroup/AdCraft/blob/1f7acdb170d773607a7912568bd2185f00191e42/README.md#L71-L113) | 广告视频生产实现；本期默认分支新增 42 个提交，涉及字幕控制、分镜进度与提示修订。选定源码核验，未生成样片或验证投放收益。 |
| [poseljacob/agentic-video-editor](https://github.com/poseljacob/agentic-video-editor) | 507 / 62 | +0 | 2026-04-14 | 以原始素材与创意 Brief 生成广告剪辑；包含 UGC 广告管线、DTC 风格及导演/剪辑/审片反馈循环。 [证据](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md#L104-L130) | 适合短视频广告素材迭代。CLI 是文档推荐路径，Web UI 标明 pre-alpha；不负责账户投放。 |
| [haoyangfeng2024/smb-adtech-platform](https://github.com/haoyangfeng2024/smb-adtech-platform) | 471 / 38 | 首次收录 | 2026-05-08 | 广告竞价与归因原型：GBM/DeepFM/GAT/PPO 出价服务、Campaign API 与多触点归因代码。 [证据](https://github.com/haoyangfeng2024/smb-adtech-platform/blob/52a00c1efb9b0a4e069c562e66f71267610d9410/README.md#L23-L58) | 适合学习竞价服务分层和降级设计。缺少模型权重时存在随机初始化或启发式路径；未证明接入真实交易所、跨媒体交付、收益、延迟或隐私合规，最近推送为 2026-05-08。 |
| [mathiaschu/meta-ads-analyzer](https://github.com/mathiaschu/meta-ads-analyzer) | 466 / 63 | +0 | 2026-02-26 | 分析 Meta Campaign/Ad Set/Ad 表现，诊断 Breakdown Effect、学习阶段、重叠、节奏与素材疲劳。 [证据](https://github.com/mathiaschu/meta-ads-analyzer/blob/9088472ddacdb89f3c5943c3db6be7b8ee25c922/README.md#L3-L14) | 广告分析 Skill；可用广告导出数据，也可配置外部 MCP 取实时数据，不能当作独立全功能执行服务器。 |
| [gomarble-ai/facebook-ads-mcp-server](https://github.com/gomarble-ai/facebook-ads-mcp-server) | 368 / 111 | +0 | 2026-08-05 | 读取 Meta 广告账户、Campaign、Ad Set、Ad、Creative 和 Insights，给 AI 提供广告数据。 [证据](https://github.com/gomarble-ai/facebook-ads-mcp-server/blob/a3b555a12dff5b888b172ef9113dd1f36d69e525/readme.md#L99-L133) | 适合广告效果分析连接器。本文不据这些读取工具推定支持创建或修改投放。 |
| [TheMattBerman/meta-ads-kit](https://github.com/TheMattBerman/meta-ads-kit) | 350 / 68 | +0 | 2026-06-10 | Meta 广告日报、素材疲劳、预算建议、广告文案、暂停/恢复及 Pixel/CAPI 检查。 [证据](https://github.com/TheMattBerman/meta-ads-kit/blob/dffa0daf6ed1e278481e9408af3be6aaf9709b28/README.md#L12-L25) | OpenClaw 广告专用工作流；上传采用 CLI-first、PAUSED/dry-run 约束，具体上传范围仍受 CLI 支持限制。 |
| [About-Intelligence/soku-cli](https://github.com/About-Intelligence/soku-cli) | 301 / 32 | 首次收录 | 2026-11-04 | 广告专用 CLI 能力：Google/Meta/TikTok 等广告报表，GAQL，自然语言 Agent 的 Campaign 与素材操作，以及待审阅变更。 [证据](https://github.com/About-Intelligence/soku-cli/blob/bdc0838a7f07c78afe37790dc3e00b6e08518465/README.md#L91-L148) | 适合把广告诊断与批准流程接入 Agent。仓库是 Soku 服务客户端，需关联账户与权限；只推荐广告相关部分，SEO/普通产品分析不在范围内。CLI 包含供人使用的 approve 命令，不代表已独立验证后端审批隔离。 |
| [zubair-trabzada/ai-ads-claude](https://github.com/zubair-trabzada/ai-ads-claude) | 285 / 99 | +0 | 2026-04-08 | 广告专用 Claude Code Skills：平台格式广告文案、视频广告脚本、关键词及预算方案。 [证据](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/README.md#L74-L103) | 优先关注 ads-copy/ads-video 素材组件；策略评分和预算预测是模型建议，没有证明可自动修改账户。 |
| [alimama-tech/AuctionNet](https://github.com/alimama-tech/AuctionNet) | 257 / 41 | +0 | 2025-04-25 | 广告拍卖与自动竞价 Agent 基准：仿真环境、数据轨迹、强化学习、在线线性规划及 Decision Transformer 策略。 [证据](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md#L14-L20) | 适合预算/CPA 约束下的离线竞价策略比较。属于仿真和训练，不能直接执行广告账户投放；Diffbid 待实现，最近推送为 2025-04-25。 |
| [zach22-1999/amazon-skills](https://github.com/zach22-1999/amazon-skills) | 249 / 52 | 首次收录 | 2026-10-15 | 仅收录 zach-search-term-report-analyzer：Amazon Ads SP/SB/SD 搜索词报告清洗、7/14/30 天指标、AI 词根分类及否词/控成本/放量建议。 [证据](https://github.com/zach22-1999/amazon-skills/blob/db1f7d108eb8c43b6de36c6a3e230ebff107e227/README.md#L61-L68) | 适合给投放人员生成可复核的搜索词决策清单；输出建议而不自动改预算、bid 或否词。需本地报表和完整分类；仓库的选品、Listing 等其他能力不在本次推荐范围。 |
| [TheMattBerman/google-ads-copilot](https://github.com/TheMattBerman/google-ads-copilot) | 241 / 47 | +0 | 2026-06-10 | 读取账户或 CSV，形成可审核草稿；文档列出否定关键词、暂停关键词/广告组、日预算调整的受控 Apply。 [证据](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md#L19-L29) | 适合 Read → Draft → Apply 设计；应以列明的写入范围评估，不能推定覆盖全部 Google Ads 操作。 |
| [brijr/meta-mcp](https://github.com/brijr/meta-mcp) | 201 / 75 | +0 | 2026-05-28 | Cloudflare Workers 上的 Meta 广告账户设置、Campaign、Ad Set、素材、受众与报表工具。 [证据](https://github.com/brijr/meta-mcp/blob/664b20617a6aee529ff31f8093e85fca7db4b7be/README.md#L73-L82) | 适合 Meta OAuth、工具组织和部署模型比较；与 Pipeboard 是不同实现。 |
| [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) | 146 / 47 | +0 | 2026-08-05 | Google Ads OAuth、GAQL 广告数据查询与关键词研究，供 AI 客户端调用。 [证据](https://github.com/gomarble-ai/google-ads-mcp-server/blob/4f922abc8f9932a5080052a222a5edb86d7a3697/README.md#L27-L35) | 适合 Google Ads 数据接入备选；文档的 account management 不足以证明全部 Campaign 写入。 |
| [DV0x/creative-ad-agent](https://github.com/DV0x/creative-ad-agent) | 127 / 28 | +0 | 2026-09-06 | 广告专用素材 Agent：品牌网页事实研究 → Hook → 视觉提示 → AI 图片，输出多广告概念与素材变体。 [证据](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md#L1-L3) | 适合为投放测试准备图片素材。依赖外部模型/图片服务；未证明发布广告、控制预算或读取真实 A/B 结果，也未验证转化提升。 |
| [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent) | 117 / 24 | +0 | 2026-11-04 | 跨渠道广告消耗、转化、CPL、预算节奏分析及报告，准备带原因和检查计划的 Campaign 变更。 [证据](https://github.com/langchain-ai/paid-media-agent/blob/c81f9950cd56449a770a9a9e5e9e0a3fad54c382/README.md#L27-L54) | 适合投放分析到审核的业务闭环。真实账户变更默认关闭，需写入策略、发布检查与授权审核。 |
| [amekala/ads-mcp](https://github.com/amekala/ads-mcp) | 106 / 23 | 首次收录 | 2026-11-03 | Adspirer 托管广告 MCP：Campaign 创建、关键词研究、预算/效果分析及 Google、Meta、Amazon、LinkedIn、TikTok 等广告工作流。 [证据](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/README.md#L44-L73) | README 声称 6 平台和 400+ 工具；注册文件指向远程 MCP，仓库主要为插件/Skills/示例，未见完整后端服务。创建默认暂停为项目方声明，平台覆盖、审批和真实写入均未实测。 |

## 低热度专项观察

以下四项都直接关联广告业务，但未达到主表门槛，**不描述为热门项目**；保留其协议、架构或控制流程的差异作为观察。

| 项目 | Stars / Forks | Stars 较上期 | 最近推送 UTC | 直接广告能力与证据 | 广告投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [prebid/salesagent](https://github.com/prebid/salesagent) | 39 / 60 | +0 | 2026-11-04 | 通过 MCP/A2A 暴露广告库存，支持媒体购买与 Google Ad Manager 等广告服务器对接。 [证据](https://github.com/prebid/salesagent/blob/960f506bdd17ed71ab606667909c7b2ec0af9b50/README.md#L3-L20) | 媒体交易与供给侧参考；README 明确为 alpha，不能以协议或示例等同于生产投放验证。 |
| [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws) | 22 / 8 | +0 | 2026-11-02 | 基于 Bedrock AgentCore 的广告多 Agent 方案，覆盖媒体规划、受众、竞价优化与发布商变现。 [证据](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8/README.md#L82-L95) | 广告专用参考架构。含演示数据与演示 UI，不是已验证的真实账户优化服务。 |
| [Synter-Media-AI/mcp-server](https://github.com/Synter-Media-AI/mcp-server) | 21 / 4 | +0 | 2026-11-03 | 广告报表、账户/Campaign 操作、预算和写后读回；README 区分托管 30+ 平台声明与本地表列 16 平台。 [证据](https://github.com/Synter-Media-AI/mcp-server/blob/73292595ea013e4de5025c9a8b73c53dc5919792/README.md#L168-L203) | 平台覆盖和 Verified 字样均为项目方声明；各平台写入深度不同。写入默认开启，可选只读，客户端确认取决于配置。 |
| [ynnickw/adport](https://github.com/ynnickw/adport) | 16 / 8 | +1 | 2026-11-04 | 11 个广告 Provider 的 CLI/MCP 控制面，含效果报表、审计及先预览后批准的写入。 [证据](https://github.com/ynnickw/adport/blob/84a27097b28172005cca4a09a10d324a2970fa61/README.md#L62-L93) | 统一广告模型与策略约束参考。README 自述实现/合同测试不证明各平台全部操作已获批并真实执行。 |

## 首次收录项目的应用价值

### Soku CLI：广告数据与待审批变更

[广告文档](https://github.com/About-Intelligence/soku-cli/blob/bdc0838a7f07c78afe37790dc3e00b6e08518465/README.md#L91-L148)展示广告账户枚举、Campaign 维度查询、GAQL 及 Meta Campaign 创建后检查 review 的流程。[广告命令实现](https://github.com/About-Intelligence/soku-cli/blob/bdc0838a7f07c78afe37790dc3e00b6e08518465/src/commands/ads.ts#L139-L154)将广告操作送往服务端动作接口，[审批命令实现](https://github.com/About-Intelligence/soku-cli/blob/bdc0838a7f07c78afe37790dc3e00b6e08518465/src/commands/review.ts#L256-L267)仍包含供人操作的 approve 命令；项目方要求 Agent 将 `approve_url` 交给用户，不能仅凭 CLI 文案认定完成了独立审批验证。

对广告运营的价值是保留结构化查询和待审变更，减少手工搬运数据。它依赖 Soku 账户、广告授权和远端服务，不能把公开 CLI 视为完整自托管平台；只收录广告数据与执行部分，SEO、普通内容发布和产品分析不纳入。已只读访问[官方 Agent 使用指南](https://soku.ai/cli/skill.md)交叉核对，未执行安装或登录步骤。

### Amazon Skills：只推荐广告搜索词报告组件

[组件介绍](https://github.com/zach22-1999/amazon-skills/blob/db1f7d108eb8c43b6de36c6a3e230ebff107e227/skills/zach-search-term-report-analyzer/README.md#L5-L15)直接面向 Amazon Ads SP/SB/SD：先确定性清洗和聚合 7/14/30 天指标，再由 AI 或人完成词根级分类，最后生成决策清单。已查看当前 Stage A / Stage C 源码；旧版脚本在 README 标为过渡入口，不用它代替当前流程。

其价值在于为否词、成本控制、放量和 Listing 反馈提供可复核依据；[输出与边界](https://github.com/zach22-1999/amazon-skills/blob/db1f7d108eb8c43b6de36c6a3e230ebff107e227/skills/zach-search-term-report-analyzer/README.md#L84-L116)说明只输出建议，不自动改预算、bid 或否词，缺订单/销售额时不伪造转化结论。它需要用户自己的报表和完整分类，本次没有输入真实店铺数据，也不推荐同仓库的非广告选品与普通 Listing 功能。

### Adspirer Ads MCP：托管广告服务接入

[平台表与功能](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/README.md#L44-L73)声明广告 Campaign、关键词、预算与效果分析；[服务注册文件](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/server.json#L1-L21)直接指向远程 MCP，[TikTok 专用 Skill](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/shared/skills/platform/adspirer-tiktok-ads/SKILL.md#L66-L78)说明广告构建次序及创建默认暂停。仓库树可见插件、Skills、安装与示例文件，本次未见完整服务端实现。

适合作为多平台广告工具接口与投放工作流的研究候选。README 的“6 平台 / 400+ 工具”是项目方服务覆盖声明，不等于本次验证了对应权限、接口、审批或真实写入。[官网接入文档](https://www.adspirer.com/docs/add-to-your-agent)在读取时还提示 ChatGPT 插件有问题，可改用自定义 MCP；本文仅记录这一文档状态，不声称已复现故障或完成可用性测试。

### SMB AdTech Platform：竞价与归因原型

[广告竞价定位](https://github.com/haoyangfeng2024/smb-adtech-platform/blob/52a00c1efb9b0a4e069c562e66f71267610d9410/README.md#L23-L58)明确面向程序化广告；代码有竞价服务、Campaign API 与多触点归因。[模型加载逻辑](https://github.com/haoyangfeng2024/smb-adtech-platform/blob/52a00c1efb9b0a4e069c562e66f71267610d9410/api/services/bidding_service.py#L117-L145)在缺少权重时会使用未拟合 GBM 或随机初始化 DeepFM，因此不能把生成一个数值视为有效的投放策略。归因代码提供多触点模型，也不自动证明归因准确或隐私合规。

适合比较 GBM、深度模型与启发式降级的接口分层。本文未接入广告交易所、训练模型或验证真实跨媒体交付，不采用 README 的收益、延迟、覆盖规模或合规宣传作为已验证结论；其最近推送为 2026-05-08，应按原型资料评估。

## 已跟踪项目的变化

- **AdCraft：** 本期 compare 为 42 个新增提交、93 个变化文件。[字幕控制代码](https://github.com/GML-MMGroup/AdCraft/blob/1f7acdb170d773607a7912568bd2185f00191e42/apps/api/app/services/agent_canvas_video_subtitles.py#L1-L26)把保存的字幕选项转为交付提示，代码默认值为开启；另外可见分镜进度和提示修订相关文件变化。可参考广告素材字幕与版本控制设计，本次未运行视频提供方或核验生成结果。
- **Adport：** 本期 2 个新增提交、37 个变化文件。[按日日期拆分](https://github.com/ynnickw/adport/blob/84a27097b28172005cca4a09a10d324a2970fa61/packages/core/src/report-dates.ts#L1-L20)将 daily 报表拆为逐日查询，单次最多 31 天；另有紧凑趋势与品牌展示组件变化。其价值是避免把周期总量误当逐日数据，仍需独立检查账户时区、币种与归因口径。
- **其余 20 项：** 本次默认分支提交与上期相同，未据此宣称功能新增。Google 官方 Ads MCP 的资产/标签写入是上期已记录的范围；Claude Ads 的禁写、AuctionNet 的仿真性质与 Ryze 的托管入口边界继续保留。

## 检索与验证范围

- 使用 8 个 GitHub 搜索表达式，覆盖广告 Agent、AI、TikTok MCP、Amazon Ads、广告素材、归因和竞价，并刷新上期 22 项。搜索条件、结果数量和入选命中写入[快照](../sources/2026-11-05-github-snapshot.json)；未发布无关搜索条目，不声称穷尽全网。
- 另尝试公开网页检索：Bing 返回不相关结果，Brave 返回 429。有效功能证据来自项目方固定提交下的 README、组件源码以及选定官网；搜索摘要不作入选证据。
- 所有入选项有直接广告用途证据；托管客户端、Skill、研究原型和可部署连接器分别说明边界。100 Stars 只是报告筛选层级，不把低热度观察凑入热门名单。
- 本次没有安装或执行候选项目，没有登录或授权广告账户、创建 Campaign、修改预算或测试真实广告。静态实现不等于权限、端到端可用性、素材质量或投放效果验证。
- 后续无合适项目时明确记录无合适项目，不以通用 Agent、普通 AI 或无广告能力的泛营销工具补足数量。
