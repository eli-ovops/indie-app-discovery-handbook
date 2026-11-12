# Starter Story 近 20 条视频整理与方法提炼

> 采集日期：2026-07-31（Asia/Shanghai）  
> 研究范围：4 条指定视频 + Starter Story 官方频道 Videos 页当前最近 20 条常规公开视频  
> 取证方式：`agent-reach` 路由至 `yt-dlp`；逐条执行 `--dump-json` 获取元数据，优先检查人工字幕，再下载自动字幕并清理滑动重复行。  
> 重要限制：本文不把标题、简介、主持人或嘉宾自报的收入当作外部已验证事实；除明确写出“画面展示”外，数字均是【视频中明确陈述】【未经外部验证】。

## 一、范围、频道身份与完成度

### 1. 官方频道身份

- 官方频道名：Starter Story
- 唯一 channel ID：`UChhw6DlKKTQ9mYSpTfXUYqA`
- Canonical channel URL：[https://www.youtube.com/channel/UChhw6DlKKTQ9mYSpTfXUYqA](https://www.youtube.com/channel/UChhw6DlKKTQ9mYSpTfXUYqA)
- Canonical handle URL：[https://www.youtube.com/@starterstory](https://www.youtube.com/@starterstory)
- 判定依据：两条指定 Starter Story 原视频及官方 Videos 页逐条元数据的 `channel_id` 一致。

### 2. 指定视频并非全部属于 Starter Story

1. `n7Obxh9-Rc8`：Starter Story 官方上传。
2. `Uoav-kiMbM8`：实际上传者为 One Person Business，channel ID `UC5sGRuouCtllvIEL1q8ay0Q`。
3. `rGLXc1GmsaI`：Starter Story 官方上传。
4. `S82teqWkATY`：实际上传者为“然冉创业说”，channel ID `UCEczTn9zhrGSalzNP-FUY5A`。

因此，本文完整保留四条指定链接，但“近期 20 条”只从上述唯一 Starter Story 官方频道取得，没有把转载、同名账号或其他创业频道混入。

### 3. 计数结论

- 指定视频：4 条。
- 官方频道近期常规公开视频：20 条。
- 指定视频与近期 20 条重合：1 条（`n7Obxh9-Rc8`）。
- 去重后实际样本：23 条。
- 近期 20 条均为约 10–19 分钟的常规长视频；没有 Shorts、预告片或纯直播占位，也没有需要特别保留的直播回放。
- 正文取得情况：人工字幕 0；自动字幕 22；自行转写 0；无法取得正文 1。
- 无正文者：`S82teqWkATY`。平台没有人工或自动字幕；`agent-reach transcribe` 兜底因本机未配置 Groq/OpenAI provider key而不可用。未向用户索取或记录密钥，也未用标题/简介冒充正文。

## 二、完整视频清单

| 序号 | 身份 | 标题 | 日期 | 时长 | 上传者 | 字幕来源 | 链接 |
|---:|---|---|---|---:|---|---|---|
| 1 | 指定＋近期 | I Grew My SaaS From $17K to $143K MRR in 4 Months | 2026-07-30 | 16:11 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=n7Obxh9-Rc8) |
| 2 | 近期 | $18K/Month From This Ridiculously Simple App Idea | 2026-07-26 | 15:36 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=V_4kiR3R4QU) |
| 3 | 近期 | I Make $50K Per Month Working 5 Hours A Week | 2026-07-23 | 13:49 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=DPb-M0Vt4uI) |
| 4 | 近期 | This Stupidly Simple App Makes $100K/Month | 2026-07-19 | 17:35 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=EQfZCe3MkTU) |
| 5 | 近期 | I Quit My Job at Meta to Build a $30K/Month SaaS | 2026-07-15 | 15:00 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=2_lpZ503ZGg) |
| 6 | 近期 | She Built This $340K/Month App in 60 Days | 2026-07-12 | 16:48 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=Eg93po_DAYo) |
| 7 | 近期 | This Insanely Simple App Makes $50K/Month | 2026-07-05 | 19:16 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=uvIcGuN2iO8) |
| 8 | 近期 | How I Work: $10M/Year Serial Entrepreneur | 2026-07-01 | 11:28 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=jjUf7lrb_xQ) |
| 9 | 近期 | How We Built This $20K/Month AI App | 2026-06-28 | 13:11 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=DiRxTfnHTaY) |
| 10 | 近期 | I Turned This Spreadsheet Into a $30K/Month Micro-SaaS | 2026-06-24 | 12:24 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=d8PdJJcEtE0) |
| 11 | 近期 | I Built a $10K/Month App With This One System | 2026-06-21 | 15:19 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=-VlJIgj6gM4) |
| 12 | 近期 | The First App I Ever Built Makes $25K/Month | 2026-06-14 | 18:00 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=Q4k8JNYKJT0) |
| 13 | 近期 | I Built A $1M SaaS In A Hidden Niche | 2026-06-10 | 13:21 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=NPpky92ZfjA) |
| 14 | 近期 | I Built Two Apps That Make $120K/Month | 2026-06-07 | 14:50 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=xWnqY2Mav4s) |
| 15 | 近期 | I Built A $30K/Month App: Here's My Exact Process | 2026-05-31 | 14:13 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=P4QodeA_lQ0) |
| 16 | 近期 | I Built A Micro-Version Of A $1B SaaS. Now I Make $50K/Month | 2026-05-28 | 11:47 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=Nnpz1wsTjBI) |
| 17 | 近期 | I Built A $30K/Month in 35 Days | 2026-05-24 | 18:20 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=vbEKEWtnndU) |
| 18 | 近期 | I Make $1.7M/Year In The Most Boring Niche Imaginable | 2026-05-21 | 16:23 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=BHhg-l9AZpM) |
| 19 | 近期 | My Two Apps Make $150K/Month Each | 2026-05-17 | 16:32 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=32vqaJa90kw) |
| 20 | 近期 | I Built a $20K/Month App in 83 Days | 2026-05-10 | 16:14 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=r4R_Hlw7sbo) |
| 21 | 指定 | Claude AI + YouTube = $72,000/Month | 2026-06-23 | 17:45 | One Person Business | 自动英文 | [YouTube](https://www.youtube.com/watch?v=Uoav-kiMbM8) |
| 22 | 指定 | How This App Makes $35K/Month | 2026-04-05 | 21:48 | Starter Story | 自动英文 | [YouTube](https://www.youtube.com/watch?v=rGLXc1GmsaI) |
| 23 | 指定 | ChatGPT 5.6 + Hostinger：4个AI副业，帮你2026年暴富。今年赚钱，究竟应该怎么做？ | 2026-07-20 | 13:00 | 然冉创业说 | 无法取得 | [YouTube](https://www.youtube.com/watch?v=S82teqWkATY) |

## 三、逐条中文内容卡

### 1. Postiz：从 $17K 到 $143K MRR（指定＋近期）

- 元数据：[视频](https://www.youtube.com/watch?v=n7Obxh9-Rc8)，2026-07-30，16:11；自动英文字幕。
- 一句话结论：已有真实产品和客户基础时，快速重定位到新的接口/代理范式，再配合趋势内容分发，可能比从零追热点更有胜率。
- 内容结构与观点：先展示 Postiz 的 MRR 与订阅者面板，再解释从普通社媒排程工具转为可被 Claude、OpenClaw 等代理调用的“agentic”工具；随后讨论趋势内容、低价 KOL repost、团队扩充、降 churn 和可靠性。主持人最后明确反对“只有趋势、没有产品”的空壳跟风。
- 数字与方法：【画面/视频陈述】创始人 Nevo 称 MRR 从约 $17K 在 4 个月升至 $143K、约 4,271 付费订阅者，曾按 $60–$350 购买影响者 quote repost；称 churn 从约 26%–28%降至 13.7%。方法是先有可用产品，再在 OpenClaw/代理话题升温时密集发布高度相关内容、改 API/产品定位、减少易坏功能并提高可靠性。
- 成功条件/失败原因：成功依赖既有产品、被新代理生态调用的技术适配、趋势时点、内容执行和可承接流量的稳定性。只复制“agentic”标签，没有产品/客户/接口，会失去核心前提。
- 对当前方向：可借鉴“已有付费工具 × 新分发/接口窗口”的交叉，而不是凭热词造产品；第一笔收入仍应来自原问题的真实付费，不应等待趋势替代验证。
- 边界与置信度：增长、订阅、churn 为【视频中明确陈述/画面展示】【未经外部验证】；“代理推荐可带到 $1M/月”是主持人【推断】，不能当预测。

### 2. Cat on Chair：设计差异化的番茄钟

- 元数据：[视频](https://www.youtube.com/watch?v=V_4kiR3R4QU)，2026-07-26，15:36；自动英文字幕。
- 一句话结论：成熟品类仍可通过强审美、具体人格和自然可传播性切入，但“偶然病毒传播”不是可复制的获客计划。
- 结构与观点：Ryan 从产品设计师转为开发者，与女友把手作项链中的“椅子上的猫”视觉转成番茄钟；重点不是功能创新，而是手工感、目标地域用户和文化传播。
- 数字与方法：【视频陈述/画面】称过去 30 天约 $18K、累计 127K 下载、当期约 24K 首次下载；年费 $19.99、终身 $29.99；首周约 3,000 下载。先做视觉原型，再用 AI 工具完成 iOS 产品，面向亚洲审美用户；RedNote 小爆发后被 Instagram app-collection 账号收录，再经台湾 Threads 二次传播。
- 成功条件/失败原因：创始人的设计能力与女友独特视觉资产不可忽略；普通番茄钟若只有换皮，没有可识别风格和分享理由，难以复现。
- 对当前方向：适合验证“同质功能 + 强视觉/文化定位”的轻量产品，但应先做素材/落地页测试或小范围付费，不把一次自然扩散当常态。
- 边界与置信度：收入、下载和价格为【视频中明确陈述】【未经外部验证】；传播链由嘉宾回忆，归因不完整。

### 3. ChartDetector AI：用 TikTok 付费广告买增长

- 元数据：[视频](https://www.youtube.com/watch?v=DPb-M0Vt4uI)，2026-07-23，13:49；自动英文字幕。
- 一句话结论：付费广告不是“投钱就增长”，而是 onboarding、硬 paywall、归因、素材和单位经济性先闭环后的放大器。
- 结构与观点：从 Telegram 股票图表分析 bot 转成移动 app；嘉宾逐步讲 onboarding、事件追踪、TikTok 创意、国家选择、预算扩张和利润监控。
- 数字与方法：【视频陈述】13 个月约 90K 下载、累计约 $260K 收入、当期约 $56K/月、月下载 13K–14K；周订阅约 $12.99、半年 $59.99；某月称收入 $43.7K、广告约 $20K、Apple 费约 15%、净利约 $11.5K、利润率约 25%；月 TikTok 投入约 $18K。素材先小预算测试，按 CPI/LTV/ROAS 判定，约每 3 天最多加 20%预算，避免学习阶段重置。
- 成功条件/失败原因：需要可测归因、明确 LTV、现金垫付能力和持续素材供给；硬 paywall 无试用可能提高现金回收，也可能伤害信任/留存，不能无条件照搬。
- 对当前方向：第一笔收入阶段不适合直接复制高广告投入；可先把广告当“付费意向实验”，用很小预算验证点击→安装→付款链。
- 边界与置信度：数据为【视频中明确陈述/部分画面展示】【未经外部验证】；股票/健康等敏感品类另有合规风险。

### 4. Go Tall：从 TikTok 评论发现身高预测需求

- 元数据：[视频](https://www.youtube.com/watch?v=EQfZCe3MkTU)，2026-07-19，17:35；自动英文字幕。
- 一句话结论：评论、DM 和早期付款比“大家说有兴趣”更强；情绪强、可演示、可生成个性结果的需求天然适合内容分发。
- 结构与观点：创始人 Michael 在同类 app 出售信息和 TikTok 评论中看到需求，也联想到自己 13 岁搜索身高计算器的经历；两天后获得首单；随后从自己做内容到 UGC，再把已验证素材变成付费广告。
- 数字与方法：【视频陈述】约 700K iOS 下载、Android 数十万；首发两天首单；早期 10–20 个 DM/天请求预测；第 5 个月约 $30K/月，后用广告放大到约 $100K/月。先用评论回复式“帮你预测”内容验证格式，约一个月纯内容实验，再扩大创作者和广告。
- 成功条件/失败原因：强焦虑/自我改善动机、立即可见结果、内容可重复生产；身高预测的科学准确性、未成年人、夸大承诺和平台政策是重大边界。
- 对当前方向：可借鉴“公开求助/评论 → 可演示小工具 → 首单”路径；不应复制靠焦虑放大的敏感承诺。
- 边界与置信度：数字为【视频自述】【未经外部验证】；“明确知道 100K views 对应下载”只说明其内部归因经验，不具普适性。

### 5. Live Tourney：从自己办高尔夫赛事切入

- 元数据：[视频](https://www.youtube.com/watch?v=2_lpZ503ZGg)，2026-07-15，15:00；自动英文字幕。
- 一句话结论：业余爱好中的重复组织工作，是比抽象“热门赛道”更可靠的产品发现入口。
- 结构与观点：Matt 办高尔夫赛事时使用过 Golf Genius，随后为自己的活动做 Live Tourney；边在 Meta 全职工作边经营约四年，最终讨论是否离职。
- 数字与方法：【视频陈述】称约 $30K/月、约 $350K ARR，年初表现对应约 $800K run rate；在 Meta 约 6 年。先服务自己的赛事，再扩到同类组织者；薪资和福利承担早期风险。
- 成功条件/失败原因：创始人真正在该活动网络内、懂赛事工作流并能接触首批客户；“喜欢某项运动就做软件”仍需核验组织者付费、替代品和销售周期。
- 对当前方向：适合从高频爱好/小商家操作中找第一位真实使用者；不应把“辞职”当里程碑，第一笔收入和可持续获客更重要。
- 边界与置信度：收入与 run rate 为【视频中明确陈述】【未经外部验证】；离职选择受个人财务、家庭和福利约束，不能复制。

### 6. Stella：个人品牌先于 manifestation app

- 元数据：[视频](https://www.youtube.com/watch?v=Eg93po_DAYo)，2026-07-12，16:48；自动英文字幕。
- 一句话结论：这是“已有巨量受众再产品化”的案例，不是零受众创业者两天做 app 就能复现的基线。
- 结构与观点：Sarah 从自己长期做冥想、affirmation、女性向内容的经验中发现“个性化 visualization/meditation”空位；两天做 MVP，2–3 个月成品；内容先验证痛点、格式和语言，再引流 app。
- 数字与方法：【视频陈述】称 2 个月超过 $300K MRR、约 200K 下载；Instagram 约 1.2M 粉丝、TikTok 约 2.8M，另有约 700K 粉账号。用“连续 7 天/听 3 次”等高收藏格式、评论观察、ManyChat、评论/评价激励和 app demo 内容转化。
- 成功条件/失败原因：巨量受众、成熟内容能力、女性用户洞察和已有信任是核心资产；如果没有这些，开发速度并不能创造相同分发。
- 对当前方向：可借鉴“先做内容/服务并观察高保存、高复访行为，再产品化”；不可拿其 MRR 作为新账号/小团队预测。
- 边界与置信度：数字均为【视频中明确陈述】【未经外部验证】；manifestation 有效果承诺与心理健康边界。

### 7. Erly：push-up alarm 与影响者分成

- 元数据：[视频](https://www.youtube.com/watch?v=uvIcGuN2iO8)，2026-07-05，19:16；自动英文字幕。
- 一句话结论：把普通刚需加上可拍成视频的行为钩子，再尽早用影响者真实带货结果验证，比继续堆功能更有效。
- 结构与观点：Jake 利用 iOS 26 AlarmKit，使闹钟必须通过俯卧撑关闭；19 天上线，7 天后首个影响者视频；购买出现后才确认并扩大。
- 数字与方法：【视频陈述】约 200K 下载、4 个月约 $50K/月；第一个影响者视频后三周累计首个 $1K，第三个月约 $30K、第四个月约 $50K。影响者按观看量/分成等方式合作，用追踪工具和收入尖峰估算效果。
- 成功条件/失败原因：平台新 API、强视觉动作、痛苦问题、影响者匹配和创意供给；视频也承认存在 luck/timing，影响者归因“极难”。
- 对当前方向：可测试“产品结果是否能在 10 秒内看懂并产生下一动作”；先验证一条内容能否带来付费，不先扩团队。
- 边界与置信度：增长为【视频自述】【未经外部验证】；归因不精确，平台窗口会消失。

### 8. Sam Parr：工作系统而非产品案例

- 元数据：[视频](https://www.youtube.com/watch?v=jjUf7lrb_xQ)，2026-07-01，11:28；自动英文字幕。
- 一句话结论：可取的是快速行动、从谈话中追问具体问题和用 AI 减少研究准备；“高强度生活方式”不构成市场验证。
- 结构与观点：展示 Sam Parr 的晨间运动、限制手机、访谈/工作流程、从大量播客访谈学习、与人交谈时连续追问“哪里不开心/问题是什么”，以及用 Claude 自动研究来宾。
- 数字与方法：【视频陈述】称其公司合计年收入超过 $10M；日常约每周运动 6 天。并未给出某个小产品的定价、首单或获客账本。
- 成功条件/失败原因：其资源、团队、品牌和长期经验远超初始创业者；日程模仿无法替代需求证据。
- 对当前方向：只采用“问题访谈与快速小实验”，删除“半年后会领先”等口号。
- 边界与置信度：收入为【个人自述】【未经外部验证】；本卡不把生产力习惯列为产品成功因果。

### 9. 3AK：田径内容账号产品化

- 元数据：[视频](https://www.youtube.com/watch?v=DiRxTfnHTaY)，2026-06-28，13:11；自动英文字幕。
- 一句话结论：既有垂直内容受众和创始人身份匹配，远比“零代码”本身更能解释首批用户。
- 结构与观点：两位大学生已有田径内容影响力，做训练/动作/社区 app；用 Claude 处理卡点，强调从自己擅长的网球、田径等垂直领域发现问题。
- 数字与方法：【视频陈述】约 40K 用户、6 个月约 $70K、当期约 $20K/月；称上架成本可低于 $500；此前交易亏损约 $3K。产品价格以年轻运动员能承受的 $10–$20 区间为思路。
- 成功条件/失败原因：已有数十万田径关注者、真实运动语境、内容信任；“无技术背景”叙事会掩盖其分发资产和高强度工作。
- 对当前方向：可以先经营/进入一个明确社区，再把已反复出现的训练记录或反馈工作流产品化；不能把上架成本等同总获客成本。
- 边界与置信度：数据为【视频自述】【未经外部验证】。

### 10. Profit AI：把服务中的表格变成 B2B 工具

- 元数据：[视频](https://www.youtube.com/watch?v=d8PdJJcEtE0)，2026-06-24，12:24；自动英文字幕。
- 一句话结论：已经被客户反复使用并愿意为服务付费的表格/流程，是最接近“已有付费市场”的轻量 SaaS 种子。
- 结构与观点：Jack 长期为电商/agency 做利润与广告分析表，先在服务中使用，后把 CSV/表格交给 Cursor/Claude Code转为 Shopify app；服务客户成为最早付费者，增长主要靠口碑。
- 数字与方法：【视频陈述】app 自上线累计约 $147K、约 $30K MRR，服务约 $40K MRR；122 用户、47 安装/43 卸载；原定价 $5K/月只有少数客户，降至 $800/月；开发约 3.5–4 个月。方法是先出售高价服务、观察重复表格、再软件化。
- 成功条件/失败原因：创始人已有客户、领域知识、数据接入和服务收入；卸载/安装比显示 churn 高，且 app 与服务收入混在叙事里，需要谨慎拆分。
- 对当前方向：高度适合“先获得第一笔产品收入、验证已有付费市场”——优先找客户已经用表格/人工解决且支付服务费的任务。
- 边界与置信度：数字为【视频陈述/部分画面】【未经外部验证】；不能把服务 MRR 当纯 SaaS。

### 11. Flame 与 VSC：先验证内容的病毒性、可持续性、转化

- 元数据：[视频](https://www.youtube.com/watch?v=-VlJIgj6gM4)，2026-06-21，15:19；自动英文字幕。
- 一句话结论：内容能传播不等于能卖产品，需同时测试 viral、sustainable、conversion（VSC）。
- 结构与观点：Flame 是情侣每日问题/AI relationship coach；团队先在 TikTok 检查同类痛点与格式是否传播，再用大量账号、UGC/AI 内容和表格追踪 hook、观看、产品意图。
- 数字与方法：【视频陈述】称约 250K 下载、50M+ organic views，8 个月从约 $3K 到 $10K MRR；目标人群是认为关系需改善但不愿付 $200 therapy 的情侣；早期 UGC 曾约 $1/60 秒。用表格记录账号、hook、内容格式和转化；避免只追高播放的泛内容。
- 成功条件/失败原因：需要内容与产品意图同场出现、格式可长期重复、账号/素材实验规模；“50M view 只到 $10K MRR”本身也说明播放不等于高价值商业结果。
- 对当前方向：在开发前先用内容测试：有人看、能重复、会点击/留下邮件/付费，三项缺一不可。
- 边界与置信度：视频中未展示当前完整收入面板（称处于出售过程）；数据为【创始人自述】【未经外部验证】。

### 12. ToneAdapt：自己的吉他痛点 + 多平台日更

- 元数据：[视频](https://www.youtube.com/watch?v=Q4k8JNYKJT0)，2026-06-14，18:00；自动英文字幕。
- 一句话结论：小而明确的爱好痛点，可先在同好评论区确认，再用真实演示内容快速获取第一笔产品收入。
- 结构与观点：Kyan 想匹配吉他音色，先问 Reddit/Instagram 评论区的吉他手，再约一周用 Cursor 做出 web/app；从第一天露脸发布产品解决过程。
- 数字与方法：【视频陈述/画面】约 100K 用户、5 个月约 $25K/月；周费约 $10、年费约 $60；近四周网站约 $11.5K、移动端约 $14K、397 活跃订阅；三个月网站约 $45K、1,400 新订阅。每天发 3 条并跨 TikTok/Instagram/YouTube/Facebook，找到胜出格式后做 50 个变体、每月让 UGC 创作者复刻约 60 条。
- 成功条件/失败原因：本人是目标用户、演示前后差异清楚、有 UGC 经验；高频周订阅和内容规模可能带来退款、疲劳及运营成本，视频未完整披露。
- 对当前方向：这是较贴合当前方向的路径：个人真实痛点→同好确认→一周 V1→当天可付款→第一天营销。
- 边界与置信度：数字为【视频中明确陈述/画面展示】【未经外部验证】。

### 13. Hiro Analytics：agency 作为聚合客户

- 元数据：[视频](https://www.youtube.com/watch?v=NPpky92ZfjA)，2026-06-10，13:21；自动英文字幕。
- 一句话结论：卖给服务许多终端客户的 agency，可用一次销售获得多席位和同质需求，但前提是长期行业经验。
- 结构与观点：Zac 先经营 email/SMS marketing agency 约 6 年，再做面向同类 agency 的自动化报表；一个 agency 可能带来 10–20 用户和多个客户席位。
- 数字与方法：【视频陈述】上线约 19 个月到 $1M ARR、当期约 $90K MRR、每月增加约 $10K MRR；额外客户席位约 $200/月；30 天免费试用。通过平台 directory 找 agency，以“接更多客户但不增员”的利益销售。
- 成功条件/失败原因：同平台、同工作流、可量化省时；早期 AWS/Snowflake 成本高，且底层平台可能自建功能。主持人承认“19 个月”背后其实有约 10 年相关学习。
- 对当前方向：优先研究“一个客户能带来多个终端使用者”的聚合渠道；不适合无行业经验者直接复制重数据栈。
- 边界与置信度：收入、churn 和增速为【视频自述/画面】【未经外部验证】。

### 14. Cardstock / Scanémon：从收藏爱好解决自己的问题

- 元数据：[视频](https://www.youtube.com/watch?v=xWnqY2Mav4s)，2026-06-07，14:50；自动英文字幕。
- 一句话结论：在自己长期参与的爱好中记录“我今天又手工查了什么”，比泛搜索 app idea 更容易获得明确用户和数据源。
- 结构与观点：Kyle 围绕卡牌收藏识别/估值与 Pokémon 扫描做两款 app；先解决自己需求、发 Reddit update，再以 TikTok slideshow/创作者分发。
- 数字与方法：【视频陈述】两款合计约 $120K/月；Cardstock 约 15K 订阅、最高约 $75K MRR、月下载约 13K；Scanémon 约 3.4K 订阅、$17K MRR、月新客户约 16K。采用 Swift/SwiftUI、RevenueCat/Superwall 类订阅基础设施。
- 成功条件/失败原因：长期爱好知识、可获取卡牌/成交数据、相机识别价值清楚；“先解决自己”只证明问题存在，不证明足够多人愿付费，仍需外部承诺。
- 对当前方向：适合从收藏、手工、运动等现有社区做第一批访谈和付费预售；记录问题清单后按重复频率筛选。
- 边界与置信度：数据为【视频自述】【未经外部验证】；标题“$120K/月”与分项展示并非完全相加一致，可能含其他收入/时间口径。

### 15. Snag：4–5 小时建 app，长期难点仍是创意与广告

- 元数据：[视频](https://www.youtube.com/watch?v=P4QodeA_lQ0)，2026-05-31，14:13；自动英文字幕。
- 一句话结论：快速开发的价值是压缩试错成本，不是跳过选题、留存与分发。
- 结构与观点：Benji 称一年做 45+ apps 后才集中 Snag（寻找附近免费物品）；先定义 3 秒内的价值展示、Figma 线框、Claude Code 实现，再以 UGC 找胜出素材并转 Meta Ads。
- 数字与方法：【视频陈述/画面】Snag 约 $30K MRR、100K authenticated users、9K conversions、累计 proceeds 超 $80K、约 3.3K App Store ratings；基础前端约 4–5 小时（不含后端）；100 个 creator 候选约筛出 9–10 个，某素材累计投约 $3K 后 ROAS 转负。
- 成功条件/失败原因：大量前序失败形成选题/创意能力、团队和广告预算；视频也承认 shiny-object syndrome，45 个 app 不是成功率。
- 对当前方向：把“快速做”放在通过需求/内容门槛之后；每次实验先写停止条件、付费信号和素材假设。
- 边界与置信度：收入等为【视频自述/画面】【未经外部验证】；4–5 小时不含后端、上架、QA、运营和营销。

### 16. Shipper：成熟大市场的微型版本

- 元数据：[视频](https://www.youtube.com/watch?v=Nnpz1wsTjBI)，2026-05-28，11:47；自动英文字幕。
- 一句话结论：已有竞争与付费市场不是坏事；关键是找到可验证的具体缺口，而不是口号式“拿 1% 市场”。
- 结构与观点：David/兄弟观察 Lovable、Base44 等 AI app builder，针对非技术用户害怕术语的问题，做更简化的 Shipper；Product Hunt 首发、Reddit 起量、竞品词 SEO、X 和 affiliate 后续。
- 数字与方法：【视频陈述/画面】称 gross volume 约 $50K–$71K/月，但面板 MRR 约 $25.6K、ARR 约 $307K；最低 $25/月；Product Hunt 首周约 $50 MRR，Reddit 从 $50 推到约 $1K MRR。研究竞品公开 roadmap、Discord 和抱怨，做“alternatives to X / X costs”高意图 SEO。
- 成功条件/失败原因：大市场、明显非技术细分、能跟随竞品节奏；“1%”不是验证，且标题把 gross volume 与 MRR 混用。
- 对当前方向：采用“已付费市场→竞品差评/流失点→一个窄差异→高意图页面/首单”，避免先算 TAM 再假设获得 1%。
- 边界与置信度：面板口径存在差异；均【未经外部验证】。

### 17. Pep AI：peptide 趋势窗口

- 元数据：[视频](https://www.youtube.com/watch?v=vbEKEWtnndU)，2026-05-24，18:20；自动英文字幕。
- 一句话结论：趋势能降低获客阻力，但窗口短、合规重，必须把等待名单和真实付款与平台风险一起判断。
- 结构与观点：Cedric 在 TikTok 发现 peptide 热度，研究同类 app 评论，2 周用 Claude/Replit 构建；发布前 Reddit 帖和约 300 人 waitlist，并找垂直影响者预热。
- 数字与方法：【视频陈述】7 周累计约 $50K、最近 28 天 MRR 约 $11K；年费 $45、月费 $10、3 天试用；某影响者 story 称带来约 $1K，另一帖当日约 $4K，口述单帖最高约 $10K。App Store 因医疗建议多次拒审。
- 成功条件/失败原因：趋势尚在上升、影响者信任、搜索量、快速上架；医疗/健康合规、科学准确性、审查和趋势衰退使其不适合作为普通轻量 app 模板。
- 对当前方向：可以把趋势当加分项，不能替代真实付费市场；敏感健康方向应排除或做更严格审查。
- 边界与置信度：数字和帖子归因为【视频自述】【未经外部验证】；标题 $30K/月、片中累计 $50K/7 周、MRR $11K 是不同口径。

### 18. Savvy Nomad：税务/迁居的“无聊高痛”流程

- 元数据：[视频](https://www.youtube.com/watch?v=BHhg-l9AZpM)，2026-05-21，16:23；自动英文字幕。
- 一句话结论：高付费往往来自用户不愿亲自处理、错误代价高、现有替代昂贵的流程，而不是“无聊”本身。
- 结构与观点：Savvy Nomad 帮助美国州税务迁居/相关流程，创始团队用步骤、模板、估算和必要时专业审核，把 agency 工作流产品化；强调 real demand、willingness to pay、低竞争。
- 数字与方法：【视频陈述】约 $1.7M/年、1,400 客户、6 名员工，称累计为客户节税约 $10M；传统 agency 可能收费 $8K–$15K，产品化方案可在 $1K–$2K 区间仍有价值感。工具含 Framer、Ghost、Ahrefs/SEO。
- 成功条件/失败原因：法规/专业知识、信任、错误责任和高价值结果；不能因为“竞争少”就低估法律、税务、人工审核和地域限制。
- 对当前方向：可借鉴“昂贵专业服务中可标准化的一段”，但当前小团队只应选低责任、低监管的邻近流程。
- 边界与置信度：收入/节税为【视频自述】【未经外部验证】；不构成税务建议。

### 19. Glam Up / Sprout：UGC 工厂化分发

- 元数据：[视频](https://www.youtube.com/watch?v=32vqaJa90kw)，2026-05-17，16:32；自动英文字幕。
- 一句话结论：当产品能被短视频自然演示时，UGC 可以系统化；但数百创作者的运营不是轻量项目冷启动基线。
- 结构与观点：Nicole 负责非技术部分和分发；Glam Up 面向美妆/护肤，Sprout 面向求职；先设计“社媒原生”的产品输出，再招募、培训、管理创作者并跨平台放大。
- 数字与方法：【视频陈述】Glam Up 称 6 个月 1M 用户、峰值 $150K MRR；Sprout 录屏口径约 $200K–$250K MRR；另两款 stealth app 称约 $200K MRR；月观看从约 100M 到 400M–500M。硬 paywall，周/月订阅；创作者从表单、UGC 群、Instagram、Reddit、平台招募，课程/Discord/负责人管理。
- 成功条件/失败原因：产品可视觉化、创意数据系统、招聘和管理能力；高观看不保证利润，视频未披露 creator 成本、退款、平台费和净利。
- 对当前方向：早期只需 3–10 位小创作者验证一种格式，不要先搭“内容工厂”。
- 边界与置信度：多个 app 和时间口径混合，全部【视频自述/未经外部验证】。

### 20. Once：承诺指标先于开发

- 元数据：[视频](https://www.youtube.com/watch?v=r4R_Hlw7sbo)，2026-05-10，16:14；自动英文字幕。
- 一句话结论：在写代码前设定有限时间和明确承诺人数，是本批样本中最贴近“先拿真实需求证据”的方法。
- 结构与观点：Once 是活动/婚礼共享一次性相机式相册；先在朋友 Halloween party 用 web 版观察真实使用，再规定 commitment metric；列 250–300 位潜在活动用户，发 2–3 句个性化冷消息，达到承诺人数才继续。
- 数字与方法：【视频陈述】上线 83 天到约 $20K–$22K 月收入，周活约 10K–12K；小聚会约 $2，150 人婚礼约 $50。承诺可为明确使用某场活动，因场景/日期/参与者具体，强于“听起来不错”。
- 成功条件/失败原因：承诺必须与真实使用场景绑定、设置截止日并耗尽个人网络；其首次 party 版本多次坏掉，但仍验证“共同相册”核心行为。
- 对当前方向：直接采用：每个候选在开发前设“10 个明确愿在某日使用/付定金/接受付费试用”的门槛。
- 边界与置信度：收入为【视频自述】【未经外部验证】；活动承诺仍弱于付款，应尽可能升级为付费。

### 21. AI faceless YouTube 教程（指定，非 Starter Story）

- 元数据：[视频](https://www.youtube.com/watch?v=Uoav-kiMbM8)，2026-06-23，17:45；One Person Business；自动英文字幕。
- 一句话结论：教程提供了竞品格式拆解和多元变现步骤，但核心收入样本与“新算法”说法缺乏独立验证，营销漏斗利益相关性很强。
- 结构与观点：找近期爆发的 faceless 频道→建立 Claude “频道大脑”→分析竞品→AI 写长脚本/配音/视觉→剪辑→发布→用数字产品补充广告收入；同时推销其 Sollo、社区和 VC/课程入口。
- 数字与方法：【视频陈述】声称某频道 2 个月超 $70K/月、多个新频道首月百万播放、其数据库有 1,000+ 个 $5K–$50K/月频道；人工 2,000 词脚本约 $250、AI 脚本低于 $1。最后承认不是平均结果、内容农场可能触碰政策、结果不保证。
- 成功条件/失败原因：选题/格式、原创增量、持续内容能力、政策合规和数字产品转化；“复制格式”容易同质化，广告收入估算、频道真实所有者和净利未核实。
- 对当前方向：只采用“先研究可见成功格式、先做一条内容与一个付费数字产品测试”；不把 faceless 流量当低风险被动收入。
- 边界与置信度：所有频道收入/算法判断为【视频中明确陈述】【未经外部验证】；发布者同时销售工具/社区，存在明显利益冲突。

### 22. MonAI：单一垂直创作者深度合作（指定）

- 元数据：[视频](https://www.youtube.com/watch?v=rGLXc1GmsaI)，2026-04-05，21:48；自动英文字幕。
- 一句话结论：一个有分成、理解产品、长期共同迭代的垂直创作者，可能优于大量一次性 UGC，但合作匹配和归因需严谨。
- 结构与观点：Flo 的个人财务 app 自己推广约 1.5 年只有 $300 MRR；与一位哥伦比亚内容创作者合作后，用每月约 3 条高质量内容和利润分成增长；视频给出寻找、个性化外联、利益对齐步骤。
- 数字与方法：【视频陈述/画面】从 $300 MRR 到约 $35K；首条视频一周 10 倍、一个月近 $8K；一条 1.7M views 视频称增约 $5K MRR。采用 hard paywall + free trial；外联强调具体看过创作者内容、展示同品类上限、最好录带名字的个性视频。
- 成功条件/失败原因：创作者受众与产品市场完全匹配、长期分成使其“有 skin in the game”、本地化市场较少竞争；单一伙伴也是集中风险，利润口径和分成未完整披露。
- 对当前方向：可先找 1 位小型 KOC 做“共同销售/按实际付费分成”的实验，而不是买曝光；先约定归因和停止条件。
- 边界与置信度：数据为【视频自述/部分画面】【未经外部验证】；“产品市场匹配问题其实是分发问题”只适用于其案例。

### 23. ChatGPT 5.6 + Hostinger 四个 AI 副业（指定，非 Starter Story）

- 元数据：[视频](https://www.youtube.com/watch?v=S82teqWkATY)，2026-07-20，13:00；上传者“然冉创业说”。
- 字幕来源：无法取得。YouTube 元数据明确显示没有人工字幕和自动字幕；`agent-reach transcribe` 返回“no provider key configured”。
- 处理结论：无法建立基于正文的一句话结论、观点结构、步骤、数字、成功/失败条件或适用性判断。标题和简介中出现 Hostinger affiliate、付费社群、咨询、课程和器材/工具链接，只能说明发布者存在商业推广关系，不能用来推断视频正文。
- 事实置信度：【元数据明确可见】标题、日期、时长、上传者、简介商业链接；其余均标记【无法取得正文】，不纳入跨视频方法票数或数字账本的实质结论。

## 四、跨视频综合提炼

### 1. 反复出现的核心方法与共同原则

1. 从自己的工作、爱好、服务客户、评论/DM 或同类产品抱怨中找具体问题。
2. 已有付费市场不是坏事；同类产品、agency、专业服务和现成表格能证明预算位置。
3. 把 V1 压到一个结果或一个可演示动作，而不是先做平台。
4. 越容易开发，越要把时间前移到承诺、付款、内容和分发实验。
5. 从第一天创建营销资产：内容、waitlist、冷外联、高意图页面或合作创作者。
6. 先找到一条能带来点击/安装/付款的渠道，再扩 UGC、广告或团队。
7. 对素材、hook、渠道和收入做表格化追踪，重复胜出格式，停止无效格式。
8. 分发资产（受众、行业客户、社区身份）通常比“零代码/AI 编程”更能解释成功。

### 2. 视频间的矛盾与口径差异

| 主题 | 口径 A | 口径 B | 本研究判断 |
|---|---|---|---|
| 先做还是先验证 | Stella/Snag 等强调几小时或两天做 MVP | Once 明确要求先达到承诺指标再写代码 | 当前项目应以 Once 为默认；只有制作成本极低且不妨碍接触用户时，原型才可作为验证工具 |
| 追趋势还是做无聊问题 | Pep AI/Postiz 借趋势窗口 | Savvy Nomad/Hiro 强调无聊、稳定、高付费 | 两者都可，但趋势路线时间/政策风险更高；当前更适合已有付费流程 |
| 自己的痛点是否足够 | ToneAdapt/Cardstock 强调 solve your own problem | VSC/Once 要求外部传播与承诺 | 自己的痛点只能生成假设，必须补外部承诺或付款 |
| 有受众是否必要 | Stella/3AK 依赖大受众 | MonAI/Once 用一个伙伴或冷外联 | 不必先有大受众，但必须有可触达渠道 |
| 付费广告是否简单 | ChartDetector 称低时间、可放大 | 多视频承认素材疲劳、ROAS 递减、归因复杂 | 只在单位经济已验证后放大，不是第一步 |
| 标题收入口径 | 常把 gross、MRR、run rate、累计收入混用 | 个别视频展示 Stripe/Superwall | 账本必须保留原口径，禁止横向直接相加 |

### 3. Starter Story 常见产品发现方式

- 自己反复遇到的问题：ToneAdapt、Cardstock/Scanémon、Live Tourney、Go Tall。
- 已有服务/表格/agency 工作流：Profit AI、Hiro Analytics、Savvy Nomad。
- 竞品/成熟市场缩小一层：Shipper、Cat on Chair、MonAI。
- 社媒评论、DM、趋势和高传播格式：Go Tall、Pep AI、Flame。
- 既有垂直受众产品化：Stella、3AK。
- 新平台能力触发旧需求的新解法：Erly 的 AlarmKit、Postiz 的 agentic/API。

### 4. 定价与商业模式模式

- B2C app：周/月/年订阅、hard paywall、free trial 或终身买断；高频周订阅很常见，但退款/续费未充分披露。
- B2B/agency：高月费 + 席位/客户扩张；Hiro 每个 agency 可带多个客户席位，Profit AI 从 $5K 降至 $800。
- 按活动/用量：Once 按人数/活动收 $2–$50。
- 服务转软件：先由服务收入验证，再把重复部分软件化。
- 内容业务：广告收入 + 数字产品/affiliate/课程，但平台政策和收入估算风险高。

### 5. MVP、上线与首次收入路径

推荐顺序不是“灵感→开发→上架”，而是：

1. 找一个当前已经发生的具体任务和现有替代支出。
2. 找到 10–30 位可触达目标用户，收集承诺/付款而非泛兴趣。
3. 用手工服务、表格、落地页、演示视频或极小原型交付结果。
4. 设定第一笔产品收入门槛与截止日期。
5. 达标后只做一个核心结果的 V1。
6. 首日开始一个渠道；记录内容/外联→访问→使用→付款。
7. 找到一条有效路径后再自动化、上广告或扩创作者。

### 6. 获客渠道归纳

- SEO：Shipper 的竞品替代/价格高意图词；Savvy Nomad 的专业内容；适合明确搜索需求，不适合纯情绪产品起步。
- 社媒自营：ToneAdapt、Flame、Go Tall；关键是演示产品结果，不是泛流量。
- KOC/KOL：MonAI 的深度利润分成、Erly 的影响者验证、Pep AI 的垂直影响者预热。
- 社区：Reddit（Shipper、Once、ToneAdapt、Cardstock）、Discord（竞品研究/用户聚集）。
- 冷启动：Once 的个人网络与活动名单、Hiro 的 agency directory。
- 付费广告：ChartDetector、Go Tall、Snag；都建立在素材和单位经济先验证之后。
- 既有受众：Stella、3AK；效果强但样本不适用于零受众。
- 口碑/客户迁移：Profit AI；最接近“已有付费市场”。

### 7. 案例按价值类型分类

- 主要卖实用价值：Live Tourney、3AK、Profit AI、Hiro、ToneAdapt、Cardstock/Scanémon、Savvy Nomad、Once、MonAI。
- 主要卖趋势窗口：Postiz agentic、Pep AI、Shipper（AI coding 大市场）、部分 faceless YouTube。
- 主要卖情绪/传播价值：Cat on Chair、Go Tall、Stella、Erly、Glam Up；它们仍有功能，但购买/传播明显受审美、焦虑、身份或趣味驱动。

### 8. 对 `/Users/USER/Documents/app` 海外轻量产品探索的适用判断

#### 高适配

- Profit AI：从已付费服务、表格或人工流程提炼软件。
- Once：承诺指标和有限时间验证。
- ToneAdapt：个人真实痛点 + 同好确认 + 快速首单。
- Hiro：通过一个聚合客户触达多个终端用户（需选更轻的数据场景）。
- MonAI：1 位深度 KOC、按实际收入分成。
- Shipper：已有付费市场 + 一个明确缺口 + 高意图词。

#### 条件适配

- Cat on Chair/Erly：需具备强视觉、文化或演示钩子。
- Cardstock/3AK/Live Tourney：需本人或合作者长期在垂直社区。
- 付费广告/UGC 工厂：只在首单、留存、单位经济闭环后。

#### 低适配或暂不适合

- Stella/3AK 的巨量既有粉丝口径，不适合作零受众预测。
- Pep AI、Go Tall 的健康/未成年人/敏感承诺风险。
- Savvy Nomad 的税务/法律责任。
- faceless YouTube 的平台政策、同质化和营销漏斗利益冲突。
- “4–5 小时 build”“两个月 $300K MRR”等极端结果，不能做计划基线。

### 9. 可采用／应避免／仍需真实验证

| 可采用的方法 | 应避免的误区 | 仍需真实验证的假设 |
|---|---|---|
| 从已付费服务、表格、人工流程找软件化单点 | 把本人痛点直接当市场 | 是否至少 10 位目标用户有同样频率和严重度 |
| 设明确承诺/付费门槛和截止日 | 用点赞、播放、waitlist 替代付款 | 承诺能否升级为定金、付费试用或预购 |
| V1 只交付一个可见结果 | 因 AI 易开发而提前做完整 app | 手工/表格版本是否已能收费 |
| 第一天做一个渠道实验 | 同时铺满所有平台 | 哪一渠道能稳定产生目标访问和付款 |
| 记录 hook→点击→使用→付款 | 只看播放和下载 | 某内容格式是否有产品意图与正毛利 |
| 先小 KOC 按实际收入分成 | 先买大曝光或搭 UGC 工厂 | 单位创作者的真实 CAC、退款和复购 |
| 在成熟市场找窄缺口 | 口号式“拿 1% TAM” | 竞品用户是否愿为差异切换 |
| 把趋势当加速器 | 把趋势当需求本身 | 趋势衰退后是否仍有基本付费需求 |

### 10. 不超过 15 条可执行原则

1. 每个候选必须指向一个今天正在发生的任务、现有替代方案和付费者。
2. 自己的痛点只产生假设；至少获得 10 个具体使用承诺，优先获得付款。
3. 先卖手工/表格/服务版，再决定是否软件化。
4. 第一笔产品收入必须早于完整产品、原生 app 或大规模基础设施投入。
5. V1 只承诺一个用户能在 10 秒内理解的结果。
6. 营销从第一天开始，但只选一个主渠道做闭环。
7. 内容测试同时看传播、可重复和付款转化，不以播放量单独过关。
8. 已有竞品是付费市场证据；从差评、流失和高意图搜索找窄缺口。
9. 趋势只能加速已存在的需求，不能替代需求。
10. 一个深度匹配、按收入分成的 KOC，优先于大量一次性曝光。
11. 付费广告只放大已验证素材和正单位经济，不负责证明需求。
12. 收入、MRR、gross volume、run rate、累计收入必须分开记录。
13. 敏感健康、税务、法律和未成年人方向默认提高门槛或排除。
14. 每轮实验预先写停止条件、预算、截止日和升级条件。
15. 把极端成功故事视为方法线索，不视为成功率或收入预测。

## 五、数字与案例账本

> “是否经外部验证”本轮统一为“否”；未做全面外部事实核查。画面展示也只证明视频中展示过某面板，不证明审计真实性。

| 视频 | 产品／创业者 | 视频声称的收入或数据 | 商业模式 | 获客方式 | 证据形态 | 是否经外部验证 |
|---|---|---|---|---|---|---|
| Postiz | Nevo / Postiz | $17K→$143K MRR/4 月；4,271 订阅；churn 约 13.7% | B2B SaaS 订阅 | X 趋势内容、低价 influencer repost、代理生态 | 口述＋画面 | 否 |
| Cat on Chair | Ryan 与女友 | 30 日约 $18K；127K 下载 | 年费 $19.99；终身 $29.99 | RedNote、Instagram collection、Threads | 口述＋画面 | 否 |
| ChartDetector AI | Timo | 当期约 $56K/月；累计 $260K；约 25% margin | 周/半年订阅、hard paywall | TikTok paid ads | 口述＋画面 | 否 |
| Go Tall | Michael | 约 $100K/月；iOS 700K+ 下载 | B2C 订阅 | TikTok 评论回复、UGC、付费广告 | 口述 | 否 |
| Live Tourney | Matt | 约 $30K/月；$350K ARR；$800K run rate | B2B/赛事 SaaS | 自己赛事、垂直圈层 | 口述 | 否 |
| Stella | Sarah | 2 月 $300K+ MRR；约 200K 下载 | B2C 订阅 | 既有百万粉丝、短视频、ManyChat | 口述 | 否 |
| Erly | Jake | 4 月约 $50K/月；200K 下载 | B2C app 订阅 | 影响者、后续规模化 | 口述 | 否 |
| Sam Parr | Sam Parr / 多家公司 | 公司合计年收入称 $10M+ | 多公司/会员等 | 个人品牌、播客等 | 个人自述 | 否 |
| 3AK | Christian / Braylin | 约 $20K/月；6 月约 $70K；40K 用户 | 运动 app 订阅/内购 | 既有田径受众 | 口述 | 否 |
| Profit AI | Jack | app $30K MRR；services 近 $40K MRR；累计 $147K | 高价 B2B SaaS＋服务 | 既有客户、口碑 | 口述＋画面 | 否 |
| Flame | On Neill | $3K→$10K MRR/8 月；250K 下载；50M+ views | B2C 订阅 | TikTok/UGC/AI 内容 | 口述；当前完整收入面板未展示 | 否 |
| ToneAdapt | Kyan | 约 $25K/月；100K 用户 | $10/周、约 $60/年 | 日更 3 条、跨平台、UGC | 口述＋画面 | 否 |
| Hiro Analytics | Zac / Brendan | 19 月 $1M ARR；约 $90K MRR | agency 月费＋客户席位 | directory、行业网络、free trial | 口述＋画面 | 否 |
| Cardstock / Scanémon | Kyle | 合计称 $120K/月；分项约 $75K＋$17K MRR | app 订阅 | Reddit、TikTok slideshow/creator | 口述 | 否 |
| Snag | Benjamin Chen | $30K MRR；100K 用户；9K conversions | 周/月/年/一次性订阅 | UGC→Meta Ads | 口述＋画面 | 否 |
| Shipper | David / Daniel | gross $50K–$71K/月；MRR $25.6K | $25+ SaaS 订阅 | Product Hunt、Reddit、SEO、X、affiliate | 口述＋画面；口径不一 | 否 |
| Pep AI | Cedric | 7 周累计 $50K；MRR $11K | $10/月、$45/年、3 天试用 | TikTok 趋势、waitlist、影响者 | 口述 | 否 |
| Savvy Nomad | Bohdan 团队 | $1.7M/年；1,400 客户；6 员工 | 高价流程产品/服务 | SEO、专业内容、口碑 | 口述 | 否 |
| Glam Up / Sprout | Nicole | 各称 $150K–$250K MRR 级；月 400M–500M views | hard paywall、周/月订阅 | 大规模 UGC 系统 | 口述＋录屏 | 否 |
| Once | Brian 与女友 | 83 天约 $20K–$22K/月；周活 10K–12K | 按活动/人数 $2–$50 | 个人网络、冷外联、场景标签 | 口述 | 否 |
| Faceless YouTube | One Person Business 引用多频道 | 某频道称 2 月 $70K/月；1,000+ 样本库 | 广告＋数字产品＋affiliate | YouTube 搜索/推荐、AI 内容 | 发布者口述/估算 | 否 |
| MonAI | Flo | $300→$35K MRR；单条 1.7M views 增约 $5K MRR | app 订阅、hard paywall+trial | 单一垂直创作者利润分成 | 口述＋画面 | 否 |
| AI 副业视频 | 然冉创业说 | 无可用正文，不能记账 | 简介可见 affiliate/课程/社群 | 无法从正文判断 | 仅元数据/简介 | 否 |

本批视频没有发现可确认的“同一个具体创业案例在两条样本中重复讲述”情况，因此未做案例行合并。相似的 UGC、iOS app 或 agency 方法是方法重复，不是同一案例重复。

## 六、研究者总判断

Starter Story 近期样本高度偏向已经成功、增长快、标题可量化的 B2C app 和 SaaS；失败者、未盈利者、退款、创作者成本、广告现金流、平台封禁和长期留存披露不足。它适合提供“去哪里找问题、怎样设计首个分发实验”的方法线索，不适合推断成功率、平均收入或开发后必然回报。

对当前海外轻量产品探索，最值得保留的不是“AI 几小时做 app”，而是三个更严格的门槛：

1. **已有付费市场**：客户正在为服务、表格、agency、竞品或手工流程付钱。
2. **第一笔产品收入**：在完整开发前，以定金、付费试用、预购或手工交付取得。
3. **第一天营销闭环**：从第一天记录渠道→目标访问→实际使用→付款，而不是发布后再想营销。

