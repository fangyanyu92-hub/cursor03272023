# 移动端用研 + AI 产品 + 动效每日资讯简报（2026-06-30）

**日期**：2026-06-30  
**本 run 覆盖的时间范围**：主题类优先覆盖过去 24 小时至 30 天内的新发布或新热门内容；专家观点/动态覆盖过去 7 天至 30 天，并在专家本人无公开新动态时补充其所在机构/平台的近期高质量内容。  
**本期是否含「移动端动效」专项条目**：是。可快速关注：
- [Introducing Figma Motion: Your Canvas Now Has a Timeline]
- [React Native - Rive：Nitro 新运行时]
- [dotLottie Interactivity with State Machines & Dynamic Theming]
- [Beyond the Toggle: How to Design Micro-Interactions That Shape User Behavior]

---

### [Introducing Figma Motion: Your Canvas Now Has a Timeline]
**来源**：Figma Blog / Config 2026  
**类型**：工具  
**是否与动效相关**：是（动效工具 / 设计到开发交付）

**摘要**：Figma 在 Config 2026 推出 Figma Motion，把时间线、关键帧、预设、缓动与 Dev Mode 代码交付放进同一个设计画布。对移动端动效学习的价值是：动效不再只是视频或口头描述，而可以像组件、变量、token 一样被复用、评审和交付。

**详细展开**
- 背景与问题：以往产品团队常把静态 UI 放在 Figma，把细腻动效放到 After Effects、Rive 或原型插件中，设计意图到工程实现之间容易丢失时序、缓动与关键帧细节。
- 主要发现/方法/功能/观点：Figma Motion 提供 Motion mode、可拖拽时间线、位置/缩放/旋转/透明度关键帧、auto keyframing、time-based comments，并在 Dev Mode 中展示可检查的时间线与 CSS、JSON、React、motion.dev 代码。
- 对移动端用研或 AI 产品经理的启示：用研评审可以把「用户是否理解状态变化」纳入原型测试，而不是等开发后再验证；AI 产品经理可把 loading、流式生成、权限确认、撤销等关键状态做成可复用 motion spec。
- 对快速掌握移动端动效的启示：先从按钮反馈、卡片展开、底部面板进出、加载状态 4 类微交互建立动效 token，再在 Dev Mode 中检查时长、缓动与关键帧是否一致。
- **原文链接**：https://www.figma.com/blog/introducing-figma-motion/

---

### [React Native - Rive：Nitro 新运行时]
**来源**：Rive Docs  
**类型**：工具  
**是否与动效相关**：是（移动端交互动效 / Rive 状态机）

**摘要**：Rive 推荐 React Native 项目迁移到新的 `@rive-app/react-native` 运行时，新版本基于 Nitro Modules，强调更好的性能、文件加载、缓存、ViewModel 数据绑定与状态机控制。对移动端动效学习的价值是：把动效当成可响应业务状态的 UI 组件，而不是一次性播放素材。

**详细展开**
- 背景与问题：React Native 应用常见动效需求已从「播放一段动画」升级为「根据用户输入、网络状态、任务结果实时变化」。传统静态动画文件难以承载复杂状态逻辑，工程侧也容易堆出难维护的触发代码。
- 主要发现/方法/功能/观点：新版运行时要求 React Native 0.78+、Expo SDK 53+、iOS 15.1+、Android SDK 24+，安装方式为 `npm install @rive-app/react-native react-native-nitro-modules`。核心 API 包括 `RiveView`、`useRiveFile`、`useRiveNumber`、`useRiveTrigger`、`useViewModelInstance`，可把数据绑定与状态机输入直接连接到产品状态。
- 对移动端用研或 AI 产品经理的启示：对 onboarding、智能助手执行中、支付成功/失败、学习类角色反馈等场景，可把「状态图」先定义清楚：idle、processing、success、error、retry，再交给动效和工程共用同一状态机。
- 对快速掌握移动端动效的启示：判断是否用 Rive 的关键问题是「动效是否需要响应输入或业务状态」。如果只是播完即可，用轻量播放方案；如果需要按钮、角色、进度、错误恢复等状态联动，优先学习 Rive state machine。
- **原文链接**：https://rive.app/docs/runtimes/react-native/react-native

---

### [dotLottie Interactivity with State Machines & Dynamic Theming]
**来源**：LottieFiles Docs  
**类型**：工具  
**是否与动效相关**：是（Lottie 状态机 / 动态主题）

