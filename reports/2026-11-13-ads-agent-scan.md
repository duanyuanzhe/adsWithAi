# Ads-only Agent/AI 项目日报：2026-11-13

## 摘要

本期以公开 GitHub 数据作为可复核主数据源，检索与广告投放、广告账户/广告系列管理、竞价与预算、受众定向、广告素材及广告效果分析直接相关的 Agent/AI/AdTech 项目。观察窗口为 `2026-11-13T12:12:24.035Z` 至 `2026-11-13T12:12:35.123Z`，即北京时间 `2026-11-13 20:12:24` 至 `20:12:35`。

- 候选仓库：42 个。
- 主表：27 个，当前 Stars `>=100`，按 Stars 降序排列。
- 低热度观察：8 个，直接广告能力明确但当前 Stars `<100`。
- 排除：7 个，虽命中广告关键词，但未满足“已有直接投放能力”的证据要求。
- 与 2026-11-08 基线相隔约 `130.13` 小时，因此本报告的变化字段不是“过去 24 小时增长”；它们是本次观察值相对 11 月 8 日快照的差值。

本期最值得持续关注的方向是：多平台 Ads MCP/Skill、带审批与预算保护的账户写操作、广告素材与视频变体、MMM/归因与预算优化，以及面向媒体交易的 Agent 协议。广告能力证据均来自项目自己的 README、文档或固定提交中的源码入口；固定提交由来源快照记录。

## 过滤规则

只有同时满足以下条件的项目才进入推荐列表：

1. 有官方 README、文档、源码或可运行功能，明确服务于广告投放或付费媒体，而不是仅能“推测改造成广告工具”。
2. 能力至少覆盖一项：广告账户或 Campaign 管理、广告预算/竞价优化、广告受众定向、投放素材生成/优化、广告效果分析/归因、媒体规划或广告投放工作流。
3. Stars/Forks 只用于公开关注度排序，不代表生产成熟度、账户可用性、投放收益或 ROAS。

通用 Agent 框架、通用 AI 工具、泛营销工具、资源清单，以及仍处于 `Planned`/`Spec Ready` 阶段的项目，不纳入推荐。

## 主表：27 个直接相关项目

