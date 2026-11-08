# 广告投放 Agent / AI 项目日报 · 2026-11-08

本期首次收录 **4 项**，刷新此前 **26 项**；合计 **26 项 ≥100 Stars 的主表项目**和 **4 项低热度观察**。只纳入第一方资料明确支持广告投放的组件。首次收录不代表新项目或当天发布；所有项目均未做真实账户或投放效果验证。

GitHub 热度观察时间：**2026-11-08 10:04:22–2026-11-08 10:04:59（Asia/Shanghai）**；原始观察时间、Forks 差值、固定源码 SHA、文件校验值见[数据快照](../sources/2026-11-08-github-snapshot.json)。热度来自各仓库 REST API 的 `stargazers_count` / `forks_count`，Stars/Forks 仅作为公开关注度代理。

比较基线为 [2026-11-05 已验证报告](https://github.com/duanyuanzhe/adsWithAi/blob/bff88639cbaa350f242842fcc05985f0ba890e4b/reports/2026-11-05-ads-agent-scan.md)，各项目间隔 **69.5–71.9 小时**，约三天，不能写成 24 小时增长。11 月 6 日与 7 日无已核验的交付物，本期不补写历史结果。四项首次收录没有历史基线。

## 本期值得关注

- **预算与广告测量：** 新增 Meridian（1,595 Stars）和 Robyn（1,534 Stars），仅推荐广告预算/频次与付费渠道分配组件。两者提供模型建议，本文未证明其能直接修改广告账户。
- **广告商品与视频素材：** 新增 FeedGen（268 Stars）与 ViGenAiR（243 Stars），分别针对 Shopping 广告 feed 与现有视频广告的素材变体，均有应用逻辑源码，需云服务和人工审核。
- **热度变化：** 跟踪项中 Ryze 入口 +86、Claude Ads +68、AdCraft +36 较突出；Soku 与多数项目变化较小，Adspirer -1。这些是相对 11 月 5 日的计数差，不能据此判断新增活跃用户、产品成熟度或投放收益。具体值及证据见主表。
- **实现变化：** Paid Media Agent 增加 Managed 模式只读后台助手与线程回访；Google Ads MCP 本期仅 README 变化，资产/标签写入并非本期新增。另有 Soku 清单、Prebid 定向/A2A、Synter 文档配置变化，详见下文。

## 热度主表（≥100 Stars）

按观察到的 GitHub 总 Stars 降序排列。达到热度门槛只表示可进入比较，不表示建议直接投入生产。表内“最近推送”是仓库 `pushed_at` 日期，可能包含非默认分支；功能变化依据固定 HEAD 和提交比较。

| 项目 | Stars / Forks | Stars 较 11-05 | 最近推送 UTC | 直接广告能力与证据 | 投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [AgriciDaniel/claude-ads](https://github.com/AgriciDaniel/claude-ads) | 10,817 / 1,567 | +68 | 2026-11-01 | 广告专用审计与优化 Skills：12 平台广告数据/导出分析、预算与渠道方案、投放节奏监测、广告素材 Brief、草稿优化。 [证据](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md#L10-L12) | 用于投放诊断与变更前审阅。清单内 12 平台账户写入均禁用；Amazon 原生导出标准化与账户健康评分也禁用。仅 Claude Code 获项目方运行验证，本文未复测。 |
| [irinabuht12-oss/google-ads-meta-ads-mcp](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp) | 7,069 / 372 | +86 | 2026-10-27 | 托管 Google/Meta 广告账户、Campaign、预算、受众、素材与效果分析入口；功能范围为 README 声明。 [证据](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md#L117-L145) | 托管服务接入仓库。当前完整树 24 个文件中未见服务端实现；Stars 反映公开关注度，不能视为完整自托管代码或服务效果。 |
| [google/meridian](https://github.com/google/meridian) | 1,595 / 311 | 首次收录 | 2026-11-07 | 广告预算建模库与预算优化 Skill：基于已拟合 MMM 模型，生成广告渠道预算分配、ROI/mROI 与频次方案。 [证据](https://github.com/google/meridian/blob/d90919820b788e217810d8d53ea6ba7bb563fd2f/skills/meridian_budget_optimization/SKILL.md#L1-L12) | 仅推荐广告预算/频次组件。需要已拟合模型及参数审核；人工检查点是 Skill 约定，未验证后端审批隔离。输出模型建议，未证明写入广告账户。 |
| [facebookexperimental/Robyn](https://github.com/facebookexperimental/Robyn) | 1,534 / 438 | 首次收录 | 2026-01-26 | 含机器学习的半自动 MMM：仅推荐 paid-media allocator，按渠道限制最大化响应，或按目标 ROAS/CPA 分配广告预算。 [证据](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/R/R/allocator.R#L31-L55) | 依赖有效模型与至少两个付费渠道；仅选付费广告分配组件。README 标注实验性，未验证因果准确度、真实收益或账户写入。 |
| [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp) | 1,358 / 282 | +8 | 2026-10-20 | Meta Campaign/Ad Set/Ad 管理、预算、定向、素材上传和效果分析。 [证据](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md#L175-L188) | 适合 Meta 执行连接器。仓库含 Python 实现；托管服务的五平台与工具总数不能直接算作本仓库覆盖。 |
| [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) | 1,128 / 353 | +10 | 2026-11-05 | GAQL 账户读取、广告资产创建、本地视频上传、标签和标签关联管理；写入采用 Propose & Confirm。 [证据](https://github.com/googleads/google-ads-mcp/blob/84aebf819eebc3d8dda6ee693c1bdb5fcf5d36d9/README.md#L14-L30) | 固定提交列出资产/标签写入，预算或竞价修改未获证实。开发者指南仍描述当前版本只读，与仓库口径不同；发行版实际启用范围未验证。视频上传仅本地 stdio；checksum 本身不构成独立审批凭证。 |
| [realkimbarrett/advertising-skills](https://github.com/realkimbarrett/advertising-skills) | 777 / 71 | +5 | 2026-03-26 | 仅收录广告创意组件：前三秒 Hook/画面/脚本构思，以及广告角度与 Hook 变体生成。 [证据](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/README.md#L42-L51) | 广告素材提示词资产；不推荐其中的邮件、落地页等泛营销部分。没有广告账户执行能力。 |
| [cohnen/mcp-google-ads](https://github.com/cohnen/mcp-google-ads) | 718 / 158 | +0 | 2025-10-16 | 通过 MCP 分析 Google Ads Campaign、广告、关键词、预算消耗与竞价策略数据。 [证据](https://github.com/cohnen/mcp-google-ads/blob/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a/README.md#L7-L35) | 适合只读分析接入比较；最近推送为 2025-10-16，采纳前需核对当前依赖与 API 兼容性。 |
| [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft) | 637 / 81 | +36 | 2026-11-05 | 面向广告视频的 Agent 工作流：创意、脚本、产品视觉、分镜、视频与最终合成。 [证据](https://github.com/GML-MMGroup/AdCraft/blob/1f7acdb170d773607a7912568bd2185f00191e42/README.md#L71-L113) | 广告视频生产实现，含字幕选项、分镜进度与提示修订逻辑。本期默认分支未变；仅核验选定源码，未生成样片或验证投放收益。 |
| [poseljacob/agentic-video-editor](https://github.com/poseljacob/agentic-video-editor) | 508 / 62 | +1 | 2026-04-14 | 以原始素材与创意 Brief 生成广告剪辑；包含 UGC 广告管线、DTC 风格及导演/剪辑/审片反馈循环。 [证据](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md#L104-L130) | 适合短视频广告素材迭代。CLI 是文档推荐路径，Web UI 标明 pre-alpha；不负责账户投放。 |
| [haoyangfeng2024/smb-adtech-platform](https://github.com/haoyangfeng2024/smb-adtech-platform) | 471 / 38 | +0 | 2026-05-08 | 广告竞价与归因原型：Campaign API 与多触点归因代码，另有 GBM/DeepFM/GAT/PPO 服务代码。 [证据](https://github.com/haoyangfeng2024/smb-adtech-platform/blob/52a00c1efb9b0a4e069c562e66f71267610d9410/README.md#L23-L58) | HTTP /bidding/bid 使用独立 BiddingModel/启发式引擎，未见接入四层服务；后者缺权重时有未训练/随机初始化路径。仅作学习参考，未验证真实交付、收益、延迟或隐私合规，最近推送为 2026-05-08。 |
| [mathiaschu/meta-ads-analyzer](https://github.com/mathiaschu/meta-ads-analyzer) | 467 / 63 | +1 | 2026-02-26 | 分析 Meta Campaign/Ad Set/Ad 表现，诊断 Breakdown Effect、学习阶段、重叠、节奏与素材疲劳。 [证据](https://github.com/mathiaschu/meta-ads-analyzer/blob/9088472ddacdb89f3c5943c3db6be7b8ee25c922/README.md#L3-L14) | 广告分析 Skill；可用广告导出数据，也可配置外部 MCP 取实时数据，不能当作独立全功能执行服务器。 |
| [gomarble-ai/facebook-ads-mcp-server](https://github.com/gomarble-ai/facebook-ads-mcp-server) | 369 / 112 | +1 | 2026-08-05 | 读取 Meta 广告账户、Campaign、Ad Set、Ad、Creative 和 Insights，给 AI 提供广告数据。 [证据](https://github.com/gomarble-ai/facebook-ads-mcp-server/blob/a3b555a12dff5b888b172ef9113dd1f36d69e525/readme.md#L99-L133) | 适合广告效果分析连接器。本文不据这些读取工具推定支持创建或修改投放。 |
| [TheMattBerman/meta-ads-kit](https://github.com/TheMattBerman/meta-ads-kit) | 350 / 68 | +0 | 2026-06-10 | Meta 广告日报、素材疲劳、预算建议、广告文案、暂停/恢复及 Pixel/CAPI 检查。 [证据](https://github.com/TheMattBerman/meta-ads-kit/blob/dffa0daf6ed1e278481e9408af3be6aaf9709b28/README.md#L12-L25) | OpenClaw 广告专用工作流；上传采用 CLI-first、PAUSED/dry-run 约束，具体上传范围仍受 CLI 支持限制。 |
| [About-Intelligence/soku-cli](https://github.com/About-Intelligence/soku-cli) | 301 / 31 | +0 | 2026-11-06 | 广告专用 CLI：Google/Meta/TikTok 等广告报表、GAQL、Campaign 与素材操作；写入受 review 与用户预设自动批准策略控制。 [证据](https://github.com/About-Intelligence/soku-cli/blob/125cb25fbdc2659c1088f7a3d657beaa54d7c60c/README.md#L91-L148) | Soku 服务客户端，仅推荐广告部分。写入通常待审；用户预设 Always approve 时可提交即执行，require_human 可强制待审。CLI 含人工 approve 命令，后端审批隔离未独立验证。 |
| [zubair-trabzada/ai-ads-claude](https://github.com/zubair-trabzada/ai-ads-claude) | 285 / 99 | +0 | 2026-04-08 | 广告专用 Claude Code Skills：平台格式广告文案、视频广告脚本、关键词及预算方案。 [证据](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/README.md#L74-L103) | 优先关注 ads-copy/ads-video 素材组件；策略评分和预算预测是模型建议，没有证明可自动修改账户。 |
| [google-marketing-solutions/feedgen](https://github.com/google-marketing-solutions/feedgen) | 268 / 43 | 首次收录 | 2026-11-04 | Shopping 广告商品 feed：用生成式 AI 改进标题、描述和缺失属性，产出 Merchant Center supplemental feed。 [证据](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/README.md#L93-L115) | 只推荐 Shopping 广告用途；Apps Script 应用依赖 Vertex AI。项目标为非官方 Google 产品，建议人工审核及约 30k 商品上限；旧模型/部署兼容性未实测。 |
| [alimama-tech/AuctionNet](https://github.com/alimama-tech/AuctionNet) | 257 / 41 | +0 | 2025-04-25 | 广告拍卖与自动竞价 Agent 基准：仿真环境、数据轨迹、强化学习、在线线性规划及 Decision Transformer 策略。 [证据](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md#L14-L20) | 适合预算/CPA 约束下的离线竞价策略比较。属于仿真和训练，不能直接执行广告账户投放；Diffbid 待实现，最近推送为 2025-04-25。 |
| [zach22-1999/amazon-skills](https://github.com/zach22-1999/amazon-skills) | 254 / 52 | +5 | 2026-10-15 | 仅收录 zach-search-term-report-analyzer：Amazon Ads SP/SB/SD 搜索词报告清洗、7/14/30 天指标、AI 词根分类及否词/控成本/放量建议。 [证据](https://github.com/zach22-1999/amazon-skills/blob/db1f7d108eb8c43b6de36c6a3e230ebff107e227/skills/zach-search-term-report-analyzer/README.md#L5-L15) | 只输出建议，不自动改预算、bid 或否词；需本地报表与完整分类。README 的缺失数据保证未获实现完全支持：品牌词/竞品词有缺订单按 0 单处理的静态分支，需人工复核。其他选品和普通 Listing 能力不推荐。 |
| [google-marketing-solutions/vigenair](https://github.com/google-marketing-solutions/vigenair) | 243 / 77 | 首次收录 | 2026-10-15 | 广告视频创意应用：用 Gemini 分析现有 Video Ad，重剪为较短广告与不同画幅/故事线变体，含渲染调用实现。 [证据](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/README.md#L190-L205) | 依赖 GCP/Vertex AI；项目标为非官方 Google 产品。片段/时长可能偏离提示，裁剪不能自动调整文字覆盖层；需要人工审片与上传，未证明自动发布 Campaign。 |
| [TheMattBerman/google-ads-copilot](https://github.com/TheMattBerman/google-ads-copilot) | 241 / 47 | +0 | 2026-06-10 | 读取账户或 CSV，形成可审核草稿；文档列出否定关键词、暂停关键词/广告组、日预算调整的受控 Apply。 [证据](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md#L19-L29) | 适合 Read → Draft → Apply 设计；应以列明的写入范围评估，不能推定覆盖全部 Google Ads 操作。 |
| [brijr/meta-mcp](https://github.com/brijr/meta-mcp) | 202 / 75 | +1 | 2026-05-28 | Cloudflare Workers 上的 Meta 广告账户设置、Campaign、Ad Set、素材、受众与报表工具。 [证据](https://github.com/brijr/meta-mcp/blob/664b20617a6aee529ff31f8093e85fca7db4b7be/README.md#L73-L82) | 适合 Meta OAuth、工具组织和部署模型比较；与 Pipeboard 是不同实现。 |
| [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) | 147 / 47 | +1 | 2026-08-05 | Google Ads OAuth、GAQL 广告数据查询与关键词研究，供 AI 客户端调用。 [证据](https://github.com/gomarble-ai/google-ads-mcp-server/blob/4f922abc8f9932a5080052a222a5edb86d7a3697/README.md#L27-L35) | 适合 Google Ads 数据接入备选；文档的 account management 不足以证明全部 Campaign 写入。 |
| [DV0x/creative-ad-agent](https://github.com/DV0x/creative-ad-agent) | 129 / 28 | +2 | 2026-09-06 | 广告专用素材 Agent：品牌网页事实研究 → Hook → 视觉提示 → AI 图片，输出多广告概念与素材变体。 [证据](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md#L1-L3) | 适合为投放测试准备图片素材。依赖外部模型/图片服务；未证明发布广告、控制预算或读取真实 A/B 结果，也未验证转化提升。 |
| [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent) | 120 / 24 | +3 | 2026-11-08 | 跨渠道广告消耗、转化、CPL 与预算节奏分析、报告及变更提案；Managed Deep Agents 模式可运行只读后台助手与一次性线程回访。 [证据](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/README.md#L106-L116) | 适合投放分析到审核的闭环。写入默认关闭，需精确提案审批、单次执行及读回；后台助手/回访仅 Managed 模式。文档与选定代码已读，未验证部署或真实投放。 |
| [amekala/ads-mcp](https://github.com/amekala/ads-mcp) | 105 / 23 | -1 | 2026-11-03 | Adspirer 托管广告 MCP：Campaign 创建、关键词研究、预算/效果分析及 Google、Meta、Amazon、LinkedIn、TikTok 等广告工作流。 [证据](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/README.md#L44-L73) | README 声称 6 平台和 400+ 工具；注册文件指向远程 MCP，仓库主要为插件/Skills/示例，未见完整后端服务。创建默认暂停为项目方声明，平台覆盖、审批和真实写入均未实测。 |

## 低热度观察（不计入热门项目）

沿用有直接广告证据的观察池，单独列示；本次没有为补足数量增加低热度线索。

| 项目 | Stars / Forks | Stars 较 11-05 | 最近推送 UTC | 直接广告能力与证据 | 投放价值与验证边界 |
|---|---:|---:|---|---|---|
| [prebid/salesagent](https://github.com/prebid/salesagent) | 39 / 60 | +0 | 2026-11-07 | 通过 MCP/A2A 暴露广告库存，支持媒体购买与 Google Ad Manager 等广告服务器对接。 [证据](https://github.com/prebid/salesagent/blob/a7a4c53f8f3dd22dee0ff90c30b5db4185da4a27/README.md#L3-L20) | 媒体交易与供给侧参考；README 明确为 alpha，不能以协议或示例等同于生产投放验证。 |
| [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws) | 22 / 8 | +0 | 2026-11-06 | 基于 Bedrock AgentCore 的广告多 Agent 方案，覆盖媒体规划、受众、竞价优化与发布商变现。 [证据](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8/README.md#L82-L95) | 广告专用参考架构。含演示数据与演示 UI，不是已验证的真实账户优化服务。 |
| [Synter-Media-AI/mcp-server](https://github.com/Synter-Media-AI/mcp-server) | 21 / 4 | +0 | 2026-11-07 | 广告报表、账户/Campaign 操作、预算和写后读回；README 区分托管 30+ 平台声明与本地表列 16 平台。 [证据](https://github.com/Synter-Media-AI/mcp-server/blob/cc1e8bb5af31b915dc9cf423b1edbdd2bf239937/README.md#L168-L203) | 平台覆盖和 Verified 字样均为项目方声明；各平台写入深度不同。写入默认开启，可选只读，客户端确认取决于配置。 |
| [ynnickw/adport](https://github.com/ynnickw/adport) | 18 / 8 | +2 | 2026-11-06 | 11 个广告 Provider 的 CLI/MCP 控制面，含效果报表、审计及先预览后批准的写入。 [证据](https://github.com/ynnickw/adport/blob/84a27097b28172005cca4a09a10d324a2970fa61/README.md#L62-L93) | 统一广告模型与策略约束参考。README 自述实现/合同测试不证明各平台全部操作已获批并真实执行。 |

## 四项首次收录：业务价值与边界

### Meridian：广告渠道预算与频次规划

[README](https://github.com/google/meridian/blob/d90919820b788e217810d8d53ea6ba7bb563fd2f/README.md#L3-L24)明确服务广告主的 ROI、未来预算分配与广告频次分析，采用 Bayesian causal inference。仓库包含[预算优化 Skill](https://github.com/google/meridian/blob/d90919820b788e217810d8d53ea6ba7bb563fd2f/skills/meridian_budget_optimization/SKILL.md#L1-L12)；[优化函数参数](https://github.com/google/meridian/blob/d90919820b788e217810d8d53ea6ba7bb563fd2f/meridian/analysis/optimizer.py#L1625-L1647)包含预算、渠道花费限制、ROI/mROI 与频次。

投放价值是将已拟合模型接到广告预算情景分析。[人工检查点](https://github.com/google/meridian/blob/d90919820b788e217810d8d53ea6ba7bb563fd2f/skills/meridian_budget_optimization/SKILL.md#L49-L84)约束参数和脚本运行，但该文本约定不等同于已验证的权限隔离。需要历史数据、已拟合模型及假设审阅；本次只推荐广告预算/频次部分，没有验证模型准确度、广告 API 写入或线上收益。

### Robyn：付费渠道预算分配

[项目说明](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/README.md#L7-L11)将其定位为实验性、半自动 MMM，包含 Ridge、进化式搜索及预算优化方法。[paid-channel allocator](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/R/R/allocator.R#L31-L55)明确按付费渠道最大化响应，或针对 ROAS/CPA 分配预算；[参数与付费媒体输入](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/R/R/allocator.R#L88-L105)及[模型/渠道检查](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/R/R/allocator.R#L151-L182)可见实际实现。

适合比较渠道饱和、广告衰减及预算限制下的分配建议。需要有效模型及至少两个付费媒体渠道；仅推荐 allocator 的广告部分。[项目边界声明](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/README.md#L47-L49)说明软件按现状提供，不能把建模结果当作已验证因果效果、账户自动操作或 ROI 承诺。

### FeedGen：Shopping 广告商品 feed

[项目定位](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/README.md#L18-L25)明确用生成式 AI 优化 Shopping feeds；[广告主用途](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/README.md#L62-L76)与[工作流](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/README.md#L93-L115)说明标题、描述、属性补齐和 Merchant Center supplemental feed。[Gemini 路由](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/src/helpers/vertex.ts#L134-L138)及[Vertex AI 请求](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/src/helpers/vertex.ts#L179-L189)可见模型调用实现。

适用于 Shopping 广告商品数据生成和审核。它是依赖托管模型的 Apps Script 应用，并非只有注册入口。仅推荐明确的 Shopping 广告用途；README 建议人工审核、约 30k 商品上限，并注明非官方 Google 产品。旧模型标识、环境兼容性及真实 CTR 提升均未运行验证，也没有据此认定支持 Campaign 或预算管理。

### ViGenAiR：视频广告重剪与格式变体

[项目定位](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/README.md#L18-L23)明确为视频广告重创作；[架构与广告流程](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/README.md#L190-L205)描述 Gemini 语义分析、较短格式重组及前后端。[渲染入口](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/service/main.py#L120-L138)调用 Combiner 的 initial/render/finalise 路径，静态可见应用实现。

适合从已有广告视频准备不同长度、故事线与画幅的投放测试素材。需 GCP/Vertex AI，片段选择与时长可能偏离提示，裁剪无法自动调整文字覆盖层。[上传步骤](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/README.md#L389-L389)将 Google Ads/YouTube 上传留给用户；不能推定自动发布、改预算或获得 A/B 实验提升。项目注明非官方 Google 产品，本次未部署或审片。

## 已跟踪项目的源文件变化

### Paid Media Agent：后台分析与回访，仍有写入门控

本期 [提交比较](https://github.com/langchain-ai/paid-media-agent/compare/c81f9950cd56449a770a9a9e5e9e0a3fad54c382...895c2cbd332ca669f7f826f63b601456b899c4e8)为 **4 个新增提交、69 个变化文件**，包括后台助手、Slack 进度/页脚、Managed Deep Agents 接入及依赖调整。[当前功能与写入约束](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/README.md#L106-L116)明确只读异步助手、一次性线程计划，以及精确提案、持久化审批、一次尝试和读回要求。

[后台助手设计](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/docs/architecture/background-and-progress.md#L12-L39)列出 account-puller、report-builder 与 general-purpose 的读工具边界；[Managed 分支](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/src/paid_media_agent/assembly.py#L309-L323)只在 managed 条件下装配 helpers。[一次性回访](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/docs/architecture/background-and-progress.md#L41-L48)使用当前线程一次性调度；[运行限制](https://github.com/langchain-ai/paid-media-agent/blob/895c2cbd332ca669f7f826f63b601456b899c4e8/README.md#L163-L171)保留默认禁写、精确审批和 kill switch，后台能力要求 Managed Deep Agents。本次只确认文档和选定源码结构，未验证部署、运行时权限或真实写入成功。

### Google Ads MCP：文档变化与第一方口径差异

本期 [提交比较](https://github.com/googleads/google-ads-mcp/compare/7452a9d49e3d350403f2610cd7125c60f6d05264...84aebf819eebc3d8dda6ee693c1bdb5fcf5d36d9)为 **2 个新增提交、1 个变化文件（README）**，移除 developer-token 配置措辞/示例；已核验的六个运行源码文件内容未变。[固定 HEAD 工具与确认协议](https://github.com/googleads/google-ads-mcp/blob/84aebf819eebc3d8dda6ee693c1bdb5fcf5d36d9/README.md#L14-L30)仍列出 GAQL、资产创建、本地视频上传与标签操作；资产/标签写入已在上期记录，不能算作本期新增，更不能扩展为已验证的预算/竞价写入。

本次成功读取的 [Google 开发者指南](https://developers.google.com/google-ads/api/docs/developer-toolkit/mcp-server)仍将当前版本描述为只读，与固定仓库 HEAD 的工具清单口径不同。本文保留两份第一方资料的差异，按固定提交记录静态能力，不据此判定某发行版或已部署服务实际启用了写工具。Propose & Confirm 是项目协议，checksum 校验本身不构成独立的人类授权证据。

### Soku、Prebid 与 Synter

- **Soku：** [提交比较](https://github.com/About-Intelligence/soku-cli/compare/bdc0838a7f07c78afe37790dc3e00b6e08518465...125cb25fbdc2659c1088f7a3d657beaa54d7c60c)为 **1 个提交、2 个生成文件**。[生成清单变化](https://github.com/About-Intelligence/soku-cli/blob/125cb25fbdc2659c1088f7a3d657beaa54d7c60c/src/generated/changelog.json)增加 `ads/bulk_create_campaigns` 输入参数变化，计数由 9 到 10；README、已审阅的广告命令与 review 客户端内容未变。清单同步不能证明托管后端功能已上线。保留通常待审、用户 Always approve 可提交即执行、`require_human` 强制待审的边界。
- **Prebid Salesagent（观察）：** [提交比较](https://github.com/prebid/salesagent/compare/960f506bdd17ed71ab606667909c7b2ec0af9b50...a7a4c53f8f3dd22dee0ff90c30b5db4185da4a27)为 **3 个提交、10 个变化文件**。选定[A2A 源码](https://github.com/prebid/salesagent/blob/a7a4c53f8f3dd22dee0ff90c30b5db4185da4a27/src/a2a_server/adcp_a2a_server.py)有显式 skill 校验与任务注册变化；[定向 UI](https://github.com/prebid/salesagent/blob/a7a4c53f8f3dd22dee0ff90c30b5db4185da4a27/static/js/targeting_widget.js)拉取当前 GAM 值、使用 `cache: 'no-store'` 并避免旧选择渲染。仍为 alpha，没有验证媒体成交或投放。
- **Synter（观察）：** [提交比较](https://github.com/Synter-Media-AI/mcp-server/compare/73292595ea013e4de5025c9a8b73c53dc5919792...cc1e8bb5af31b915dc9cf423b1edbdd2bf239937)为 **9 个提交、7 个变化文件**，涉及平台/价格措辞、[REST 合约/错误/路由说明](https://github.com/Synter-Media-AI/mcp-server/blob/cc1e8bb5af31b915dc9cf423b1edbdd2bf239937/skills/synter-ads/SKILL.md)、配置与 demo；README 内容未变。不能将托管 30+ 平台宣传或配置文字变化视为生产平台覆盖已验证扩大。

其余 **21 个已跟踪项目**的默认分支 HEAD 与 11 月 5 日相同。AdCraft 虽增加 36 Stars，源码 HEAD 没有变化；Adport 虽增加 2 Stars，也没有默认分支新增。Claude Ads 的禁写、Amazon 搜索词分析静态缺失订单分支、SMB 原型的独立 HTTP 竞价引擎与缺权重降级、AuctionNet 的仿真性质，以及 Ryze/Adspirer 的托管入口边界继续保留。

## 检索、来源与验证范围

- 补充研究实际发起 **17 组公开网页查询**并读取 **2 个 GitHub 组织仓库清单**，检查额外候选元数据；另有主流程 3 条公开检索。查询原文与 API 路径写入快照。部分网页查询未返回可用结果，未据此判定项目不存在；不声称穷尽全网。
- 候选功能证据来自固定默认分支提交下的 README、Skills 与选定源码。本期覆盖 **97 个文件**，记录并检查 SHA-256 与 Git blob SHA1；仅抽查源码，不宣称审计整个实现。非官方 Google 产品声明保留在对应项目边界。
- 另交叉读取 Soku、Adspirer 与 Google 的官方页面；官网快照保留 URL、观察时间及哈希，不固定网页未来内容。两条猜测的 Google 文档路径返回 404，未用作能力证据。
- 可部署应用、云服务客户端、广告专用 Skill 与建模/仿真原型分别注明。混合营销仓库仅推荐有广告投放证据的组件；新增低星线索未纳入主表或用来补数量。
- 未安装或运行候选项目，未登录或授权广告账户，未创建 Campaign、修改预算或发起媒体购买。源码与文档不证明权限、端到端可用性、素材质量、归因准确度或投放收益。
- 本次四项新增均符合范围；后续没有合适项目时将明确记录无合适项目，不以通用 Agent 或无直接广告能力的泛营销工具补足。
