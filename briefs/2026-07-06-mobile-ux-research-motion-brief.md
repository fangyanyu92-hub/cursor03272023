# 移动端用户研究 + AI 产品 + 移动端动效每日资讯简报

**日期**：2026-07-06  
**本 run 覆盖的时间范围**：主题类优先覆盖过去 24 小时至 30 天内新发布或新热门内容；专家观点/动态覆盖过去 7 天至 30 天，并在专家本人无新内容时补充其机构/平台高质量内容。  
**本期是否含「移动端动效」专项条目**：是。重点可先看：
- [SketchDynamics: Exploring Free-Form Sketches for Dynamic Intent Expression in Animation Generation]
- [dotLottie State Machines: Interactive State-Driven Animations]
- [Why One UI 8 is the first version that understands attention spans]

---

### [Self-Evolving Systems: Moving Beyond Deterministic Interfaces to Adaptive Generative Interfaces]

**来源**：Google Research  
**类型**：方法论  
**是否与动效相关**：是（动态生成界面 / 实时界面重构，偏交互表达而非传统转场动效）

**摘要**：Google Research 提出 Adaptive Generative Interfaces：界面不再只是固定布局，而是可依据用户意图实时生成、扩展和重构功能。对 AI 产品经理的价值是，把“降低导航税”作为可测量的体验目标；对动效设计的启发是，动态变化必须服务于意图、层级和任务推进，而不是只追求视觉炫技。

**详细展开**
- **背景与问题**：复杂软件中的功能越来越多，传统确定性界面依赖固定信息架构和固定路径，用户需要在菜单、页面和控件之间反复寻找，形成较高的 navigation tax。
- **主要发现/方法/功能/观点**：研究提出三类机制：Directed synthesis（用户直接命令生成新功能）、Inferred synthesis（从未满足需求推断并生成能力）、Real-time adaptation（实时调整视觉与功能结构）。研究以数字银行原型 Penny 做被试内比较实验，N=72，采用 counterbalanced Latin Square 控制顺序效应；Adaptive generative 版本 SUS 得分 84.38，显著高于确定性界面的 53.96，差异 30.42 分，p < 0.0001，效应量 d=1.04。
- **启示（含动效）**：AI 产品设计应从“设计一个页面”转向“设计一组可约束的生成规则”。若用于移动端，动态重构应有明确的运动语义：新生成能力用可追踪的进入动效标明来源，界面重排用轻量布局过渡降低迷失感，高风险操作保持稳定位置和确认节奏。
- **原文链接**：https://research.google/pubs/self-evolving-systems-moving-beyond-deterministic-interfaces-to-adaptive-generative-interfaces/

---

### [Mapping the Design Space of User Experience for Computer Use Agents]

**来源**：Apple Machine Learning Research  
**类型**：方法论  
**是否与动效相关**：否

**摘要**：Apple 研究团队把 Computer Use Agents 的 UX 设计空间拆成 prompts、可解释性、用户控制、心智模型等维度，并用专家访谈与 Wizard-of-Oz 用户研究验证。它适合 AI 产品经理用作 agent 功能评审清单：不仅看能不能完成任务，还要看用户是否理解、能否接管、是否信任。

**详细展开**
- **背景与问题**：LLM-based computer use agents 已能操作界面元素执行用户命令，但业界对“用户希望怎样与这类 agent 协作”仍缺少系统化 UX 地图。
- **主要发现/方法/功能/观点**：研究分两阶段：第一阶段复盘既有系统并访谈 8 位 UX 与 AI 从业者，形成 UX consideration taxonomy；第二阶段对 20 名参与者做 Wizard-of-Oz 研究，由研究者扮演网页端 computer-use agent，观察正常、出错和高风险任务中的用户反应。
- **启示（含动效）**：做移动端 agent 时，建议把“解释当前动作”“允许暂停/撤销”“显示下一步意图”“出错时明确恢复路径”纳入原型测试。若涉及界面动效，动效不应掩盖 agent 的真实操作边界，而应辅助展示 agent 正在看哪里、将要点哪里、用户何时可以介入。
- **原文链接**：https://machinelearning.apple.com/research/mapping

---

### [SketchDynamics: Exploring Free-Form Sketches for Dynamic Intent Expression in Animation Generation]

