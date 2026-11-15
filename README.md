# Garena GMAP R4 · Codex 原型 Skill

两个 skill 分工：

- `$game-brainstorm`：拿到题目后和你一起发散、挑选、打磨创意，可以画几张一屏草图对比，最后把选定的想法写进 `prototype/BRIEF.md`。不写原型代码。
- `$game-prototype`：按 BRIEF.md 做单文件 HTML，负责修改、修 bug 和交付前复查。默认交付为 `prototype/index.html`，可双击打开。

具体题目决定提交和讲解要求。

## Windows 现场用法

1. 在 [GitHub 仓库](https://github.com/WeijieCao77/garena_skill) 的 `main` 分支点 **Code → Download ZIP**，用 Windows 的 **全部解压缩** 解压。打开公司提供的 Codex，选择包含 `AGENTS.md` 和 `.agents` 的项目目录（通常是 `garena_skill-main`）。
2. 在 Codex 输入 `$`，确认能看到 `game-brainstorm` 和 `game-prototype`。如果找不到，先确认项目目录，再新开会话或重启 Codex。CLI 也可用 `/skills` 查看。必要时可把 `.agents\skills\` 下的这两个文件夹复制到 `%USERPROFILE%\.agents\skills\`。
3. 权限保持默认（只能写当前项目、需要时才询问）。不要开“完全访问”；如果每次改文件都弹审批，就把权限切到允许写入当前项目的那一档。
4. 打开 [`PROMPTS.md`](PROMPTS.md)：A0 检查环境 → A1 贴题目发散 → A2 来回聊 → A3 收敛 → A4 定下来 → A5 换 `$game-prototype` 开工。之后按需要用 B 和 C 两部分的模板。
5. 若现场无法发现 skill，直接让 Codex 读取 `.agents/skills/game-brainstorm/SKILL.md`（做原型时换成 `game-prototype`）并按它执行，再贴题目。若 ZIP 无法下载但浏览器能访问文件，直接复制 `SKILL.md` 正文进 Codex。正文足以启动，参考文件可按需补充。
6. 在资源管理器双击 `prototype\index.html`，或在 PowerShell 运行 `Start-Process .\prototype\index.html`。用实际的玩家控件走一遍，再按题目要求提交。

Codex 的项目和用户 skill 路径见 [OpenAI 官方文档](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)。

## 仓库内容

| 路径 | 用途 |
| --- | --- |
| `AGENTS.md` | 每轮自动加载的工作规则：每条消息只做一件事、BRIEF.md 记录状态、Locked 不动、自动存档、简短汇报。 |
| `PROMPTS.md` | 现场提示词模板：开场、中间改动、修 bug、回退、交付前、上下文管理。 |
| `.ignore` | 让 `rg` 搜索跳过 `extras/` 和 `examples/`，减少无关读取。 |
| `.agents/skills/game-brainstorm/` | 创意 skill：发散角度卡（lenses）、游戏里的 AI 角色清单、Garena 游戏与题型速查。 |
| `.agents/skills/game-prototype/` | 制作和复查 skill：UI 指南、验收清单、演示提示。`assets/scaffold.html` 是可直接打开的组队样例，可复用单步选择流程的骨架。 |
| `examples/codm-rookie-camp/` | 原有 CODM 新兵训练营样例。可对照较完整的演示规模。 |
| `.agents/skills/frontend-design/`、`.agents/skills/game-engine/` | 手动调用的外部参考，分别用于扩展设计探索和真正的小游戏。 |
| `extras/` | 赛前练习或定向复盘用的可选参考。 |
| `prototype/` | 现场原型输出目录。 |

## 赛前盲练

任选一道没做过的题。用同一题开两个空白会话，分别只贴题目、贴题目并调用 skill。对照首次可点击所需时间、必做项通过数、关键边界是否可演示，以及首屏能否一眼找到主操作。再用另一题复测，把两次顺序对调。

- 排位题：设计一个横屏赛后界面。玩家能比较两条复盘建议，选择下一局练习目标，并看到目标已生效。演示本局数据不足的状态。
- 社交题：设计一个可按语言和目标找队友的组队功能。玩家能找到合适队伍、发起请求并看到结果。演示目标房间刚刚满员的状态。
