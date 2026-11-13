# 备选 skill 目录（按功能和契合度排序）

这些参考适合赛前练习和定向复盘。主 skill 已内置常见题型的取舍和基础 UI 检查。遇到具体问题时，可按需阅读一份参考，例如让 Codex 读 `extras/skills/gd-fairness-frustration-audit/SKILL.md`，只检查排位失败后是否解释了公平规则。

表中的星级表示与限时原型的匹配程度。按题目判断是否需要使用；其中的工具和工作流要求以现场环境为准。

---

## A. 需求和设计思考（BRIEF 阶段，最体现“对游戏功能的理解”）

| Skill | 它实际做什么 | 在我们这里怎么用 | 契合度 |
|---|---|---|---|
| gd-five-options | 对一个问题强制生成至少 5 个不同方案并比较 | 练习时探索多个方向，现场只在存在关键取舍时比较 | ★★★ |
| gd-peak-end-audit | 用“峰终定律”检查玩家最记得的高光时刻和结尾 | 设计惊喜时刻和演示的最后一幕 | ★★★ |
| gd-ftue-hero-journey-audit | 用“英雄之旅”检查新手引导和首局体验 | 题目涉及新玩家、新手引导、首周留存时 | ★★★（新玩家题） |
| gd-fairness-frustration-audit | 检查玩家会不会觉得被坑、难度是否“输得服气” | 竞技玩家、匹配、排位、抽奖类题目 | ★★★（竞技题） |
| gd-social-satisfaction-matrix | 把社交功能按“带来满足/带来不满”做矩阵评估 | 社交玩家、组队、公会、好友类题目 | ★★★（社交题） |
| gd-goal-density-and-immediacy-audit | 检查玩家是否随时有下一个目标、能否安全退出、有没有回来的理由 | 每日任务、回流、活动日历类题目 | ★★ |
| gd-perceived-randomness-audit | 评估随机机制在玩家眼里是否公平 | 抽奖、宝箱、掉落、保底设计 | ★★ |
| gd-premium-pass-audit | 审查通行证的价值、免费线平衡、奖励节奏 | 题目涉及 Battle Pass / Booyah Pass | ★★ |
| gd-kpi-coverage-audit | 检查指标是否只看了容易衡量的那部分 | 写“主指标 + 护栏指标”时自查 | ★★ |
| gd-feature-prioritization | 按影响、成本、战略契合给功能排序 | 决定 3 个必做交互的先后 | ★★ |
| gd-player-persona-extractor | 从设计反推“为谁设计”和“反面人群” | 目标玩家写不清楚时 | ★★ |
| gd-granular-player-motivation-audit | 用细分动机分类检查功能服务了哪些玩家动机 | 讲“为什么玩家会在意”时补论据 | ★ |
| gd-core-loop-extractor | 提炼功能的核心循环（行动 → 反馈 → 奖励 → 再来） | 设计说明里画核心循环 | ★★ |
| gd-friction-journey-audit | 找出玩家在流程中卡住、流失的地方 | 优化原型的点击流程 | ★ |
| gd-prototype-intent-audit | 判断原型是用来“说服”还是“验证” | 开工前定原型的范围，按题目选择 | ★ |
| gd-pitch-deck-audit | 审查推介材料的清晰度和说服力 | 写演示讲稿后自查结构 | ★ |
| game-monetization | F2P 经济、虚拟货币、抽奖法规（概率公示、地区限制） | 涉及付费、抽奖、商城时避免踩雷 | ★★ |
| gamification-loops | 积分、徽章、连续签到、进度条背后的心理学 | 任务和成长线设计 | ★★ |
| game-ui-design | 游戏 UI 的可读性、HUD、竞技游戏信息层级 | 界面层级和信息密度 | ★★ |
| game-design-core | 核心循环、动机、手感等游戏设计基础 | 通用参考 | ★ |

## B. 文案和界面质量（搭骨架和打磨阶段）

