# 广告投放 Agent 项目日报：2026-11-02

> 调研时间：2026-11-02 08:56（Asia/Shanghai）
> 目标范围：只收录能直接连接广告平台、管理广告账户/广告系列、执行付费媒体分析，或提供广告技术（AdTech）投放工作流的 Agent/AI 项目。
> 热度口径：GitHub Stars、Forks、近期更新时间和项目官方描述；数据会随 GitHub 变化，本报告记录的是本次扫描时的观察值。

## 结论

今天有 8 个项目满足“与广告投放直接相关”的硬性条件：

- **Google Ads MCP Server** 是热度最高且来自广告平台官方组织的候选，适合作为 Google Ads 数据和工具接入层。
- **Meta MCP** 和 **Paid Media Agent** 的社区热度和业务覆盖较强，前者偏 Meta Marketing API 控制面，后者偏跨渠道分析、报告和人工审核后的变更。
- **Adport**、**GoMarble** 和 **YieldAgent** 更接近可直接用于投放运营的 Agent 工作流，分别强调多平台控制、绩效营销操作和安全的草稿式投放。
- **AWS Guidance for Advertising Agents** 更像完整的广告技术多 Agent 参考架构，覆盖媒体规划、受众、竞价优化和发布商收入等链路，适合做架构研究。

GitHub 热度是公开代理指标，不能等同于生产可靠性、真实活跃用户或投放效果。涉及真实账户和预算的项目，应重点查看权限、审批、草稿/预览、审计日志和平台 API 限制。

## 候选项目

