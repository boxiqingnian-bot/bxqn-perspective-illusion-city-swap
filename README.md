# bxqn-perspective-illusion-city-swap

用 Perspective Illusion 做某个城市、某个景观的插画风动画的傻瓜式编排 Skill。

你只需要说想做哪个城市、哪个景观，剩下的路由它牵着走：检查并安装执行 Skill → 补齐缺的信息 → 生成提示词 → 自动执行出预览。

## 它做什么

- **查依赖**：先检查本地有没有 perspective-illusion 执行 Skill，没有就自动从 GitHub 仓库 `dotslashsimran/simcraft` 安装（MIT 许可证，保留原作者署名），并检查 Node.js、Python 3、FFmpeg。
- **缺哪补哪**：城市和景观都说了就直接开工；只说了城市，就给该城市的景观候选点选；什么都没说，就先问城市。
- **两个可选项**：招牌/大厦霓虹灯牌可以自带文字或参考图，BGM 可以自带一首；都不给就走默认（本地通用招牌＋城市环境底噪）。
- **自动接力执行**：提示词确认后在同一会话里自动执行，交付带声音、可连续播放的动态预览，确认前不做高清渲染。

## 安装

任选一种：

- **一句话装**：把下面这句发给你的 AI 助手，它会自己装好——「帮我安装这个 Skill：https://github.com/boxiqingnian-bot/bxqn-perspective-illusion-city-swap」
- **命令行装**：`npx skills add boxiqingnian-bot/bxqn-perspective-illusion-city-swap`
- **手动装**：下载本仓库 ZIP，解压后把文件夹放进你的客户端（Claude Code、Codex 等支持 Skill 的环境）的 skills 目录。

装好之后，之后在对话里说出 Skill 名或直接说想做哪个城市的透视错觉动画，就能调用。

包内文件：

- `SKILL.md`：编排 Skill 本体。
- `references/base-prompt-template.md`：参数化母本模板，机制层固定、城市层为空位。

## 使用

在对话里说一句，例如：「用 Perspective Illusion 做一个 A 市 B 地标的雨夜动画」，或者把一段已有的城市版提示词发给助手、说要改到哪个城市。

## 依赖与致谢

- 执行 Skill：[dotslashsimran/simcraft](https://github.com/dotslashsimran/simcraft) 中的 perspective-illusion（MIT License，作者 Simran Sachdeva）。本 Skill 只通过生成的提示词与它交接，不包含它的代码。

## 许可

本 Skill 采用 MIT 许可证，见 LICENSE 文件。可以自由使用、修改和分发，包括商业用途；分发时请保留版权声明。
