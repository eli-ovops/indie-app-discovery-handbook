# Reddit 近期 iOS App 开发、推广与变现证据池（只读）

> 调研日：2026-08-12；主窗口：2026-05-14—2026-08-12（90 天），其中 30 天为 2026-07-13—2026-08-12。仅使用 OpenCLI 回读的公开 Reddit 帖子与可见评论；无登录、发帖、评论、下载 App 或外部写入。所有下载、收入、MRR、转化等数字均为 **【创始人自述】**，除非行内另记；没有把 upvote、评论、下载或评分当留存。

## 一屏摘要

- **样本**：80 条独立可读 Reddit 帖子或父帖中可见评论证据，8 个已确认存在的 subreddit：r/SideProject 29、r/iOSProgramming 17、r/indiehackers 12、r/iosapps 6、r/startups 6、r/Entrepreneur 5、r/iosdev 3、r/SwiftUI 2。
- **日期**：30 天 68 条；31—90 天 10 条；91—180 天 2 条（E22、E79，单列且未与 90 天混算）。失败/低下载/无收入/强反证 34/80（42.5%）。标签可重叠：开发/技术 29，获客/推广 31，变现/定价 24，失败/反证 34。
- **最强结论【推断】**：独立开发者的可重复工作不是“上架即增长”，而是把一个窄痛点转成一个可展示的结果，再逐一测量“内容/渠道 → 商店页 → 核心动作 → 再次使用/付费”。多个样本明确显示：下载、等候名单和 App Store 展示均不足以证明 R。
- **最强反证【创始人自述】**：Fitly 648 展示、124 页面访问、25 下载仍为 0 trial、0 订阅、$0；PetsenseAI 的真实用户都只使用一次；Flash 进入 50+ Facebook 群后仍是 $0 MRR；两款已上线 AI App 因无营销而无收入。
- **P0 边界【建议】**：这不是为自律宠物提出新方向。可借的是证据方法：先让朋友完成一次真实“开始专注→被拦截→回到宠物/结束”核心循环，随后只看 D2/D7 自然复用与付费意愿；没有 C/R 不扩张变现或开发范围。

## 口径与限制

【事实】通过 `agent-reach doctor --json` 确认 Reddit 的 active backend 为 OpenCLI，并先用 `subreddit-info` 确认上述 8 个社区真实存在、公开可读。每个链接均为被 `opencli reddit read` 回读的帖子；评论证据在其父帖中可读。App Store/官网链接仅在原帖提供时存在，**本报告没有下载、购买或逐一外部反查**，故“存在性”除原帖链接外均为【待验证】。

局限：这是 Reddit 自选披露样本，不能估计总体成功率；部分帖子明显带推广目的，数字也无法审计；评论多为经验/建议而非实验。因此“出现次数”是本证据池内的出现次数，不是行业比例。

## 80 条证据池

字段：`日期｜社区｜身份/阶段｜App/场景｜具体动作与量化结果｜V-S-C-R｜标签；可信度/缺口｜链接`。  
“高”=作者给出可解释行为或漏斗；“中”=作者自述但无法外验；“低”=评论建议、无量化或推广语。

### A. 开发、技术与创意来源（E01–E29）

