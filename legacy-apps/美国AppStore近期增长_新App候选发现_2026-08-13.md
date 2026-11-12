# 美国 App Store 近期增长：新 App 候选发现（2026-08-13）

> 查询日期：2026-08-13（Asia/Shanghai；美国商店页面为 `us` 区）。状态：**严格只读发现；0 个绿灯、0 个开发授权、0 次下载/注册/付费/外联/发布**。本报告中的最高结论只到“值得进入非开发验证设计”。

## 一屏摘要

- 【事实】本轮从美国 App Store 当前免费总榜与 16 个分类榜中保留 **50 个真实 App 信号**，覆盖 Books、Developer Tools、Productivity、Health & Fitness、Photo & Video、Music、Weather、Sports、Reference、Navigation、Entertainment、Shopping、Graphics & Design、Lifestyle、Social Networking、News、Food & Drink 等领域；详情均链接至美国区商店页。
- 【事实】Apple Lookup/商店页核验了 50 个 App 的首发、最近更新、总评分量与免费/IAP 状态；对 50 个 ID 均尝试美国区最新评论 RSS，只有 8 个返回正文，共 **381 条可计数评论窗口**（近 30 日 329、31–90 日 27、其余更早 25）。RSS 空响应不等于 0 条评论。
- 【事实】跨平台可直接核验的动态信号包括：MenuFit 在 Google Play 为 **100K+** 安装档位、FlockHopper 为 **10K+**；精确下载不可得，未作估算。[MenuFit Google Play](https://play.google.com/store/apps/details?id=com.myhealthymenu.app) · [FlockHopper Google Play](https://play.google.com/store/apps/details?id=com.dontgetflocked.flockhopper)
- 【推断】相对最有信息量的信号不是“大而全 AI”，而是六类单结果：**重启后本地开发依赖就绪收据、同机位复拍叠影、今晚观星计划卡、每周私人照片明信片、木工开工前可行性收据、共享日历变更摘要**。它们均仍缺真实输入、核心动作完成、无催促复用和付款。
- 【事实】最热但不可复制的对象集中在品牌开屏（7 Brew）、短剧内容/投放矩阵、奖励提现、约会/校园社交图谱、赛事票务/球队数据、实时警情内容、通用 AI 影像算力与版权库。
- 【结论】**没有候选证据强到足以挑战当前 P0。**当前最强也只是“榜位 + 商店正文/工作流 + 相邻跨平台信号”，缺的仍是同一明确人群对新承诺的 V/S/C/R：多个独立传播、20 个变量清晰的内容实验、真实输入并完成结果、无催促二次使用，以及付款/订金。

## 0. 第一性原理、红队与证据口径

### 0.1 最小充分推导

- 根目标不是找到“热门 App”，而是找到个人开发者可在 2–6 周实现核心闭环、并能用真实行为证伪的新产品构型。
- 必要条件：用户与时刻清楚；单一结果几分钟可见；不依赖网络效应、大内容库、复杂企业销售或不可得 API；传播结果与产品价值一致；隐私、版权和平台规则允许。
- 本轮事实只能证明“公开市场存在行为信号”；榜位、评分总量、更新和第三方安装档位都不能单独证明近期自然增长、留存或付费。
- 失败条件：只能靠品牌/买量/内容库存；关键数据不可合法获得；结果涉及金融、医疗、法律、诊断或安全判断；真实用户不愿提交输入；分享不带来核心动作；二次使用需催促。

### 0.2 对抗式反证

| 攻击/误用方式 | 阻断证据 | 残余风险与修正 |
|---|---|---|
| 把 2026-08-13 单日榜位写成“最近上升” | 表中逐项写“榜单时点”，无历史榜位即标弱 | 以后需 30/90 天多时点榜位序列 |
| 把总评分量写成近期评价增长 | 仅 8 个 RSS 返回 dated 正文；其余标不可计数 | Apple RSS 选择性空响应；需下一轮重复快照或公开第三方序列 |
| 把 Google Play 安装档位当 iOS 下载 | 仅写 Android 档位，不外推 iOS | 跨平台人群和投放可能不同 |
| 从短剧、社交、奖励、票务热度偷换为个人可复制 | 明列内容/网络/品牌/资金/数据资产 | 即使做窄功能，也可能仍被原平台入口锁死 |
| 以“更好看/更简单”作为楔子 | 30 个候选均绑定高摩擦时刻和单一结果 | 仍需真实选择实验，桌研无法证明差异重要 |
| 以商店评论替代 C/R | V-S-C-R 表只把评论作为问题/工作流线索 | 评论者是选择偏差样本，且不等于无催促复用 |
| AI 输出静默错误 | 深核逐项列准确性、版权、隐私与人工校验 | 任何高风险结果均不得进入候选推荐 |

### 0.3 渠道与标签

- 【事实】使用 agent-reach：Jina Reader/公开网页与 Apple RSS 可用；Exa 未配置；Reddit 的 OpenCLI 缺 Chrome 扩展；YouTube 已有 `yt-dlp` 但未配置 JS runtime；未安装或改配置。
- 【事实】Product Hunt 首页当前返回安全验证，feed 经 Reader 只返回空壳，故没有把 Product Hunt 票数写入证据。[Product Hunt](https://www.producthunt.com/)
- 【事实】TikTok/Reddit 登录墙或正文不可读时未绕过；AppMagic、Sensor Tower、Similarweb 本轮未取得可公开归因到这些 50 个对象的时序页，未使用付费或摘要数字。
- 标签：`【事实】` 官方页面/可复核元数据；`【平台估算】` 平台公开档位而非精确下载；`【用户正文】` 商店公开评论的短摘要；`【推断】` 从信号反推的构型；`【待验证】` 需要真实行为。

## A. 50 个原始信号池

> 强度：中 = 至少“当前榜位 + 新上架/dated 评论/跨平台档位”中的两个；弱 = 单日榜位 + 总评分/更新；很弱 = 品牌事件、新上架但几乎无用户证据。排名是 2026-08-13 快照，不代表上升幅度。

| # | 领域 / App | 当前公开信号 | 近期增长拆分与强弱 | 可复制性初判 |
|---:|---|---|---|---|
| 1 | Food · [7 Brew Coffee](https://apps.apple.com/us/app/7-brew-coffee/id6762023973) | 【事实】总榜 #1；8-11 首发，6 个评分 | 榜单时点+品牌上新；很弱，未见评论 RSS | 品牌门店资产，不可复制 |
| 2 | Books · [Scroll The Bible](https://apps.apple.com/us/app/scroll-the-bible/id6756558351) | 【事实】Books #1；2025-12 首发；7.6K 评分 | 当前榜+8-02 更新；弱，未得 dated 评论 | 内容/宗教分发强，方法可看 |
| 3 | Books · [BookWatch](https://apps.apple.com/us/app/bookwatch-visual-learning/id1660054787) | 【事实】Books #18；11K 评分；8-09 更新 | 当前榜+更新；弱 | 大内容与版权不可轻复制 |
| 4 | Books · [Y/n](https://apps.apple.com/us/app/y-n/id6744907251) | 【事实】Books #20；4.3K 评分；8-12 更新 | RSS 可见窗口 100 条均近 30 日；中，但内容/投放来源未知 | 内容社区依赖 |
| 5 | Productivity · [Saturn Calendar](https://apps.apple.com/us/app/saturn-calendar/id1454483188) | 【事实】#15；67.7K 评分；8-10 更新 | 单日榜+大存量；弱 | 校园图谱/日历数据依赖 |
| 6 | Developer Tools · [LocalDevVPN](https://apps.apple.com/us/app/localdevvpn/id6755608044) | 【事实】#10；81 评分；2025-12 首发 | 当前榜+小体量；弱，评论描述重启后服务失效 | 可反推窄开发收据 |
| 7 | Developer Tools · [Codex Relay](https://apps.apple.com/us/app/codex-relay-remote-codex-app/id6764463488) | 【事实】#27；2026-05 首发；46 评分 | RSS 31–90 日 2 条；中弱 | 依赖 Codex/本地 server，安全敏感 |
| 8 | Developer Tools · [Rev for Vercel](https://apps.apple.com/us/app/rev-for-vercel/id6740740427) | 【事实】#36；89 评分；6-17 更新 | 单日榜+小存量；弱 | 依赖 Vercel API/生态 |
| 9 | Health · [MenuFit](https://apps.apple.com/us/app/menufit-healthy-eating-out/id6746144481) | 【事实】#7；53K 评分；7-17 更新 | 【平台估算】Play 100K+、12.3K 评论；中 | 菜单数据与营养准确性风险 |
| 10 | Health · [Cal AI](https://apps.apple.com/us/app/cal-ai-calorie-tracker/id6480417616) | 【事实】#6；353K 评分；8-11 更新 | RSS 50 条均近 30 日；中，但买量未知 | 类目已拥挤，健康准确性风险 |
| 11 | Health · [WeWard](https://apps.apple.com/us/app/weward-walking-rewards-app/id1454213029) | 【事实】#12；108K 评分 | 7-14 更新+大存量；弱 | 奖励资金与商户网络不可复制 |
| 12 | Health · [RISE](https://apps.apple.com/us/app/rise-sleep-tracker/id1453884781) | 【事实】#19；65K 评分；8-12 更新 | 单日榜+更新；弱 | 健康推断/长期算法重 |
| 13 | Photo · [Retro](https://apps.apple.com/us/app/retro-photos-with-friends/id6443709020) | 【事实】#10；11K 评分；8-07 更新 | 当前榜+编辑推荐存量；弱 | 社交图谱不可复制，周节奏可借 |
| 14 | Photo · [Cantina](https://apps.apple.com/us/app/cantina-ai-video-characters/id1018368216) | 【事实】#9；70K 评分；8-04 更新 | 单日榜+老存量；弱 | 模型、角色与社交网络重 |
| 15 | Photo · [Blackmagic Camera](https://apps.apple.com/us/app/blackmagic-camera/id6449580241) | 【事实】#24；21.5K 评分；7-22 更新 | 当前榜+硬件/品牌；弱 | 品牌与专业视频栈不可复制 |
| 16 | Photo · [ism](https://apps.apple.com/us/app/ism-retro-camera-vintage/id1580668065) | 【事实】#32；10.4K 评分；8-06 更新 | 单日榜+滤镜存量；弱 | 审美滤镜本身非楔子 |
| 17 | Music · [MusiChic](https://apps.apple.com/us/app/musichic-offline-music-player/id6751705626) | 【事实】#15；5.6K 评分；6-16 更新 | 2025-09 首发+当前榜；弱 | 音源/版权边界高 |
| 18 | Music · [Speaker Cleaner](https://apps.apple.com/us/app/speaker-cleaner-eject-water/id6761820807) | 【事实】#16；2026-04 首发；2.7K 评分 | 新品+当前榜；中弱，投放未知 | 单功能清楚但效果/误导风险 |
| 19 | Music · [Strum](https://apps.apple.com/us/app/strum-play-guitar/id6749384181) | 【事实】#29；19K 评分；8-06 更新 | 2025-08 首发+当前榜；弱 | 教学内容与曲库重 |
| 20 | Music · [Airbuds](https://apps.apple.com/us/app/airbuds-widget/id1638906106) | 【事实】#48；159K 评分；8-11 更新 | Google Play 页面可见 53.3K 评论、8-06 更新；中 | 音乐平台 API+社交图谱 |
| 21 | Weather · [WeatherWise](https://apps.apple.com/us/app/weatherwise-app/id6736407724) | 【事实】#11；737 评分；6-12 更新 | 当前榜+小存量；弱 | 天气 API 可做，差异需重验 |
| 22 | Weather · [Meteor Shower: Alerts](https://apps.apple.com/us/app/meteor-shower-alerts/id6788636545) | 【事实】#20；8-03 首发、0 评分 | 新品+榜位但无用户证据；很弱 | 单一事件结果清楚，可做 |
| 23 | Weather · [Tornado Tracker](https://apps.apple.com/us/app/tornado-tracker-by-tornadopath/id6756027933) | 【事实】#33；1.4K 评分；8-11 更新 | 2025-12 首发+当前榜；弱 | 涉及安全判断，排除候选 |
| 24 | Weather · [Precip](https://apps.apple.com/us/app/precip-rain-today-forecast/id6471449887) | 【事实】#34；5.6K 评分；8-10 更新 | 单日榜+更新；弱 | 与既有环境单值重复，仅对照 |
| 25 | Sports · [NorCal](https://apps.apple.com/us/app/norcal/id6771761943) | 【事实】#6；8-06 首发、1 评分 | 联赛/赛季事件；很弱 | 组织数据与分发不可复制 |
| 26 | Sports · [FIKA FOOTBALL](https://apps.apple.com/us/app/fika-football-live-scores/id6757428412) | 【事实】#20；2026-01 首发、5 评分 | 当前榜但几乎无正文；很弱 | 实时体育数据授权重 |
| 27 | Sports · [Fans First Tickets](https://apps.apple.com/us/app/fans-first-tickets/id6475806539) | 【事实】#22；84 评分、2.8 分 | RSS 29 条，近30日2、31–90日2；事件型中弱 | Banana Ball 品牌/票务资产不可复制 |
| 28 | Sports · [Card Ladder](https://apps.apple.com/us/app/card-ladder/id1541535971) | 【事实】#48；7.3K 评分；8-08 更新 | 单日榜+存量；弱 | 价格数据/卡库重；体育卡已研究 |
| 29 | Reference · [CoinIn](https://apps.apple.com/us/app/coinin-coin-scan-identifier/id1672111368) | 【事实】#9；96.7K 评分；8-13 更新 | 榜位+当天更新；弱 | 估值误导，最多借“ provenance ”工作流 |
| 30 | Reference · [HoloDex](https://apps.apple.com/us/app/holodex-tcg-scan-collect/id6747442689) | 【事实】#14；20.9K 评分；7-21 更新 | 2025-09 首发+当前榜；弱 | TCG 数据/商标/卡库重 |
| 31 | Reference · [Bible Note](https://apps.apple.com/us/app/bible-note-sermon-notes/id6743159952) | 【事实】#17；23.7K 评分；8-11 更新 | 2025-04 首发+当前榜；弱 | 录音隐私与转写成本 |
| 32 | Reference · [WoodSense](https://apps.apple.com/us/app/woodsense-wood-plans-guides/id6754165620) | 【事实】#33；8.9K 评分；8-06 更新 | RSS 50：近30日36、31–90日14；中 | AI 识木准确性差；可借开工前约束核对 |
| 33 | Reference · [Brickify](https://apps.apple.com/us/app/brickify-collection-tracker/id6758356210) | 【事实】#34；2026-02 首发；4K 评分 | 新品+当前榜；中弱 | LEGO 商标/数据；与既有 LEGO 研究重复 |
| 34 | Navigation · [FlockHopper](https://apps.apple.com/us/app/flockhopper/id6762170253) | 【事实】#7；2026-04 首发；163 评分 | 【平台估算】Play 10K+；中 | 单人开发信号好，但众包数据/驾驶安全高风险 |
| 35 | Navigation · [Speedometer Simple](https://apps.apple.com/us/app/speedometer-simple/id939507215) | 【事实】#16；124K 评分；8-09 更新 | 老 App 单日榜；弱 | 单结果清楚，驾驶安全约束 |
| 36 | Entertainment · [PineDrama](https://apps.apple.com/us/app/pinedrama-short-dramas/id6754134922) | 【事实】#3；2025-12 首发；13.6K 评分 | 新品+高榜位；中但投放未知 | 内容库/买量不可复制 |
| 37 | Entertainment · [StoryReel](https://apps.apple.com/us/app/storyreel-exclusive-drama/id6761538521) | 【事实】#7；2026-04 首发；22.4K 评分 | 新品+高榜位；中但投放未知 | 同上 |
| 38 | Entertainment · [VibeShort](https://apps.apple.com/us/app/vibeshort-ai-short-dramas/id6758667154) | 【事实】#15；2026-02 首发；26K 评分 | 新品+榜位；中但来源不明 | 内容/版权/买量 |
| 39 | Entertainment · [Soda Reels](https://apps.apple.com/us/app/soda-reels/id6758488784) | 【事实】#20；2026-02 首发；19.5K 评分 | 新品+榜位；中但来源不明 | 内容矩阵不可复制 |
| 40 | Shopping · [DealSeek](https://apps.apple.com/us/app/dealseek-coupons-discounts/id6745274862) | 【事实】#15；68K 评分；7-09 更新 | 2025-06 首发+大评分；中但奖励/买量未知 | 商户/联盟/补贴网络重 |
| 41 | Shopping · [Rips by Triumph](https://apps.apple.com/us/app/rips-by-triumph/id6751921248) | 【事实】#7；2025-10 首发；160K 评分 | 新品+高榜+大评分；中强但来源不明 | 直播拆卡、库存、支付、网络不可复制 |
| 42 | Shopping · [KashKick](https://apps.apple.com/us/app/kashkick-get-paid-to-have-fun/id1667151711) | 【事实】#17；104K 评分 | RSS 50 条均近30日；中 | 奖励资金/广告归因不可复制 |
| 43 | Design · [ReShoot](https://apps.apple.com/us/app/reshoot-ai-photos-edits/id6751296351) | 【事实】#3；2025-09 首发；14K 评分 | 新品+高榜；中但模型营销/投放未知 | 大而全不可取，可借“复拍一致性” |
| 44 | Design · [Tattoo AI](https://apps.apple.com/us/app/tattoo-ai-tattoo-design/id6479689893) | 【事实】#4；50.9K 评分 | RSS 50：近30日41、31–90日9；中 | 身体效果误导、同质化严重 |
| 45 | Design · [Piñata Farms](https://apps.apple.com/us/app/pi%C3%B1ata-farms-meme-generator/id1461925825) | 【事实】#12；46K 评分；8-11 更新 | 老 App 重新活跃；弱中 | 模板版权/肖像/社交网络风险 |
| 46 | Design · [Modyfy](https://apps.apple.com/us/app/modyfy-ai-car-designer/id6762754163) | 【事实】#13；2026-05 首发；697 评分 | 新品+榜位；中弱 | 可分享结果强，准确落地弱 |
| 47 | Lifestyle · [Duet Dating](https://apps.apple.com/us/app/duet-dating-app-chat-meet/id1673723000) | 【事实】#16；100K 评分；8-13 更新 | RSS 50 条均近30日；中 | 约会网络、审核、安全不可复制 |
| 48 | Social · [Valid](https://apps.apple.com/us/app/valid-compliment-classmates/id6755367062) | 【事实】#16；2025-12 首发；845 评分 | 新品+榜位；中弱 | 校园图谱、未成年人隐私不可复制 |
| 49 | Social · [Howbout](https://apps.apple.com/us/app/howbout-shared-calendar/id1477248221) | 【事实】#30；48K 评分；7-31 更新 | 单日榜+大存量；弱 | 社交图谱重，可借“变更摘要” |
| 50 | News · [CrimeRadar](https://apps.apple.com/us/app/crimeradar-dispatch-audio/id6746114452) | 【事实】#3；2025-05 首发；32K 评分 | 新品+高榜；中但媒体事件/投放未知 | 实时音频授权、隐私与安全，不可复制 |

## B. 30 个全新产品构型

> 已用现有“机会/初筛/AppIdea研究”报告关键词去重。下列不含：专注宠物、发型试戴、水印相机、周易反思、针织 WIP、活动 QR 相册、视频/音频学习卡、会议一页行动、网站 QA 截图包、PDF 有声化、房间表面替换、照片清理、宠物交接卡、Etsy 投递核对、小说连续性、播客 show-notes，以及旧报告里的反向音频、环境单值、菜谱捕获、轮播素材、AI 编程额度、视频取帧、情侣问答等。

| ID | 新候选句式 | 反推信号 | 单一结果 / 初步边界 | 首要反证 |
|---|---|---|---|---|
| C01 | 帮助【在真机上演示 localhost 的独立开发者】在【电脑或手机重启后】完成【本地依赖全绿的可分享就绪收据】 | LocalDevVPN | 探测用户指定端口/证书/局域网地址；生成红绿卡 | iOS 后台/网络权限；愿付费未知 |
| C02 | 帮助【离开电脑的 AI 编程用户】在【任务等待输入时】完成【只处理阻塞项的审批卡】 | Codex Relay | 显示变更摘要、风险、允许/拒绝；不做终端 | 集成与安全；已有 Codex/Paseo/T3 Code |
| C03 | 帮助【移动端测试 web demo 的开发者】在【把链接发给客户前】完成【“外部设备可达/不可达”的一次性收据】 | LocalDevVPN/Rev | URL、证书、LAN/公网三项；不做网站 QA 截图 | 与网络诊断工具竞争，价值频率低 |
| C04 | 帮助【有非医疗饮食偏好的聚餐者】在【坐下看菜单时】完成【三项可点菜的并列卡】 | MenuFit | 用户输入预算/素食/蛋白偏好；只引用菜单 | 菜单数据更新；不可做过敏安全保证 |
| C05 | 帮助【三至六人聚餐组织者】在【选餐厅前】完成【全员偏好交集的一页选择】 | MenuFit | 分享一次性表单→3 个交集餐厅 | 地点/菜单 API，分享转化未知 |
| C06 | 帮助【不想经营社交账号的家庭成员】在【周日晚上】完成【本周 9 张照片明信片】 | Retro | 本地选图、自动排版、导出 PDF/图片 | 与相册/模板竞争；是否周复用未知 |
| C07 | 帮助【给不会发帖的长辈分享近况的家庭】在【每周一次】完成【无需注册即可查看的只读照片包】 | Retro 评论 | 一次性加密链接、到期、无 feed | 托管成本/隐私；链接分享仍需网络 |
| C08 | 帮助【偶尔观星的城市居民】在【今晚出门前】完成【何时、朝哪、看多久的观星计划卡】 | Meteor Shower | 天文计算+天气可见度，单地点，离线缓存 | 天气误差；新 App 尚无用户证据 |
| C09 | 帮助【拍流星的手机摄影者】在【流星雨前一小时】完成【机位、朝向、开始时间的拍摄清单】 | Meteor Shower | 不承诺成片；只做计划卡 | 设备差异，需避免安全/成功保证 |
| C10 | 帮助【安排非关键户外活动的人】在【未来 3 小时】完成【去/等/改时段的证据卡】 | WeatherWise | 显示降雨、风、体感原始值与阈值 | 与天气 App 竞争；不可用于安全活动 |
| C11 | 帮助【周末木工新手】在【购买木料前】完成【现有工具和板材能否做该方案的可行性收据】 | WoodSense 评论 | 用户输入工具、板厚、单位；列缺口，不给安全指导 | 规格准确性、责任边界 |
| C12 | 帮助【拿到英文木工 cut list 的美国 DIY 用户】在【去建材店前】完成【英制分数、损耗和采购根数清单】 | WoodSense 评论 | 仅数值换算/排版；可打印 | 优化算法同类多；频率低 |
| C13 | 帮助【用公开视频学手作的人】在【决定是否开工前】完成【材料、工具、耗时三项提取卡】 | WoodSense/BookWatch | 仅处理用户提供文字/链接元数据 | 视频版权与抽取准确性；不做教程库 |
| C14 | 帮助【已买活动票的一家人】在【出门前一天】完成【每张票可打开、可转赠、可进钱包的演练收据】 | Fans First 评论 | 用户逐项确认并截图本地存证 | 无票务 API 时需手工；不能保证入场 |
| C15 | 帮助【替家人保管多张电子票的人】在【转票之前】完成【收件人、邮箱、票号后三位核对卡】 | Fans First | 本地 checklist；不接触票据付款 | 仍可能涉及敏感数据，频率低 |
| C16 | 帮助【做健身/装修/作品进度对比的创作者】在【第二次拍摄时】完成【与上次同机位的半透明叠影】 | ReShoot/Blackmagic | 相机网格、轮廓、距离提示；不生成内容 | 与相机网格同类；需证明付费 |
| C17 | 帮助【独自拍商品短视频的卖家】在【补拍镜头时】完成【焦段、机位、光线与留白一致的复拍卡】 | Blackmagic/ReShoot | 从用户上次照片提取构图参考 | 与 Etsy 投递核对不同；仍需真实复拍效果 |
| C18 | 帮助【小团队内容制作者】在【交给他人补拍前】完成【一张可视化镜头复刻说明】 | Blackmagic | 参考图+4 个可量化条件 | 专业工具已可做；团队付费不明 |
| C19 | 帮助【朋友群里的梗图制作者】在【拿到自有视频片段时】完成【三帧可编辑表情故事板】 | Piñata Farms | 不提供版权模板/人脸库，只处理自有素材 | 肖像同意、骚扰与深伪风险 |
| C20 | 帮助【吉他自学者】在【练同一小节 10 分钟后】完成【前后 10 秒 A/B 进步卡】 | Strum | 本地录音、波形/节拍对齐、导出 | 音乐版权；留存是否来自练习而非 App |
| C21 | 帮助【跨音乐平台的朋友】在【每周五】完成【各自 3 首“本周最想分享”交换卡】 | Airbuds | 手动选歌/链接，不抓完整历史 | Spotify/Apple Music 深链差异；社交冷启动 |
| C22 | 帮助【参加线下讲道/公开课的人】在【结束后两分钟】完成【一个引用、一个问题、一个行动的个人卡】 | Bible Note | 手动输入优先；不录整场、不做总结 | 与会议行动/学习卡相邻；需证明场景差异 |
| C23 | 帮助【视觉解释视频的制作者】在【发布前】完成【旁白与画面是否错位的逐段异常清单】 | BookWatch 用户差评 | 用户上传自有脚本+低清预览；仅标错位 | 视频处理成本；与网站 QA 不同但属 prosumer QA |
| C24 | 帮助【收藏旧币但不做估值的人】在【把一枚币放回盒前】完成【来源、年份、盒位标签】 | CoinIn | OCR+用户确认+打印小标签 | 录入负担；避免估值与真伪判断 |
| C25 | 帮助【收藏品交易会摊主】在【一天结束前】完成【只含自有物品的“新增/售出/待核”差异卡】 | HoloDex/Card Ladder | 扫码/手动；不提供市场价 | 与旧库存研究相邻，若持续录入失败即停 |
| C26 | 帮助【频繁改时间的朋友小组】在【重新打开共享日历时】完成【自上次查看后只显示变更的摘要】 | Howbout | iCalendar 导入/本地 diff；不建社交网 | 日历权限/时区；原生通知可能足够 |
| C27 | 帮助【组织小型球赛的家长】在【比赛当天早上】完成【地点、时间、装备三项变化卡】 | NorCal/Team apps | 从组织者粘贴的文本生成卡；不接联盟数据 | 现有群聊足够；需真实转发行为 |
| C28 | 帮助【改装车爱好者】在【比较两套外观方案时】完成【同角度、仅一处变化的对照卡】 | Modyfy | 用户照片+遮罩一个部件；不承诺实车效果 | 与房间表面替换方法相邻；AI 几何不稳 |
| C29 | 帮助【独立卖家补拍同一 SKU】在【几周后重拍时】完成【与旧主图一致的构图合格提示】 | ReShoot | 参考叠影+边距/角度检查；不上传平台 | 与商品拍摄工具竞争，须测节省时间 |
| C30 | 帮助【需要解释隐私取舍的普通驾驶者】在【选导航前】完成【最快、最少追踪、最少高速三路线差异卡】 | FlockHopper | 只展示数据来源/覆盖率；不承诺避开监控 | 地图/众包数据重，驾驶安全与政策风险 |

## C. 前 12 深核

> “两条正文/工作流”优先使用美国 App Store 公开评论；无评论的新 App 使用官方商店描述中的两条公开工作流，并明确不是用户证据。价格为商店页面当日列示的可见 IAP，可能因实验/地区存在多个档位。

| # / 构型 | 官方与用户正文/工作流 | 价格 / 竞争反查 | 传播钩子与 MVP 边界 | 技术、隐私、版权风险 / 初判 |
|---|---|---|---|---|
| D1 C01 本地依赖就绪收据 | [LocalDevVPN](https://apps.apple.com/us/app/localdevvpn/id6755608044)【事实】#10、81 评分、免费且声明不收集数据。<br>【用户正文】一位用户称重启后必须先打开 App，否则依赖服务失败；另一位称 iOS 26.4 调试报错显示混乱。 | 免费，无可见 IAP。竞争搜索多返回通用 VPN，窄本地开发关键词反而稀疏；相邻为 Tailscale/Charles/Surge。 | 分享红绿收据天然适合 issue/群聊。MVP：3 个用户自填依赖、一次探测、时间戳与导出，不建 VPN。 | iOS LAN 权限、证书与后台限制；若无法可靠区分“本机错/网络错”即停。**值得非开发验证设计。** |
| D2 C02 阻塞审批卡 | [Codex Relay](https://apps.apple.com/us/app/codex-relay-remote-codex-app/id6764463488)【事实】#27、46 评分、免费。<br>【用户正文】一位用户认可在 iPhone 使用 Codex；另一位警告改功能后常引入新 bug，仍需完整测试。 | 免费；搜索反查有 [Paseo](https://apps.apple.com/us/app/paseo-remote-coding-agents/id6758887924)、[T3 Code](https://apps.apple.com/us/app/t3-code-remote-claude-more/id6787819824) 与远程桌面。 | “你只剩 1 个阻塞决定”可截图传播。MVP 只做只读摘要+允许/拒绝，不开 shell、不展示 secret。 | 本地 relay、认证、提示注入、误授权；不能把移动批准写成代码正确。**观察。** |
| D3 C04 聚餐三选一卡 | [MenuFit](https://apps.apple.com/us/app/menufit-healthy-eating-out/id6746144481)【事实】iOS #7、53K 评分；[Google Play](https://play.google.com/store/apps/details?id=com.myhealthymenu.app) 为 100K+。<br>【用户正文】公开评论一边认可外食场景，一边指出“几乎无法按宣传工作”和热量数据不准。 | IAP 可见 `$9.99–$48` 多档。竞争：[MacroMenu](https://apps.apple.com/us/app/macromenu-eat-out-stay-fit/id6758923027)、[MenuScore](https://apps.apple.com/us/app/menuscore-eat-out-healthy/id6759840357)。 | 结果卡可发给同行者。MVP 只处理用户拍下/粘贴的当前菜单，输出 3 个偏好匹配项并引用原文。 | OCR、菜单变化、营养推断；明确排除过敏、疾病、热量准确承诺。**观察，风险偏高。** |
| D4 C06 每周 9 图明信片 | [Retro](https://apps.apple.com/us/app/retro-photos-with-friends/id6443709020)【事实】#10、11K 评分。<br>【用户正文】用户喜欢无广告/无算法；另一条指出 93 岁家人不会发帖，却因“发帖后才能看”受阻。 | 月 `$4.99`、年约 `$35.99`。竞争搜索有 [Day One](https://apps.apple.com/us/app/day-one-daily-journal-diary/id1044867788)、[Birdy](https://apps.apple.com/us/app/birdy-photo-video-journal/id1537856610)；Retro 自身网络/品牌强。 | 导出明信片就是传播物。MVP：本地选 9 图、1 句、固定模板、导出；不建账号/feed/群聊。 | 照片权限、EXIF、家庭隐私；“漂亮模板”不能成为唯一楔子，必须验证周复用。**值得非开发验证设计。** |
| D5 C08 今晚观星计划卡 | [Meteor Shower: Alerts](https://apps.apple.com/us/app/meteor-shower-alerts/id6788636545)【事实】8-03 首发、Weather #20、尚无评分。<br>【公开工作流而非用户正文】按位置给峰值/辐射点/暗夜窗口；按月相与暮光给可见度分数。 | 周 `$4.99`、终身 `$29.99`。竞争：[Shooting Star & Meteor Shower](https://apps.apple.com/us/app/shooting-star-meteor-shower/id6758892020)、[MeteorActive](https://apps.apple.com/us/app/meteoractive/id1205712190)、`$0.99` [Meteor Shower Guide](https://apps.apple.com/us/app/meteor-shower-guide/id451911714)。 | “今晚 22:40，东北，20 分钟”极易展示。MVP：单地点、5 场主要流星雨、卡片导出；不做 AR。 | 天文计算可本地，天气 API 需缓存；必须展示不确定性。新 App 无用户证据。**值得非开发验证设计，但证据弱。** |
| D6 C14 票务演练收据 | [Fans First Tickets](https://apps.apple.com/us/app/fans-first-tickets/id6475806539)【事实】#22、2.8 分。<br>【用户正文】有人因强密码/确认框无法完成注册；有人能买到临场票；另有用户反馈市场不可购买、换邮箱后被锁。 | 免费。竞争为 [See Tickets Wallet](https://apps.apple.com/us/app/see-tickets-wallet/id1477319091)、SeatGeek、Tixr、StubHub 与 Apple Wallet。 | “全家 4 张票均已演练”可发群。MVP 完全手工 checklist+本地截图，不接支付/售票。 | 截图含条码/个人信息；必须自动遮挡，不保证入场。低频且原生 Wallet 很强。**仅观察。** |
| D7 C11 木工开工前可行性收据 | [WoodSense](https://apps.apple.com/us/app/woodsense-wood-plans-guides/id6754165620)【事实】#33；RSS 近30日36、31–90日14。<br>【用户正文】一位用户喜欢工具/木料预告但要求英寸/厘米而非毫米及真实照片；另一位实测 16 个标注木样仅 2 个识别正确；还有用户找不到宣传的自建设计入口。 | IAP 约 `$3.99/$29.99/$39.99`。竞争：[WoodCraft](https://apps.apple.com/us/app/woodcraft-wood-plans-guides/id6786504668)、[TimberTinker](https://apps.apple.com/us/app/timbertinker-woodworking-3d/id6738879966)。 | 采购清单/缺口卡天然可打印。MVP 不识木、不生成结构，只核单位、工具、板厚、采购根数。 | 输入规格错误仍会误导；不提供承重/安全建议。**值得非开发验证设计。** |
| D8 C30 路线取舍卡 | [FlockHopper](https://apps.apple.com/us/app/flockhopper/id6762170253)【事实】iOS #7；[Google Play](https://play.google.com/store/apps/details?id=com.dontgetflocked.flockhopper) 10K+。<br>【公开工作流】每次给最快/较少 ALPR 两路线；地图展示摄像头并声明社区数据不完整。商店评论认可隐私目标，也有人要求覆盖/体验改进。 | 免费，Tip Jar `$4.99–$49.99`。竞争搜索多为通用离线导航；核心地图基于开源 Ferrostar，但数据资产是门槛。 | 路线差异截图传播性强。MVP 若做，只能做静态“数据来源与覆盖差异”，不做驾驶导航。 | 位置隐私、众包准确性、规避执法误用、驾驶安全；残余风险过高。**热门方法信号，不推荐实现。** |
| D9 C16 同机位复拍叠影 | [ReShoot](https://apps.apple.com/us/app/reshoot-ai-photos-edits/id6751296351)【事实】Design #3、14K 评分。<br>【公开工作流】单自拍生成多类造型；旧照片增强/合成/商品图。评论同时有快速效果赞许与试用扣费/结果失望。 | 周订阅可见 `$7.99–$14.99`，月 `$7.99`，点数 `$2.99/$4.99`。竞争搜索多为 Retake/Reface/YouCam，而“同机位复拍”可用相机网格类替代。 | 真实 before/after 是产品结果也是传播物。MVP 不用生成式 AI：透明叠影、轮廓、边距、导出对比。 | 人像本地处理优先；相册隐私、姿态误差；若原生相机网格足够即停。**值得非开发验证设计。** |
| D10 C19 自有片段三帧梗图 | [Piñata Farms](https://apps.apple.com/us/app/pi%C3%B1ata-farms-meme-generator/id1461925825)【事实】#12、46K 评分。<br>【用户正文】早期用户喜欢“从他人模板再创作”的循环；后续用户抱怨改版变复杂；另有用户称单次付费生成失败或无音频。 | 周 `$6.99`、月 `$7.99`、年 `$39.99/$49.99`，单次 `$1.99–$4.99`。竞争：Mug Life、Reface、Meta Meme。 | 结果高度可分享。MVP 仅处理用户自有片段/贴纸，默认水印“edited”，无公共 feed。 | 肖像同意、骚扰、深伪、模板版权、算力；安全负担高。**观察，不进前六。** |
| D11 C22 一引一问一行动卡 | [Bible Note](https://apps.apple.com/us/app/bible-note-sermon-notes/id6743159952)【事实】#17、24K 评分。<br>【公开工作流】录讲道→转写/搜索；摘要→经文/洞见/行动闪卡。用户评论既肯定捕捉与学习，也有“很好但是……”的功能摩擦。 | 周约 `$6.99–$8.99`、年约 `$39.99–$69.99`。竞争：[Sermon Notes](https://apps.apple.com/us/app/sermon-notes-hear-learn-live/id683912245) 与通用录音笔记。 | 小卡可在小组内分享。MVP 只手动输入 3 个字段，不录音、不转写、不收宗教档案。 | 宗教/个人反思敏感数据；与既有会议行动、学习卡方法相邻，去重新意不足。**降级为对照。** |
| D12 C23 旁白画面错位清单 | [BookWatch](https://apps.apple.com/us/app/bookwatch-visual-learning/id1660054787)【事实】Books #18、11K 评分。<br>【用户正文】有人看到婚姻主题视频却出现股市画面；有人认为视觉任意、重形式轻内容；另有评论指冻结、无声和书籍不可访问。 | 月 `$12.99`，年/试用可见 `$24.99–$139.99` 多档。竞争：[Actofy](https://apps.apple.com/us/app/actofy-visual-book-summaries/id6737353977)、Blinkist、Shortform。 | QA 异常清单可直接交剪辑者。MVP：用户自有脚本+低清视频，每 10 秒对齐关键词，人工确认。 | 视频/模型成本、误报、上传隐私；不能处理受版权保护内容库。**值得非开发验证设计，prosumer 小样本。** |

## D. 最多 6 个值得继续验证的方向（仍不开发）

### 1. C01 重启后本地开发依赖就绪收据

- 支持：【用户正文】明确出现“重启后未先打开工具→依赖服务失败”的后果；LocalDevVPN 当前 Developer Tools #10，窄场景真实。
- 反证：只有 81 个评分且无近期评论序列；免费工具、脚本、系统诊断可能已足够。
- 第一批用户在哪里：使用 iPhone/iPad 真机调 localhost、StikDebug、局域网 demo 的独立 iOS/web 开发者；GitHub Issues、iOS 开发论坛、相关工具社区（下一轮只公开招募，不外联前需授权）。
- 最小非开发验证：给 8 人一张可点击原型；让其在真实重启/演示前手工填 3 个依赖并导出收据。C = 5 人真实完成探测并把收据发到 issue/群；R = 7 天内至少 3 人无催促再用。
- 停止：少于 3/8 遇到该问题；现有脚本一次解决；无人愿付 `$5` 买断或 `$1/月`。

### 2. C16 同机位复拍叠影

- 支持：before/after 结果一分钟可理解、自然可分享；通用生成式相机热度证明“可见结果”强，但此构型不依赖生成模型。
- 反证：原生网格/三脚架/现有 overlay 相机可能足够；“更好看”不是楔子。
- 第一批用户在哪里：健身进度、房屋改造、手工作品、商品补拍创作者的公开社区与短视频账号。
- 最小非开发验证：Figma/视频模拟“上次轮廓覆盖实时相机”；让 10 人用自己的两张照片手工复拍。C = 6 人拍成；V = 至少 3 人主动分享对比；R = 14 天内 3 人第二次用。
- 停止：复拍节省不足 2 分钟；大多数只需系统网格；分享发生但没人再次拍。

### 3. C08 今晚观星计划卡

- 支持：一句话与首次反馈极清楚；可本地天文计算；新 App 上线十天进入 Weather #20，说明事件型入口可能存在。
- 反证：0 评分，无用户正文；榜位可能由上新/季节/ASO 而非自然增长；免费网页和天文 App 多。
- 第一批用户在哪里：美国观星、露营、城市摄影的公开社群；近期 Perseids 搜索者。
- 最小非开发验证：不用 App，做地点+日期网页表单，人工返回 1 张计划卡。C = 15 个真实地点输入中 8 人按卡出门/设提醒；R = 下一场流星雨有 3 人主动回来。
- 停止：天气不确定性导致错误承诺；用户只收藏不出门；免费搜索已足够。

### 4. C06 每周私人 9 图明信片

- 支持：Retro 评论明确喜欢无广告/无算法，但长辈被“必须发帖才可看”卡住；本地导出避开社交网络冷启动。
- 反证：相册自动回忆、Canva 模板和家庭群聊已足够；固定周节奏可能形成负担。
- 第一批用户在哪里：跨城市家庭、给祖父母分享孩子近况的家长、隐私优先照片用户。
- 最小非开发验证：连续两周用模板人工交付；C = 10 户中 6 户真实选 9 图并发出；R = 第 2 周 4 户无催促再次提交；付款 = 2 户愿付 `$3/月` 或 `$20/年`。
- 停止：选图超过 5 分钟；接收者仍要求相册链接；第 2 周复用少于 3 户。

### 5. C11 木工开工前可行性收据

- 支持：WoodSense 的 dated 评论直接暴露单位、工具、材料、真实图与方案可达性的具体摩擦；50 条 RSS 中 36 条在近30日。
- 反证：AI 识木实测反证强，不能沿用；专业 cut-list 优化器与木工计划站成熟；低频。
- 第一批用户在哪里：美国 beginner woodworking、DIY 家具、Home Depot/Lowe’s 项目社区中的周末新手。
- 最小非开发验证：让 8 人带一份真实计划、现有工具和板材；人工返回“可做/缺什么/单位换算”收据。C = 5 人据此改变采购；付款 = 2 人愿为一次收据付 `$5`。
- 停止：需要结构/承重/安全判断；输入规格经常不全；用户只要免费计算器。

### 6. C26 共享日历“自上次查看后变更摘要”

- 支持：Howbout #30、48K 评分说明共享安排行为存在；“变化”比再造日历更窄，结果适合转发。
- 反证：Apple/Google 日历通知可能已足够；时区、重复事件、取消/恢复会造成错报；API 权限敏感。
- 第一批用户在哪里：旅行小组、业余球队家长、轮班朋友群；优先已有共享 iCalendar 的人。
- 最小非开发验证：用户导出两份去敏 ICS，人工 diff 生成变更卡。C = 10 组中 6 组转发；R = 14 天内 3 组再次上传；停止前不请求日历写权限。
- 停止：多数变化在原群聊已清楚；误报率 >10%；无人愿授予只读权限。

### V-S-C-R 汇总

| 方向 | V（传播） | S（两周约20实验） | C（真实动作） | R（无催促复用） | 当前判定 |
|---|---|---|---|---|---|
| C01 开发就绪收据 | issue/群内收据可传播【待验证】 | 依赖数/平台/错误解释可单变量 | 真重启后探测并发送 | 下一次重启/演示再用 | 值得设计验证 |
| C16 复拍叠影 | before/after 天然展示 | 人群/叠影强度/提示方式 | 用自己的旧图完成复拍 | 下一周/下一阶段再拍 | 值得设计验证 |
| C08 观星卡 | 地点+时间卡可转发 | 城市/事件/提醒时点 | 提交地点并真实出门/设提醒 | 下一次天象主动回来 | 值得设计验证，证据最弱 |
| C06 周明信片 | 接收者即分发对象 | 人群/张数/模板/节奏 | 真实选图并发出 | 第二周再做 | 值得设计验证 |
| C11 木工收据 | 采购卡可带去门店/分享 | 计划类型/单位/工具输入 | 按收据改变采购 | 下一项目回来 | 值得设计验证 |
| C26 日历变更卡 | 群内转发 | 小组/事件/摘要格式 | 上传真实 ICS 并转发 | 下一批变化再用 | 值得设计验证 |

## E. 15+ 条反证 / 失败案例

1. 【事实】7 Brew 两天内新上架并到总榜 #1，但这是门店品牌事件，不能证明独立工具获客。
2. 【事实】Meteor Shower 进入 Weather #20 却仍 0 评分；榜位不能替代用户行为。
3. 【事实】WoodSense 的标注木样实测评论为 2/16 正确；漂亮 AI 识别不能越过准确性。
4. 【用户正文】WoodSense 宣传自建设计，但用户找不到新增入口；商店文案不能替代可完成工作流。
5. 【用户正文】MenuFit 有“热量不准/几乎不按宣传工作”的反证；健康偏好工具不能提供过敏或医疗保证。
6. 【用户正文】BookWatch 出现旁白主题与画面错位、冻结和无声；大量 AI 内容会把内容 QA 变成核心成本。
7. 【用户正文】Fans First 的强密码确认、市场购买、改邮箱均能阻断进场前任务；强制 App 并不等于好产品。
8. 【事实】PineDrama、StoryReel、VibeShort、Soda Reels 同期高榜，但内容库、版权、投放与订阅漏斗均不可由个人 2–6 周复制。
9. 【事实】Rips by Triumph 在上架不足一年已有 160K 评分且 Shopping #7，但直播拆卡、库存、支付、信任和网络效应是核心资产。
10. 【事实】KashKick 的 50 条 RSS 均在近30日，不等于自然增长；奖励资金与广告归因可能制造行为。
11. 【事实】Duet Dating 的近30日评论流与 100K 总评分不能转移给无网络的新产品；约会审核与安全是停止级约束。
12. 【事实】Valid 的校园赞美机制涉及未成年人、校园图谱和匿名互动风险，不适合个人轻量复制。
13. 【事实】CrimeRadar News #3 依赖实时 dispatch 音频、地域覆盖、内容权利和公共安全语境。
14. 【事实】FlockHopper 的跨平台信号真实，但社区摄像头数据不完整；把“少摄像头路线”写成保证会造成安全和政策风险。
15. 【事实】ReShoot/Piñata 的强传播结果伴随周订阅、多次单次付费、生成失败、肖像与版权风险；UGC 可传播不等于健康商业。
16. 【事实】Airbuds 的核心是朋友音乐活动和音乐服务 API；社交图谱与平台接入不是一个 widget 可以复制的。
17. 【事实】NorCal/FIKA/Saturn 的榜位与赛季/校园时点相关，组织数据与既有分发渠道不能转移给通用工具。
18. 【推断】C22 讲道行动卡与既有“会议一页行动/音频学习卡”方法相邻，若不能证明宗教场景产生不同购买理由，应去重淘汰。
19. 【推断】C25 收藏差异卡与既有库存研究相邻；若用户不愿持续录入，即使扫描准确也应停止。
20. 【事实】Product Hunt 当前不可读、Reddit/TikTok 正文不可用；缺少这些渠道不是“没有传播”，也不能被商店评论静默替代。

## F. 热门但不可复制，以及是否挑战 P0

### 热门但不可复制

- 品牌/线下入口：7 Brew、NorCal、Fans First。
- 内容+买量：PineDrama、StoryReel、VibeShort、Soda Reels、BookWatch。
- 奖励/交易资金：WeWard、DealSeek、KashKick、Rips。
- 网络图谱/审核：Duet、Valid、Retro、Airbuds、Saturn。
- 数据/实时权利：CrimeRadar、FIKA、Card Ladder、HoloDex、FlockHopper。
- 模型/版权/肖像：Cantina、ReShoot、Tattoo AI、Piñata、Modyfy。

### 对当前 P0 的结论

【结论】没有挑战 P0 的强证据。本轮六个推荐方向的最高证据只有：

- C01 有一个明确故障后果与当前窄榜位，但没有购买/复用；
- C16 有强展示性，但尚未证明原生网格不能替代；
- C08 有新上架榜位，但 0 评分；
- C06 有用户对“无算法+长辈只读”的正文，但原产品依赖社交图谱；
- C11 有具体用户摩擦和 dated 评论流，但原产品准确性反证强；
- C26 有大存量相邻产品，但差异构型仍是推断。

要挑战 P0，至少还缺：同一人群/承诺/核心动作下的多个独立传播（V）、两周 20 个单变量实验可执行性（S）、真实用户提交自己的输入并完成结果（C）、无催促二次使用（R），以及真实付款。任何一个方向只有播放、榜位、评分、下载档位、原型点击或口头愿用，都不得升级。

## G. 证据计数、来源分布与运行卫生

- 原始信号池：**50 App / 16+ 领域**。
- 新构型：**30**；前 12 深核：**12**；建议进入非开发验证设计：**6**；绿灯：**0**。
- Apple：当前免费总榜 1 个、分类榜 16 个；50 个商店/Lookup 对象；50 个最新评论 RSS ID 尝试。
- 评论：8 个 App 返回可计数 RSS，共 381 条；近30日329、31–90日27、90日前25。其余 42 个 RSS 为空响应，不能写 0。
- Google Play：公开搜索 8 组；精确打开 3 个对象页；可计数安装档位 2 个（MenuFit 100K+、FlockHopper 10K+），Airbuds 页可见 53.3K 评论但本次抓取未显示安装档位。
- 公开用户正文：前 12 深核中 9 个取得 App Store 评论摘要；Meteor 使用 2 个官方公开工作流、不是用户证据；所有引用均指向可点击商店页。
- Product Hunt：feed/首页 2 次只读访问；首页安全验证、feed 空壳，0 个可计数信号。
- Reddit/TikTok/YouTube：0 个可计数正文；原因分别为 OpenCLI 扩展缺失/登录与正文限制/YouTube JS runtime 未配置。未安装、未登录、未绕过。
- AppMagic/Sensor Tower/Similarweb：0 个本轮对象级时序数字；未使用登录墙、付费数据或搜索摘要估算。
- 去重：读取/扫描 `/Users/USER/Documents/app` 下 6 份核心“机会/初筛/AppIdea研究”报告，并以用户点名排除清单二次过滤；相邻项在表内标为对照或降级，不计新推荐。
- 临时文件：**无**。网络内容均流式读取；未下载 App、视频、图片或数据包。
- 唯一新增文件：本报告；未修改 AGENTS.md、源码或既有报告。

## 关键入口

- [Apple 美国区免费总榜（查询 2026-08-13）](https://rss.marketingtools.apple.com/api/v2/us/apps/top-free/100/apps.json)
- [Apple 美国区 Developer Tools 免费榜](https://apps.apple.com/us/iphone/charts/6026?chart=top-free)
- [Apple 美国区 Weather 免费榜](https://apps.apple.com/us/iphone/charts/6001?chart=top-free)
- [Apple 美国区 Reference 免费榜](https://apps.apple.com/us/iphone/charts/6006?chart=top-free)
- [Apple 美国区 Graphics & Design 免费榜](https://apps.apple.com/us/iphone/charts/6027?chart=top-free)
- [Google Play MenuFit](https://play.google.com/store/apps/details?id=com.myhealthymenu.app)
- [Google Play FlockHopper](https://play.google.com/store/apps/details?id=com.dontgetflocked.flockhopper)