| Skill | 它实际做什么 | 在我们这里怎么用 | 契合度 |
|---|---|---|---|
| ux-copy | 按钮、空状态、错误提示等界面文案的写法 | 让原型里的每句话都短、清楚、像真游戏 | ★★★ |
| design-critique | 按可用性、层级、一致性给出结构化设计反馈 | 骨架完成后自查一遍 | ★★ |
| no-ai-design-slop | 被动质量关卡，去掉“一看就是 AI 做的”设计 | 打磨阶段最后过一遍 | ★★ |
| design-first-ui-prompting | 把模糊想法写成紧凑的 UI 规格提示词 | 你给 Codex 写改样式的指令时参考 | ★★ |
| fixing-accessibility | 按钮标签、键盘焦点、对比度检查 | 最后的快速检查 | ★ |

## C. 动效和游戏手感（让原型“有游戏感”）

| Skill | 它实际做什么 | 在我们这里怎么用 | 契合度 |
|---|---|---|---|
| web-animation-design | 缓动曲线、时长、弹簧动画的具体数值规则 | 奖励弹窗、按钮反馈、进度条动画的参数 | ★★★ |
| game-feel | 按事件大小分级的“手感”：震屏、停顿、弹跳、数字弹出 | 领奖、升级、胜利时的反馈强度（例子是 Godot，取规则写原生 JS） | ★★★ |
| animation-systems | 产品级动效的原则、默认值、编排方式 | 页面元素出场顺序 | ★★ |
| build-game-audio-feedback | 操作音效、静音开关、手机音频解锁 | 想给领奖加音效时（用 Web Audio，不用素材文件） | ★★ |
| emil-design-eng | 打磨细节和“该不该动”的判断 | 整体打磨参考（篇幅长） | ★ |
| animate | 按正确顺序从零做一个动画 | 做某个关键动画时 | ★ |
| review-animations | 严格审查动效代码 | 时间充裕时 | ★ |
| find-animation-opportunities | 只读地找出哪里值得加动画 | 时间充裕时 | ★ |
| fixing-motion-performance | 修动画卡顿 | 动画掉帧时 | ★ |

## D. 测试和其他（偶尔用）

| Skill | 它实际做什么 | 在我们这里怎么用 | 契合度 |
|---|---|---|---|
| break-ui | 用最极端但真实的数据测试界面（超长名字、0 个物品） | 演示前快速检查会不会撑破布局 | ★ |
| test-playable-web-games | 网页游戏的测试矩阵 | 主流程已有 QA 清单，作为补充 | ★ |
| iterate-until-verified | “执行 → 验证 → 修正”循环 | 只取循环思路 | ★ |
| build-game-inventory | 背包、掉落、装备的数据结构 | 题目涉及道具系统时 | ★ |
| game-ui-ux | HUD 和菜单的布局、安全区（引擎向） | 少用 | ★ |
| prototype | 同一个组件做几个不同版本供挑选 | 很花时间，一般不用 | ★ |

## 许可证说明
- 每个文件夹都保留了原作者的许可证。
- `gd-*` 来自 Stanislav Stankovic 的 game-design-skills-bundle，许可证是 **PolyForm Noncommercial 1.0.0**，只允许**非商业**使用（个人学习、面试准备属于非商业）。Required Notice: Copyright Stanislav Stankovic (https://www.stane-island.net/)。不要把它们用到商业项目里。
- 其余为 MIT 或 Apache-2.0。

## 看过但没收录
| Skill | 原因 |
|---|---|
| baseline-ui | 强制使用 Tailwind 和 React，和单个原生 HTML 冲突 |
| gd-one-page-design-doc | 需要 `pip install reportlab` 生成 PDF |
| Claude-Code-Game-Studios（quick-design、team-live-ops、ux-design） | 依赖它自己的多代理工作室框架和文档结构，单独拿出来用不了 |
| GameDesignOS game-concept-architect | 面向全新游戏立项，不是单个功能；带评测文件，偏重 |
| Impeccable / Taste | 需要运行自带脚本、Node 和浏览器，Taste 还会自动执行命令 |
| ui-ux-pro-max | 依赖 Python 脚本 |
| anthropics web-artifacts-builder | 需要 Node 打包 |
| Whaocaii ai-game-skills | 多代理 + Python 流水线，偏重 |
| prototype-fast（gamedev-skills） | 主张灰盒、不做美术，和“要能演示”冲突 |
