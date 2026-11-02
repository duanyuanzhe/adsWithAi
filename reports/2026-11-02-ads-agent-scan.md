# 广告投放 Agent / AI 项目日报：2026-11-02

> 报告整理时间：2026-11-02 09:43:13（Asia/Shanghai）。
> GitHub 元数据采集窗口：2026-11-02 09:26:15 — 2026-11-02 09:30:26（Asia/Shanghai）；每个项目的精确 UTC 采集时间见[数据快照](../sources/2026-11-02-github-snapshot.json)。
> 范围：直接服务广告账户、Campaign、预算/竞价、受众、用于投放的广告素材、广告效果分析/归因，或广告媒体交易的 Agent / AI 项目。

## 本日判断

本次主表收录 **15 个达到 100 Stars 的广告相关项目**，另列 **4 个低于该门槛的专项观察项目**。100 Stars 只是本日报的分层口径，不代表行业标准或成熟度。所有入选项均有项目方 README 或具体组件作为广告相关证据；不以通用 Agent 框架填充数量。

- **关注度与可复用实现分别判断。** 本次观察值最高的是 `irinabuht12-oss/google-ads-meta-ads-mcp`（6,772 Stars），但它主要是 Ryze 托管服务接入入口；静态仓库树未发现服务端代码。可自行研究的连接器优先比较 Pipeboard 的 Meta MCP（1,344 Stars）与 Google 官方组织的 Google Ads MCP（1,104 Stars）。
- **素材生产也有明确的广告专用实现。** AdCraft（562 Stars）和 Agentic Video Editor（507 Stars）分别覆盖广告视频生产与 UGC/DTC 广告剪辑；两个广告 Skills 项目则只按其广告素材组件纳入，不能据此推断具备账户执行能力。
- **分析类项目符合条件。** Meta Ads Analyzer（464 Stars）、Google Ads 分析 MCP、Paid Media Agent 等直接处理广告账户或广告导出数据；不要求每个项目都能修改广告。
- **较新的业务闭环值得跟踪，但热度不等于效果。** Paid Media Agent 的最近推送为 2026-11-01 21:15:51 UTC；其价值在于跨渠道诊断、报告和审核后的变更。Prebid、AWS、Synter、Adport 的观察价值分别在媒体交易、参考架构、多平台运营与预览审批。

## 热度口径与检索边界

1. 通过公开网页发现候选，并在 GitHub 搜索广告 Agent、Ads MCP、广告创意及媒体购买相关项目，再核对项目方材料。本次补充检索表达式、结果数量及入选项目命中保存在[数据快照](../sources/2026-11-02-github-snapshot.json)中；本报告不声称穷尽全网。
2. Stars、Forks 来自 GitHub 仓库 API 的本次观察值；表内按 Stars 降序排列。它们不是日增量、真实用户量、广告消耗规模或真实投放效果。没有历史基线，不推断“今日爆火”或增长速度。
3. 表内最近推送使用 `pushed_at`，完整秒级时间保存在快照中；它可能来自其他分支，不等同于最近发布、默认分支功能变化或上线时间。`updated_at` 也被保留，但不拿它替代代码推送。
4. 功能证据链接固定到采集时的默认分支提交；快照同时记录提交 SHA、README 路径、Git blob SHA 与文件 SHA-256，避免后续 README 变化造成证据漂移。
5. 同作者不同仓库可能共享服务或连接器，不能相加成为独立产品/用户数量。托管服务宣传、Skill 提示词、参考架构与可部署实现也不视作同一成熟度。

## 100 Stars 以上的广告相关项目

