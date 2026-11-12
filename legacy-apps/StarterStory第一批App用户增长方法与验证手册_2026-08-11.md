# Starter Story 第一批 App 用户增长方法与验证手册

日期：2026-08-11｜性质：严格只读桌研；未发布、未外联、未注册、未登录、未付费。

## 先给结论

- 【建议】对“无美国个人品牌、单人、面向英语用户”的独立 App，第一条渠道应是**在一个高意图、问题已发生的垂直社区中，用一个可立即看懂的结果演示，逐个邀请 10 名合格用户完成真实核心动作**。这比先上 Product Hunt、先买量或泛发短视频更能验证需求。
- 【推断】Starter Story 样本最一致的模式不是“找到流量秘诀”，而是：先用已有关系/垂直社区/个性化邀请得到可交谈的少量人；看他们是否完成任务；根据行为与直接反馈改产品；只有激活和复用成立，才放大内容、KOC、ASO 或广告。
- 【事实】目录页在未登录时只展示 12 个中的前 4 个，随后出现免费账户注册墙；页面使用相对发布时间，显示“many videos”，没有提供可核验总量或完整分页。因此本报告只将可公开读取的单篇页面计入样本，**不声称已穷尽 Starter Story**。[目录页](https://www.starterstory.com/episodes)
- 【重要限制】所有收入、下载、播放、排名和“有效”陈述，除非另标，均为【创始人自述】或节目文字稿，并非审计事实。样本偏向愿意公开讲成功故事的幸存者；不能从中推出某渠道的平均转化率。

第一周只做：确定一个产品的一类高意图用户和一个唯一核心动作；准备 30 秒演示与最小事件追踪；邀请 10 位合格测试者。**不是**发广告、追求下载、做大量 SEO，也不是问“你会不会用”。

“有人愿意用”的最低证明是：合格用户安装/打开后完成核心动作，并在没有催促的情况下于次日或其自然使用周期再次使用、或主动索取下一次使用机会。点赞、收藏、邮箱、waitlist、下载、Product Hunt 名次和“听起来不错”均不是绿灯。

## 1. 研究边界、方法与证据等级

### 可访问性盘点

【事实】[Starter Story Episodes](https://www.starterstory.com/episodes) 是带有收入、成本、业务类型、niche、增长方式等筛选器的视频库；匿名可见的前四个条目显示 2–16 天前的相对日期，随后即要求邮箱/登录。目录没有对匿名访问者暴露总量、下一页或稳定更新时间字段。故“内容更新时间”只能描述为页面所显示的相对发布时间；“总量”不可确认。

【事实】本轮未试图输入邮箱、建立账户、绕过注册墙或付费墙。若某单篇被 Jina Reader 限流或网页需登录，便停止该路径；本报告只使用其已公开索引到的短段和其他可公开读取样本，不将受限正文当证据。

### 抽样与读法

候选池来自目录中可见的 episode、站内公开案例页、以及对 `site:starterstory.com` 的公开网页索引检索。深读样本 25 个：17 个典型故事/案例页、8 个公开 episode/视频文字稿；涵盖 consumer/mobile、prosumer、轻量 B2B/creator 工具。后两类只用于抽取冷启动动作，不能替代消费 App 留存证据。

标签含义：

- 【事实】公开页面结构、原始链接可见内容或研究操作事实。
- 【创始人自述】创始人在 Starter Story 页面/文字稿中的数字与经历。
- 【推断】基于多案例的归纳，不能当作因果证明。
- 【建议】为本项目给出的原创可执行方案。
- 【待验证】必须由本次真实用户实验确认，不能用桌研替代。

## 2. 25 个深读案例台账

“结果”刻意按漏斗层级写，`曝光/访问/注册/下载` 不等于 `核心动作/复用/付费`。`—` 表示原文未给可核验数字或行为。

| # | 产品/创始人 | 类型与目标用户 | 当时阶段 | 第一批用户渠道与具体动作 | 花费/人数/时间 | 获得的真实结果（层级） | 依赖条件、可复制性 | 原始链接 |
|---|---|---|---|---|---|---|---|---|
| 1 | Really Simple Store / Drew Thomas | 简单电商建店，卖家 | 公开初期 | Product Hunt；在 OST 等社区持续展示进度；PH 当天手工邮件每个新注册者 | 未披露 | 【自述】PH 最大一波注册、日榜前十；邮件带来连接与使用洞察；没有复用数据 | 社区长期身份，不是一次硬广；“手工跟进”高可复制 | [案例](https://www.starterstory.com/stories/how-i-launched-and-monetized-a-really-simple-app) |
| 2 | Pika / Rishi Mohan | 截图美化工具，设计师/创作者 | 第一周原型 | 一周后在 X 软发布、DM 对话，再上 PH | 数日 V1 | 【自述】PH 600+ upvotes、日第 2；有人明确愿为特性付费；250+ 客户为后期结果 | 其 maker 受众是优势；“付费特性请求”比赞更强，可复制的是先卖特性 | [案例](https://www.starterstory.com/stories/pika) |
| 3 | Card Curator / Tomo Matsuo | 信用卡奖励 App，旅行/信用卡用户 | alpha→beta→公开 | 先给亲友 200 人 alpha，再软发布；社媒与 Reels；PH | 【自述】alpha 约 200 人、约半数开始使用；2019–21 | 使用/反馈而非只注册；后期广告+influencer 增长但非首批证据 | 金融敏感、亲友样本偏差、约 $200K 自筹/融资，不能照搬预算 | [案例](https://www.starterstory.com/stories/how-a-credit-card-funded-trip-inspired-me-to-start-a-credit-card-reward-app) |
| 4 | Pallyy / Phil Pallen | 社媒排程，社媒经理/agency | 上线 | PH 后发现受众不在 PH；朋友的停运站点 301 导流；SEO | 【自述】300–500 日访问，低转化但有最初付费；长期 churn 高 | 有现成相关站点/朋友是不可复制资产；PH 失败本身是强反证 | [案例](https://www.starterstory.com/stories/i-learned-to-code-and-my-first-app-makes-2k-month) |
| 5 | Inbox Zero / Elie Steinbock | 开源 AI 邮箱工具，技术用户 | V0/V1 | 朋友、X、自己所在 mastermind；150 人 waitlist；PH、HN、YouTube/GitHub Trending | 【自述】构建约 5 月；waitlist 约 150；PH 获数千用户和首 100 客户 | 注册/客户；HN 流量更高但自述转化更低 | 自有 YouTube、开源与 GitHub Trending 是大前提；适合技术产品，不等于通用 App | [案例](https://www.starterstory.com/stories/inbox-zero) |
| 6 | VideoFast / Rexan Wong | 视频编辑/图像工具，创作者 | 构建中→上线 | 边做边在 X 发 demo；r/sideproject；PH | 【自述】已有 4.5K X followers；PH 首日 600+ 用户；首笔收入次日 | 用户/收入；没有 D7 数据 | 先积累受众、16 岁故事性、PH/名人转发均为混杂因素 | [案例](https://www.starterstory.com/stories/videofast) |
| 7 | Plans Collective | 活动组织 mobile App | 上架后 | iOS/Android 上线，后续社媒、SEO、ASO、广告并行 | 【自述】约两月 500+ 用户、150+ 创建活动 | 创建活动是核心动作；目标是 25% 留存，非已证留存 | 有 5 名承包商（设计、开发、社媒、SEO/ASO）；不符合单人冷启动 | [案例](https://www.starterstory.com/stories/plans-collective-on-creating-an-event-planning-mobile-app-with-250-users) |
| 8 | viral.app / Felix 等 | 短视频分析，creator/营销人 | 从想法到上线 | 为 X 预热、build in public；免费小工具；相关 Reddit 贴价值回复而非硬推 | 【自述】首帖 50K views、100+ signup 和 trials；第 2 天首订阅 | 注册/试用/首订阅；SEO 尚未有流量 | 合伙人已在 consumer-app 圈发内容，三人团队；可复用的是“回复问题+软展示” | [案例](https://www.starterstory.com/stories/viral-app) |
| 9 | Discotech / 三位创始人 | 夜生活预订 marketplace | 上线前→早期 | 先与 venue owner/promoter 访谈，得到合作口头承诺；后转向免费 guest list 与票务；web 补入口 | 【自述】初期获客很慢；新增免费 guest list 后自然下载增长 | 合作承诺、购买/报名是强动作；多年后口碑/SEO | 双边市场、融资与行业伙伴不可直接复制；但先验证供需两端高度可复制 | [案例](https://www.starterstory.com/stories/how-3-college-friends-created-the-opentable-for-nightlife-1m-year) |
| 10 | Textero | AI 写作工具，学生/写作者 | 上线后 | Google 搜索，后才 Google Ads；Instagram Reels、Pinterest 指南 | 【自述】最初客户两月后来自搜索；10K 日点击曾因算法更新骤降 | 客户，但核心使用/复用未披露 | SEO 是慢渠道且 Google 更新风险高；写作产品还受教育诚信政策限制 | [案例](https://www.starterstory.com/stories/textero) |
| 11 | FriendsWith | 社交电商 App，年轻创作者/购物者 | 上线后 | 先试 Google/Facebook 广告和邮件失败；转有机 TikTok；先从网站购买再引导进 App | 【自述】首日新西兰 App Store 前 50；到 1K 用户很慢 | 下载/排名/评分，未给早期复用；明确广告 ROI 不佳 | 商品、联盟和奖励机制、疫情时期不可复制；“web 先解释，App 留存”可借鉴 | [案例](https://www.starterstory.com/stories/how-the-pandemic-made-us-start-a-174k-year-company) |
| 12 | Planndu | 任务/生产力 App | beta→正式版 | 科技圈朋友和生产力社区专家先测；PH/社媒；每周生产力博客 | 【自述】首位年订阅者+数百注册；以 analytics 发现“说”和“用”不一致 | 付费是强信号；复用仅定性 | 朋友/专家非代表样本；其“每周博客”是后续 SEO，非一周获客 | [案例](https://www.starterstory.com/stories/planndu) |
| 13 | Founder private-chat App | 创始人私密聊天室 mobile App | alpha→beta | 开发期积累 waitlist；先私有 alpha 25 人，随后把 100 waitlist 用户放入 beta | 【自述】waitlist 600；首周 100 用户并迅速发现 bugs | 使用/反馈；未证明长期留存 | waitlist 本身不是验证；真正可借鉴的是分批 beta、先找大错误 | [案例](https://www.starterstory.com/how-to-launch-an-app) |
| 14 | Fastlane / Gaurav | AI 短视频工具，独立开发者/创业者 | beta→发布 | waitlist、两轮 beta；已有 X 个人品牌、LinkedIn、PH | 【自述】X 首帖 210K+ views，PH 日第 3；首单是 beta 用户为保留访问而付款 | beta 用户付费是强信号 | 已有个人品牌，首日大额/ARR 不可外推；可复制的是 beta 付费续用判断 | [案例](https://www.starterstory.com/stories/fastlane-create-winning-short-form-content-in-seconds) |
| 15 | Uptrends.ai | 投资信息 App→专业人士工具 | consumer MVP→pivot | X + 本地创业活动收集数百 waitlist；Twitter/LinkedIn/Substack/Discord；之后访谈 12 位专业人士、mockup、先收款 | 【自述】数千注册/20K 用户却难付费；后来先收款再开发 | **反证**：注册和 20K 用户不等于 PMF；专业用户预付款最强 | 金融领域有合规/风险；最值得复制的是先访谈→原型→预付 | [案例](https://www.starterstory.com/stories/uptrends-ai-track-trending-stocks) |
| 16 | FocusTask / Vojtech Rinik | To-do App | usable prototype/beta | 从 waitlist 选 10 人逐一邮件、约演示 call；旧 Pomodoro/任务 App 内引流，X 截图 | 【自述】第一通 call 带来首个付费；又获少量 beta 客户 | 付费；用户反复要求 mobile 形成需求线索 | 等了一年才找用户是创始人自认的错误；旧产品流量不是零起点 | [案例](https://www.starterstory.com/stories/focustask) |
| 17 | Receipt AI | 收据处理 App | 发布 | waitlist；PH、LinkedIn、X、Reddit 重复传播 | 未披露 | 【自述】首单来自 waitlist；早期评价促迭代 | 付费强于“积极回应”；但来源归因和复用未披露 | [案例](https://www.starterstory.com/stories/receipt-ai) |
| 18 | Cat on Chair / Ryan | Pomodoro 猫咪 App，消费者 | beta→上架 | 在 Rednote 邀数千 beta；修 bug；后由 Instagram 收藏型帖子与 Threads 自传播 | 【自述】首周约 3K 下载；Instagram 一帖 200 万 views 后下载/收入隔夜翻倍 | 下载/收入；beta 后仍有严重 bug，未给留存 | 女友已有插画账号粉丝、偶发爆款和跨区传播不可规划；“先收反馈再迭代”可借鉴 | [episode](https://www.starterstory.com/stories/18k-month-from-this-ridiculously-simple-app-idea) |
| 19 | $30K/month Mobile App / Eyal & Yahli | 体育预测 consumer App | 已获流量但低 PMF→重做 | 先花数千美元 influencer marketing；再用数据和访谈发现用户要的是不同结果 | 【自述】约 20 下载/日、5–10 users/日却卡 1–2K MRR；重做后付费转化 >50% | **反证**：流量/试用不能证明价值；转化与续费才是信号 | 赌博/体育预测与付费 influencer 不适合作为本项目策略；产品重构逻辑可借鉴 | [episode](https://www.starterstory.com/stories/how-we-built-it-30k-month-mobile-app) |
| 20 | $1M Mobile App Playbook / Stephen | 戒电子烟 consumer App | 内容验证→增长 | 在 TikTok 研究高表现内容的“hook/story/CTA”结构；先有机测试原创短视频，再放大赢家 | 未披露该轮合格用户数 | 内容播放是需求线索，不是使用证据；其主张为再以产品数据确认 | 只能合法借鉴问题、结构和拍摄逻辑，**不能复制脚本、镜头、素材或声称医疗效果** | [episode](https://www.starterstory.com/stories/the-1m-mobile-app-playbook) |
| 21 | 3 iPhone Apps / Blake Anderson | RizGPT、Umax、Cal AI 等消费 App | 规模化叙述 | 主张 TikTok/Instagram、influencer 和上线前内容验证 | 未披露可分离的首 10 用户数据 | 曝光/收入混在叙述中，不能当首批用户因果证据 | 多 App、合作人、巨大规模与现成营销能力；仅作“先验证内容钩子”的弱证据 | [episode](https://www.starterstory.com/stories/he-made-10m-with-3-iphone-apps) |
| 22 | 本地化热量 App / Tomer | 本地语言 calorie tracking | 上线后扩张 | 先研究同类和本地内容；低 CPM 付费广告到约 $20K/月后，再和大 influencer revenue share | 【自述】上线一年后 $80K/月；先获社会证明才签达人 | 收入为自述，未给早期留存 | 创始人懂本地 fitness 市场且认识大达人；大 influencer/rev-share 是后期，不是首 10 人动作 | [episode](https://www.starterstory.com/stories/i-copied-a-huge-app-now-i-make-80k-month) |
| 23 | Pawns.app / Karolis Toleikis | 被动收入/带宽共享 App | 上线 | 社媒、比赛、社区、referral；让最初用户晒 payout proof | 未披露首批人数 | payout 可能是实际完成动作，但经济激励带来选择偏差 | 隐私、安全、地域和代理业务风险高；抽奖/补贴不可用于验证自然意愿 | [案例](https://www.starterstory.com/stories/pawns-app) |
| 24 | LeadFlow / Adrian Berisha | 冷邮件工具，销售团队/solopreneur | 上线 | 先问营销网络；用产品自身冷邮件+LinkedIn；提供 done-with-you 设置 | 【自述】约 60 meetings/月，首 campaign 后 3 天有首批付费 | 付费及被帮助完成任务 | B2B 网络、已有 agency 经验、实施服务；只能借鉴“拿问题证据的个性邀请”，不可泛发 spam | [案例](https://www.starterstory.com/stories/leadflow-ai-cold-email-automation-for-sales-teams) |
| 25 | Vidovo / Felix 等 | UGC creator/品牌平台 | 早期 | Discord、cold email、和创作者谈；最早内容几乎无人理会，三周后健康品牌回复 | 【自述】第一单 5 条视频/$750；最初客户多来自 cold email | 客户付费、交付、复购为较强 B2B 信号 | 两面市场、创始人有 TikTok/Discord 经验；不能把“几百封”误写成低成本秒见效 | [案例](https://www.starterstory.com/stories/vidovo-com-ugc-video-ads-made-easy) |

## 3. 重复方法：出现次数、适用阶段与失败方式

计数规则：【事实】为上表 25 篇中明确提及该方法的篇数；同一篇即使多次做也只记一次。它是样本出现频率，不是效果排名或成功率。

| 方法 | 出现数 / 25 | 最适用阶段 | 最小可复制动作 | 常见失败/不要照搬 |
|---|---:|---|---|---|
| 手工找已在抱怨/正被问题困扰的人（访谈、问题证据） | 8 | 未完成、beta | 从公开讨论/已有社群找 20 个有明确场景的人；请其提交一项真实输入或看 demo 后做任务 | 只问“你会不会用”；把亲友的礼貌当需求；给人贴标签或骚扰私域 |
| 在垂直社区持续分享过程/价值回复 | 10 | 构建中到 50 人 | 先回答一个具体问题，附 30 秒原创建果演示；只邀请合适者测试 | 把社区当广告牌、复制别人的热门帖、忽略 subreddit/群规；Pallyy 证明 PH/泛社区可能受众错位 |
| 个性化私信/邮件邀请 | 7 | 0–10、B2B/高意图 prosumer | 说明你为何想到此人、一个具体观察、一次 10 分钟测试请求和退出权 | 批量模板、从竞品评论区抓名单、无同意群发；初期回复少并不自动等于产品失败 |
| 人工结果或协助 onboarding | 4 | 未完成、TestFlight | 替用户完成一次真实结果、观察其卡点；不承诺持续人工服务 | 误把“创始人替你做完”当产品自助可用；服务成本掩盖产品价值 |
| waitlist / landing page / mockup | 7 | 未完成到 beta | 让用户完成真实场景输入并选择测试时间；把名单用于逐个测试，不用作成功宣言 | 邮箱/预约本身不是真实使用；Uptrends 与 Founder-chat 都说明要继续看行为 |
| Product Hunt / Hacker News / Reddit 等 launch 面 | 12 | beta 稳定、已有激活路径后 | 只用作一次流量与反馈 burst；在来源层记录到核心动作与次日回访 | PH 排名/赞是曝光；Pallyy 受众不在 PH，Inbox Zero 的 HN 高流量也可能低转化；不能操纵投票 |
| 短视频 demo（TikTok/Instagram/YouTube） | 9 | 先测试钩子；再 10–100 | 原创 15–30 秒“问题→一次动作→即时结果”演示，CTA 只招一个明确测试者群 | 爆款、已有粉丝和名人转发不可计划；观看不等于安装，安装不等于复用 |
| KOC/creator 免费体验、佣金或合作 | 5 | 激活/复用已成立后的 50–100+ | 找 3–5 位受众与场景高度一致的微型创作者，按可追踪激活/结果而非播放付费 | 大 influencer、收入分成、抽奖、补贴都会扭曲需求；先有社会证明再谈合作 |
| App Store 关键词/ASO | 4 | 已上架后的长期需求捕获 | 为一个具体任务词准备商店截图、首屏、事件归因 | 慢、需稳定页面与评价；不能替代首 10 人验证，也不能诱导评分 |
| SEO / free tool / template | 9 | 10–100 后的长期积累 | 发布一个真正完成小任务的免费工具/模板，记录来源到核心动作 | 起效慢且有算法风险（Textero）；不能以“有访问”当 PMF；AI 批量文可能不排名 |
| 既有受众、newsletter、旧产品/客户迁移 | 10 | 任何阶段，但非零起点 | 若本来就有，透明地邀请其中符合场景者；单独标记来源偏差 | 不是新开发者可复制的渠道；Pika、VideoFast、Inbox Zero、Fastlane、Cat on Chair 均含这个混杂因素 |
| 付费广告 | 8 | 50–100 后，且已有激活/复用 | 只对已证明的一个钩子做小样本来源测试，并完整算到核心动作/复用 | Pallyy、FriendsWith、Planndu、Discotech 都记录了 ROI 差或变负；绝不在尚未有留存前用广告“制造成功” |

### 最值得复制的 5–8 项

1. 【建议】从真实问题和已发生的行为开始：一对一找正在做替代方案、明确抱怨或已投入时间的人；让对方给出真实输入。Discotech 的伙伴访谈、Uptrends 的 12 位专业人士访谈与预付款是最强案例。[Discotech](https://www.starterstory.com/stories/how-3-college-friends-created-the-opentable-for-nightlife-1m-year)｜[Uptrends](https://www.starterstory.com/stories/uptrends-ai-track-trending-stocks)
2. 【建议】用小规模、逐人 beta 验证：先 10–25，再 50–100，不把所有名单同时倒进不稳定版本。Founder-chat 的 25 人 alpha 是可借鉴的分批方式。[案例](https://www.starterstory.com/how-to-launch-an-app)
3. 【建议】把 waitlist 当作招募池，而非成功指标；挑 10 人逐一 demo/观察，像 FocusTask 一样争取第一次真实付费或真实任务完成。[FocusTask](https://www.starterstory.com/stories/focustask)
4. 【建议】在垂直社区先贡献与演示“过程/结果”，而不是硬广；回复中的实际问题决定产品表述。Really Simple Store、viral.app 都提供这种线索。[Really Simple Store](https://www.starterstory.com/stories/how-i-launched-and-monetized-a-really-simple-app)｜[viral.app](https://www.starterstory.com/stories/viral-app)
5. 【建议】短视频只验证可理解性和钩子：制作原创 30 秒任务演示；把播放与安装、核心动作、D2/D7 分开记录。Pika 的早期 X demo 与 Cat on Chair 的 beta→迭代是更稳的部分，不是追逐后来的爆款。[Pika](https://www.starterstory.com/stories/pika)｜[Cat on Chair](https://www.starterstory.com/stories/18k-month-from-this-ridiculously-simple-app-idea)
6. 【建议】从第一天记录漏斗与退出点，优先解决“用户做了试用却没有留下”的问题。$30K App 明确显示有下载和 trial 仍可能产品不对；Planndu 也指出言语反馈会与行为相反。[案例](https://www.starterstory.com/stories/how-we-built-it-30k-month-mobile-app)｜[Planndu](https://www.starterstory.com/stories/planndu)
7. 【建议】对于频率较低的任务型产品，先提供网页/轻入口，再在完成价值后再要求安装；Discotech 和 FriendsWith 都有“先降低下载摩擦”的反思。[Discotech](https://www.starterstory.com/stories/how-3-college-friends-created-the-opentable-for-nightlife-1m-year)｜[FriendsWith](https://www.starterstory.com/stories/how-the-pandemic-made-us-start-a-174k-year-company)
8. 【建议】只在已证明激活与复用后，才以小 KOC、ASO、SEO/free tool 或广告扩大；广告应放大已验证钩子，不负责发现 PMF。[Pallyy 的反例](https://www.starterstory.com/stories/i-learned-to-code-and-my-first-app-makes-2k-month)｜[Discotech 的反例](https://www.starterstory.com/stories/how-3-college-friends-created-the-opentable-for-nightlife-1m-year)

### 最不应复制的 3–5 项

- 【建议】不要把 PH/HN/Reddit 排名、播放量或首周下载当“第一批真实用户”。这是一次曝光层事件；Pallyy 亲述 PH 受众错位，$30K App 也说明有流量却没有正确价值。[Pallyy](https://www.starterstory.com/stories/i-learned-to-code-and-my-first-app-makes-2k-month)｜[$30K App](https://www.starterstory.com/stories/how-we-built-it-30k-month-mobile-app)
- 【建议】不要照搬有大受众/名人/既有客户的“启动”。VideoFast、Inbox Zero、Fastlane、Cat on Chair 都有既有渠道或偶发推荐；必须在报告中把它们从零起点方法中剥离。[VideoFast](https://www.starterstory.com/stories/videofast)｜[Inbox Zero](https://www.starterstory.com/stories/inbox-zero)｜[Fastlane](https://www.starterstory.com/stories/fastlane-create-winning-short-form-content-in-seconds)
- 【建议】不要在留存前买量、抽奖或补贴。它只能购买一次动作，且可能产生“为奖励而来”的样本；Pawns 的比赛/首批 payout 与 Card Curator 的后期付费增长都不适合验证自然需求。[Pawns](https://www.starterstory.com/stories/pawns-app)｜[Card Curator](https://www.starterstory.com/stories/how-a-credit-card-funded-trip-inspired-me-to-start-a-credit-card-reward-app)
- 【建议】不要复制竞品的文案、镜头、品牌、素材、用户列表或 UI；只能合法借鉴“问题、受众、内容结构、一次动作和衡量方式”。
- 【建议】不要把后期 SEO、巨量内容、海外大 influencer、融资或媒体报道倒填为“首批用户来源”。它们需要时间、资产、预算或平台窗口，且站内样本常把不同阶段混在一起。

## 4. 适合当前三款 App 的渠道优先级

### 通用优先级（中国开发者 → 美国英语用户、无海外大受众）

1. 【建议】**高意图一对一招募 + 小型垂直社区的价值型贴/回复**：成本低、可看行为、时区可异步；首 10 人首选。
2. 【建议】**原创建果 demo 的短视频/图文**：不是求 viral，而是验证“陌生人能否 30 秒理解并愿意完成一次任务”；首 10–50 人。
3. 【建议】**TestFlight 定向 cohort + 人工 onboarding**：前提是 iOS build/关键权限真实可用；首 10–50 人。
4. 【建议】**小 KOC 体验/共同演示**：前提是 activation 与复用已成立，目标 50–100。
5. 【建议】**App Store ASO 和一个免费小工具/模板**：长期需求捕获，适合 50–100 之后。
6. 【建议】**广告**：最后。仅当来源→核心动作、D7/自然使用周期复用、及（若收费）试用/付费均已成立，才做小额、可停的素材测试。

不适合优先：泛 Product Hunt（除非受众就是 maker）、泛 Hacker News、在 Reddit/Discord 无语境硬贴、广撒 cold DM、购买大号投放、广泛 SEO、用虚假评论/刷量或绕平台规则。

### 水印相机：首批用户入口

【建议】先选**每天需要把“刚拍的现场照片”发给客户或归档的美国独立从业者**，而不是泛“喜欢拍照的人”。可从以下社区类型中选择一个最窄切口：

- home-service/field-service（屋顶、清洁、维修、园艺等）的小企业主；
- real-estate listing/物业现场记录人员；
- 小型 e-commerce/二手卖家，需要统一品牌标识的产品图。

内容钩子：`I turn 8 job-site photos into client-ready proof with date, location and logo in under a minute.` 用自己的样图和原创录屏展示“原片→选择模板→导出一张可发客户的图”。

用户动作：上传**自己当天的一张**工作照片，选择一个日期/地点/品牌字段，导出/分享。衡量：进入页→上传→导出→48 小时内再次导出第二批照片；不要以观看量或“模板好看”判断。

不适合：摄影审美泛人群、纯滤镜标签、PH、先做广告；以及涉及精确位置时未经说明收集/公开用户位置。

### 周易反思：首批用户入口

【建议】只定位为 **I Ching-inspired reflection prompt / decision journal**，不做预测、金融、医疗、心理治疗或命运承诺。首个群体可选“已使用 journaling、mindfulness 或 decision-making prompt 的英语用户”，在反思写作、创意卡片、东亚文化学习等社区类型中找**愿意写下真实两难问题**的人；不要进入脆弱心理健康或危机人群做招募。

内容钩子：`Stuck on a decision? Draw one reflection prompt, write one honest answer, revisit it tomorrow — no prediction.`

用户动作：写下一件真实但非敏感的两难，抽取一条反思提示，完成至少 80 字自己的回应，并在次日打开旧记录补一行“我实际做了什么”。衡量：完成首条反思→D2 主动复看/补记；是否更清晰的自评只能作补充，不能替代复用。

不适合：占卜准确性宣传、承诺“预测/改变命运”、金融交易/关系/医疗建议内容、面向未成年人或困境人群的定向营销、靠猎奇短视频泛流量。

### 自律宠物：首批用户入口

【建议】首个群体应是**使用 iPhone、已明确想减少某一分心 App、愿意在学习/创作/深度工作前做一次真实专注 session 的英语用户**。社区类型：数字健康/专注习惯、学习 accountability、独立创作者的深度工作群；不以 ADHD/临床治疗身份或疗效承诺切入。

内容钩子：`Before I start a 25-minute study block, I choose the distraction app, make a tiny commitment, and keep one pet alive by returning.` 录屏必须准确反映真实可用的 Family Controls/Shield 能力；在授权或真实设备未验证前，只用故事板说明，不能假称已拦截。

用户动作：选择一个自己确实会刷的 App → 开始一次 25 分钟专注 session → session 完成后返回宠物/记录一次。衡量：开始 session、完成 session、次日自行再开始一次；若核心机制依赖 Family Controls，则只在真实 iPhone 上记录并明确技术前提。

不适合：泛“可爱宠物游戏”受众、PH 作为首渠道、还没真实可用就招募 TestFlight、以焦虑/诊断为卖点、先买激励下载。

## 5. 7–14 天：区分礼貌点赞与真实使用的实验

### 共同规则

【建议】每次只测试一个“人群 × 场景 × 核心动作”。同一批人只收到一次邀请；反馈问题在完成任务后再问；D2/D7 复用窗口内不以提醒催回。邀请码、来源、版本和核心事件须能关联，且只收最低必要信息。

原创邀请模板结构（按产品替换方括号内容，不复制任何案例文案）：

> Hi [first name] — I noticed you [specific public, non-sensitive context]. I’m testing a very small tool for [one job-to-be-done], not selling anything today. Could you try one [5–10 minute] task using your own [photo/decision/focus session] and tell me where it breaks? If it isn’t relevant, a simple “not for me” is completely useful. I’ll only use your contact for this test and will not add you to a list without permission.

#### A. App 尚未完成：说明页 + 30 秒录屏/故事板

| 项目 | 设计 |
|---|---|
| 筛选 | 过去 7 天真实出现过目标场景；能描述现有做法；英语用户；避免亲友便利样本超过 20% |
| 招募 | 邀请 30 位合格者：15 位来自一个垂直社区的价值回复/公开报名，15 位为经上下文挑选的个性邀请；不买量 |
| 唯一核心动作 | 提交一项真实输入（现场照片 / 非敏感两难 / 一次即将开始的专注时段），完成可点击故事板中的“得到结果”步骤；对未完成 App 可在 24 小时内人工返回一次结果样例 |
| 记录事件 | 来源、合格、看完录屏、开始任务、提交真实输入、拿到结果、是否主动追问/选择下一次试用；不得把留邮箱单列为成功 |
| 成功阈值 | 30 位合格受邀中，至少 12 位完成真实输入，且至少 6 位主动追问结果、要求 beta 名额或愿意给出具体可替代现有做法的证据 |
| 失败/切换 | 少于 6 位完成输入：先检查人群或钩子；12 位完成但少于 3 位想继续：问题价值/结果不足；立刻换切口或核心结果，不继续扩招 |

#### B. TestFlight 可用：定向 beta

| 项目 | 设计 |
|---|---|
| 前提 | build 可安装、核心路径可走通、隐私/权限解释准确；自律宠物还须真实 iPhone 上的授权能力已验证，未满足则退回 A |
| 筛选与招募 | 20 位合格 iPhone 用户；来自 A 的高意图者优先，其余来自同一窄社区；不以熟人“帮忙”补数 |
| 唯一核心动作 | 水印相机：导出一张自己的客户/归档图；周易反思：完成一条真实反思并保存；自律宠物：完成一次真实专注 session 并返回宠物 |
| 记录事件 | invite sent、install、first open、开始动作、完成动作、耗时、错误/退出点、D2 无催促复用、D7 无催促复用、主动反馈/分享；反馈文本与行为分列 |
| 成功阈值 | 20 个合格邀请中 ≥12 安装、≥10 完成核心动作、≥6 在 D2 无催促复用；若自然使用周期较低，D7 ≥5 次第二次有价值动作可替代 D2 |
| 失败/切换 | 安装 <6：招募承诺或入口不对；完成 <6：onboarding/产品路径不对；完成 ≥10 但 D2 <3：价值/触发频率不对。暂停扩散，访谈完成者与沉默者各 3 位后改一个假设 |

#### C. App Store 已上架：小批量渠道测试

| 项目 | 设计 |
|---|---|
| 筛选与渠道 | 50 位“来自两个可区分入口”的合格到达者：一个垂直社区的原创教育/demo 内容，另一个为 1:1 邀请或 3–5 位小 KOC 的明确体验帖；不同时开五个渠道 |
| 唯一核心动作 | 与 B 相同，确保商店文案、首屏与动作完全一致 |
| 记录事件 | source/content ID、商店页打开、安装、首开、核心动作完成、完成耗时、D2、D7、第二次有价值动作、付费/分享（如适用）、退出原因 |
| 成功阈值 | ≥20 安装、≥12 核心动作、≥6 D7 无催促复用（或低频产品在 7 天内第二次导出/回顾）；两个来源中至少一个到核心动作率可重复 |
| 停止/换切口 | 50 位合格到达者少于 5 位核心动作：先改首屏/场景/动作，不买广告；核心动作有但 D7 <3：停扩大渠道，改产品频率或结果；只有某一来源有效时砍掉其他来源 |

## 6. 第一批 10、50、100 用户的操作手册

### 0–10：高意图、逐人观察（第 1–7 天）

1. 写下一个 ICP 句子、一个场景和一个唯一动作；为每个产品只选上节的一个入口。
2. 从一个垂直社区类型/已有合格联系人构成 30 人候选池，记录为什么该人合格；不抓取竞品评论者名单、不群发。
3. 发送最多 10 个个性邀请；每人给一个 5–10 分钟任务，不要求正面反馈。
4. 每天看完成/退出事件，和 1–2 个完成者、1–2 个未完成者交流；一次只改一个阻塞点。
5. 达到 B 的小样本阈值前，**零广告、零大 KOC、零“上线庆祝”**。

### 10–50：只复用已被行为证明的入口（第 8–14 天）

1. 把 0–10 中转化到核心动作最高的一个问题表述做成 2–3 个原创 demo 变体。
2. 在同一类社区用有用内容/问题回答引入，不跨到无关大社区；每条内容的 CTA 仅为测试核心动作。
3. 对安装却未完成、完成却未复用的人各抽样 3–5 位，验证阻塞原因是否一致。
4. 保留人工 onboarding，但把重复解释写成首屏、FAQ 或短录屏；不要把人工成功误记为产品成功。

### 50–100：只放大已经激活且复用的路径

1. 要求至少一个来源在 20+ 合格到达者中稳定达到核心动作 ≥50%，并达到对应自然周期复用阈值，才引入 3–5 位微型创作者或开始 ASO/free tool。
2. KOC 只给透明试用/按可追踪结果的合作；不要购买假流量、评价或要求虚假背书。
3. ASO 只围绕用户真实使用的一个任务词；SEO/free tool 作为 4–12 周投资，不计为本周增长。
4. **广告的放大前置条件**：一个来源的落地页→安装、安装→核心动作、核心动作→D7/自然周期第二次价值动作均稳定；若收费，还需看到试用后续用/付费意愿。任何一环未过，广告只能扩大噪音。

## 7. 统一追踪表（仅结构，不创建文件）

| 用户来源 | 是否合格 | 是否安装 | 是否完成核心动作 | 完成耗时 | 是否再次使用 | 主动分享/邀请 | 退出原因 |
|---|---|---|---|---|---|---|---|
| 例如：`r/productivity 的价值回复 A` / `个人邀请 B` / `原创 demo C` | Y/N + 合格理由 | Y/N | Y/N + 动作名 | 分钟 | D2/D7/自然周期：Y/N + 时间 | Y/N + 非强制证据 | 选择困难、权限、价值不够、价格、bug、时机、未知 |

建议额外加内部字段：`匿名受试者 ID、邀请日期、版本、内容 ID、首次打开、开始动作、完成动作、D2、D7、是否被提醒`。绝不把私人敏感输入、照片原件、精确位置或账号凭证写进增长表。

## 8. 对抗式检查：为什么不能把本报告当绿灯

| 前提/误用方式 | 可证伪阻断证据 | 修正与闭环 |
|---|---|---|
| “很多下载/点赞，所以会留下来” | Uptrends 有数千/20K 用户仍发现消费者不愿付；$30K App 有安装/试用却留不住 | 只看核心动作 + 无催促 D2/D7 或自然周期复用；不足即改切口 |
| “一个 viral 视频可复制” | Cat on Chair 有既有插画粉丝和偶发大帖；VideoFast 有 X 受众/名人放大 | 先用小内容测试理解和动作；不把播放设为成功 |
| “PH/广告能找到用户” | Pallyy 说 PH 受众错误；Discotech、FriendsWith、Planndu 都披露广告 ROI/成本问题 | PH 仅一次反馈 burst；广告只在留存后做可停的小实验 |
| “waitlist/亲友愿意等于需求” | Founder-chat 的真正价值在 alpha/beta 发现 bugs；亲友样本易礼貌偏差 | waitlist 中挑人完成真实任务；亲友比例受限，行为优先 |
| “把竞品营销照搬最快” | 内容、商标、素材、名单和平台操纵都有侵权/封禁风险；市场、年代和算法变动 | 只抽象合法方法；所有脚本、素材、demo 均原创；遵守社区与商店规则 |

残余风险：【待验证】美国英语受众的社区可达性、时区回复速度、各产品的真实首个任务频率、iOS 权限与商店路径，都无法由案例桌研证明。尤其自律宠物的 Family Controls 能力、用户授权与真实设备回锁仍须单独以真实 iPhone 证据验证。

## 9. 最终决策卡

- **最优第一渠道**：【建议】对三个当前方向都先做“一个窄场景的高意图 1:1 招募 + 30 秒原创结果演示”；其中最先建议试**自律宠物的 iPhone 专注/数字健康高意图 cohort**，但仅在其真实设备核心能力可用时。若该能力未就绪，先做水印相机的现场工作照片 cohort；周易反思保持娱乐/反思定位。
- **第一周只做什么**：【建议】一款 App、一个人群、一个核心动作、10 个合格邀请、事件追踪、D2 无催促回访。其他均暂缓。
- **什么结果证明“有人愿意用”**：【建议】至少 6 名合格 beta 用户完成真实核心动作，且至少 3–6 名在没有催促下于 D2 或自然使用周期再次完成有价值动作；收费产品再加至少一笔非诱导付费/预付。
- **什么结果应停止或改产品**：【建议】30 个合格邀请中少于 6 人愿意提交真实输入；或 10+ 人完成动作但 D2 <3，且完成者无法指出具体替代方案/复用时机。停止扩渠道，换人群、结果或核心动作。
- **最终边界**：【事实】这是案例桌研与实验设计，不是用户行为证据；**不得宣布绿灯**。只有按上表取得真实安装/动作/无催促复用（并视业务模型取得付费）后，才可进入下一轮决策。

## 来源与研究运行说明

- 目录结构与匿名访问限制：[Starter Story Episodes](https://www.starterstory.com/episodes)
- 样本原始链接均已逐行列于第 2 节；为避免版权问题，本报告未复制长文或长视频逐字稿，仅作短摘录级事实转述。
- 本轮使用公开网页阅读；没有读取 YouTube 字幕来作为关键证据，也没有以搜索标题或搜索摘要代替视频正文。部分页面是 Starter Story 的公开视频文字稿，已在表中标为 `episode`。
- 【事实】运行态 model/effort/额度在本线程不可读取，故无法确认实际是否为建议的 Terra high；未将其假装为已确认事实。
