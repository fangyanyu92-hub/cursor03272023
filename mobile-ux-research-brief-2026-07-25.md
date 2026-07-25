# 移动端用户研究与动效资讯简报｜2026-07-25

**日期**：2026 年 7 月 25 日  
**本 run 覆盖范围**：主题类优先检索 2026-06-25～2026-07-25（并优先核验上次 run 于 2026-07-24T01:04:52Z 结束后的新增）；专家观点/动态检索近 7～30 天。  
**本期收录**：7 条（6 条新收录、1 条往期精选）。  
**本期含「移动端动效」专项条目**：是。快速扫读建议先看：

- [Expressive Design: Google's UX Research]
- [Unveiling the User Experience Design of Mobile Animations…（往期精选）]
- [Google Gemini Logo Drop Animation]
- [BurnBar Streak Flame Animation]

> 去重说明：近期滑窗内的 Google CHI 论文《Usability Hasn’t Peaked》、M3 Expressive Motion Theming、Figma Motion、Lottie Creator 2.0、AniMINT、Apple Pare、NN/g「Crafting AI Explanations」及近两周系统横评均不重复推送。本期改以 Google Design 的表达性研究长文（与 CHI 论文互补的研究过程稿）、7 月 17 日新挂出的 SeerGuard，以及 7 月 24 日新上线的 60fps 动效案例为主。

---

### [Expressive Design: Google's UX Research]
**来源**：Google Design / Material Research  
**类型**：方法论  
**是否与动效相关**：是（表达性设计 / 颜色·形状·尺寸·运动协同 / 注意力引导）

**摘要**：Google 用 3 年、46 项研究、超过 18,000 名参与者支撑 Material 3 Expressive，指出可用性并未触顶：表达性设计在眼动与任务效率上均优于既有 Material 3，且对 45 岁以上用户的注视速度差距有明显拉平。对动效学习的价值是：运动不是装饰层，而是与颜色、形状、尺寸、容纳（containment）并列的「可见层级」工具。

**详细展开**
- **背景与问题**：业界常认为移动 UI 已高度同质化，再加视觉表达会损害效率；研究团队则追问「能否在提高情感连接的同时提升可用性」。
- **主要发现/方法/观点**：方法组合包括眼动、问卷/焦点小组、偏好实验与可用性任务。实验室眼动中，用户对关键控件的注视可达对照版的数倍更快（文中以邮件「发送」为例）；跨 10 款应用的对比任务也显示关键动作点击更快。年轻用户对表达性设计偏好尤其强（18–24 岁可达约 87%），同时可及性相关指标（更大触控、更高对比）也被纳入取舍。失败案例如打散的歌单布局说明：破坏既有交互范式时，表达性会反噬可用性。
- **启示（含动效）**：移动端动效应服务于「关键动作更强运动对比、次要区域弱反馈」；把 duration / spring / 空间 vs 效果（spatial vs effects）做成可复用 motion token，并在 Reduce Motion 下保留层级信息。落地时先锁定主路径再加表达，而不是先做花活再补可用性。
- **原文链接**：https://design.google/library/expressive-material-design-google-research

---

### [SeerGuard: A Safety Framework for Mobile GUI Agents via World Model Prediction]
**来源**：JIUTIAN Research / arXiv（2026-07-17）  
**类型**：方法论  
**是否与动效相关**：否（但与「动作后果可视化 / 状态预演」产品形态相邻）

**摘要**：面向移动 GUI Agent 的「后果感知」安全框架：在执行前做指令筛查与动作级风险评估，用语义下一状态预测代替像素级世界模型。对 AI 产品经理的核心价值是把安全从「事后告警」前移为「预演—拦截—保留效用」的可度量闸门。

**详细展开**
- **背景与问题**：移动端一次误触即可造成支付、隐私或删数等不可逆后果；仅靠恶意指令过滤或事后轨迹判定，都难以覆盖「指令看似无害、落在当前界面却危险」的场景。
- **主要发现/方法/观点**：SeerGuard 含指令级筛选与动作级评估两段；SAWM（Safety-Augmented World Model）在截图+候选动作上预测语义下一状态、安全标签与简短理由。评估同时报告 Safety-Utility Score 与 Risk-Cost Score，避免「只会拒答」的伪安全。文中在 Qwen3-VL-8B 上报告 SUS 从 0.191 升至 0.596（ω=0.8）、RCS 从 0.347 降至 0.130（α=0.8）。
- **启示**：Agent 产品应用研清单应同时测「高风险拒绝率、良性任务完成率、误拒成本」；交互上可把「将发生什么」做成可确认的状态预览（确认卡、差异高亮、可撤销窗口），而不是只给抽象风险分。注意样本与基准边界：结果来自论文报告的 MobileSafetyBench 设定，迁移到自有业务仍需场景重标定。
- **原文链接**：https://arxiv.org/abs/2607.15550

---

### [Unveiling the User Experience Design of Mobile Animations from the Cognitive and Emotional Perspective]（往期精选）
**来源**：International Journal of Human–Computer Interaction / 广东工业大学 & Griffith University  
**类型**：方法论  
**是否与动效相关**：是（转场动效 / 注意捕获 / PAD 情绪映射）  
**首次收录日期**：2026-05-28

**摘要**：这篇开放获取研究用眼动 + PAD 情绪量表，在 Garrett UX 框架的结构/框架/表现层上，把移动动画参数映射到注意与情绪结果：任务相关动态更快抓眼；加速运动优于匀速/减速；左→右偏温和，自下而上与放大偏惊讶，硬切更接近无聊。

**本次新增启发角度**
- 可与本期 Google 表达性研究并读：前者给「层级对比提升效率」的系统证据，本篇给「具体缓动与转场方向如何改情绪」的微观参数表——适合直接写成动效 A/B 实验矩阵。
- 对 AI 产品等待态：优先测「加速 vs 匀速」对首次注视与主观无聊的影响，而不是只比插画精美度。

**详细展开**
- **背景与问题**：移动动画研究多停在案例与功能描述，缺少跨 UX 层级、同时量化认知与情绪的框架。
- **主要发现/方法/观点**：结构层关注页面转场，框架层关注布局/控件反馈，表现层关注速度与样式；眼动指标含首次注视等，情绪用 PAD 距离最近基本情绪标签。结果支持「动态优于静态（任务相关时）」「加速更易首抓注意」「转场风格分化情绪」。作者也提醒实验室生态效度可能放大显著线索效果。
- **动效启示**：建立三层 token——结构（转场方向/时长）、框架（控件反馈强度）、表现（加速曲线）；主任务路径用加速/强对比，背景装饰降到接近静态；硬切仅用于低情绪成本的工具流。Reduce Motion 时用颜色/尺寸层级替代位移。
- **原文链接**：https://doi.org/10.1080/10447318.2026.2630289

---

### [Google Gemini Logo Drop Animation]
**来源**：60fps.design / Google Gemini  
**类型**：案例研究  
**是否与动效相关**：是（模式切换 / Logo Morph / 语音助手状态）

**摘要**：进入 Gemini Live 时，四角星标自屏幕中心下坠并形变为底部发光声波，同时 Hold/End 控件与顶部信息条淡入。适合学习「语音模式切换如何用一次 morph 完成身份→状态→控件」三拍叙事。

**详细展开**
- **背景与问题**：语音助手从静默 UI 切到实时对话时，若只换文案或切页，用户难以确认「已进入可说状态」。
- **主要功能/观点**：Logo drop → morph 为波形 → 控件淡入，把品牌符号直接变成状态载体；页面发布时间戳为 2026-07-24 UTC。
- **动效启示**：模式切换动效预算建议压在一次连续变形内，避免多段并行抢注意；Reduce Motion 可保留波形静态图标 + 文案状态，去掉坠落位移。来源为交互展示站，无转化或理解度实验数据，仅作模式假设。
- **原文链接**：https://60fps.design/shots/google-gemini-logo-drop-animation

---

### [BurnBar Streak Flame Animation]
**来源**：60fps.design / BurnBar  
**类型**：案例研究  
**是否与动效相关**：是（Bottom Sheet / Idle 动效 / Spring 日历转场）

**摘要**：「最长连续记录」底部面板以弹簧上滑入场，中心火焰持续 idle 扭动，日历左右切换用快速水平滑移 + 月份名交叉淡入。适合拆解 gamification 场景里「入场强调一次、内容区保持轻量 idle」的节奏分配。

**详细展开**
- **背景与问题**：连续打卡类面板既要庆祝成就，又要让用户继续浏览日历；全程高能量动效容易造成疲劳。
- **主要功能/观点**：入场用一次 spring bounce；火焰做低幅度连续 idle；月份切换用短促 slide + crossfade。页面时间戳为 2026-07-24 UTC。
- **动效启示**：把动效强度分成「入场一次性 / 内容区 ambient / 导航 snappy」三档 token；ambient 必须可关（电池、Reduce Motion、前台专注模式）。展示站同样缺少效果实验，落地前应用研验证 idle 是否干扰读数。
- **原文链接**：https://60fps.design/shots/burnbar-streak-flame-animation

---

### [iOS 27 vs Android 17: I used both, and it’s hard to pick a winner]
**来源**：iGeeksBlog / Ava  
**类型**：移动设备竞品分析  
**是否与动效相关**：是（系统动画流畅度 / bounce / Liquid Glass 透明度控制）

**摘要**：作者在双系统 beta 间切换后的一手体验对比：Android 17 强调更快动画、Quick Settings 轻微弹跳与多任务气泡；iOS 27 强调 Liquid Glass 透明度滑杆、锁屏时钟可缩小与整体一致性。结论偏向「Android 更兴奋，iOS 更可靠」——适合用研做系统动效启发式清单，而非当作实验室结论。

**详细展开**
- **背景与问题**：旗舰系统年更常被功能表淹没，缺少对日常感知节奏（动画速度、材质、多任务打断）的对照描述。
- **主要发现/观点**：设计上 iOS 27 的视觉第一印象更强，Android 17 的日常微改进（模糊、弹跳、可定制搜索栏快捷方式）更「天天碰到」；性能上双方都更快，但实现路径不同（Apple 公布启动/传输等优化数字，Android 侧强调内存限制与多任务）。文章为评测体，含主观胜负判定。
- **启示（含动效）**：竞品用研可固定四项动效观察：转场时长主观快慢、跟手弹性、材质透明是否伤害可读、多任务浮层是否打断主任务。把「兴奋」与「可靠」拆成可打分量表，避免只记功能有无。
- **原文链接**：https://www.igeeksblog.com/ios-27-vs-android-17/

---

### [Types of AI Explanations]
**来源**：Nielsen Norman Group（专家相关：Kate Moran 所在机构；为《Crafting AI Explanations…》侧栏）  
**类型**：专家观点/动态  
**是否与动效相关**：否

**摘要**：NN/g 把企业 AI 解释整理为四组对立：局部/全局、可直接解释/事后解释、静态/交互、模型侧/数据侧，并点出 Agent 场景下「行动计划预览」更接近事前说明而非事后合理化。适合 AI PM 把「解释」写成可配置能力，而不是一段固定文案。

**详细展开**
- **背景与问题**：同一套模型要服务管理者、建造者与业务专家时，单一解释粒度会同时造成信息过载与信任不足。
- **主要观点**：局部解释回答「这一次为什么」；全局解释回答「系统通常怎么判」。Agent 若能在执行前展示步骤计划，解释应前置为可审预览。交互式解释适合跨角色共审；数据侧解释则用相似历史案例帮助领域专家校验。
- **启示**：用研与产品评审可按角色勾选默认解释类型，并规定高风险动作必须提供「计划预览 + 可追问」；界面上用渐进披露，避免把模型权重故事塞给终端用户。本文是 taxonomy 侧栏，不是新的对照实验。
- **原文链接**：https://www.nngroup.com/articles/ai-explanations/
