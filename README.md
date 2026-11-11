# qwskill

qwskill 目前开源了两个 Skill：「AI 采访 Skill」和「升维 Skill」

qws 采访帮创作者解决缺素材、缺选题的问题，把你脑子里零散、还没说清楚的经历和想法，变成可以继续创作的素材和选题

让通用 Agent 动手之前，先调用 qws 升维：它先找到正确的问题，再找出一条更短的解决路线，Agent 照着去做，就能省掉大量无效的试错，不限领域

## 有哪些 Skill

- **qws 采访** `/qws-interview`

  不用写提纲，也不用先把观点想清楚。AI 一次只问一个问题，不带引导地追问，把你做得到却说不清的经验和判断，也就是隐性知识，问清楚，整理成能直接继续创作的知识稿，同时挖出还能展开的选题和素材，完整采访记录也会保留。[详细说明](skills/qws-interview/README.md)

- **qws 升维** `/qws-zoom-out`

  通用 Agent 什么都能做，但每次都靠临场发挥，时好时坏，你问什么它就顺着答什么，你得一遍遍把它拉回来。还没开始时，它帮你先找对路；已经卡住时，它不急着帮你改下一版，先帮你跳出局部。[详细说明](skills/qws-zoom-out/README.md)

## 安装与更新

支持 Codex、Claude Code、Grok、豆包、WorkBuddy，以及其他支持 Skills 的 Agent

### 还没有安装：安装 qwskill

在能够运行 `npx` 的终端中执行，会一次装好全部 Skill：

```bash
npx -y skills add QianWenFlow/qwskill -g --all
```

### 已经安装：装上新的 Skill，并更新到最新版

再执行一次上面的安装命令即可：新开源的 Skill 会装上，已经装过的 Skill 也会更新到最新版

## 使用

直接调用对应 Skill：

```text
/qws-interview
/qws-zoom-out
```

不确定该用哪一个时，可以通过统一入口调用，它会根据你的请求选择对应的 Skill：

```text
/qws
```

例如：

> /qws-interview 想做自媒体，却总觉得自己没什么可讲。请采访我，帮我找选题。

> /qws-zoom-out 两个方案各有道理，问了几个 AI 也拿不定主意。到底选哪个？

<details>
<summary><strong>文件结构</strong></summary>

```text
qwskill/
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    ├── qws/
    │   └── SKILL.md
    ├── qws-interview/
    │   ├── README.md
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   ├── scripts/
    │   │   └── verify_theory_overlay.py
    │   └── references/
    │       ├── contract-writer-protocol.md
    │       ├── interview-workflow.md
    │       └── knowledge-validation.md
    └── qws-zoom-out/
        ├── README.md
        ├── SKILL.md
        ├── agents/openai.yaml
        └── references/
            ├── system-scope-model.md
            ├── method-sources.md
            ├── landing-ai.md
            ├── landing-text.md
            └── landing-content.md
```

</details>

## 项目信息

- 作者：[千文Flow](https://x.com/QianWenFlow)
- 特别感谢 dontbesilent 开源的 [dbskill](https://github.com/dontbesilent2025/dbskill)，为本项目的结构校验与开源准备提供了工具支持

## 许可证

本项目采用 [CC BY-NC 4.0](LICENSE) 许可证

- 个人使用、学习、研究与非商业项目可以直接使用
- 公开发布衍生作品时，请注明来源
- 商业用途需要单独授权，请联系作者