| 排名依据 | 项目 | Stars / Forks | 直接广告投放证据 | 适合关注的方向 |
|---|---|---:|---|---|
| 1 | [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp) | 1,104 / 343 | Google 官方组织维护的 MCP Server，直接连接 Google Ads API，并为 LLM/Agent 提供账户搜索、资源元数据和报告相关资源 | Google Ads 接入层、账户查询、报表和工具命名空间治理 |
| 2 | [brijr/meta-mcp](https://github.com/brijr/meta-mcp) | 201 / 75 | README 明确覆盖 Meta Ads 账户设置、Campaign、Ad Set、Creative、Audience、Reporting 和 Batch 工作流，当前注册 39 个工具 | Meta 广告全链路工具、OAuth、多租户和业务权限 |
| 3 | [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent) | 116 / 24 | README 明确定位为 Paid Media Agent，支持跨账户的 Campaign 分析、报告和提交审核的 Campaign 变更 | 跨渠道分析、预算节奏、异常解释、人工审核闭环 |
| 4 | [byadsco/meta-ads-mcp](https://github.com/byadsco/meta-ads-mcp) | 25 / 18 | 项目描述直接定位为 Meta Ads MCP，面向 agency multi-account 和 cloud-ready 场景 | 代理商多账户、Meta Ads 托管和云部署 |
| 5 | [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws) | 22 / 8 | AWS 方案明确展示广告工作流的多 Agent 协作，覆盖媒体规划、受众定向、实时竞价优化和发布商收入管理 | AdTech 多 Agent 架构、竞价优化、买方/卖方协同 |
| 6 | [ynnickw/adport](https://github.com/ynnickw/adport) | 15 / 8 | README 将其定义为 Paid Media control plane，支持 11 个广告平台、MCP/CLI、报表和策略保护的写操作预览 | 多平台账户统一管理、预算变更审批、审计和策略护栏 |
| 7 | [gomarble-ai/marketing-agent](https://github.com/gomarble-ai/marketing-agent) | 15 / 2 | README 明确面向 paid media teams，支持广告账户分析、创意疲劳识别、Campaign Launch，以及 Meta/Google Ads/TikTok 等渠道技能 | 绩效营销日常运营、素材分析、预算调整和排期 Agent |
| 8 | [TensorOpsAI/YieldAgent](https://github.com/TensorOpsAI/YieldAgent) | 13 / 2 | README 展示以广告技术为核心的 Agent，包含受众解析、Reach 估算、预算底线、Campaign proposal 和 DRAFT 创建 | 受众与预算校验、平台连接器、审批后生成草稿 |

## 重点项目分析

### 1. Google Ads MCP Server

- **官方证据**：仓库位于 `googleads` 组织，README 直接链接 Google Ads API；MCP 工具面包括账户搜索和资源元数据，资源面包括 discovery document、metrics、segments 和 release notes。
- **投放价值**：适合成为广告 Agent 的 Google Ads 原生工具层，让 Agent 查询账户、理解资源字段和报告指标，再由上层工作流负责诊断、建议和审批。
- **边界**：它更像 Google Ads API 的 Agent 接入层，不能仅凭 MCP 暴露就推断所有写操作、审批和真实投放流程已经具备；落地时要逐项核对工具配置和账户权限。

### 2. Meta MCP

- **官方证据**：README 明确列出 Campaign、Ad Set、Creative、Audience、Targeting、Reporting 和 Insights 等工具族，并使用 Meta Graph API 与 OAuth。
- **投放价值**：覆盖面接近 Meta 广告操作控制面，适合研究多租户工作区、账号绑定、访问令牌加密、权限和报告工具如何组织。
- **边界**：项目需要自建 Cloudflare Worker、Meta App、JWT 和存储绑定；开源仓库本身不等于可直接连接生产账户。

### 3. Paid Media Agent

- **官方证据**：项目直接定位为跨渠道 Campaign 分析和报告，README 提到 spend、conversions、cost per lead、budget pacing、异常调查和提交审核的 Campaign 变更；连接范围包含 Google Ads、Meta Ads、TikTok Ads、Pinterest Ads、Snap Ads、Reddit Ads、LinkedIn Ads、X Ads 和 OpenAI Ads 等。
- **投放价值**：最适合作为“广告数据分析 Agent + 人工审核变更”的参考实现，尤其适合观察如何把指标计算、解释、报告和写权限拆开。
- **边界**：实时写入默认关闭，真实账户能力依赖连接器、平台权限和运行配置；离线 Demo 不代表真实投放成功。

### 4. Adport

- **官方证据**：README 明确支持 11 个广告平台，并提供统一 Provider、CLI 和 MCP 工具；写操作先返回预览、预算变化、策略校验和短期审批 ID。
- **投放价值**：对 `adsWithAi` 最有参考价值的是统一广告平台模型、策略护栏、预览后应用、账户级预算上限和追加审计记录。
- **边界**：项目较新，仓库中的合同测试和实现覆盖不能直接证明所有平台的真实操作都成功；需要按平台核验权限和指标差异。

### 5. GoMarble Marketing Agent

- **官方证据**：README 直接面向 paid media teams，提供诊断 ROAS、创意分析、削减浪费、调整预算、Campaign Launch、Campaign 管理和跨渠道报告等技能。
- **投放价值**：适合作为绩效营销运营流程的产品化参考，特别是“解释发生了什么 → 提出动作 → 等待批准 → 执行 → 回报”的闭环。
- **边界**：部分能力依赖 GoMarble 服务端连接器和账户计划，开源仓库中的技能文本不应单独视为已验证的生产执行能力。

### 6. YieldAgent

- **官方证据**：README 展示了围绕 Campaign proposal 的 Agent Console，先解析真实平台的定向分类、估算 Reach、核对预算底线，再经过人工批准创建 DRAFT；默认不直接激活投放。
- **投放价值**：其“平台规则来自工具、写操作只创建草稿、激活仍需人工完成”的安全模型，适合用于 `adsWithAi` 的 Campaign 创建和预算变更设计。
- **边界**：当前更偏连接器和投放提案参考，不能把 DRAFT 创建等同于线上消耗或投放结果。

## 对 adsWithAi 的建议

1. **先做只读统一层**：优先参考 Google Ads MCP、Meta MCP 和 Adport，把账户、Campaign、Ad Set、Creative、Audience、Insights、预算和归因字段统一成内部模型，同时保留平台原始字段。
2. **把分析和写入分开**：参考 Paid Media Agent 和 GoMarble，把诊断、异常、创意疲劳、预算建议和报表作为只读能力；写操作必须生成结构化变更计划。
3. **所有花费相关动作先预览、再审批、后执行**：参考 Adport 和 YieldAgent，Campaign 新建默认暂停或 DRAFT，预算、竞价、状态和素材变更保存 before/after、理由、操作者和审计记录。
4. **先覆盖两大平台，再扩展平台**：Google Ads 和 Meta Ads 的账户、Campaign、Ad Set/Ad Group、Creative、Audience、Insights、Budget 是第一阶段的最小闭环；TikTok、LinkedIn、Reddit 等平台作为连接器扩展。
5. **报告保留数据时间和来源**：每个结论都记录查询时间、账户时区、归因窗口、币种、平台 API 版本和原始查询，避免跨平台指标直接比较。

## 本次排除

- 通用 Agent 框架、通用 MCP 集合和通用营销技能库：无法证明直接操作广告投放。
- 仅提供广告监测、广告情报或广告数据研究，未提供投放账户、Campaign、预算、竞价或广告执行能力的项目。
- 仅在描述中声称“可以用于广告”，但 README、官方文档或代码没有直接广告平台能力证据的项目。

## 数据来源

所有项目链接均指向项目官方 GitHub 仓库；项目功能判断来自各仓库 README 和公开文档。Stars、Forks、更新时间取自 GitHub 仓库公开元数据，记录于 2026-11-02 08:56（Asia/Shanghai）。
