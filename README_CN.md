<h4 align="right"><a href="README.md">English</a> | <strong>中文</strong> | <a href="README_TW.md">繁體</a> | <a href="README_JA.md">日本語</a> | <a href="README_KR.md">한국어</a></h4>

<div align="center">
  <img src="skills/kami/assets/images/logo.svg" width="120" />
  <h1>Kami</h1>
  <p><b>好内容，值得好版面。</b></p>
  <a href="https://github.com/tw93/kami/stargazers"><img src="https://img.shields.io/github/stars/tw93/kami?style=flat-square" alt="Stars"></a>
  <a href="https://github.com/tw93/kami/releases"><img src="https://img.shields.io/github/v/tag/tw93/kami?label=version&style=flat-square" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License"></a>
  <a href="https://twitter.com/HiTw93"><img src="https://img.shields.io/badge/follow-Tw93-red?style=flat-square&logo=Twitter" alt="Twitter"></a>
</div>

## 缘起

Kami 为 AI Agent 提供具有纸张质感的文档排版规范与模板。可输出精美的 PDF、高清长图，或导出为可编辑的 PowerPoint 演示文件。

Kami（紙，かみ）在日文中意为“纸”。它内置 8 种出版级文档模板、一套产品落地页系统，以及严格的内容与版式检查门禁。