**摘要**：dotLottie v2 体系把传统 Lottie 扩展到状态机与动态主题，React Native、iOS、Android、Web 等运行时均支持基础状态机、事件、guards、context variables 与主题切换。对移动端动效学习的价值是：Lottie 也在从「播放格式」走向「可交互动效格式」。

**详细展开**
- 背景与问题：很多团队已经沉淀了大量 After Effects/Lottie 资产，但在移动端落地时常遇到「无法表达用户输入」「深浅色主题要导出多套」「成功/失败状态要拆多个文件」等问题。
- 主要发现/方法/功能/观点：dotLottie interactivity 支持 string、numeric、pointer events，支持 guards、context variables、multi-animation，以及基础主题、runtime theme switching、fill/stroke 颜色覆盖。React Native 可使用 `@lottiefiles/dotlottie-react-native`，并通过 `stateMachineFire`、`stateMachineSetNumericInput`、`onStateMachineTransition` 等方法控制运行时状态。
- 对移动端用研或 AI 产品经理的启示：在 AI 产品中，等待、生成中、置信度变化、结果修正、错误兜底都可映射为状态机，而不是只用一个无限转圈 loading；这能降低用户对「黑盒等待」的焦虑。
- 对快速掌握移动端动效的启示：学习 Lottie 时不要只学导出 JSON，也要学 `.lottie` 如何封装状态机和主题；建立「事件 -> 状态 -> 过渡 -> 可访问性替代」的验收清单。
- **原文链接**：https://docs.lottiefiles.com/en/format/dotlottie/interactivity

---

### [Beyond the Toggle: How to Design Micro-Interactions That Shape User Behavior, Build Trust, and Make Products Memorable]
**来源**：Timothy Graf  
**类型**：方法论  
**是否与动效相关**：是（微交互方法论 / 动效 token）

**摘要**：文章把微交互定义为塑造信任、反馈、品牌记忆与感知性能的最小功能单元，而不是「好看的细节」。对移动端动效学习的价值是：每个动效都要回答触发、反馈、规则、循环/模式四件事，并纳入设计系统。

**详细展开**
- 背景与问题：移动端微交互经常被当作上线前的 polish，导致不同页面的按钮、卡片、弹窗、手势反馈节奏不一致，用户形成不了稳定预期。
- 主要发现/方法/功能/观点：文章强调移动端受屏幕尺寸、触控与手势约束，反馈要跟随用户手指；建议定义 fast、standard、slow、deliberate 等 duration tokens，以及 standard、decelerate、accelerate、spring 等 easing tokens，并明确产品动效是效率型还是表达型。
- 对移动端用研或 AI 产品经理的启示：微交互可以作为研究假设被验证，例如「撤销反馈是否降低误操作焦虑」「生成中分步反馈是否提高等待容忍度」「手势阻尼是否让底部面板更可控」。
- 对快速掌握移动端动效的启示：先建立 3 层动效库：即时反馈（100ms 级）、状态变化（200-350ms）、空间转场（350ms+）；同时默认尊重 Reduce Motion，用淡入、静态确认或即时状态替代非必要位移。
- **原文链接**：https://timgraf.com/ux-design/beyond-the-toggle-how-to-design-micro-interactions-that-shape-user-behavior-build-trust-and-make-products-memorable/

---

### [Pingquanqi（平权器）：A Cross-Domain Sociotechnical Framework for Human-Agent Interaction Governance]
**来源**：arXiv（2606.26573）  
**类型**：方法论  
**是否与动效相关**：否

**摘要**：这篇预印本提出 Human-Agent Interaction Governance Framework（HAIGF），将其定位为类似 WCAG 的 Agent 框架层交互设计协议，核心关注认知公平、透明度、受控摩擦与渐进止损。对 AI 产品经理的价值是：Agent 体验不只要「能完成任务」，还要管理用户的理解成本、机会成本与可退出权。

**详细展开**
- 背景与问题：Agent 产品会把复杂决策、工具调用和执行链路隐藏在系统内部，用户可能在不理解成本、风险和替代路径的情况下被动接受 AI 的推进。
- 主要发现/方法/功能/观点：作者提出四类研究空白与对应机制：token-to-lifetime transparency、proactive knowledge leveling、progressive stop-loss、controlled friction，并通过 arXiv、Semantic Scholar、CrossRef、中文可访问数据库等进行交叉检索论证。
- 对移动端用研或 AI 产品经理的启示：移动端 Agent 更容易因为屏幕小而隐藏信息，应在关键节点设计「暂停、解释、比较、撤回」机制；把用户接管频率、误授权率、撤销后恢复成功率纳入研究指标。
- **原文链接**：https://arxiv.org/abs/2606.26573

---