**来源**：CHI 2026 / HKUST  
**类型**：方法论  
**是否与动效相关**：是（动画生成 / 动态意图表达）

**摘要**：SketchDynamics 研究如何让用户用自由草图向视觉语言模型表达“元素如何随时间和空间变化”。对移动端动效学习的价值是：先表达 dynamic intent，再谈关键帧；动效需求不应只写“更丝滑”，而要描述路径、速度、节奏和状态变化意图。

**详细展开**
- **背景与问题**：现有动画生成工具常把草图限制为固定命令或预定义符号，忽略了设计师和用户在自由草图中表达动态意图的自然方式。
- **主要发现/方法/功能/观点**：研究实现了 sketch storyboard to motion graphics 工作流，让用户通过自由草图向 VLM 表达动态意图，并经过三阶段、24 名参与者研究迭代界面。结果显示，草图能以较低输入成本传递运动意图，但其歧义性要求系统保留澄清和反馈回路。
- **启示（含动效）**：移动端动效需求可采用“草图 + 语义标注”的方式沉淀：例如“卡片从列表位置扩展到详情页，图片保持空间连续，CTA 延迟 80-120ms 出现”。这有助于 PM、设计师和工程师围绕同一套运动意图沟通，而不是反复对齐抽象形容词。
- **原文链接**：https://programs.sigchi.org/chi/2026/program/content/222469

---

### [Notational Animating: An Interactive Approach to Creating and Editing Animation Keyframes]

**来源**：CHI 2026 / University of Waterloo / Adobe Research  
**类型**：方法论  
**是否与动效相关**：是（动画关键帧 / GenAI 动效创作）  
**收录状态**：往期精选补位，首次收录日期：2026-06-25

**摘要**：这项 CHI 2026 Honorable Mention 研究把动画师常用的运动标注形式化为 source、path、target，并通过系统生成关键帧。相比上次收录，本次新增启发角度是：移动端团队可以把“动效标注法”变成需求模板，降低 PM、设计和开发之间的解释损耗。

**详细展开**
- **背景与问题**：动画师常用箭头、速度线、路径、姿态等 notation 表达力、路径和动态，但这些标注高度上下文化，AI 或工具很难稳定理解。
- **主要发现/方法/功能/观点**：研究分析 135 个真实世界草图，将高层运动标注形式化为结构化动画表示，并构建系统把标注翻译成 intended animation，同时提供动态 UI widgets 做精细参数控制，形成闭环反馈以处理歧义。
- **启示（含动效）**：移动端动效规范可以补一个“notation 层”：入口、路径、目标、持续时间、强调程度、是否可被 Reduce Motion 降级。这样既能保留表达性设计的灵活度，也能避免每个页面都用孤立、不可复用的动效描述。
- **原文链接**：https://programs.sigchi.org/chi/2026/program/content/222027

---

### [dotLottie State Machines: Interactive State-Driven Animations]

**来源**：LottieFiles Developer Portal  
**类型**：工具  
**是否与动效相关**：是（Lottie 状态机 / 移动端交互动效落地）

**摘要**：dotLottie 的 State Machines 文档更新到 2026-06-29，明确把状态、转场、输入和交互逻辑封装在 `.lottie` 文件中。对移动端动效学习的价值是：Lottie 不再只适合播放型动画，也开始支持更可移植的交互状态逻辑。

**详细展开**
- **背景与问题**：传统 Lottie 常被用于 onboarding、loading、成功反馈等线性播放场景；一旦需要点击、指针事件、自定义信号等交互，往往要在各端重复写胶水代码。
- **主要发现/方法/功能/观点**：dotLottie state machine 由 Inputs、Interactions、States、Transitions 四部分组成，状态机文件保存在 `.lottie` 包内 `s/` 目录，并在 `manifest.json` 中引用。官方说明其逻辑可在 web、iOS、Android、React Native 等运行时复用。
- **启示（含动效）**：如果移动端团队已有大量 Lottie 资产，可先把高频反馈（按钮状态、收藏/取消、加载成功/失败）改造成状态机，而不是立即迁移到 Rive。动效 token 层面建议同步定义：默认状态、按下状态、成功状态、错误状态、降级静态状态。
- **原文链接**：https://docs.lottiefiles.com/en/format/dotlottie/interactivity/state-machines

---

### [Why One UI 8 is the first version that understands attention spans]