| # | 项目 | Stars / Forks | 相对 11-08 | 直接广告能力与证据 |
|---:|---|---:|---:|---|
| 1 | [AgriciDaniel/claude-ads](https://github.com/AgriciDaniel/claude-ads/tree/fc3908e786c318776df89a3a098333da377364be) | 11,000 / 1,593 | +183 / +26 | Claude-first paid-media operations，覆盖 12 个广告平台；审计、确定性发现、证据覆盖、报告及能力门控的账户变更。证据：[README](https://github.com/AgriciDaniel/claude-ads/blob/fc3908e786c318776df89a3a098333da377364be/README.md)。 |
| 2 | [irinabuht12-oss/google-ads-meta-ads-mcp](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/tree/a4911a848c5c698484f6d02b84e1585010895a44) | 7,530 / 375 | +461 / +3 | Google Ads + Meta Ads 远程 MCP，含 OAuth、审批门控写操作及账户/报表能力。证据：[README](https://github.com/irinabuht12-oss/google-ads-meta-ads-mcp/blob/a4911a848c5c698484f6d02b84e1585010895a44/README.md)。 |
| 3 | [google/meridian](https://github.com/google/meridian/tree/d8c182861a77e90dfc4cadfeed9b840d82cb91de) | 1,603 / 312 | +8 / +1 | 面向广告主的 MMM，支持媒体贡献、预算分配与投放优化；仓库含 `skills/meridian_budget_optimization/SKILL.md`。证据：[README](https://github.com/google/meridian/blob/d8c182861a77e90dfc4cadfeed9b840d82cb91de/README.md)。 |
| 4 | [facebookexperimental/Robyn](https://github.com/facebookexperimental/Robyn/tree/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58) | 1,536 / 439 | +2 / +1 | Meta 的开源 MMM/预算优化工具，用于媒体效果建模、渠道贡献和投放预算决策。证据：[README](https://github.com/facebookexperimental/Robyn/blob/aab4226ed5e40196cdbd82ff7fbbff55e91e1f58/README.md)。 |
| 5 | [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp/tree/63d0e5e29f2cf823f7f5317a77e66151eceb7415) | 1,367 / 284 | +9 / +2 | Meta Marketing API 的 MCP 接入，服务 Campaign、广告、受众与洞察查询/操作。证据：[README](https://github.com/pipeboard-co/meta-ads-mcp/blob/63d0e5e29f2cf823f7f5317a77e66151eceb7415/README.md)。 |
| 6 | [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp/tree/cda852701fb5787dc4d79281f37da795ac09b97d) | 1,169 / 370 | +41 / +17 | Google 官方 Ads MCP；源码包含资产创建、标签、视频上传等投放操作入口。证据：[README](https://github.com/googleads/google-ads-mcp/blob/cda852701fb5787dc4d79281f37da795ac09b97d/README.md)、[`create_asset.py`](https://github.com/googleads/google-ads-mcp/blob/cda852701fb5787dc4d79281f37da795ac09b97d/ads_mcp/tools/create_asset.py)。 |
| 7 | [realkimbarrett/advertising-skills](https://github.com/realkimbarrett/advertising-skills/tree/45f4a4a1dabe24113193369b55b929b1de4ff04a) | 788 / 72 | +11 / +1 | 广告平台 Agent Skills，围绕账户审计、Campaign 操作、素材和报告等付费媒体流程。证据：[README](https://github.com/realkimbarrett/advertising-skills/blob/45f4a4a1dabe24113193369b55b929b1de4ff04a/README.md)。 |
| 8 | [cohnen/mcp-google-ads](https://github.com/cohnen/mcp-google-ads/tree/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a) | 721 / 157 | +3 / -1 | Google Ads MCP，直接面向账户查询、Campaign 管理和效果数据。证据：[README](https://github.com/cohnen/mcp-google-ads/blob/461a1d673cf1c369e8b95fc9b5b1d9cb7f3ebb4a/README.md)。 |
| 9 | [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft/tree/29c8f2c8abc985d0181c4531f12b21a7ee9df864) | 695 / 87 | +58 / +6 | 面向广告营销的 Agent 应用，源码含 `apps/api/agent/skills/*`，覆盖广告策略、素材和投放工作流。证据：[README](https://github.com/GML-MMGroup/AdCraft/blob/29c8f2c8abc985d0181c4531f12b21a7ee9df864/README.md)。 |
| 10 | [poseljacob/agentic-video-editor](https://github.com/poseljacob/agentic-video-editor/tree/47248b577046b0563e57e78edad86a3106c6faab) | 511 / 62 | +3 / 0 | Agentic 视频素材编辑，适用于广告视频生成、改版和批量创意生产；纳入原因是其仓库功能直接面向可投放视频素材。证据：[README](https://github.com/poseljacob/agentic-video-editor/blob/47248b577046b0563e57e78edad86a3106c6faab/README.md)。 |
| 11 | [haoyangfeng2024/smb-adtech-platform](https://github.com/haoyangfeng2024/smb-adtech-platform/tree/52a00c1efb9b0a4e069c562e66f71267610d9410) | 471 / 38 | 0 / 0 | 面向 SMB 的广告技术平台，包含广告账户、Campaign 与投放管理能力。证据：[README](https://github.com/haoyangfeng2024/smb-adtech-platform/blob/52a00c1efb9b0a4e069c562e66f71267610d9410/README.md)。 |
| 12 | [mathiaschu/meta-ads-analyzer](https://github.com/mathiaschu/meta-ads-analyzer/tree/9088472ddacdb89f3c5943c3db6be7b8ee25c922) | 470 / 64 | +3 / +1 | Meta Ads 数据分析与洞察，直接用于 Campaign/广告效果复盘。证据：[README](https://github.com/mathiaschu/meta-ads-analyzer/blob/9088472ddacdb89f3c5943c3db6be7b8ee25c922/README.md)。 |
| 13 | [gomarble-ai/facebook-ads-mcp-server](https://github.com/gomarble-ai/facebook-ads-mcp-server/tree/a3b555a12dff5b888b172ef9113dd1f36d69e525) | 370 / 112 | +1 / 0 | Facebook/Meta Ads MCP，覆盖投放账户、Campaign 和广告数据读写。证据：[README](https://github.com/gomarble-ai/facebook-ads-mcp-server/blob/a3b555a12dff5b888b172ef9113dd1f36d69e525/README.md)。 |
| 14 | [TheMattBerman/meta-ads-kit](https://github.com/TheMattBerman/meta-ads-kit/tree/dffa0daf6ed1e278481e9408af3be6aaf9709b28) | 354 / 69 | +4 / +1 | Meta Ads 操作工具包，面向广告账户、Campaign、广告组、素材和报告。证据：[README](https://github.com/TheMattBerman/meta-ads-kit/blob/dffa0daf6ed1e278481e9408af3be6aaf9709b28/README.md)。 |
| 15 | [About-Intelligence/soku-cli](https://github.com/About-Intelligence/soku-cli/tree/e88e2e0571ab5367d57c617e3677bee761f8265a) | 301 / 31 | 0 / 0 | 广告 CLI/Skills；源码中的广告命令和 Skill 直接支持投放操作、检查与报告。证据：[README](https://github.com/About-Intelligence/soku-cli/blob/e88e2e0571ab5367d57c617e3677bee761f8265a/README.md)、[`src/generated/changelog.json`](https://github.com/About-Intelligence/soku-cli/blob/e88e2e0571ab5367d57c617e3677bee761f8265a/src/generated/changelog.json)。 |
| 16 | [zubair-trabzada/ai-ads-claude](https://github.com/zubair-trabzada/ai-ads-claude/tree/d1df3f544249191cbc600c8301e2b9d5ddd121c8) | 287 / 98 | +2 / -1 | 明确面向广告工作的 Claude/AI Skills，覆盖广告分析、创意和投放辅助。证据：[README](https://github.com/zubair-trabzada/ai-ads-claude/blob/d1df3f544249191cbc600c8301e2b9d5ddd121c8/README.md)。 |
| 17 | [google-marketing-solutions/feedgen](https://github.com/google-marketing-solutions/feedgen/tree/545be8a7b217246b30bce928ac51bd32918657b3) | 269 / 43 | +1 / 0 | 商品广告/购物投放的 Feed 生成与优化，服务于广告素材和商品投放准备。证据：[README](https://github.com/google-marketing-solutions/feedgen/blob/545be8a7b217246b30bce928ac51bd32918657b3/README.md)。 |
| 18 | [zach22-1999/amazon-skills](https://github.com/zach22-1999/amazon-skills/tree/db1f7d108eb8c43b6de36c6a3e230ebff107e227) | 260 / 54 | +6 / +2 | Amazon Ads 相关 Agent Skills，直接服务 Sponsored Ads 账户、Campaign、关键词和报表流程。证据：[README](https://github.com/zach22-1999/amazon-skills/blob/db1f7d108eb8c43b6de36c6a3e230ebff107e227/README.md)。 |
| 19 | [alimama-tech/AuctionNet](https://github.com/alimama-tech/AuctionNet/tree/c20de631a40e24669d1d6a8e2acefd8f492f172d) | 259 / 41 | +2 / 0 | 阿里妈妈广告竞价/拍卖研究与优化框架，属于直接广告竞价基础设施。证据：[README](https://github.com/alimama-tech/AuctionNet/blob/c20de631a40e24669d1d6a8e2acefd8f492f172d/README.md)。 |
| 20 | [google-marketing-solutions/vigenair](https://github.com/google-marketing-solutions/vigenair/tree/31096ced99c25072b120e8a93869f5f9491122f0) | 243 / 77 | 0 / 0 | 面向视频广告创意生产/优化的 Google Marketing Solutions 项目。证据：[README](https://github.com/google-marketing-solutions/vigenair/blob/31096ced99c25072b120e8a93869f5f9491122f0/README.md)。 |
| 21 | [TheMattBerman/google-ads-copilot](https://github.com/TheMattBerman/google-ads-copilot/tree/2c253ee988b5540465317cde0cd4d6915dc2b382) | 241 / 48 | 0 / +1 | Google Ads Copilot，面向账户查询、Campaign 规划与优化建议。证据：[README](https://github.com/TheMattBerman/google-ads-copilot/blob/2c253ee988b5540465317cde0cd4d6915dc2b382/README.md)。 |
| 22 | [aronhy/marketing-skill-hub](https://github.com/aronhy/marketing-skill-hub/tree/5bb9103564a559b40b8cf91b67c340d9b2f77005) | 227 / 39 | 未建立基线 | 仅推荐其中明确的 Meta Ads、Google Ads、TikTok Ads Skills；邮件、开发信等泛营销能力不纳入本报告。证据：[README](https://github.com/aronhy/marketing-skill-hub/blob/5bb9103564a559b40b8cf91b67c340d9b2f77005/README.md)。 |
| 23 | [brijr/meta-mcp](https://github.com/brijr/meta-mcp/tree/664b20617a6aee529ff31f8093e85fca7db4b7be) | 202 / 75 | 0 / 0 | Meta 广告/营销 API MCP 接入，面向广告账户和投放数据工作流。证据：[README](https://github.com/brijr/meta-mcp/blob/664b20617a6aee529ff31f8093e85fca7db4b7be/README.md)。 |
| 24 | [gomarble-ai/google-ads-mcp-server](https://github.com/gomarble-ai/google-ads-mcp-server/tree/4f922abc8f9932a5080052a222a5edb86d7a3697) | 147 / 47 | 0 / 0 | Google Ads MCP Server，直接用于 Ads 账户、Campaign 与效果数据访问。证据：[README](https://github.com/gomarble-ai/google-ads-mcp-server/blob/4f922abc8f9932a5080052a222a5edb86d7a3697/README.md)。 |
| 25 | [DV0x/creative-ad-agent](https://github.com/DV0x/creative-ad-agent/tree/751b9e5146604dc65049bd0f62dcbdad6212f8a3) | 131 / 28 | +2 / 0 | 广告创意 Agent，直接面向广告文案/视觉创意生成和优化。证据：[README](https://github.com/DV0x/creative-ad-agent/blob/751b9e5146604dc65049bd0f62dcbdad6212f8a3/README.md)。 |
| 26 | [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent/tree/2daf3f80f31a16f40c74fbd7fc603a5def24cb61) | 128 / 25 | +8 / +1 | 开源 Paid Media Agent，明确覆盖 Google Ads、Meta Ads、Reddit、LinkedIn、X 和 OpenAI Ads 的分析、报告及经审阅变更。证据：[README](https://github.com/langchain-ai/paid-media-agent/blob/2daf3f80f31a16f40c74fbd7fc603a5def24cb61/README.md)、[`docs/architecture/background-and-progress.md`](https://github.com/langchain-ai/paid-media-agent/blob/2daf3f80f31a16f40c74fbd7fc603a5def24cb61/docs/architecture/background-and-progress.md)。 |
| 27 | [amekala/ads-mcp](https://github.com/amekala/ads-mcp/tree/1fbb85c11ad71776919c64912b08bb0f9d003861) | 107 / 23 | +2 / 0 | Ads MCP，面向广告平台账户、Campaign 和投放数据操作。证据：[README](https://github.com/amekala/ads-mcp/blob/1fbb85c11ad71776919c64912b08bb0f9d003861/README.md)。 |

## 低热度观察：8 个直接相关项目

这些项目广告投放相关性明确，但当前 Stars 不足 100，暂不与主表项目混排。

| 项目 | Stars / Forks | 相对 11-08 | 观察理由与证据 |
|---|---:|---:|---|
| [mikusnuz/meta-ads-mcp](https://github.com/mikusnuz/meta-ads-mcp/tree/ccb44893acbe860b3b4d239de9ea829b75e50d9b) | 94 / 26 | 新发现 | Meta Marketing API v25.0 MCP，README 和工具直接覆盖 Campaign、Ads、Audiences、Budget、Creatives、Insights。 |
| [imrenagicom/adsctl](https://github.com/imrenagicom/adsctl/tree/c244f0da6536e7afc0b38d42fe245cbffc7f6988) | 76 / 6 | 新发现 | 广告 CLI/Skill，支持可恢复的 Campaign launch，适用于 shell 或 AI Agent。证据：[README](https://github.com/imrenagicom/adsctl/blob/c244f0da6536e7afc0b38d42fe245cbffc7f6988/README.md)。 |
| [Bin-Huang/google-ads-open-cli](https://github.com/Bin-Huang/google-ads-open-cli/tree/d848bb410e38a7f28fcb36abc0aeed2b16b4df82) | 48 / 5 | 新发现 | Google Ads CLI 与 Agent Skills，源码含 Campaign/targeting 命令。证据：[README](https://github.com/Bin-Huang/google-ads-open-cli/blob/d848bb410e38a7f28fcb36abc0aeed2b16b4df82/README.md)。 |
| [prebid/salesagent](https://github.com/prebid/salesagent/tree/b42c810498a5eec298afbd11201df4932ce2700c) | 40 / 60 | +1 / 0 | 基于 AdCP Media Buy 的媒体销售 Agent，涉及广告目标定向、媒体交易和订单执行。证据：[README](https://github.com/prebid/salesagent/blob/b42c810498a5eec298afbd11201df4932ce2700c/README.md)。 |
| [aws-solutions-library-samples/guidance-for-advertising-agents-on-aws](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/tree/646214fa6c88c659adec57d02acc2749b8be9130) | 22 / 8 | 0 / 0 | AWS 广告 Agent 参考实现，包含媒体规划、受众、Campaign、实时竞价与 publisher revenue demo。证据：[README](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/blob/646214fa6c88c659adec57d02acc2749b8be9130/README.md)。 |
| [Synter-Media-AI/mcp-server](https://github.com/Synter-Media-AI/mcp-server/tree/7ed94f094f68a968b8676f0780295df8f535433e) | 21 / 4 | 0 / 0 | 多广告平台 MCP，声明读取 43 个广告平台、16 个核心平台的受控 Campaign 写入及 spend guardrails；含 `skills/synter-ads/SKILL.md`。证据：[README](https://github.com/Synter-Media-AI/mcp-server/blob/7ed94f094f68a968b8676f0780295df8f535433e/README.md)。 |
| [spotify/ads-agentic-tools](https://github.com/spotify/ads-agentic-tools/tree/1647e6c6fbd7304f5e3c721045d75be641584a0b) | 20 / 21 | 新发现 | Spotify 广告 Campaign Agent，支持创建 Campaign、受众定向、启动广告和拉取效果报告。证据：[README](https://github.com/spotify/ads-agentic-tools/blob/1647e6c6fbd7304f5e3c721045d75be641584a0b/README.md)。 |
| [ynnickw/adport](https://github.com/ynnickw/adport/tree/9382eb06a3c6dfc9b25c8a2d197a2d2d8220d992) | 19 / 8 | +1 / 0 | 多平台 Ads 管理，提供账户连接、媒体操作、分析及 policy-guarded writes。证据：[README](https://github.com/ynnickw/adport/blob/9382eb06a3c6dfc9b25c8a2d197a2d2d8220d992/README.md)。 |

## 本期 HEAD 变化

以下项目相对 2026-11-08 快照的默认分支 HEAD 发生变化。这里只记录静态提交变化，不自动推断功能升级或生产行为变化。

- [google/meridian](https://github.com/google/meridian/compare/d90919820b788e217810d8d53ea6ba7bb563fd2f...d8c182861a77e90dfc4cadfeed9b840d82cb91de)
- [googleads/google-ads-mcp](https://github.com/googleads/google-ads-mcp/compare/84aebf819eebc3d8dda6ee693c1bdb5fcf5d36d9...cda852701fb5787dc4d79281f37da795ac09b97d)
- [GML-MMGroup/AdCraft](https://github.com/GML-MMGroup/AdCraft/compare/1f7acdb170d773607a7912568bd2185f00191e42...29c8f2c8abc985d0181c4531f12b21a7ee9df864)
- [About-Intelligence/soku-cli](https://github.com/About-Intelligence/soku-cli/compare/125cb25fbdc2659c1088f7a3d657beaa54d7c60c...e88e2e0571ab5367d57c617e3677bee761f8265a)
- [langchain-ai/paid-media-agent](https://github.com/langchain-ai/paid-media-agent/compare/895c2cbd332ca669f7f826f63b601456b899c4e8...2daf3f80f31a16f40c74fbd7fc603a5def24cb61)
- [prebid/salesagent](https://github.com/prebid/salesagent/compare/a7a4c53f8f3dd22dee0ff90c30b5db4185da4a27...b42c810498a5eec298afbd11201df4932ce2700c)
- [AWS advertising agents guidance](https://github.com/aws-solutions-library-samples/guidance-for-advertising-agents-on-aws/compare/e3cd9035a1c40bee9e74de55c6e4e8ae755c4bc8...646214fa6c88c659adec57d02acc2749b8be9130)
- [Synter MCP server](https://github.com/Synter-Media-AI/mcp-server/compare/cc1e8bb5af31b915dc9cf423b1edbdd2bf239937...7ed94f094f68a968b8676f0780295df8f535433e)
- [adport](https://github.com/ynnickw/adport/compare/84a27097b28172005cca4a09a10d324a2970fa61...9382eb06a3c6dfc9b25c8a2d197a2d2d8220d992)

## 排除项目：7 个

这些项目被检索命中，但本期不推送：

- [itallstartedwithaidea/advertising-hub](https://github.com/itallstartedwithaidea/advertising-hub/tree/b434ed0f0beaa22fb9b1b2aa6b790a75f9f87545)：README 方向相关，但大量能力仍标为 `Spec Ready`/`Planned`，缺少已验证的直接投放功能。
- [jshorwitz/awesome-agentic-advertising](https://github.com/jshorwitz/awesome-agentic-advertising/tree/c0f848484290dfd7430c13a4044db9624b05b5d2)：广告 Agent 资源清单，不是可验证的直接投放项目。
- [attainmentlabs/meta-ads-mcp](https://github.com/attainmentlabs/meta-ads-mcp/tree/5e3d18dc134c3ab3e53a2ddb30264187b2629fd1)：未达到本期对现成功能证据的门槛。
- [adsuploader/meta-ads-mcp](https://github.com/adsuploader/meta-ads-mcp/tree/d33ce681c802b449c0fadb8726ee82bd80cacd7f)：未达到本期对现成功能证据的门槛。
- [mrpaidsocial/hermes-ad-agent](https://github.com/mrpaidsocial/hermes-ad-agent/tree/9a705dffa5827269d75e23b3f136309fbb3f321)：未达到本期对现成功能证据的门槛。
- [bartlomiejborzucki/meta-ads-agent](https://github.com/bartlomiejborzucki/meta-ads-agent/tree/98701b34f8f4d80d002e3f7aadd8e3b9ca63e4c3)：未达到本期对现成功能证据的门槛。
- [get-mcp-ads/meta-ads-mcp-server](https://github.com/get-mcp-ads/meta-ads-mcp-server/tree/52fa3417b0695a96409e61333ab0eb0a5a6f9a13)：未达到本期对现成功能证据的门槛。

## 检索范围与验证边界

- 检索词共 4 组：`"Google Ads" agent OR "Meta Ads" agent`、`paid media agent`、`advertising agentic advertising AI`、`ads MCP advertising campaign`。
- 来源快照：[2026-11-13-github-snapshot.json](../sources/2026-11-13-github-snapshot.json)，SHA-256：`21719e4c476faca01e0e04aef0f64245223fb212c64e019298f5397c8cf38e74`。
- 本期以 GitHub 公开仓库元数据、README 和固定 HEAD 源码为主要证据；无法固定、无法复核的热度不纳入排序。
- 未安装或运行任何候选项目。
- 未登录任何广告账户，未创建 Campaign，未修改预算，未发起媒体购买，也未验证真实投放效果、转化或 ROAS。
- Stars/Forks 是公开关注度代理，不代表项目质量、生产可用性、广告账户权限或业务结果。