### [Designing AI Agents: 4 Lessons from China’s Qwen Agent]
**来源**：Nielsen Norman Group（专家相关：Kate Moran 所在机构 NN/g）  
**类型**：专家观点/动态  
**是否与动效相关**：否

**摘要**：NN/g 基于 6 名中国参与者的远程可用性研究，拆解 Qwen Agent 在点奶茶、订票等移动任务中的发现：可发现性、熟悉模式、个人数据处理和用户自主权是 Agent 可用性的关键。对 AI 产品经理的价值是：Agent 的能力不足以建立信任，必须让用户看懂入口、流程、费用和授权。

**详细展开**
- 背景与问题：中国超级 App 生态给 Agent 提供了支付、配送、出行等任务闭环，但用户仍把聊天机器人理解为「问答工具」，不一定会自然想到用它完成交易。
- 主要发现/方法/功能/观点：NN/g 发现 Qwen 通过冗余入口降低发现成本，但预填 prompt 若过于具体会造成误导；复用外卖/订票熟悉界面能降低学习成本；过早展示完整地址会引发隐私恐慌；价格、运费、行李额等决策关键信息若缺失，会抵消 Agent 提效。
- 对移动端用研或 AI 产品经理的启示：Agent 研究任务应覆盖端到端闭环，不只看「用户能否触发 Agent」。重点观察用户何时失去控制感、何时切回传统 App、何时开始怀疑数据权限。
- **原文链接**：https://www.nngroup.com/articles/designing-ai-agents/

---

### [One UI 8.5 vs. iOS 26: Speed Test and Performance Comparison]
**来源**：Geeky Gadgets / Nick Ackerman  
**类型**：移动设备竞品分析  
**是否与动效相关**：是（系统转场动画 / 流畅度体验对比）

**摘要**：文章对 Galaxy S25 上的 One UI 8.5 与 iPhone 17 上的 iOS 26 做速度、导航、动画、App 启动、游戏与多任务对比，结论倾向于 One UI 8.5 更快，iOS 26 更强调视觉精致与生态一致性。对移动端动效学习的价值是：动效评价不能只看「是否漂亮」，还要看它是否拖慢导航节奏。

**详细展开**
- 背景与问题：iOS 26 与 One UI 8.5 都在强化系统级动效与视觉风格，但用户日常感知往往来自启动、切换、返回、缩放、相机变焦等高频路径。
- 主要发现/方法/功能/观点：对比认为 One UI 8.5 的导航动画和转场更偏效率，减少菜单与 App 间移动的延迟；iOS 26 动效更精致、视觉更沉浸，但在部分交互中会显得更慢。相机部分则呈现 iPhone 启动快、变焦更顺滑，Galaxy 在功能和自定义上补足。
- 对移动端用研或 AI 产品经理的启示：竞品分析应把「动效感受」拆为速度、连续性、响应性、可预期性、审美一致性五项，而不是笼统写「流畅」。
- 对快速掌握移动端动效的启示：做系统或 App 动效评审时，用高频任务录屏逐帧看：动画是否等输入、是否阻塞下一步、是否用过长缓动制造高级感但牺牲效率。
- **原文链接**：https://www.geeky-gadgets.com/one-ui-8-5-vs-ios-26/

---

### [AI 时代三重门]
**来源**：人人都是产品经理 / 黄钊 hanniman（AI 产品经理大本营相关专家）  
**类型**：专家观点/动态  
**是否与动效相关**：否

**摘要**：黄钊 hanniman 在 2026-06-16 的文章中讨论 AI 时代产品经理与个体能力分层，强调 AI Agent 与 AI Coding 时代需要产品经理亲自下场构建、验证和交付。对 AI 产品经理的价值是：能力重心从写需求转向能定义问题、搭建原型、做评测并完成闭环。

**详细展开**
- 背景与问题：AI 工具降低了原型、代码和内容生产门槛，但也放大了产品经理之间的执行差距；只会描述需求的人，容易被能直接构建和验证的人替代。
- 主要发现/方法/功能/观点：文章将 AI 时代个体路径概括为不同层级的选择，强调从被动消费 AI 到主动使用 AI 构建产品的转变；结合黄钊长期关注的 AI 产品经理能力模型，重点落在 Builder 心态、AI Coding、实战交付与非共识判断。
- 对移动端用研或 AI 产品经理的启示：AI PM 的研究闭环可以更短：先用 AI 快速产出交互原型，再用小样本任务测试验证风险，最后用 eval 指标沉淀成产品验收标准。
- **原文链接**：https://www.woshipm.com/ai/6414314.html