**来源**：Android Police  
**类型**：移动设备竞品分析  
**是否与动效相关**：是（系统动效 / 注意力负担 / 非线性动画）

**摘要**：Android Police 将 One UI 8 的体验变化概括为“尊重注意力”：减少通知打断、用 10/90 多任务布局突出主任务，并通过更自然的非线性动画降低理解成本。对移动端动效学习的价值是：流畅不是唯一目标，可预测、易跟随、少打断同样是动效质量。

**详细展开**
- **背景与问题**：One UI 长期被认为功能丰富但负担较重，复杂设置、通知墙和多层菜单会持续消耗用户注意力。
- **主要发现/方法/功能/观点**：文章指出 One UI 8 使用 Now Bar / Now Brief 让实时信息留在更合适的位置；10/90 分屏让主应用占据视觉中心；锁屏根据情境展示信息；动画从僵硬匀速转向非线性 ease-out，让元素更像真实物体一样进入和停靠。
- **启示（含动效）**：做移动端竞品分析时，不只记录“动画快不快”，还要记录运动如何帮助用户理解结构：AOD 到锁屏再到桌面的连续关系、通知进入的层级、次要信息是否以低打断方式呈现。动效评审可增加“是否减少认知负担”这一维度。
- **原文链接**：https://www.androidpolice.com/one-ui-8-calmer-design/

---

### [The Methodological Problems Hiding in Your Research Tools]

**来源**：Nielsen Norman Group（专家相关：Kate Moran 所在机构 NN/g）  
**类型**：专家观点/动态  
**是否与动效相关**：否

**摘要**：NN/g 提醒：AI 正在进入研究计划、访谈主持和分析环节，但很多工具本身缺乏扎实的研究方法论基础，可能把“自信的错误研究”规模化。对用户研究员与 AI PM 的价值是，采购和使用 AI 用研工具时要验证方法支持，而不是只看自动化演示。

**详细展开**
- **背景与问题**：过去研究工具最多只是降低效率或带来绕路；现在 AI 工具会直接生成任务、主持测试、分析数据，如果方法论有缺陷，影响会被快速放大。
- **主要发现/方法/功能/观点**：文章列出三类典型问题：量化可用性测试缺少多成功 URL 和任务随机化等基础能力；分析工具过度依赖文字 transcript，忽视用户沉默时的视频行为；工具界面混淆用户访谈和可用性测试，导致新手把评估研究做成“问意见”。
- **启示（含动效）**：AI 产品经理在引入 AI research tool 时，应做真实项目 pilot，并检查：任务是否诱导、是否能随机化、是否能标注行为视频、AI moderator 是否允许研究员接管。对动效测试也一样，不能只问“好不好看”，要观察行为、完成率、误触和注意力转移。
- **原文链接**：https://www.nngroup.com/articles/research-tool-problems/

---

### [闭关三个月，我把自己变成了一个“全能Builder”]

**来源**：人人都是产品经理 / 黄钊 hanniman（AI 产品经理大本营）  
**类型**：专家观点/动态  
**是否与动效相关**：否

**摘要**：黄钊 hanniman 复盘自己用 AI Coding 从零重写 ExcelMaster v2 的经历，强调 AI 产品经理要从写 PRD 转向能端到端 build、测试和交付。对 AI PM 的启发是：Agent 时代的产品判断力来自真实生产约束，而不是 demo 级验证。

**详细展开**
- **背景与问题**：AI 产品经理如果只停留在需求文档、prompt 或 demo，很难理解 agentic 工具在真实工程、用户反馈、上线稳定性中的边界。
- **主要发现/方法/功能/观点**：文章提到 ExcelMaster v2 包含前端、后端、服务端、Agent、LLM Proxy、官网、CI/CD、自动化测试等，代码库约 30 万行；作者还开源了 Argus Automation 这类 Computer Use MCP 插件，并用 Agent 看护自动化测试，让 AI 夜间执行真实用户疑难 Excel case。
- **启示（含动效）**：对 AI 产品经理来说，未来竞争力是把用户洞察、工程可行性、测试闭环放在同一张桌上。即使是移动端动效需求，也应从“想要高级感”转成可交付约束：性能预算、降级策略、状态机边界、异常场景和自动化回归。
- **原文链接**：https://www.woshipm.com/ai/6412345.html