|#|记录|
|---|---|
|E01|2026-08-12｜r/SideProject｜solo founder｜PetsenseAI iOS 宠物情绪识别｜发现 “maybe later” 被永久写入本地标记，导致每位真实用户只用一次；改为稍后再问，并增加新旧扫描对比作为二次打开理由｜R：明确 0 回访，修复待验证｜开发+失败；中（创始人自述）｜[帖](https://www.reddit.com/r/SideProject/comments/1vlz4jt/the_bug_that_was_worse_than_any_feature_i_couldve/)|
|E02|2026-08-12｜r/SideProject｜个人开发者｜Vizix iOS 视频效果｜从自己未成功的 TikTok 习惯追踪推广和反复出现的 TTS/游戏背景视频中发现创意；先做 3 个 shader POC，再扩至 56 效果｜V：观察到内容形式；S：先小 POC｜开发+创意+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlwmrk/i_got_tired_of_seeing_every_story_video_use_the/)|
|E03|2026-08-12｜r/SideProject｜夜间/周末 solo｜Kindmemo iOS｜个人遗忘痛点；SwiftUI+SwiftData、仅本地/可选私有 CloudKit，无后端；定价 $1.99 买断｜C/R 尚无，零评分零受众｜开发+变现；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlu2xi/i_built_a_second_memory_for_my_friendships_and/)|
|E04|2026-08-11｜r/iOSProgramming｜已上线开发者｜Tokyo Glance｜SwiftUI 原生 Map，约 1,400 个移动标注性能差后改成单 overlay 自绘；Bun/Hono/Mongo/Zod 后端，RevenueCat、WidgetKit、FCM｜开发过程；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1vit3ud/shipped_my_tokyo_transit_app_3000_live_vehicles/)|
|E05|2026-08-08｜r/iOSProgramming｜同行评论｜Tokyo Glance｜解释大量 MKAnnotationView 的 UIKit 生命周期开销；支持“一个 overlay pass”方案，提醒电池/热压力｜开发反证；低（评论经验）｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1vit3ud/shipped_my_tokyo_transit_app_3000_live_vehicles/)|
|E06|2026-08-07｜r/iOSProgramming｜提交审核的开发者｜富剪贴板键盘扩展｜缩小捕获时图片、硬缓存上限、富文本代替真实 View；扩展读取专用索引而非主 store｜开发+平台约束；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1vhpuic/constraints_i_ran_into_building_a_keyboard/)|
|E07|2026-08-07｜r/iOSProgramming｜同行评论｜键盘扩展｜建议 App Group 用单向数据流，主 App 唯一写者；版本化快照、原子替换、扩展不做 migration｜开发反证；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1vhpuic/constraints_i_ran_into_building_a_keyboard/)|
|E08|2026-08-01｜r/SwiftUI｜开发者｜日更投票 App｜iOS 18 SwiftUI：TabView 页面、延迟目的地、避免后台/时区导致 timer 状态漂移｜开发；中｜[帖](https://www.reddit.com/r/SwiftUI/comments/1vctua2/5_swiftui_patterns_that_helped_me_build_a/)|
|E09|2026-08-01｜r/SwiftUI｜同行评论｜日更投票 App｜建议 iOS 18 用 NavigationStack/navigationDestination 代替旧 LazyView workaround｜开发；低｜[帖/评](https://www.reddit.com/r/SwiftUI/comments/1vctua2/5_swiftui_patterns_that_helped_me_build_a/)|
|E10|2026-08-11｜r/iOSProgramming｜国际电话 App 运营者｜VoIP｜从 IAP 改 Stripe/Apple Pay，按作者称首提审通过；前提是通话服务在 App 外消费，不能外推数字内容｜开发+变现+政策；中，合规须以 Apple 现行规则复核｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1vlf4nc/we_removed_inapp_purchases_from_our_ios_and/)|
|E11|2026-08-11｜r/iOSProgramming｜同行评论｜审核流程｜建议在审核备注中给 demo 账号和精确测试路径，减少“找不到功能”往返｜开发+政策；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1vlf4nc/we_removed_inapp_purchases_from_our_ios_and/)|
|E12|2026-08-11｜r/iosapps｜首个 iOS 开发者｜FocusLift｜本人 ADHD 训练休息刷 feed 的痛点；把 Screen Time blocking 嵌入训练日志，锁住选定 App 但保留计时/音乐/记录｜创意+开发；中｜[帖](https://www.reddit.com/r/iosapps/comments/1vl2ett/focuslift_a_workout_app_for_people_with_adhs_i/)|
|E13|2026-08-11｜r/iosapps｜评论用户｜FocusLift｜指出设置似乎需先订阅，表明价值体验前已有付费摩擦｜C 反证｜低｜[帖/评](https://www.reddit.com/r/iosapps/comments/1vl2ett/focuslift_a_workout_app_for_people_with_adhs_i/)|
|E14|2026-08-01｜r/iosdev｜首个 solo developer｜Precursor Hourly Screen Time｜从“日总限额不合用”切入；承认 iOS 用量追踪不一致、同时间最多 8 个 App group｜创意+开发约束；中｜[帖](https://www.reddit.com/r/iosdev/comments/1vci0mp/no_screen_time_app_lets_you_control_your_limits/)|
|E15|2026-05-16｜r/iOSProgramming｜solo iOS 开发者｜Habitvs｜Swift/SwiftUI+HealthKit+WidgetKit+Watch；10 天 100 首下、7 重下、622 页访；无 D2/D7｜开发+C，R 缺失；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1tevcsj/i_launched_my_first_ios_app_10_days_ago_and_would/)|
|E16|2026-05-16｜r/iOSProgramming｜评论者/下载者｜Habitvs｜在较旧 iPhone 上发现设置 sheet 溢屏，说明真实设备差异需在早期验收｜开发反证；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1tevcsj/i_launched_my_first_ios_app_10_days_ago_and_would/)|
|E17|2026-08-11｜r/iosapps｜新手开发者｜Maxlyft/AlarmCroc｜从 Swift+UserDefaults 遗失数据，经历 Core Data 同步问题，再用 Firebase/D1；作者承认架构改善没有带来转化｜开发+失败；中｜[帖](https://www.reddit.com/r/iosapps/comments/1vlif0i/my_app_journey_15_years_in_the_making_everything/)|
|E18|2026-08-11｜r/iosapps｜同行评论｜Maxlyft｜明确指出零转化更像 offer/paywall 未验证，不能用数据库重构替代市场验证｜失败反证；低｜[帖/评](https://www.reddit.com/r/iosapps/comments/1vlif0i/my_app_journey_15_years_in_the_making_everything/)|
|E19|2026-08-11｜r/SideProject｜AI App 卖方｜Impulse Delay｜React Native+FastAPI、iOS widget、RevenueCat billing；已上线但称没有营销和收入｜开发+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vib6y9/selling_two_productionready_ai_apps_live_on_the/)|
|E20|2026-08-11｜r/SideProject｜健身 App 创始人｜Fitly iPhone/Watch｜数月构建训练、营养、恢复的宽产品；上线一周后怀疑承诺过宽/Pro 价值不清，而非代码问题｜开发+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vler3y/25_downloads_0_trial_starts_i_think_i_built_too/)|
|E21|2026-08-11｜r/SideProject｜政治新闻 App 作者｜LLM 新闻聚合｜数月开发，月烧 >$150 无付费；评论质疑“LLM wrapper”差异和免费替代｜开发+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vljtuj/im_burning_over_150_usd_per_month_on_my_political/)|
|E22|2026-04-21（91—180 天）｜r/iOSProgramming｜隐私优先 mood tracker 作者｜InnerPulse｜无分析 SDK/云/邮件；以隐私换取几乎没有用户漏斗数据，需靠定性反馈｜开发+测量取舍；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1srjpmo/i_launched_a_mental_health_app_solo_with_zero/)|
|E23|2026-07-11｜r/indiehackers｜Android car locator 作者｜Apparcao｜.NET MAUI+Blazor Hybrid；蓝牙断连触发一次定位而非持续 GPS，以电量/隐私为差异｜创意+开发；中｜[帖](https://www.reddit.com/r/indiehackers/comments/1uubcet/building_an_android_car_locator_tool_to_solve_my/)|
|E24|2026-07-11｜r/indiehackers｜同行评论｜Apparcao｜建议把激活定义为首次自动停车记录而非安装，并把“不耗电”放进 ASO 搜索意图｜C 定义；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1uubcet/building_an_android_car_locator_tool_to_solve_my/)|
|E25|2026-07-23｜r/startups｜技术+营销共同创始人｜mobile app 概念｜讨论先 Figma/视频/可视化还是先 MVP；多条评论支持先用轻原型和用户研究，避免编码锁定｜创意+开发；中（讨论非结果）｜[帖](https://www.reddit.com/r/startups/comments/1uzt1wo/market_validation_prototype_or_mvp_i_will_not/)|
|E26|2026-07-23｜r/startups｜同行评论｜mobile app 概念｜“解释能做什么”不等于验证；纸面/交互原型可先推翻假设｜C 反证；低｜[帖/评](https://www.reddit.com/r/startups/comments/1uzt1wo/market_validation_prototype_or_mvp_i_will_not/)|
|E27|2026-08-11｜r/SideProject｜solo 产品作者｜Kindmemo｜把竞品的 guilt/streak/score 作为反向创意约束，捕捉必须快过遗忘｜创意来源：竞品厌烦；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlu2xi/i_built_a_second_memory_for_my_friendships_and/)|
|E28|2026-08-10｜r/SideProject｜solo developer｜ShipContent｜把自己的 PR→社媒发布 context switching 作为痛点，AI 读 diff 生成草稿，但 beta 0 用户｜创意+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlhxli/i_built_a_tool_to_turn_my_github_prs_into/)|
|E29|2026-08-10｜r/SideProject｜评论试用者｜ShipContent｜发现帖中说“接 repo”，落地页却只有 waitlist；要求明确审核时间与演示，定位首屏承诺/动作不一致｜C 反证；低｜[帖/评](https://www.reddit.com/r/SideProject/comments/1vlhxli/i_built_a_tool_to_turn_my_github_prs_into/)|

### B. 第一批用户与可重复推广（E30–E60）

|#|记录|
|---|---|
|E30|2026-08-11｜r/SideProject｜Flash 创始人｜婚礼相机 App｜4 个月 solo 后加入 50+ Facebook 群并开始发帖；免费限 5 人，MRR $0｜推广+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlqpav/4_months_of_solo_dev_launched_flash_a_wedding/)|
|E31|2026-08-11｜r/SideProject｜Vizix 作者｜视频效果 App｜少量付费广告尚可、TikTok 中性习惯帖失败；从失败内容消费中发现新人群｜推广+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlwmrk/i_got_tired_of_seeing_every_story_video_use_the/)|
|E32|2026-08-10｜r/indiehackers｜Glance 创始人夫妇｜日历 App｜数月自然日增 1–2 用户；一次小更新后 5 日突增 400+，无投放/无 listing 改动；来源未知｜获客；中，不能归因于更新｜[帖](https://www.reddit.com/r/indiehackers/comments/1vkfimr/after_months_of_averaging_12_users_per_day_we/)|
|E33|2026-08-10｜r/indiehackers｜评论者｜Glance｜建议在 Play Console 分 search/explore/referral 查突增来源，不能只凭时序归功更新｜归因反证；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1vkfimr/after_months_of_averaging_12_users_per_day_we/)|
|E34|2026-08-10｜r/SideProject｜ActionClip 作者｜Mac App｜只在 r/macapps 做一个窄发布，称 7 天无付费投放获 $700+ lifetime gross；用 TrustMRR 链接佐证但本报告未外验｜推广+付费 C；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vkv45y/i_made_usd_700_in_a_week_with_my_new_mac_app_here/)|
|E35|2026-07-25｜r/indiehackers｜solo paid App 作者｜Mac App｜每个社区独立折扣码做归因，却同时换社区和文案，作者承认实验混杂｜推广+失败；中｜[帖](https://www.reddit.com/r/indiehackers/comments/1v1dsxx/i_finally_set_up_attribution_then_ruined_my_own/)|
|E36|2026-07-25｜r/indiehackers｜评论者｜Mac App｜建议同一社区/近似时段只改一个变量；低样本的 3 比 1 销售仍可能噪声｜S 方法+反证；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1v1dsxx/i_finally_set_up_attribution_then_ruined_my_own/)|
|E37|2026-07-20｜r/indiehackers｜Mac App 作者｜Mac only App｜把 “Mac” 放得太后，吸来 Windows 错配兴趣；承认无清洁前后数据，只观察少了错误对话｜定位+归因反证；中｜[帖](https://www.reddit.com/r/indiehackers/comments/1v5t3hb/i_buried_the_single_most_important_qualifying/)|
|E38|2026-07-20｜r/indiehackers｜评论者｜Mac only App｜强调合格使用而非点击；平台、受众、价格是内容首屏要先筛的约束｜S/C；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1v5t3hb/i_buried_the_single_most_important_qualifying/)|
|E39|2026-08-10｜r/SideProject｜AbleScan 作者｜无障碍扫描器｜5 个项目均零收入；自认过去只完成“构建/部署/付款”，没完成让陌生人使用的后半程｜获客+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vkihes/ive_shipped_5_side_projects_with_zero_revenue/)|
|E40|2026-08-10｜r/SideProject｜SweePic 创始人｜照片清理 App｜连续一个月 Instagram/TikTok #challenge；称收入 $48→$87、订阅 7→10，但商店展示 -15.6%、页访 -27.3%｜内容推广混合结果；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vjzntk/sweepic_summer_challenge_revenue_up_81_but_app/)|
|E41|2026-08-11｜r/iOSProgramming｜Habitvs 作者｜虚拟宠物健康 App｜10 天 1.68K 展示、622 页面访问、100 首下；展示到下载的 C 有但无 D2/D7｜漏斗而非留存；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1tevcsj/i_launched_my_first_ios_app_10_days_ago_and_would/)|
|E42|2026-08-11｜r/iOSProgramming｜评论者（称 5M+ 自然下载）｜Habitvs｜建议低竞争关键词、现代截图、多语言/本地价；数字和方法均未外验｜ASO；低-中｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1tevcsj/i_launched_my_first_ios_app_10_days_ago_and_would/)|
|E43|2026-06-09｜r/iOSProgramming｜长期 iOS 开发者｜App Store search｜称更新 UX/订阅/截图/关键词后自然可见度仍难提升；评论提外部营销与 Search Ads 成本不适合多数 indie｜推广失败；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1u0z95j/the_app_store_search_wall_why_quality_alone_no/)|
|E44|2026-06-09｜r/iOSProgramming｜评论者｜App Store search｜反驳“质量自然获分发”：AI 降低复制成本，需不可轻易复制的意义/差异｜定位反证；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1u0z95j/the_app_store_search_wall_why_quality_alone_no/)|
|E45|2026-07-23｜r/startups｜travel mobile app 创始人｜获客提问｜计划 1k waitlist→100–200 beta；评论质问“没有用户何来验证”｜获客+失败；中｜[帖](https://www.reddit.com/r/startups/comments/1v3rklv/how_to_get_users_i_will_not_promote/)|
|E46|2026-07-23｜r/startups｜评论者｜travel mobile app｜建议从目标人群现有社区开始 radical listening；不应做完再“附加社区”｜创意/获客；低｜[帖/评](https://www.reddit.com/r/startups/comments/1v3rklv/how_to_get_users_i_will_not_promote/)|
|E47|2026-07-18｜r/indiehackers｜todo+pixel game 作者｜未上线 App｜landing page + Meta ads 得 101 waitlist；页面转化 5–7%，最佳 CPL 约 $3.92，iMac split-screen 素材胜像素角色｜S：创意素材实验；中｜[帖](https://www.reddit.com/r/indiehackers/comments/1vb41j3/i_got_100_strangers_to_actually_sign_up_for/)|
|E48|2026-07-18｜r/indiehackers｜评论者｜todo+pixel game｜反证：waitlist/评论不等于付费；冷流量先理解工作流而非审美；可用单问题更新维持等待者｜C/S；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1vb41j3/i_got_100_strangers_to_actually_sign_up_for/)|
|E49|2026-07-23｜r/Entrepreneur｜新闻 podcast App 作者｜已上架｜想靠 1,200 LinkedIn 联系人、朋友下载到 500 trial；承认 App Store 自然上架不会有结果，基础设施成本制约增长｜推广+失败风险；中｜[帖](https://www.reddit.com/r/Entrepreneur/comments/1v873xt/launching_an_app_and_getting_users_even_trial/)|
|E50|2026-07-23｜r/Entrepreneur｜AutoModerator/规则｜新闻 podcast App｜社区明示禁未授权自我推广/DM/链接，免费供给需进入指定帖；渠道规则本身会阻断分发｜平台反证；高（规则文本）｜[帖/评](https://www.reddit.com/r/Entrepreneur/comments/1v873xt/launching_an_app_and_getting_users_even_trial/)|
|E51|2026-07-23｜r/Entrepreneur｜评论者｜新闻 podcast App｜区分“每天只有几次页面访问”与“数百访问 0 trial”：前者不能下结论，后者才是 listing/承诺问题｜C 测量；低｜[帖/评](https://www.reddit.com/r/Entrepreneur/comments/1v873xt/launching_an_app_and_getting_users_even_trial/)|
|E52|2026-07-23｜r/Entrepreneur｜15+ 年创始人｜B2B SaaS（可迁移方法）｜建议 3–4 周明确 launch date、Product Hunt 作为约束、先获取案例/推荐和真实使用，非把正反馈当验证｜S/C；中（经验）｜[帖](https://www.reddit.com/r/Entrepreneur/comments/1v3la4h/building_is_too_easy_now_heres_how_to_actually/)|
|E53|2026-07-23｜r/Entrepreneur｜评论者｜launch 方法｜建议从第一天公开讨论问题，积累 20/50 个有痛点的人；launch 是交付给已等待者，不是向零受众介绍｜获客+V；低｜[帖/评](https://www.reddit.com/r/Entrepreneur/comments/1v3la4h/building_is_too_easy_now_heres_how_to_actually/)|
|E54|2026-08-12｜r/SideProject｜政治新闻 App 评论者｜新闻 App｜指出免费用户很难等同付费；广告要很大展示量，建议先问 free-user 数和成本｜推广/商业模式反证；低｜[帖/评](https://www.reddit.com/r/SideProject/comments/1vljtuj/im_burning_over_150_usd_per_month_on_my_political/)|
|E55|2026-08-11｜r/SideProject｜Flash 创始人｜婚礼 App｜“50+ 群+开始发帖”是曝光动作，MRR $0，不能称为第一批付费用户｜C 失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlqpav/4_months_of_solo_dev_launched_flash_a_wedding/)|
|E56|2026-08-11｜r/iosapps｜FocusLift 评论者｜训练+屏蔽 App｜“想试试”只是口头兴趣，不算下载、完成训练或复用｜C 口径反证；低｜[帖/评](https://www.reddit.com/r/iosapps/comments/1vl2ett/focuslift_a_workout_app_for_people_with_adhs_i/)|
|E57|2026-08-10｜r/SideProject｜Fitly 作者｜fitness App｜648 展示→124 页访→25 下载→0 trial；建议先访谈前 25 用户、修 activation，再获客｜C 失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vler3y/25_downloads_0_trial_starts_i_think_i_built_too/)|
|E58|2026-08-10｜r/SideProject｜PetsenseAI 作者｜pet AI App｜初以为是广告/关键词/截图问题，后来发现是返回理由和 signup bug；获客优化不能代替留存诊断｜R 反证；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlz4jt/the_bug_that_was_worse_than_any_feature_i_couldve/)|
|E59|2026-08-05｜r/iosdev｜首发付费 App 作者｜生产力 App｜称无营销、家人早期购买后 24h 到 Paid Productivity #24；作者也承认新 App honeymoon boost，故不能归因成功｜V/C 证据弱；中｜[帖](https://www.reddit.com/r/iosdev/comments/1vfy653/i_made_24_paid_productivity_on_my_first_24h_on/)|
|E60|2026-08-04｜r/iosdev｜solo iOS 开发者｜三款 freemium App｜称“每天至少一单”但收入仍小；让所有重要功能用 sample data 先体验，重度/自定义才收费｜获客+付费 C；中｜[帖](https://www.reddit.com/r/iosdev/comments/1vfbkzb/my_first_perfect_week_as_a_solo_ios_developer_at/)|

### C. 定价、变现、留存与失败反证（E61–E80）

|#|记录|
|---|---|
|E61|2026-08-12｜r/SideProject｜Vizix 作者｜内容创作 App｜6 个效果免费，其余按 10/20 效果包买断；明确“不订阅、买后可用”，适合可积累资产｜变现；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlwmrk/i_got_tired_of_seeing_every_story_video_use_the/)|
|E62|2026-08-11｜r/SideProject｜Fitly 作者｜fitness App｜25 下载但 0 trial/订阅/$0；认为应将 paywall 放到首个完整 workout 后并收集访谈，尚未验证｜变现+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vler3y/25_downloads_0_trial_starts_i_think_i_built_too/)|
|E63|2026-08-11｜r/SideProject｜iOS 开发者｜旅行 App｜零付费转化时，将 lifetime IAP 从 $39.99 提至 $49.99、年订阅 $19.99 不变；理由是低流量期更易改价，非已验证最优价格｜定价；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vjsc5y/i_raised_my_lifetime_iap_25_before_earning_a/)|
|E64|2026-08-11｜r/SideProject｜评论者｜lifetime IAP｜称自己约 800 销售后提价，旧用户评论不满；支持在无人关注期先测试价格｜定价反证；低｜[帖/评](https://www.reddit.com/r/SideProject/comments/1vjsc5y/i_raised_my_lifetime_iap_25_before_earning_a/)|
|E65|2026-08-10｜r/SideProject｜ActionClip 作者｜Mac App｜称一个相关社区带来 7 天 $700+ lifetime gross；不是 MRR，且未核验 TrustMRR｜一次性买断 C；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vkv45y/i_made_usd_700_in_a_week_with_my_new_mac_app_here/)|
|E66|2026-08-10｜r/SideProject｜SweePic 创始人｜照片清理订阅 App｜称社媒月挑战期间收入 +81%、活跃订阅 +43%，而页访下跌；不能从相关性推论内容已可规模化｜订阅+失败反证；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vjzntk/sweepic_summer_challenge_revenue_up_81_but_app/)|
|E67|2026-08-11｜r/SideProject｜Kindmemo 作者｜个人 CRM｜$1.99 paid upfront，想验证是否仍有人愿意买“完成 App”；上线数周仍零评分/零受众｜买断+失败未定；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlu2xi/i_built_a_second_memory_for_my_friendships_and/)|
|E68|2026-08-11｜r/SideProject｜政治新闻 App 作者｜LLM news App｜每月成本 >$150、没有付费客户，显示持续推理成本和未验证 willingness-to-pay 是硬停止风险｜变现+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vljtuj/im_burning_over_150_usd_per_month_on_my_political/)|
|E69|2026-08-10｜r/SideProject｜AI App 卖方｜ResumeOpti/Impulse Delay｜称两款已上 App Store，含 RevenueCat+Stripe/订阅层但“no revenue yet”；功能完整/合规并非付费证据｜变现+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vib6y9/selling_two_productionready_ai_apps_live_on_the/)|
|E70|2026-08-10｜r/SideProject｜AbleScan 作者｜无障碍 SaaS｜免费扫、付费解锁修复清单/PDF；此前 5 个项目零收入，陌生人一次实际使用才被称为进展｜freemium+失败；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vkihes/ive_shipped_5_side_projects_with_zero_revenue/)|
|E71|2026-08-11｜r/iosapps｜FocusLift 作者｜ADHD fitness App｜用户指出设置入口似乎在订阅后，属于在“第一次获益”前收费的摩擦；未报告真实转换｜订阅反证；低-中｜[帖/评](https://www.reddit.com/r/iosapps/comments/1vl2ett/focuslift_a_workout_app_for_people_with_adhs_i/)|
|E72|2026-07-27｜r/indiehackers｜niche reading App 作者｜Hexbrief｜仅 30+ 用户，作者仍在收反馈；评论建议先观察保存/跳过等真实使用模式，别急装 paywall/广告｜R/变现门槛；中｜[帖](https://www.reddit.com/r/indiehackers/comments/1v7txl9/how_would_you_monetize_a_niche_reading_app_for/)|
|E73|2026-07-27｜r/indiehackers｜评论者｜Hexbrief｜“30 users 不是 distribution 问题而是 data 问题”；广告需体量且会伤 high-signal 承诺｜变现反证；低｜[帖/评](https://www.reddit.com/r/indiehackers/comments/1v7txl9/how_would_you_monetize_a_niche_reading_app_for/)|
|E74|2026-07-16｜r/startups｜儿童言语/自闭症游戏公司｜4 mobile games｜IAP/订阅销售低，被迫考虑另 3 款上广告，作者也不愿儿童 App 放广告｜广告/订阅失败；中｜[帖](https://www.reddit.com/r/startups/comments/1vjy58y/our_sales_are_super_low_what_can_we_do_to_fix_it/)|
|E75|2026-07-16｜r/startups｜评论者｜儿童教育 App｜建议 SLP/学校/早干预机构推荐或 license，而不是只让家长在商店自找；这是建议，未提供成功数据｜服务/机构变现；低｜[帖/评](https://www.reddit.com/r/startups/comments/1vjy58y/our_sales_are_super_low_what_can_we_do_to_fix_it/)|
|E76|2026-07-24｜r/iOSProgramming｜开源作者｜AppRankly 分析看板｜自托管 App Store/Google Play 数据看板；把“看指标”工程化但本身没有用户转化/收入证据｜测量基础设施；中｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1v54gv2/open_source_apprankly_selfhosted_dashboard_for/)|
|E77|2026-07-24｜r/iOSProgramming｜评论者｜AppRankly｜指出默认通知 topic 可能泄露应用名和安装统计，提醒分析工具的隐私/配置风险｜测量反证；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1v54gv2/open_source_apprankly_selfhosted_dashboard_for/)|
|E78|2026-05-09｜r/iOSProgramming｜评论者｜niche utility｜称 $2.99 买断改 free+7-day trial、两封触发邮件和明晰 paywall 后付费约 3x、week-2 retention 改善；单个评论，必须复验｜订阅/留存；低｜[帖/评](https://www.reddit.com/r/iOSProgramming/comments/1teszbt/growth_hacking_your_way_to_success_what_did_you_do/)|
|E79|2026-05-09（91—180 天）｜r/iOSProgramming｜iPad App 作者｜promo code giveaway｜主动问 giveaway 是否有长期留存、是否吸引 freebie hunters；评论称 promo-code 用户不能写 App 评价，且免费多带 tester 非留存用户｜促销反证；中/低｜[帖](https://www.reddit.com/r/iOSProgramming/comments/1t844vb/anyone_here_run_a_promo_code_giveaway_for_their/)|
|E80|2026-08-12｜r/SideProject｜PetsenseAI 作者｜pet AI App｜明确将“每人仅一次 session”与“新旧扫描比较”区分：前者是 R 失败，后者只是待验的回访假设｜R 定义；中｜[帖](https://www.reddit.com/r/SideProject/comments/1vlz4jt/the_bug_that_was_worse_than_any_feature_i_couldve/)|

## 统计：开发方式、创意来源与常见坑

|证据池内出现|次数|可得结论|
|---|---:|---|
|个人痛点/自身工作流|12|最常见创意起点；只代表创作者有痛，不代表市场已付费。|
|竞品缺陷/反向承诺（无订阅、无 guilt、少耗电）|8|适合做明确 wedge，但仍要测是否驱动核心动作。|
|SwiftUI/原生 Apple framework|10|常见于轻量 iOS；扩展、地图、后台/Screen Time 有真实约束。|
|本地优先/SwiftData/Core Data/CloudKit|7|隐私可成定位，代价是归因/跨设备/反馈测量变弱。|
|后端/Firebase/Supabase 类替代/自建 API|6|多次成为重构焦点；样本反证“架构优化≠转化”。|
|跨端（React Native、MAUI 等）|3|样本只说明使用，不证明更快或更会卖。|
|AI 辅助/AI wrapper|8|加快构建且使同质品增多；若无法解释不可替代价值，易被质疑。|
|先做 POC/原型再扩展|5|有利于低成本否定假设；原型展示本身仍不是 C。|

创意来源计数（可重叠）：个人痛点 12、竞品差评/不满 8、内容/社区观察 5、已有服务工作流 4、ASO/关键词 4、AI wrapper 6。没有任何一类在本池中同时带来可审计的 R，因此不应以“出现多”宣布成功。

## 推广渠道：正反证与适用阶段

|渠道|出现|正向可见证据|强反证/限制|适合的阶段|
|---|---:|---|---|---|
|Reddit 价值帖/社区|12|相关社区的一次窄发布被称带来 ActionClip $700 gross|多社区禁自推、链接或 DM；一个发布不可复现|问题访谈、反馈、窄受众验证|
|TikTok/Instagram 内容|6|SweePic 订阅收入同期上涨；Vizix 从内容形态发现创意|Vizix 习惯追踪中性帖失败；SweePic 的商店流量反降|测钩子与结果演示，不把播放当 C|
|App Store ASO/截图/本地化|10|Habitvs 的 listing 有 10.1% 访客→下载；多评论提出关键词/截图|自然检索很难、平台 honeymoon/算法无法归因|已有明确搜索意图与短承诺后|
|Meta/付费广告|4|todo game 101 waitlist，CPL 约 $3.92|waitlist 不等于付费/留存；需创意单变量测|先测曝光→落地页表达|
|Facebook 群/社区加入|3|Flash 加入 50+ 群|同期 MRR $0，群数量不代表转化|只在合规的具体问题场景中|
|朋友/既有人脉|4|首日排名样本有家人早购|不代表冷用户；会污染测量|内部 smoke，不计作市场 C|
|Product Hunt/launch 日|2|被用作设置节奏|不等于流量/留存|建立交付截止而非唯一获客|
|合作方/KOC/机构|4|儿童产品评论提出 therapist/school 推荐路径|全为建议，尚无该帖的量化结果|有高信任推荐者且价值可被其说明时|

**两周 20 条单变量内容实验框架（仅设计，不发布）**

固定受众、固定 CTA、同一商店页/同一核心动作，避免同时更换平台与话术。每条只改变一个变量；记录曝光、合格点击、安装、首次完成“开始专注→屏蔽生效→回到宠物/结束”、D2、D7、自然分享/付费意愿。

|变量组|5 个变体（共 20 条）|
|---|---|
|痛点钩子|休息/刷短视频失控；学习启动困难；“再看 5 分钟”；家长式屏蔽反感；专注后即时陪伴|
|结果演示|开始前；屏蔽生效；短时完成；宠物状态变化；结束后回顾|
|受众 qualifier|学生备考；远程工作者；ADHD 自述者（不作医疗承诺）；短视频分心者；晚间拖延者|
|表达形式|真实手持录屏；一镜到底；问题→动作；反常识失败；用户任务清单|

停止条件【建议】：若完成 20 条后没有可复现的“合格点击→真实安装→首次核心动作”提升，或首次动作后无任何自然 D2 信号，则停增内容量，回到受众/承诺/首屏和实际设备核心循环诊断；不得以播放、点赞或下载替代。

## 变现模式与适用条件

|模式|池内证据|适用条件【推断】|主要反证|
|---|---|---|---|
|买断/paid upfront|Kindmemo $1.99、niche utility $4.99、ActionClip lifetime|一次性、可离线、价值即刻且可长期持有|高意图才会买；171 下载不说明复用；过早定价需实验|
|Freemium + lifetime/IAP|Vizix packs、三款 freemium App、Fitly|免费先完成一个可感知结果，再为扩展/自定义收费|Fitly 25 下载 0 trial；复杂或早期 paywall 会阻断体验|
|订阅 + trial|Fitly、SweePic、reading App 讨论|持续内容、持续成本或自然周期复用已出现时|SweePic 指标混杂；30 users 不应急于上广告/订阅|
|广告|儿童游戏、新闻 App 评论|免费高频且可承受广告，且规模足够|儿童场景品牌/伦理冲突；评论称需要百万级展示，未证实|
|服务/机构许可|儿童 App 的 therapist/school 建议|买方与使用者不同、专业方能背书/部署|只是建议，尚未有该样本实际成交|
|外部支付|VoIP Stripe 案例|仅外部消费服务且符合当期商店政策时|不能泛化到数字内容；须官方规则复核|

## 第一批 10 / 50 / 100 用户：可检验的定义

|门槛|合格方法|不计入|
|---|---|---|
|前 10|10 个非开发者实际安装，并至少完成一次核心动作；逐人记录卡点和是否愿在无提醒下次日再用|朋友口头说“想试”、浏览、waitlist、作者自用|
|前 50|50 个合格安装来源可区分；每个渠道/文案只改一个变量；看首次核心动作率|总展示、帖子的评分、混在多个渠道的折扣码|
|前 100|100 个完成首个核心动作，按获取周追 D2/D7；至少有若干自然复用/推荐或支付动作|101 个冷广告 waitlist、下载量、商店排名|

## V-S-C-R 判断与最常见失败模式

- **V【事实+推断】**：重复出现的是“个人明确痛点 + 可在一眼看到结果的窄承诺”，如训练休息时屏蔽、小时重置 Screen Time、停车自动保存、照片清理。它们只是内容/问题钩子；样本没有证明任何一个自律宠物版本已形成传播。
- **S【建议】**：Reddit 相关问题帖、短录屏、ASO 截图首屏和 landing-page 素材可以在两周各做 20 个单变量变体；不要同时换平台、受众、话术、价格。
- **C【事实】**：可承认的是安装、完成核心动作、trial start、购买；Fitly 的 25 下载/0 trial说明安装仍不足。waitlist、点赞、评论、家人购买都不算外部 C。
- **R【事实】**：本池只有 PetsenseAI 明确报告“零回访”这种 R 失败，个别评论自述 week-2 retention 改善。几乎没有可审计 D2/D7，因此 Reddit 样本不能给商业绿灯。
- **高频失败模式【事实】**：开发先于分发（E39）；承诺太宽/首屏不清（E20/E29）；错误受众点击（E37）；paywall 早于价值（E13/E20）；App Store 可见度弱/算法不可归因（E32/E43）；平台自推规则阻断（E50）；免费/AI 替代而无差异（E21）；成本先于付费（E68）；安装后无二次理由或 bug（E01/E80）。

## 对“自律宠物”可直接借鉴的最多 10 条方法

1. 【建议】把 C 固定为一次真实的“启动→屏蔽确实生效→完成/回到宠物”，不以安装代替。
2. 【建议】先做朋友可操作的首轮 10 人，不扩到公开推广；每人记录从哪一步退出。
3. 【建议】在首屏把受众、iPhone/Screen Time 条件和即时结果讲清，避免获得不可能使用的点击。
4. 【建议】给第二次打开一个明确理由（下一次专注、宠物反馈、周期回顾），并先量 D2/D7；这直接回应 E01 的“一次即走”。
5. 【建议】20 条内容只测一个变量：痛点、结果画面、受众或形式；渠道和 CTA 保持一致。
6. 【建议】给每个来源独立但不混杂的落地页/短链接或记录，先测点击与首次动作；不要假装能由 App Store 销售反推全部归因。
7. 【建议】在朋友能持续复用前不急着定订阅；若将来收费，先让用户感受一次核心价值。
8. 【建议】把 Family Controls 的真实 iPhone 可用性、限制数/恢复路径作为产品风险独立验证，不用模拟器或文案替代。
9. 【建议】隐私定位若保留，要设计最小化、用户可理解的本地指标/访谈补足“完全没有行为信息”的盲区。
10. 【建议】若 20 个合格实验和首批朋友使用后仍无核心动作或 D2，停止增加功能与推广预算，重审承诺与摩擦。

## 来源索引与结构化回报总控

- **来源索引**：E01–E80 的行内链接为唯一正文来源；每条均通过同一帖的 OpenCLI `read` 返回正文/可见评论。重点反证：E01/E20/E30/E39/E43/E50/E57/E68/E69/E80。
- **证据计数**：80 独立帖子/评论；30 天 68，31—90 天 10，91—180 天 2；8 subreddit；失败/强反证 34（42.5%）；开发 29、推广 31、变现 24、失败 34（重叠计）。
- **最强支持**：E34（相关社区的窄发布带作者称 $700 gross）、E47（素材测试的 CPL 与 waitlist 漏斗）、E60（freemium 的实际销售自述）。均仍为创始人自述，未作外部审计。
- **最强反证**：E57（25 下载/0 trial）、E01/E80（0 回访）、E30/E55（50+ 群但 $0 MRR）、E69（上线/订阅基础设施完整仍无收入）。
- **报告**：`/Users/USER/Documents/app/Reddit近期iOSApp开发推广变现证据_2026-08-12.md`；仅新增本文件。磁盘卫生：无下载、无构建、无解压、无生成大文件；外部边界：未发帖/评论/登录/下载/购买/操作账号。
- **工具限制**：OpenCLI 可读取公开可见帖与有限评论，但不能证明作者身份、数字真实性或完整评论树；未进行 App Store/官网逐项外验，故相关存在性为【待验证】。实际模型/effort 运行态不可读，不能确认建议的 Terra high 是否生效。