三部曲之一：[Kaku](https://github.com/tw93/Kaku) (書く) 编写代码，[Waza](https://github.com/tw93/Waza) (技) 磨炼习惯，[Kami](https://github.com/tw93/Kami) (紙) 交付文档。

## 样例展示

多种格式与语言的实际 PDF 输出样本，点击任意卡片即可查看完整文件。

<table>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-musk-resume.pdf"><img src="site/assets/demos/demo-musk-resume.png" alt="创始人简历"></a>
    <br><b>两页简历</b> · 英文
    <br><sub>刚好两页，重要经历清清楚楚</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kami-print.pdf"><img src="site/assets/demos/demo-kami-print.png" alt="Kami 打印一页纸"></a>
    <br><b>单页简报</b> · 中文
    <br><sub>一页讲透要点，随手打印也舒服</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-tesla.pdf"><img src="site/assets/demos/demo-tesla.png" alt="Tesla 财报分析"></a>
    <br><b>研究报告</b> · 中文
    <br><sub>排版层次清晰，核心数据一眼看懂</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-agent-slides.pdf"><img src="site/assets/demos/demo-agent-slides.png" alt="演讲幻灯片" /></a>
    <br><b>演讲幻灯</b> · 英文
    <br><sub>没有花哨杂乱，每页都干干净净</sub>
  </td>
</tr>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-mole.pdf"><img src="site/assets/demos/demo-mole.png" alt="Mole 产品简报"></a>
    <br><b>One-Pager</b> · 英文
    <br><sub>Mole 软件介绍，单页精简版</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-letter.pdf"><img src="site/assets/demos/demo-letter.png" alt="推荐信"></a>
    <br><b>信件</b> · 中文
    <br><sub>正式推荐信，1 页</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-changelog.pdf"><img src="site/assets/demos/demo-changelog.png" alt="更新日志"></a>
    <br><b>更新日志</b> · 英文
    <br><sub>Mole v1.7.1 发布说明</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kaku.pdf"><img src="site/assets/demos/demo-kaku.png" alt="Kaku 作品集"></a>
    <br><b>作品集</b> · 日本語
    <br><sub>Kaku 终端作品集，7 页</sub>
  </td>
</tr>
</table>

## 安装

**Claude Code、Codex、Cursor 与其他 Agent**

```bash
npx skills add tw93/kami -a claude-code codex cursor -g -y
```

或者直接告诉 Agent 自动安装：
> 请阅读 https://kami.tw93.fun/llms.txt 为我安装 Kami

技能会统一存放在 `~/.agents/skills` 共享目录中。Claude Code 自动建立软链接；Codex、Cursor 以及所有支持该规范的 Agent 会自动将其识别为 `/kami`。后续通过 `npx skills update -g -y` 即可静默升级。

**Host Plugin 插件安装**（如果你更偏好平台原生命令，命名空间为 `/kami:kami`；要求 Claude Code v2.1.142 或更高版本）：

```bash
# Claude Code（升级命令：claude plugin update kami）
/plugin marketplace add tw93/kami
/plugin install kami@kami

# Codex（升级命令：codex plugin marketplace upgrade kami，然后 codex plugin add kami@kami）
codex plugin marketplace add tw93/kami
codex plugin add kami@kami
```

**Claude Desktop**：从 GitHub Releases 下载正式打包的 [kami.zip](https://github.com/tw93/kami/releases/latest/download/kami.zip)（不要下载仓库源代码 ZIP），打开 设置 > Skills > "+" > Create skill 上传即可。后续升级点击卡片上的 "..." 选择 Replace 替换为最新包。

大型中文字体不打包进发布压缩包：`skills/kami/scripts/ensure-fonts.sh` 会自动检测并将缺失字体安装到本地系统字体目录中；在本地仓库开发时，脚本会将字体复制进技能目录，模板会优先读取本地字体，未安装时才回退至 jsDelivr CDN。

Kami 每天至多执行一次静默版本检查，并在发现新版本时在对话中轻巧提醒。检查只会读取本地 XDG 缓存标记与 GitHub 公开 Release 信息，绝不上传任何用户文档与对话内容；离线或无缓存目录时自动静默跳过。

## 使用

无需记忆斜杠命令，用日常自然语言吩咐 Agent 即可自动触发。

### 支持语言

英文与中文支持最完整；日文和韩文通过专属字体回退与版式微调支持，并在交付前逐份检查效果：

| 语言 | 支持程度 | 默认衬线字体 |
| :--- | :--- | :--- |
| **English** | 完整支持 | Charter |
| **中文**（简体 / 繁體） | 完整支持 | TsangerJinKai02（仓耳今楷） |
| **日本語** | 字体回退与逐份检查 | YuMincho（游明朝） |
| **한국어** | 字体回退与逐份检查 | Source Han Serif K（思源宋体 韩文） |

各语言日常提示词示例：

- 中文：`帮我做一份一页纸` / `帮我排版一份长文档` / `帮我写一封正式信件` / `帮我做一份作品集` / `帮我做一份简历` / `帮我做一套演讲幻灯片` / `帮我做一份 Markdown 风格的演示稿` / `帮我做一个产品落地页`
- English: `make a one-pager for my startup` / `turn this research into a long doc` / `write a formal letter` / `make a portfolio of my projects` / `build me a resume` / `design a slide deck for my talk` / `make this talk as a Marp deck` / `build a landing page for my app`
- 日本語: `スタートアップ向けの一枚資料を作って` / `この調査を長文レポートに整えて` / `正式な依頼文を作って` / `プロジェクト作品集を作って` / `履歴書を作って` / `登壇用スライドを作って` / `Marp で登壇スライドを作って` / `アプリのランディングページを作って`
- 한국어: `스타트업 원페이저를 만들어줘` / `이 리서치를 장문 문서로 정리해줘` / `정식 레터를 작성해줘` / `프로젝트 포트폴리오를 만들어줘` / `이력서를 만들어줘` / `발표용 슬라이드를 만들어줘` / `Marp 슬라이드로 만들어줘` / `앱 랜딩 페이지를 만들어줘`

**个人品牌偏好配置**（可选）

创建 `~/.config/kami/brand.md` 保存你的个人偏好、品牌主色、默认习惯与写作语气。完整示例参见 [brand.example.md](skills/kami/references/brand.example.md)。

文件顶部为 YAML 格式字段（姓名、职位、邮箱、品牌色、语言、纸张尺寸、文风），正文为自由格式 Markdown。当用户未指定明确排版参数时，Kami 会优先采用配置中的偏好；用户在对话中的明确指令始终保持最高优先级。配置好后无需在每次对话中反复向 AI 叮嘱个人偏好。

## 设计规范

默认采用温暖的浅米色底（`#f5f4ed`）、油墨蓝强调色（`#1B365D`）和经典衬线字体。模板依靠字号层级与留白节奏区分标题、正文与标注，不搞花哨装饰。

- **模板体系**：8 款出版级文档模板：一页纸、长文档、信件、作品集、简历、幻灯片、研报与更新日志，以及配套的多语言落地页系统（支持 EN、CN、KO）。
- **专业图表**：18 种行内原生 SVG 图表，包括研报级系统架构图。时序图、类图与实体关系图可直接写 Mermaid 源码：由 [beautiful-mermaid](https://github.com/lukilabs/beautiful-mermaid) 渲染为 SVG，并通过 `skills/kami/scripts/mermaid_normalize.py` 自动重着色为 Kami 墨蓝温润色系，无需本地安装 Node 环境。
- **幻灯片**：支持 3 条交付路径：默认 WeasyPrint HTML 转高精度 PDF；按需通过 python-pptx 导出可二次编辑的 PPTX；以及位于 `skills/kami/assets/templates/marp/` 的 Markdown 优先 Marp 方案。
- **代码高亮**：安装 Pygments 后自动支持语法着色；未安装时依然可正常生成纯黑灰代码块，不中断流程。
- **严苛检查**：JSON Schema 先行校验输入数据完整性；覆盖率检测防止关键内容在排版时遗漏；交付前通过页面图片逐页校验节奏、孤行与排版平衡。
- **本地 MCP 服务**：内置零外部依赖的 MCP 服务器（`skills/kami/scripts/mcp_server.py`），提供环境自检、渲染、门禁检查与截图工具，任何兼容 MCP 的 Agent 均可直接调用。
- **白底打印模式**：浅米底色是屏幕阅读的最佳默认；同时也支持一键白底模式，适合家庭和办公室黑白/彩色打印机打印，依然保留卡片与表格的温暖底色。完整配方见 [production.md](skills/kami/references/production.md)。

**字体约定**：每份文档全页仅使用单一衬线字体。中文：仓耳今楷（TsangerJinKai02）；日文：游明朝（YuMincho）；韩文：思源宋体（Source Han Serif K）；英文：Charter。详见 [授权条款](#授权条款)。

完整设计手册：[design.md](skills/kami/references/design.md)。快速备忘单：[CHEATSHEET.md](skills/kami/CHEATSHEET.md)。

## 不止于文档

同一套排版规则不仅能输出印刷级文档，也同样适用于产品官网搭建与 AI 绘图模型的提示词指导。

<table>
<tr>
  <td align="center" width="25%" valign="top">
    <a href="https://kami.tw93.fun"><img src="site/assets/showcase/kami-landing.png" alt="Kami 落地页" height="150"></a>
    <br><b>Kami</b> · 产品落地页
    <br><sub>设计系统官方网站</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <a href="https://mole.fit"><img src="site/assets/showcase/mole-landing.png" alt="Mole 落地页" height="150"></a>
    <br><b>Mole</b> · 产品落地页
    <br><sub>macOS 系统清理工具</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-spatialvla.png" alt="SpatialVLA 架构重绘" height="150">
    <br><b>架构图重绘</b> · 英文
    <br><sub>SpatialVLA 论文图 1 重构</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-tesla-optimus.png" alt="Tesla Optimus 专利图" height="150">
    <br><b>专利图排版</b> · 中文
    <br><sub>Tesla Optimus 专利图一览</sub>
  </td>
</tr>
</table>

落地页模板支持直接部署为轻快的多语言官网。在支持图像生成的客户端中，Kami 会调用绘图能力；在纯文本模型中，Kami 也会给出完整的构图提示词供绘图模型使用：

```text
Redraw this as a clean editorial diagram. Background: warm parchment (#f5f4ed), never pure white. One accent only, ink blue (#1B365D); everything else in warm gray with a yellow-brown undertone, no other colors. Thin single-line geometric strokes and simple flat icons. No gradients, no drop shadows, no 3D. Labels in a serif typeface. Generous whitespace, calm and composed, like a figure in a well-typeset report.
```

<sub>上图由 ChatGPT Images 单次生成完成，无任何人工后期修图。Kami 负责给出精细要求，绘图模型负责落笔绘制。</sub>

## 背景

我喜欢美股投资，经常让 Claude 写研究报告。每次出来的东西都是同一种默认文档的样子：灰扑扑的，结构不清晰，格式老旧，换个对话就换一套排版，没有一份让人想读下去。于是我开始一条一条地调字体、配色、间距，直到报告变成一份自己真正愿意看的页面。

后来要去做《你不知道的 Agent：原理、架构与工程实践》分享，手上已经有文档，不想再做 PPT，就用 Claude Design 按自己的设计风格来排版，反复调了很多轮，最后慢慢满意了。再后来加入 SVG 图表，统一配色和间距，逐渐用在常写的各种文档上，再把模板和规则整理成了现在的 Kami。

## 支持作者

- 购买我做的 Mac 清理工具 [Mole for Mac](https://mole.fit)，是对我最直接的支持。
- 如果 Kami 帮到了你，欢迎给它一个 Star，[在 Twitter 分享](https://twitter.com/intent/tweet?url=https://github.com/tw93/kami&text=Kami%20-%20A%20quiet%20design%20system%20for%20professional%20documents.)，或提交 Issue 和 PR。
- 我有两只猫：汤圆、可乐。如果 Kami 让你顺手，欢迎<a href="https://cats.tw93.fun?name=Kami" target="_blank">请她们吃罐头 🥩</a>。

<details>
<summary>这些可爱的朋友已经请过啦 🐱</summary>
<br/>
<a href="https://cats.tw93.fun?name=Kami"><img src="https://cdn.jsdelivr.net/gh/tw93/sponsors@main/assets/sponsors.svg" width="1000" loading="lazy" /></a>
</details>

## 授权条款

Kami 核心代码与模板遵循 MIT 协议开源，欢迎自由使用与贡献。

**字体许可**：仓耳今楷（TsangerJinKai02）个人非商用免费，商用授权请前往 [tsanger.cn](https://tsanger.cn)；Charter、游明朝（YuMincho）、思源宋体（Source Han Serif K）遵循 OFL 开源许可，相关 CJK 回退字体为系统自带或开源授权。
