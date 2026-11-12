# Chrome＋YouTube 研究通行证：公开桌研与非开发验证设计

日期：2026-08-09  
阶段：公开桌面研究与验证设计  
决策状态：**继续做行为验证设计；本轮没有绿灯**  
边界：未开发、未写代码、未创建扩展、未外联、未注册、未付款、未发布。

## 一、一屏结论

### 决策：继续做行为验证设计

- 【事实】问题真实且足够具体：本轮纳入 **40 条独立真实用户正文**，来源分布为 Reddit 27、Mozilla Add-ons 用户评价 10、YouTube 实际评论 3；其中 **9 条**明确描述“为学习、编码、工作或指定视频进入 YouTube 后偏航”，**12 条**涉及 blocker／去推荐工具失效、绕过、跨端逃逸或工作流损伤，**14 条**构成反证。类别可重叠，未把下载量、星级、点赞或产品作者自述计作留存或付费。
- 【事实】最强支持不是泛泛“我会拖延”，而是可复述的链路：技术教程／课程／工作问题 → 打开 YouTube → Shorts、侧栏、搜索后推荐或“短休息” → 30–180 分钟偏航 → 原任务延误、兴趣耗尽或上下文丢失。例如 [ADHD 学习帖](https://www.reddit.com/r/ADHD/comments/177gfh6/)、[教授课程帖](https://www.reddit.com/r/GetStudying/comments/pex6il/)、[编码分心帖](https://www.reddit.com/r/Python/comments/1qknt6c/)、[工作时段帖](https://www.reddit.com/r/productivity/comments/13bt35w/)。
- 【事实】最强反证是现有组合已经非常接近完整闭环：Unhook 可隐藏主页、侧栏、Shorts、评论、片尾推荐及关闭自动播放；Purpose Browser 已提供“进入前写目标＋计时＋常驻意图条”；Intention 已提供访问前暂停、临时解锁时长和到期暂停；Aware 也提供意图、计时和浮动提醒。[Unhook 官方商店页](https://chromewebstore.google.com/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid)、[Purpose Browser](https://www.purposebrowser.com/)、[Intention](https://www.getintention.com/)、[Aware](https://getaware.app/)。
- 【推断】因此待证的不是“去推荐是否有效”，而只有一个极薄增量：**到期时把用户带回进入 YouTube 前写下的原任务，是否比 Unhook＋Purpose/Intention 更能恢复行动，同时不造成打断和上下文损失。**
- 【事实】反例表明自动打断可能有害：有人使用计时 blocker 后更焦虑；有人被定时提示打断；有人付费使用 Freedom 后，block 开始时丢失正在读的文章标题/地址；Mozilla 评价也指出隐藏片尾后视频结束变成黑屏、难判断是否结束。[工作时段讨论](https://www.reddit.com/r/productivity/comments/13bt35w/)、[计时器反效果](https://www.reddit.com/r/productivity/comments/zchfmg/)、[Freedom 丢上下文](https://www.reddit.com/r/nosurf/comments/1os7cky/)、[Unhook 评价](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)。
- 【待验证】只有当窄人群在真实任务中表现出“现有组合仍会在主动搜索后偏航”，且自动返回使超时下降、任务完成不下降、打断投诉可控，才值得讨论原型；否则停止。

### 最小判断式

`问题频率` × `现有组合后的剩余偏航` × `自动返回的净收益` × `权限接受度` 必须同时为正。任何一项为零，都不应开发。

## 二、最窄目标用户与高频触发时刻

### 首批只保留：英语市场的自学型技术学习者／早期独立开发者

定义：主要在桌面 Chrome 上，每周至少 3 天用 YouTube 查编程教程、修 bug、学技术工具或完成明确课程；最近一周至少发生 2 次、每次至少 10 分钟的偏航；能说出原任务、第一步偏航、后果和 workaround。

高频触发时刻：

1. 卡在一个 bug／工具操作上，准备看一个 5–10 分钟教程。
2. 学一门技术课，需打开一个已知 lecture／playlist。
3. 想用“quick break”缓冲困难任务，结果被教程、视频 essay 或 Shorts 接管。
4. 完成目标视频后，片尾、侧栏或搜索结果继续引出“相关但非当前任务”的内容。

### 人群比较

| 人群 | 问题一致性 | 可触达性 | 现有证据 | 核心冲突 | 本轮结论 |
|---|---:|---:|---|---|---|
| 自学型技术学习者／早期独立开发者 | 高 | 高 | 编码 10–15 分钟后开 YouTube 丢一小时；软件工程师因工作需要技术教程，无法整站屏蔽 | 仍可能主动搜索偏航；技术用户也更容易禁用扩展 | **首批验证** |
| 一般在线学习者 | 很高 | 很高 | 课程、JEE、lecture、Shorts 偏航证据最多 | 年龄、付费能力和任务类型过散 | 作为招募池，不作为最终商业标签 |
| 自由职业内容工作者 | 中 | 中 | “工作需要 YouTube”有个别证据 | 推荐、评论、趋势本身可能是工作输入 | 暂不首测 |
| 研究型创作者 | 中 | 中 | 信息频道／行业视频容易形成“生产力伪装” | 发现新素材依赖推荐链，去推荐可能降低工作质量 | 暂不首测 |
| 所有拖延者／ADHD 人群 | 低 | 高 | 痛点强但异质、涉及医疗标签 | 非 YouTube 专属，跨端和行为问题更大 | 明确排除泛化 |

【推断】最容易触达且问题最一致的是“自学型技术学习者／早期独立开发者”，但他们未必最愿付费；本轮应先验证行为增量，不应提前优化收入。

## 三、需求证据与反证表

### A. 明确的任务内偏航

| # | 正文事实（短转述） | 原任务 → 偏航 → 后果 | 判断 | 来源 |
|---:|---|---|---|---|
| 1 | 为研究／学习打开 YouTube，Shorts 自动播放，三小时后忘记所学 | 查一个问题 → Shorts → 3 小时、失去学习兴趣 | 【事实】强支持 | [Reddit](https://www.reddit.com/r/ADHD/comments/177gfh6/) |
| 2 | 打开教授的 40 分钟 lecture，却看足球等视频一整天 | 课程 → 其他视频 → 一小时任务拖到全天 | 【事实】强支持 | [Reddit](https://www.reddit.com/r/GetStudying/comments/pex6il/) |
| 3 | JEE 化学视频后转到 cricket highlights，90 分钟后才意识到 | 指定课程 → 推荐 → 90 分钟 | 【事实】强支持 | [Reddit](https://www.reddit.com/r/GetStudying/comments/1t9bzz6/) |
| 4 | 工作难题／不舒服的对话前看“一个 quick video”，一个变五个或二十个 | 工作 → 休息视频 → 连续观看 | 【事实】支持；也说明入口可能是主动逃避 | [Reddit](https://www.reddit.com/r/productivity/comments/13bt35w/) |
| 5 | 编码 10–15 分钟后随机搜索、开 YouTube，下一次看时间已过一小时 | 编码 → 快速休息 → 1 小时、失去 flow | 【事实】强支持首批人群 | [Reddit](https://www.reddit.com/r/Python/comments/1qknt6c/) |
| 6 | 先看目标视频前会消费 30–60 分钟推荐，点第一条后忘记原目的 | 工作／教育视频 → 第一推荐 → 30–60 分钟 | 【事实】强支持常驻任务锚点 | [Reddit](https://www.reddit.com/r/productivity/comments/og55y1/) |
| 7 | 只订阅教育频道仍不断刷推荐并点开无生产力内容 | 学习 → 推荐页 → 持续滚动 | 【事实】推荐质量“教育化”仍不等于当前任务 | [Reddit](https://www.reddit.com/r/productivity/comments/hka5p0/) |
| 8 | 软件工程师不能整站屏蔽，因为要查技术教程／修 bug；曾一天看 4 小时 | 工作资料 → 推荐 → 过度观看 | 【事实】最接近职业用途 | [Reddit](https://www.reddit.com/r/nosurf/comments/c26jt9/) |
| 9 | 需要 YouTube 工作，但只想永远移除 Shorts；把 Shorts 比作桌上的烟 | 工作 → Shorts → 复发 | 【事实】需求极窄但拒付倾向强 | [Reddit](https://www.reddit.com/r/productivity/comments/1tcpr68/) |

### B. 现有工具不足、绕过和失效

| # | 用户正文 | 对本闭环的意义 | 来源 |
|---:|---|---|---|
| 10 | Unhook 的片尾卡重新出现，随后又 binge 数小时 | 【事实】页面变化／维护失效会直接恢复偏航 | [Reddit](https://www.reddit.com/r/nosurf/comments/1qdrffz/) |
| 11 | 时间限制扩展有明显绕过路径，用户预计自己会绕过 | 【事实】仅 timer 不构成可靠控制 | [Reddit](https://www.reddit.com/r/GetStudying/comments/pex6il/) |
| 12 | 给工作与娱乐分账号／设备仍会切过去；计时器到点声响本身会打断 | 【事实】跨端逃逸＋打断风险 | [Reddit](https://www.reddit.com/r/productivity/comments/zchfmg/) |
| 13 | 付费 Freedom 后仍可删除当前 session | 【事实】付款不等于不可绕过 | [Reddit](https://www.reddit.com/r/digitalminimalism/comments/z8tz4a/) |
| 14 | “用 Freedom 屏蔽 Freedom”后仍找到抢先关闭的时间差漏洞 | 【事实】强制工具会诱发对抗性绕过 | [同帖评论](https://www.reddit.com/r/digitalminimalism/comments/z8tz4a/) |
| 15 | 浏览器扩展太容易作弊，禁用后就恢复 | 【事实】技术人群尤其会绕过 | [编码帖评论](https://www.reddit.com/r/Python/comments/1qknt6c/) |
| 16 | 近期 Mozilla 评价报告新标签页破坏播放、浏览器冻结、卸载后变快 | 【事实】页面兼容与性能是持续维护成本；Firefox 证据不可直接等同 Chrome | [评价列表](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)（ID 2726100、2725914、2725321） |
| 17 | YouTube 评论询问如何只屏蔽主页但保留搜索、如何在锁定时继续查有用信息 | 【事实】“保留研究能力”是必要条件 | [评论 1](https://www.youtube.com/watch?v=2qDE048ovsI&lc=UgyKRg_dnEwFtSFf6_x4AaABAg.9zNhV3z6f_JA8JdO7FKJSL)、[评论 2](https://www.youtube.com/watch?v=2qDE048ovsI&lc=UgzFgXU6hd_QVSmbAsB4AaABAg) |

### C. 主动寻找的反证

| # | 反证正文 | 反证力度 | 来源 |
|---:|---|---|---|
| 18 | 有人称 Unhook 是用过最好的扩展，直接节省时间与精力；另一人称桌面问题“完全解决” | 【事实】现有去推荐方案可能已经够用 | [Reddit 1](https://www.reddit.com/r/nosurf/comments/1af9uyc/)、[Reddit 2](https://www.reddit.com/r/nosurf/comments/1fxixxr/) |
| 19 | 学术型用户通过 watch later 和训练推荐，得到以 lecture 为主的有益推荐 | 【事实】推荐不总是敌人；隐藏可能损失发现价值 | [Reddit](https://www.reddit.com/r/nosurf/comments/c26jt9/) |
| 20 | 关闭观看历史、用隐身窗口或独立学习账号即可让主页接近空白 | 【事实】无新产品替代路径成立 | [Reddit](https://www.reddit.com/r/nosurf/comments/1fc2hyx/) |
| 21 | blocker 让人一天结束时更焦虑，因此只在确有重要任务时使用 | 【事实】持续强制并非普适 | [Reddit](https://www.reddit.com/r/productivity/comments/13bt35w/) |
| 22 | 付费 blocker 开始后丢失文章标题和地址，用户认为“谁会想要这样” | 【事实】自动返回若抹掉上下文会制造损失 | [Reddit](https://www.reddit.com/r/nosurf/comments/1os7cky/) |
| 23 | one sec 付费用户称无效，因为只是从一个 app 跳到另一个 | 【事实】入口级摩擦可能迁移行为而非解决行为 | [Reddit](https://www.reddit.com/r/one_sec/comments/1iehmhg/) |
| 24 | Mozilla 用户希望保留侧栏推荐，只移除 playlist/live chat/fundraiser，显示精细可配置比“一刀切”更重要 | 【事实】自动隐藏全部会过度约束 | [Mozilla 评价](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)（ID 2734674） |
| 25 | Mozilla 用户称 Unhook 数月来已让观看变得有意图；另一人称对 rabbit hole 的效果出乎意料 | 【事实】组合中的去推荐部分已被用户验证 | [Mozilla 评价](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)（ID 2732286、2731092） |
| 26 | 隐藏片尾后视频直接黑屏，用户无法判断是否结束 | 【事实】“到期／结束”反馈若设计不好会增加认知成本 | [Mozilla 评价](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)（ID 2726402） |
| 27 | YouTube 评论指出 kiosk mode 可轻易绕过 blocker | 【事实】强制性表述不可兑现 | [YouTube 评论](https://www.youtube.com/watch?v=2qDE048ovsI&lc=UgwNeyMH89J_6_tp0B14AaABAg) |

### 证据审计

- 【事实】计数口径：不同作者的一条帖子或评论计一条；同作者在同一线程的追评合并；跨版重复发布、纯推广帖、bot、删除/无正文、搜索摘要不计。
- 【事实】40 条正文中，直接展示在上表的是代表性 27 条；其余用于交叉核对权限恐惧、付费、兼容和 workaround。
- 【推断】学生／学习者样本明显多于自由职业者和研究型创作者，不能把“学习痛点强”外推为英语自由职业者市场规模。
- 【待验证】频率仍依赖自述，缺少 7 天逐次事件日志；桌研不能证明复用、留存或付费。

## 四、现有组合方案对照：Unhook＋Intention/Aware 是否已足够

| 闭环步骤 | Unhook | Intention | Purpose Browser | Aware | 待验证方案的可能增量 |
|---|---|---|---|---|---|
| 进入前写唯一目的 | 无 | 官方页未显示自由文本目的，只显示访问前暂停与设时长 | 有：进入前设明确目标 | 有：设意图 | 一次设置，专门绑定 YouTube session |
| 5/10 分钟通行 | 无 | 有：指定临时解锁时长 | 有：内置 timer | 有：可选时限 | 只给 5/10 两档，减少配置 |
| 隐藏推荐、Shorts、评论、片尾 | **完整覆盖** | 不负责页面去推荐 | 不负责页面去推荐 | “smart blocking”但非 YouTube 元素级 | 与 Unhook 功能重叠，不应自称创新 |
| 持续显示原任务 | 无 | 官方页未证明常驻原任务 | 有：ever-present intention bar | 有：浮动 reminder | 只在 YouTube 显示，可能更少干扰 |
| 持续显示剩余时间 | 无 | 有计时／到期暂停 | 有 timer | 有 countdown | 基本已覆盖 |
| 到期处理 | 无 | 暂停 browsing | 有 timer，但官方页未写自动回原任务 | 可 pause/resume/edit | **唯一明确待证增量：保留上下文后返回原任务** |

【事实】[Unhook](https://chromewebstore.google.com/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid) 当前官方列出的隐藏项已经覆盖本项目想隐藏的四类页面元素；[Purpose Browser](https://www.purposebrowser.com/) 的“目标＋计时＋常驻条”与本项目高度同构；[Intention](https://www.getintention.com/) 到期会暂停浏览；[Aware](https://getaware.app/) 当前免费层宣称包含意图、timer、浮动条、blocking 和本地统计。

【推断】对大多数桌面用户，**Unhook＋Purpose Browser 已经足够**。新方案只有在三种情形同时成立时才有增量：

1. 用户不愿配置两个扩展，且配置成本真实导致弃用；
2. 主动搜索后仍会偏航，单纯隐藏 feed 不够；
3. 到期后的“返回原任务”比普通 block/暂停更能恢复行动，并且不丢失视频时间点、笔记、标签页和研究线索。

【待验证】若受试者用现有组合一周后，偏航已下降到可接受水平，立即停止本项目，不以“体验更完整”继续开发。

## 五、权限、技术、隐私和平台风险

### 权限与隐私

- 【事实】Chrome 官方说明：自动向页面注入 content script 需要匹配页面的 host permission；也可用 `activeTab` 获得临时权限。若要在 YouTube 打开时自动隐藏页面并持续显示任务条，通常需要 YouTube host 权限。[Chrome content scripts](https://developer.chrome.com/docs/extensions/develop/concepts/content-scripts)、[chrome.scripting](https://developer.chrome.com/docs/extensions/reference/api/scripting)。
- 【事实】用户可把扩展的站点访问设置为“点击时／当前站点／所有站点”，也可随时移除扩展。[Chrome 扩展管理](https://support.google.com/chrome/answer/2664769)。
- 【事实】Chrome Web Store Limited Use 要求数据收集只服务于公开的单一目的；浏览活动只有在明确面向用户的功能确实需要时才可收集／传输。[Limited Use](https://developer.chrome.com/docs/webstore/program-policies/limited-use)、[User Data FAQ](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq)。
- 【事实】Unhook 官方隐私政策称扩展数据仅留在浏览器本地存储、不传输或收集；其商店页声明开发者不收集／使用数据。[Unhook 隐私](https://unhook.app/privacy-policy)、[商店页](https://chromewebstore.google.com/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid)。这是开发者声明，不等同于本轮独立代码审计。
- 【事实】真实用户确有信任疑问：“看起来很好，但安全吗／能信吗？”[Unhook 讨论](https://www.reddit.com/r/nosurf/comments/1af9uyc/)。

【推断】最低可信权限边界应仅为 `https://www.youtube.com/*`（若需要移动网页再单列 `https://m.youtube.com/*`），原任务和 timer 本地存储，默认零账号、零同步、零远端分析。任何“所有网站”访问都会显著削弱安装意愿，也不符合此极窄单一目的。

### 技术与平台风险

- 【事实】Unhook Chrome 商店页当前为 1.6.9、2026-03-21 更新；Mozilla API 显示同版本并列出 `storage`、`webRequest`、YouTube 两个 host 权限。商店显示的 100 万用户、4.9 星／4.4K ratings 只能说明分发与满意度信号，不能证明本闭环留存。[Chrome Web Store](https://chromewebstore.google.com/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid)、[Mozilla Add-ons](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/)。
- 【事实】2026 年 6–7 月 Mozilla 评价集中报告播放冻结、标签页失效和卸载后恢复速度，说明 YouTube 页面与浏览器更新会制造维护风险；这些是 Firefox 证据，不能直接声称 Chrome 同样故障。[评价列表](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)。
- 【事实】Chrome 可禁用不符合新要求的旧扩展，用户需寻找替代。[Chrome 官方帮助](https://support.google.com/chrome/answer/2664769)。
- 【推断】“到期自动返回”必须定义为**不关闭视频、不丢时间点、不销毁标签页**；更安全的验证版本应先显示任务卡并提供“完成／返回任务／延长 2 分钟”三选一，而不是无条件跳转。无条件跳转只作为单独实验变量。

### 风险表

| 风险 | 误用／攻击方式 | 阻断证据 | 残余风险 | 修正与闭环 |
|---|---|---|---|---|
| 证据被自推广污染 | 产品作者以“我也有痛点”包装推广 | 排除跨版重复和纯推广帖；优先多年旧帖、用户评论、官方评价 | Reddit 仍有选择偏差 | 招募时要求最近一次具体事件，不展示产品名 |
| 把问题存在当成产品缺口 | 只统计偏航正文，不测 Unhook＋Purpose | 官方功能对照显示现有组合高度覆盖 | 配置摩擦是否重要未知 | 必须设置现有组合对照组 |
| 自动返回伤害研究 | 视频被中断、笔记／标签／时间点丢失 | Freedom 与 Unhook 用户已报告上下文／结束反馈问题 | 模拟原型仍可能低估真实打断 | 记录 interruption cost；超过阈值即停 |
| 权限恐惧 | 请求所有网站或历史权限 | Chrome 官方允许精确站点控制；用户有安全疑问 | 企业托管浏览器可能完全禁止安装 | 仅 YouTube 权限；把拒装者作为失败样本而非排除 |
| 绕过与跨端迁移 | 禁用扩展、改浏览器、拿手机 | 多条正文已证明 | 无法靠 Chrome 扩展解决手机 | 首轮只测桌面；若 >25% session 跨端逃逸则停 |
| 误判付费 | 把 Freedom/Opal 购买映射到本窄功能 | 已找到付费与退款／弃用两侧证据 | 无真实 checkout | 商业化留在后续单独实验 |

## 六、自然获客地图

本节只评估，不外联。

| 入口 | 具体位置／关键词 | 内容钩子 | 可触达性 | 限制 |
|---|---|---|---|---|
| Reddit 学习 | r/GetStudying、r/studytips、r/learnprogramming | “YouTube 是课程入口也是偏航入口；请复盘最近一次” | 高：已有大量可复述事件 | 学生偏多；不少版限制调研／自推广，发帖前必须读规则 |
| Reddit 工作／戒网 | r/productivity、r/nosurf、r/digitalminimalism | “Unhook 已够用吗？主动搜索后还会不会偏航？” | 高：反证丰富 | 解决方案熟练用户自选择偏差；r/nosurf 不等于付费人群 |
| 独立开发者 | r/SideProject、r/indiehackers、Indie Hackers | “查一个 bug 的 5 分钟教程，何时变成 60 分钟？” | 中：易触达技术用户 | builder 容易讨论方案而非真实行为；严禁把点赞当需求 |
| YouTube | Unhook、Cold Turkey、distraction-free YouTube、study-with-me 视频评论区 | “如何保留 search 但去掉 rabbit hole？” | 中：评论与情境高度相关 | 评论抽取 best-effort；不可批量骚扰或把回复当招募许可 |
| Chrome／Firefox 商店 | Unhook、UnTrap、Intention 评价与支持页 | “失效、权限、playlist、性能、结束反馈” | 低（获客）／高（问题发现） | 评价者通常不可直接联系；CWS 本轮未取到单条正文 |
| Product Hunt | productivity、focus、browser extension | “与 Unhook＋Purpose 的盲测结果” | 中低 | 以 makers 为主，launch 兴奋不等于持续使用 |
| 搜索 | `block youtube recommendations but keep search`、`youtube tutorial rabbit hole`、`youtube for work but distracted`、`Unhook not working`、`Chrome extension read and change data on youtube safe` | 具体结果导向的比较页／复盘模板 | 中 | SEO 流量意图混杂；先验证关键词带来的正文质量，不看单纯搜索量 |

【推断】首批招募最合适的组合是 r/learnprogramming／r/GetStudying 的技术学习者，加 r/productivity／r/nosurf 的现有 Unhook 用户作为反证组。Product Hunt 只适合后期展示验证结果，不适合证明问题。

## 七、7–14 天非开发验证方案

### 目标

不验证“大家讨厌分心”，只验证：在真实技术研究任务中，**拟议流程相对 Unhook＋Purpose/Intention 是否产生可测的增量净收益**。

### 招募与筛选

- 招募 12 人，完成目标至少 8 人。
- 必须：英语用户；桌面 Chrome 为主要研究入口；每周至少 3 天用 YouTube 查技术资料；最近 7 天至少 2 次偏航 ≥10 分钟；可复述最近一次原任务、偏航第一步、持续时间、后果和 workaround。
- 分层：4 名已有 Unhook／同类去推荐工具用户，4 名用普通 blocker／timer，4 名未使用工具但有明确偏航。
- 排除：主要在手机／TV；工作必须持续看推荐、评论或趋势；浏览器由公司策略禁止扩展；主要问题是全平台娱乐而非 YouTube 任务内偏航。

筛选问题：

1. “请讲最近一次为了完成什么任务打开 YouTube；你点开的第一条非任务内容是什么？”
2. “从进入到意识到偏航过了多久？原任务产生了什么实际后果？”
3. “过去 7 天发生几次？请给出至少两个日期或场景。”
4. “你试过哪些 workaround？哪一步被你绕过或失效？”
5. “你是否安装过需要读取／修改 YouTube 页面数据的扩展？为何接受、拒绝或卸载？”
6. “你的工作是否依赖推荐、评论或关联视频发现素材？”

### 流程

**第 1–3 天：事件日记，不装新工具**

- 每次为任务进入 YouTube 时记录：原任务、预计时长、入口、第一步偏航、总时长、是否完成、跨端迁移、后果。
- 只记录，不纠正；得到真实基线频率。

**第 4–7 天：现有组合对照**

- 使用 Unhook＋Purpose Browser 或 Unhook＋Intention（以受试者兼容性为准）。
- 保持相同字段，额外记录配置时间、权限犹豫、功能失效、主动搜索后偏航、是否禁用扩展。
- 这是“现有方案是否已足够”的淘汰门，不是预热新产品。

**第 8–10 天：主持式无代码演示／故事板测试**

- 同一人完成两个等难度的 10 分钟技术查询任务，顺序随机：A 为现有组合；B 为拟议流程故事板／主持式模拟。
- B 流程：写唯一目的 → 选 5/10 分钟 → 模拟隐藏四类元素 → 常驻任务和倒计时 → 到期展示任务卡。
- 到期分两种随机处理：B1 无条件回原任务；B2 保留当前视频和时间点，显示“返回原任务／延长 2 分钟／完成”。
- 不创建扩展；若后续确需可交互原型，须另行授权，且只为验证这一个差异。

**第 11–14 天：复盘与选择**

- 不问“你喜欢吗”，而问：愿否在下一次真实任务继续使用哪一套；要求解释放弃另一套的行为原因。
- 展示精确权限文案：“只在 youtube.com 读取并修改页面，以隐藏指定元素并显示本地任务／计时；不读取其他网站、不上传任务或历史。”记录安装／拒绝。
- 商业化只做价格敏感度与替代比较，不收款、不把口头愿付当购买。

### 指标

| 指标 | 定义 | 证明什么 |
|---|---|---|
| 任务内偏航率 | session 中是否打开非原任务视频／Shorts／评论 | 核心行为是否减少 |
| 首次偏航时间 | 从进入 YouTube 到第一步非任务动作 | 摩擦是否延后偏航 |
| 超额时间 | 实际 YouTube 时长 − 预设通行时长 | timer 是否有效 |
| 原任务完成率 | 规定窗口内是否得到可用答案／完成 lecture 段 | 防止“少看但没完成” |
| 到期 60 秒恢复率 | 到期后 60 秒内是否回到原任务动作 | 自动返回的唯一增量 |
| 主动搜索后偏航 | 隐藏 feed 后，是否仍从 search／相关视频偏航 | Unhook 之后是否还有问题 |
| 打断成本 | 有用视频被截断、笔记／时间点／标签丢失、烦躁 1–5 | 净收益而非强制成功 |
| 绕过／跨端率 | 禁用扩展、换浏览器、拿手机 | Chrome-only 的失败边界 |
| 权限接受率 | 看完精确权限后愿安装的合格者比例 | 可分发性，不等于留存 |

### 成功阈值

必须全部达到：

1. 至少 8 人完成；其中至少 6 人的基线日记出现 ≥2 次任务内偏航，且中位单次损失 ≥15 分钟。
2. 在使用现有组合后，仍至少 5/8 出现主动搜索后的偏航或到期后继续游走，证明组合存在剩余问题。
3. 拟议到期处理相对现有组合：偏航率下降 ≥30%，超额时间中位数下降 ≥30%，到期 60 秒恢复率提高 ≥25 个百分点。
4. 原任务完成率不低于现有组合超过 10 个百分点；打断烦躁中位数 ≤2/5；上下文丢失 ≤1/8 session。
5. 看完精确 YouTube-only 权限说明后，至少 6/8 愿在自己的 Chrome 安装测试。
6. 至少 5/8 明确选择未来一周继续使用拟议流程，而不是现有组合。

### 失败阈值与立即停止条件

任一成立即停止，不做原型：

- 少于 5/12 能给出两次最近、可核的任务内偏航；
- 现有组合已让 ≥60% 合格者达到“无需更多帮助”；
- 自动返回使任务完成率下降 >10 个百分点，或 >25% session 出现有用内容被截断／上下文丢失；
- YouTube-only 权限接受率 <50%；
- >25% session 通过手机／其他浏览器逃逸；
- 多数偏航发生在主动逃避工作而非 YouTube 页面诱因，隐藏页面不改变行为；
- 目标用户的工作需要评论、推荐和关联视频，去推荐损害研究质量；
- 只有“喜欢概念／会试试”的口头反馈，没有日记、任务或复用行为改善。

## 八、商业化仅作为待验证假设

### 支持

- 【事实】相邻品类存在真实付款：Freedom 官方当前年付折算 $3.33/月、月付 $8.99、Forever $99.50；Opal 官方为 $99.99/年、$19.99/月、$399 lifetime；one sec 官方网页店显示 $19.99/年。[Freedom](https://freedom.to/premium?source=perks)、[Opal](https://opalapp.com/pricing)、[one sec](https://web.one-sec.app/store)。
- 【事实】有用户以约 $80 买 Freedom lifetime 后持续使用并表示满意；one sec 付费用户称多年使用后社媒时长减半；也有用户明确表示 $9/月“值得换回时间”。[Freedom 购买后追评](https://www.reddit.com/r/digitalminimalism/comments/1gwo82w/)、[one sec Premium](https://www.reddit.com/r/one_sec/comments/1iehmhg/)、[Freedom 讨论](https://www.reddit.com/r/nosurf/comments/1r0kro7/)。

### 反证

- 【事实】Unhook、Purpose Browser 和 Aware 当前免费层已覆盖大部分能力；关闭观看历史、独立账号、隐身模式也是免费替代。
- 【事实】有工作用户明确说“原则上不会付钱限制自己的设备”，只想免费移除 Shorts；另有付费 Freedom 用户因可绕过而后悔，或因 block 丢失上下文认为付费不值。[拒付帖](https://www.reddit.com/r/productivity/comments/1tcpr68/)、[后悔购买](https://www.reddit.com/r/digitalminimalism/comments/z8tz4a/)、[丢上下文](https://www.reddit.com/r/nosurf/comments/1os7cky/)。
- 【事实】Opal 用户报告订阅太贵、battery drain、卸载；同时也有人反驳并报告正常使用，说明定价与体验高度分群。[Opal 讨论](https://www.reddit.com/r/nosurf/comments/1r0hjaq/)。

### 假设

- 【待验证】若只提供 Chrome＋YouTube 单一闭环，**低价买断（建议测试 $9／$15／$19 三档）比订阅更合理**；订阅只有在跨设备、持续兼容维护或可证明的行为报告产生持续价值时才可能成立。
- 【推断】不能用 Freedom/Opal 的一般生产力付款证明本窄功能愿付；下一阶段若通过行为门，须单独做真实 checkout／可退款预订实验。当前不收款。

## 九、尚缺证据与下一轮唯一建议

### 尚缺

1. 【待验证】目标职业样本不足：本轮学生／学习者正文远多于英语自由职业者、独立开发者和研究型创作者。
2. 【待验证】缺 7 天逐次日志，无法判断真实频率、中位损失和 workaround 成功率。
3. 【待验证】缺现有组合对照；桌研只证明功能存在，未证明配置成本和真实效果。
4. 【待验证】“自动返回”没有真实任务数据；目前同时有支持逻辑和强打断反证。
5. 【待验证】没有权限安装转化、7 天复用和真实支付行为。
6. 【渠道限制】Chrome Web Store 本轮可读取官方功能、版本、总体评分和隐私声明，但公开文本路线未取得单条 CWS 评论正文；以 Mozilla 官方评论 API 补充兼容／卸载正文，并明确不能等同 Chrome。

### 下一轮唯一建议

执行上节的 **“3 天事件日记＋4 天 Unhook＋Purpose/Intention 对照＋8 人主持式交叉测试”**。不创建扩展；若现有组合已足够或自动返回的净收益不过阈值，立即停止。未经总控验收，不启动招募、原型或下一阶段。

## 十、来源清单与渠道限制

### 真实用户正文主来源

- Reddit 任务偏航：[177gfh6](https://www.reddit.com/r/ADHD/comments/177gfh6/)、[pex6il](https://www.reddit.com/r/GetStudying/comments/pex6il/)、[1t9bzz6](https://www.reddit.com/r/GetStudying/comments/1t9bzz6/)、[c26jt9](https://www.reddit.com/r/nosurf/comments/c26jt9/)、[13bt35w](https://www.reddit.com/r/productivity/comments/13bt35w/)、[1qknt6c](https://www.reddit.com/r/Python/comments/1qknt6c/)、[og55y1](https://www.reddit.com/r/productivity/comments/og55y1/)、[hka5p0](https://www.reddit.com/r/productivity/comments/hka5p0/)、[1heojmj](https://www.reddit.com/r/productivity/comments/1heojmj/)。
- Reddit 工具与反证：[1qdrffz](https://www.reddit.com/r/nosurf/comments/1qdrffz/)、[1af9uyc](https://www.reddit.com/r/nosurf/comments/1af9uyc/)、[1fxixxr](https://www.reddit.com/r/nosurf/comments/1fxixxr/)、[1fc2hyx](https://www.reddit.com/r/nosurf/comments/1fc2hyx/)、[zchfmg](https://www.reddit.com/r/productivity/comments/zchfmg/)、[1os7cky](https://www.reddit.com/r/nosurf/comments/1os7cky/)、[1gwo82w](https://www.reddit.com/r/digitalminimalism/comments/1gwo82w/)、[1str3rf](https://www.reddit.com/r/ProductivityApps/comments/1str3rf/)、[1iehmhg](https://www.reddit.com/r/one_sec/comments/1iehmhg/)、[1tcpr68](https://www.reddit.com/r/productivity/comments/1tcpr68/)、[z8tz4a](https://www.reddit.com/r/digitalminimalism/comments/z8tz4a/)、[1r0hjaq](https://www.reddit.com/r/nosurf/comments/1r0hjaq/)、[1r0kro7](https://www.reddit.com/r/nosurf/comments/1r0kro7/)。
- Mozilla Add-ons：Unhook 公开[评价列表](https://addons.mozilla.org/en-US/firefox/addon/youtube-recommended-videos/reviews/)，本轮使用 10 位不同作者的正文，重点 review ID：2734674、2732286、2731092、2726402、2726100、2725914、2725321、2721193、2718662。
- YouTube：通过 yt-dlp best-effort 实际读取[该视频](https://www.youtube.com/watch?v=2qDE048ovsI)的评论，纳入 3 位不同作者关于保留搜索、保留有用信息和 kiosk 绕过的正文。

### 40 条计数台账

| 渠道 | 纳入作者／正文标识 | 数量 |
|---|---|---:|
| Reddit | FormerDraw、Snoo74899、1t9bzz6 OP（账号已删除）、satvikpendem、clumsyAmeba、Original_Map3501、ezzeddinabdallah、hka5p0 OP（账号已删除）、PierGan、Sproutz_RD、Morrisonhotel82、1af9uyc 正向评论者（账号已删除）、1moreCopy、1af9uyc playlist 反对者（账号已删除）、PiterKiwi、LasedKremlun、ray_newman、_T0fuu_、zchfmg OP（账号已删除）、Marteco、p0lyhuman、dorabora57、Internal_Candidate65、g_junkin4200、Rja12345、Very_Good_Juju、f311a | 27 |
| Mozilla Add-ons | KillerSnowGoons、an3s、maltebp、meancloth、RideThePigGir、CaptBasil、Diamond、Mathéos、Firefox user 14968709、Ledvi | 10 |
| YouTube | @isaiahyanez3444、@Ingenarius、@Rohan-l6d | 3 |
| **合计** | 可见账号按不同作者去重；已删除账号只在不同独立线程语境中各计一条，不将同线程同作者追评重复计数 | **40** |

### 官方易变事实

- [Unhook Chrome Web Store](https://chromewebstore.google.com/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid)、[Unhook 隐私政策](https://unhook.app/privacy-policy)
- [Purpose Browser](https://www.purposebrowser.com/)、[Intention](https://www.getintention.com/)、[Aware](https://getaware.app/)
- [Chrome content scripts](https://developer.chrome.com/docs/extensions/develop/concepts/content-scripts)、[Chrome 扩展权限管理](https://support.google.com/chrome/answer/2664769)、[Chrome Web Store Limited Use](https://developer.chrome.com/docs/webstore/program-policies/limited-use)
- [Freedom 价格](https://freedom.to/premium?source=perks)、[Freedom 免费／付费功能](https://support.freedom.to/en/articles/13764747-what-s-included-in-free-and-premium-plans)、[Opal 价格](https://opalapp.com/pricing)、[one sec 价格](https://web.one-sec.app/store)

### 渠道与工具限制

- agent-reach v1.5.0 的 `doctor --json` 和 PTY 重试均返回空输出，无法取得可展示的 `active_backend`；随后按 Skill 首选命令实测 OpenCLI Reddit 可返回完整正文，rdt 未安装。
- agent-reach 的 Exa 路由失败，原错为 `Unknown MCP server 'exa'`；发现阶段降级为公开网页搜索，所有计入配额的 Reddit 候选再用 OpenCLI 读取正文，未用搜索摘要冒充正文。
- Reddit OpenCLI 有速率／相关性漂移，采用窄查询、分批读取和去重；未登录或不可访问内容不编造。
- YouTube 评论为 yt-dlp 网页抓取 best-effort，目标视频约 134 条评论，本轮实际抽取 40 条，仅 3 条达到任务相关标准；不宣称完整。
- Chrome Web Store 单条评论正文未能通过公开文本路线读取；只使用其官方详情与总体数据。Mozilla 评论用于补充，不跨浏览器偷换。
- 未读取来源会话 019fe4e5-c13b-7db0-9cc8-48da04fcceaf；本报告以委派摘要为基线，没有假装已读。
- 已按 Skill 执行 `agent-reach check-update`；当前版本为 v1.5.0，但 GitHub API 速率限制导致检查在工具内重试 3 次后失败。本轮未自行更新。
- 当前执行环境未提供可核验的运行态 model／effort／额度字段，因此未声称已确认，也未据此扩大任务或进行高风险动作。

## 治理与最终状态

- 结论：**继续做行为验证设计；没有绿灯。**
- 最强支持：至少 9 条正文给出明确的任务 → YouTube → 偏航 → 时间／任务后果链。
- 最强反证：Unhook＋Purpose/Intention 已覆盖绝大多数闭环；自动返回可能打断和丢上下文。
- 下一步：仅提交总控验收；未经验收不招募、不开发、不做原型、不付款、不发布。
- 无越界声明：本轮只做公开只读研究；除本报告外未修改项目业务文件。临时 YouTube 元数据仅写入 `/tmp/yt-research-*.info.json`，用于评论读取，体量很小，不属于项目产物。