| 项目 | Stars / Forks | 最近推送（UTC） | 广告投放直接证据 | 应用价值与边界 |
|---|---:|---|---|---|
| [irinabuht12-oss/google-ads-meta-ads-mcp](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp) | 6,772 / 372 | 2026-10-27 | Google/Meta 广告账户、Campaign、素材、受众与效果查询；README 声明写入需批准。 [证据](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md#L117-L145) | 托管服务入口。已查看的仓库树没有服务端实现，不能把 6,772 Stars 解读成可自行部署的完整代码。 |
| [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp) | 1,344 / 282 | 2026-10-20 | Meta Campaign/Ad Set/Ad 管理、预算、定向、素材上传和效果分析。 [证据](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md#L175-L188) | 适合 Meta 执行连接器。仓库含 Python 实现；托管服务的五平台与工具总数不能直接算作本仓库覆盖。 |
| [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) | 1,104 / 343 | 2026-10-26 | Google Ads API 账户查询、可访问客户枚举及资源元数据，供 LLM/Agent 使用。 [证据](https://github.com/googleads/google-ads-mcp/blob/9a78cbdceebae71a6bc8483bdec333695834ef9c/README.md#L7-L24) | Google 广告官方组织项目，适合账户报表与 GAQL 接入。本文核验的是读取工具，未证明预算或竞价写入。 |
| [realkimbarrett/advertising-skills](https://github.com/realkimbarrett/advertising-skills) | 769 / 68 | 2026-03-26 | 仅收录广告创意组件：前三秒 Hook/画面/脚本构思，以及广告角度与 Hook 变体生成。 [证据](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/README.md#L42-L51) | 广告素材提示词资产；不推荐其中的邮件、落地页等泛营销部分。没有广告账户执行能力。 |
| [cohnen/mcp-google-ads](https://github.com/cohnen/mcp-google-ads) | 717 / 157 | 2025-10-16 | 通过 MCP 分析 Google Ads Campaign、广告、关键词、预算消耗与竞价策略数据。 [证据](https://github.com/cohnen/mcp-google-ads/blob/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a/README.md#L7-L35) | 适合只读分析接入比较；最近推送为 2025-10-16，采纳前需核对当前依赖与 API 兼容性。 |
| [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft) | 562 / 76 | 2026-10-31 | 面向广告视频的 Agent 工作流：创意、脚本、产品视觉、分镜、视频与最终合成。 [证据](https://github.com/GML-MMGroup/AdCraft/blob/0e6317d618a9d2065b3b6639c91b5119c1563e92/README.md#L71-L113) | 广告素材生产方向；仓库树可见前后端实现。尚未运行生成，也未验证视频质量、成本或投放效果。 |
| [poseljacob/agentic-video-editor](https://github.com/poseljacob/agentic-video-editor) | 507 / 62 | 2026-04-14 | 以原始素材与创意 Brief 生成广告剪辑；包含 UGC 广告管线、DTC 风格及导演/剪辑/审片反馈循环。 [证据](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md#L104-L130) | 适合短视频广告素材迭代。CLI 是文档推荐路径，Web UI 标明 pre-alpha；不负责账户投放。 |
| [mathiaschu/meta-ads-analyzer](https://github.com/mathiaschu/meta-ads-analyzer) | 464 / 63 | 2026-02-26 | 分析 Meta Campaign/Ad Set/Ad 表现，诊断 Breakdown Effect、学习阶段、重叠、节奏与素材疲劳。 [证据](https://github.com/mathiaschu/meta-ads-analyzer/blob/9088472ddacdb89f3c5943c3db6be7b8ee25c922/README.md#L3-L14) | 广告分析 Skill；可用广告导出数据，也可配置外部 MCP 取实时数据，不能当作独立全功能执行服务器。 |
| [gomarble-ai/facebook-ads-mcp-server](https://github.com/gomarble-ai/facebook-ads-mcp-server) | 366 / 111 | 2026-08-05 | 读取 Meta 广告账户、Campaign、Ad Set、Ad、Creative 和 Insights，给 AI 提供广告数据。 [证据](https://github.com/gomarble-ai/facebook-ads-mcp-server/blob/a3b555a12dff5b888b172ef9113dd1f36d69e525/readme.md#L99-L133) | 适合广告效果分析连接器。本文不据这些读取工具推定支持创建或修改投放。 |
| [TheMattBerman/meta-ads-kit](https://github.com/TheMattBerman/meta-ads-kit) | 348 / 67 | 2026-06-10 | Meta 广告日报、素材疲劳、预算建议、广告文案、暂停/恢复及 Pixel/CAPI 检查。 [证据](https://github.com/TheMattBerman/meta-ads-kit/blob/dffa0daf6ed1e278481e9408af3be6aaf9709b28/README.md#L12-L25) | OpenClaw 广告专用工作流；上传采用 CLI-first、PAUSED/dry-run 约束，具体上传范围仍受 CLI 支持限制。 |
| [zubair-trabzada/ai-ads-claude](https://github.com/zubair-trabzada/ai-ads-claude) | 283 / 99 | 2026-04-08 | 广告专用 Claude Code Skills：平台格式广告文案、视频广告脚本、关键词及预算方案。 [证据](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/README.md#L74-L103) | 优先关注 ads-copy/ads-video 素材组件；策略评分和预算预测是模型建议，没有证明可自动修改账户。 |
| [TheMattBerman/google-ads-copilot](https://github.com/TheMattBerman/google-ads-copilot) | 241 / 47 | 2026-06-10 | 读取账户或 CSV，形成可审核草稿；文档列出否定关键词、暂停关键词/广告组、日预算调整的受控 Apply。 [证据](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md#L19-L29) | 适合 Read → Draft → Apply 设计；应以列明的写入范围评估，不能推定覆盖全部 Google Ads 操作。 |
| [brijr/meta-mcp](https://github.com/brijr/meta-mcp) | 201 / 75 | 2026-05-28 | Cloudflare Workers 上的 Meta 广告账户设置、Campaign、Ad Set、素材、受众与报表工具。 [证据](https://github.com/brijr/meta-mcp/blob/664b20617a6aee529ff31f8093e85fca7db4b7be/README.md#L73-L82) | 适合 Meta OAuth、工具组织和部署模型比较；与 Pipeboard 是不同实现。 |
| [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server) | 146 / 47 | 2026-08-05 | Google Ads OAuth、GAQL 广告数据查询与关键词研究，供 AI 客户端调用。 [证据](https://github.com/gomarble-ai/google-ads-mcp-server/blob/4f922abc8f9932a5080052a222a5edb86d7a3697/README.md#L27-L35) | 适合 Google Ads 数据接入备选；文档的 account management 不足以证明全部 Campaign 写入。 |
| [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent) | 116 / 24 | 2026-11-01 | 跨渠道广告消耗、转化、CPL、预算节奏分析及报告，准备带原因和检查计划的 Campaign 变更。 [证据](https://github.com/langchain-ai/paid-media-agent/blob/c81f9950cd56449a770a9a9e5e9e0a3fad54c382/README.md#L27-L54) | 适合投放分析到审核的业务闭环。真实账户变更默认关闭，需写入策略、发布检查与授权审核。 |

## 低热度专项观察

以下四项都与广告投放直接相关，但仅有 15–39 Stars，**不称作热门项目，也不与主表的关注度等量比较**。保留它们是因为广告链路或实现设计有明确差异。

| 项目 | Stars / Forks | 最近推送（UTC） | 广告投放直接证据 | 应用价值与边界 |
|---|---:|---|---|---|
| [prebid/salesagent](https://github.com/prebid/salesagent) | 39 / 60 | 2026-10-28 | 通过 MCP/A2A 暴露广告库存，支持媒体购买与 Google Ad Manager 等广告服务器对接。 [证据](https://github.com/prebid/salesagent/blob/1c202df28c6715bd00fb638197fe5bc08fb163d3/README.md#L3-L20) | 媒体交易与供给侧参考；README 明确为 alpha，不能以协议或示例等同于生产投放验证。 |
| [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws) | 22 / 8 | 2026-10-29 | 基于 Bedrock AgentCore 的广告多 Agent 方案，覆盖媒体规划、受众、竞价优化与发布商变现。 [证据](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/13239f178ad8ea749fbdc258300f7141ef9ec306/README.md#L82-L95) | 广告专用参考架构。含演示数据与演示 UI，不是已验证的真实账户优化服务。 |
| [Synter-Media-AI/mcp-server](https://github.com/Synter-Media-AI/mcp-server) | 21 / 4 | 2026-10-31 | README 明确为 16 个广告平台提供读写，写入/创建深度随平台 API 而异。 [证据](https://github.com/Synter-Media-AI/mcp-server/blob/6ed95d885030a218d675e3177b6e1f7732f124d2/README.md#L150-L168) | 跨平台广告运营参考。写入默认开启，可选只读；客户端确认行为取决于客户端配置。 |
| [ynnickw/adport](https://github.com/ynnickw/adport) | 15 / 8 | 2026-11-01 | 11 个广告 Provider 的 CLI/MCP 控制面，含效果报表、审计及先预览后批准的写入。 [证据](https://github.com/ynnickw/adport/blob/f6515a3ac94b185941ef9bb31e32d59f563bef11/README.md#L62-L93) | 统一广告模型与策略约束参考。README 自述实现/合同测试不证明各平台全部操作已获批并真实执行。 |

## 对 adsWithAi 最有参考价值的能力

### 1. 广告数据与执行连接器

Google 官方项目的账户搜索、客户枚举与资源元数据适合建立 Google Ads 数据层；Pipeboard 的 Meta 项目覆盖 Campaign、素材、预算和定向操作。建议保留平台原始字段、币种、账户时区、归因窗口与 API 版本，再构建统一对象。两者的功能范围来自 [Google Ads README](https://github.com/googleads/google-ads-mcp/blob/9a78cbdceebae71a6bc8483bdec333695834ef9c/README.md) 与 [Pipeboard README](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md)；本文未连接广告账户测试。

Ryze 的高星值可作为关注度信号，但其公开仓库在所核验提交下是文档/接入入口；没有发现可直接部署的服务端实现。不能因 README 列出工具数量就认定获得了对应开源代码或实际服务验证。相关提交和仓库树信息已存入快照。

### 2. 分析、草稿、审批、执行与读回

[Paid Media Agent](https://github.com/langchain-ai/paid-media-agent/blob/c81f9950cd56449a770a9a9e5e9e0a3fad54c382/README.md) 明确把真实账户写入默认关闭；[Google Ads Copilot](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md) 列出了当前支持的 Apply 范围；[Adport](https://github.com/ynnickw/adport/blob/f6515a3ac94b185941ef9bb31e32d59f563bef11/README.md) 展示了预览、完全匹配参数的批准、预算上限与审计记录。对 adsWithAi 的设计建议是：先用只读数据生成可追溯诊断，花费相关变更形成结构化 before/after 草稿，经明确批准后执行，再读回检查结果。这里描述的是建议采用的控制流程，不是已实现功能。

### 3. 广告素材生产与提示词组件

[AdCraft](https://github.com/GML-MMGroup/AdCraft/blob/0e6317d618a9d2065b3b6639c91b5119c1563e92/README.md) 将脚本、分镜、视频和资产管理串成广告生产工作流；[Agentic Video Editor](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md) 使用 UGC 广告管线及 DTC 风格，迭代剪辑与审片。它们适合参考广告素材的版本记录、复用和人工验收设计。本文未生成样片，也未验证 CTR、CVR、ROAS 改善。

对于提示词资产，只推荐有明确广告输出的部分：[scroll-stopping-creative](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/skills/operator-os/scroll-stopping-creative/SKILL.md) 输出广告 Hook/视觉/脚本构思，[ad-angle-multiplier](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/skills/operator-os/ad-angle-multiplier/SKILL.md) 生成广告角度；[ads-copy](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/skills/ads-copy/SKILL.md) 定义平台广告格式与多文案变体。它们是需要模型执行和人工审核的广告专用 Skills；本文未验证模型输出是否符合最新平台规范，不把同仓库的泛营销部分列为推荐。

### 4. 多平台写入的证据要细分

[Synter README](https://github.com/Synter-Media-AI/mcp-server/blob/6ed95d885030a218d675e3177b6e1f7732f124d2/README.md) 当前写的是 **16 个平台的读写**；仓库 description 的“43”与 README 不一致，本文按正文中可核对的平台表记录为 16，不合并成“43 平台完整支持”。README 同时说明写入默认开启、可选 `--read-only`，并提供 `dry_run`、花费限制、写后读回与审计；**客户端是否要求确认取决于客户端及配置**，不能描述成所有调用都必经人工审批。

Adport 的 11 平台也是项目方文档覆盖声明；其 README 明确提醒：实现和合同测试不证明每个广告平台的全部操作已获权限并在真实账户成功。后续若做集成，需要按平台、动作、权限和指标分别验证。

### 5. 广告媒体交易与多 Agent 架构

[Prebid Sales Agent](https://github.com/prebid/salesagent/blob/1c202df28c6715bd00fb638197fe5bc08fb163d3/README.md) 直接服务广告库存发现与媒体购买，并以 alpha 状态交付；[AWS Advertising Agents Guidance](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/13239f178ad8ea749fbdc258300f7141ef9ec306/README.md) 展示广告价值链中的多 Agent 协作，但包含演示数据。两者适合作为交易接口与职责拆分参考，不能直接当作生产竞价收益或真实交付验证。

## 筛选时排除的范围

- 通用 Agent 框架、通用 MCP 集合、普通代码助手，以及仅推测“改造后可用于广告”的项目。
- 只做自然流量 SEO、普通社媒发帖、邮件营销、CRM 或销售线索，且没有直接广告素材、广告账户分析或投放工作流证据的泛营销项目。
- 仅因名称含 `AD` 被搜索命中的 Active Directory 等非广告项目。
- 只有广告库抓取/展示，且没有广告效果分析、投放素材生成/优化或其他直接投放工作流的项目。广告数据分析或归因本身可以入选，并不要求账户写入。

没有固定凑数目标；若后续某日无合适项目，应直接记录无合适项目。

## 数据与验证说明

- 每行均链接项目仓库及固定提交下的第一方证据；统计与来源明细见 [2026-11-02 GitHub 数据快照](../sources/2026-11-02-github-snapshot.json)。公开网页搜索仅用于发现和交叉核对，统计以现场 GitHub API 为准。
- 本次核验包括 README、选定组件文件、部分仓库树及 GitHub 公开元数据。没有安装或执行这些项目，没有授权广告账户、创建 Campaign、修改预算或测试真实投放。
- 因此，“入选”表示其公开材料能够证明直接服务广告业务；实际可用性、权限、平台兼容性、输出质量和投放收益仍需独立验证。
