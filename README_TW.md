<div align="center">
  <img src="skills/kami/assets/images/logo.svg" width="120" />
  <h1>Kami</h1>
  <p><b>好內容，值得好版面</b></p>
  <p><a href="README.md">English</a> · <a href="README_CN.md">中文</a> · 繁體 · <a href="README_JA.md">日本語</a> · <a href="README_KR.md">한국어</a></p>
  <a href="https://github.com/tw93/kami/stargazers"><img src="https://img.shields.io/github/stars/tw93/kami?style=flat-square" alt="Stars"></a>
  <a href="https://github.com/tw93/kami/releases"><img src="https://img.shields.io/github/v/tag/tw93/kami?label=version&style=flat-square" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License"></a>
  <a href="https://twitter.com/HiTw93"><img src="https://img.shields.io/badge/follow-Tw93-red?style=flat-square&logo=Twitter" alt="Twitter"></a>
</div>

## 緣起

Kami 為 AI Agent 提供具有紙張質感的排版規範與文件範本。可輸出精美的 PDF、高解析度長圖，或匯出為可編輯的 PowerPoint 簡報。

Kami（紙，かみ）在日文中意為「紙」。它內建 8 種出版級文件範本、一套產品落地頁系統，以及嚴格的內容與版式檢查機制。

三部曲之一：[Kaku](https://github.com/tw93/Kaku) (書く) 編寫程式碼，[Waza](https://github.com/tw93/Waza) (技) 磨練習慣，[Kami](https://github.com/tw93/Kami) (紙) 交付文件。

## 範例展示

多種格式與語言的實際 PDF 輸出樣本，點選任意卡片即可檢視完整文件。

<table>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-musk-resume.pdf"><img src="site/assets/demos/demo-musk-resume.png" alt="創辦人履歷"></a>
    <br><b>兩頁簡歷</b> · 英文
    <br><sub>剛好兩頁，重要經歷清清楚楚</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kami-print.pdf"><img src="site/assets/demos/demo-kami-print.png" alt="Kami 列印一頁紙"></a>
    <br><b>單頁簡報</b> · 中文
    <br><sub>一頁講透要點，隨手列印也舒服</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-tesla.pdf"><img src="site/assets/demos/demo-tesla.png" alt="Tesla 財報分析"></a>
    <br><b>研究報告</b> · 中文
    <br><sub>排版層次清晰，核心數據一眼看懂</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-agent-slides.pdf"><img src="site/assets/demos/demo-agent-slides.png" alt="演講投影片" /></a>
    <br><b>演講投影片</b> · 英文
    <br><sub>沒有花哨雜亂，每頁都乾乾淨淨</sub>
  </td>
</tr>
<tr>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-mole.pdf"><img src="site/assets/demos/demo-mole.png" alt="Mole 產品簡報"></a>
    <br><b>One-Pager</b> · 英文
    <br><sub>Mole 軟體介紹，單頁精簡版</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-letter.pdf"><img src="site/assets/demos/demo-letter.png" alt="推薦信"></a>
    <br><b>信件</b> · 中文
    <br><sub>正式推薦信，1 頁</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-changelog.pdf"><img src="site/assets/demos/demo-changelog.png" alt="更新日誌"></a>
    <br><b>更新日誌</b> · 英文
    <br><sub>Mole v1.7.1 發布說明</sub>
  </td>
  <td align="center" width="25%">
    <a href="site/assets/demos/demo-kaku.pdf"><img src="site/assets/demos/demo-kaku.png" alt="Kaku 作品集"></a>
    <br><b>作品集</b> · 日本語
    <br><sub>Kaku 終端機作品集，7 頁</sub>
  </td>
</tr>
</table>

## 安裝

**Claude Code、Codex、Cursor 與其他 Agent**

```bash
npx skills add tw93/kami -a claude-code codex cursor -g -y
```

或者直接告訴 Agent 自動安裝：
> 請閱讀 https://kami.tw93.fun/llms.txt 為我安裝 Kami

技能會統一存放在 `~/.agents/skills` 共享目錄中。Claude Code 自動建立符號連結；Codex、Cursor 以及所有支援該規範的 Agent 會自動將其識別為 `/kami`。後續透過 `npx skills update -g -y` 即可更新。

**Host Plugin 外掛安裝**（若偏好平台原生指令，命名空間為 `/kami:kami`；要求 Claude Code v2.1.142 或更高版本）：

```bash
# Claude Code（升級指令：claude plugin update kami）
/plugin marketplace add tw93/kami
/plugin install kami@kami

# Codex（升級指令：codex plugin marketplace upgrade kami，然後 codex plugin add kami@kami）
codex plugin marketplace add tw93/kami
codex plugin add kami@kami
```

**Claude Desktop**：從 GitHub Releases 下載正式打包的 [kami.zip](https://github.com/tw93/kami/releases/latest/download/kami.zip)（請勿下載原始碼 ZIP），開啟 設定 > Skills > "+" > Create skill 上傳即可。後續升級點擊卡片上的 "..." 選擇 Replace 替換為最新包。

大型中文字型不隨發行包打包：`skills/kami/scripts/ensure-fonts.sh` 會自動檢測並將缺失字型安裝至本機系統字型目錄中；在本機儲存庫開發時，指令碼會將字型複製進技能目錄，範本會優先讀取本機字型，未安裝時才回退至 jsDelivr CDN。

Kami 每天至多執行一次靜默版本檢查，並在發現新版本時在對話中輕巧提醒。檢查只會讀取本機 XDG 快取標記與 GitHub 公開 Release 資訊，絕不傳送任何使用者文件與對話內容；離線或無快取目錄時自動靜默跳過。

## 使用

無需記憶斜線指令，用日常自然語言向 Agent 提出需求即可自動觸發。

### 支援語言

英文與中文支援最完整；日文與韓文透過專屬字型回退與版式微調支援，並在交付前逐份檢查效果：

| 語言 | 支援程度 | 預設襯線字型 |
| :--- | :--- | :--- |
| **English** | 完整支援 | Charter |
| **中文**（簡體 / 繁體） | 完整支援 | TsangerJinKai02（倉耳今楷） |
| **日本語** | 字型回退與逐份檢查 | YuMincho（游明朝） |
| **한국어** | 字型回退與逐份檢查 | Source Han Serif K（思源宋體 韓文） |

各語言提示詞範例：

- 中文：`幫我做一份一頁紙` / `幫我排版一份長文件` / `幫我寫一封正式信件` / `幫我做一份作品集` / `幫我做一份履歷` / `幫我做一套演講投影片` / `幫我做一份 Markdown 風格的簡報稿` / `幫我做一個產品落地頁`
- English: `make a one-pager for my startup` / `turn this research into a long doc` / `write a formal letter` / `make a portfolio of my projects` / `build me a resume` / `design a slide deck for my talk` / `make this talk as a Marp deck` / `build a landing page for my app`
- 日本語: `スタートアップ向けの一枚資料を作って` / `この調査を長文レポートに整えて` / `正式な依頼文を作って` / `プロジェクト作品集を作って` / `履歴書を作って` / `登壇用スライドを作って` / `Marp で登壇スライドを作って` / `アプリのランディングページを作って`
- 한국어: `스타트업 원페이저를 만들어줘` / `이 리서치를 장문 문서로 정리해줘` / `정식 레터를 작성해줘` / `프로젝트 포트폴리오를 만들어줘` / `이력서를 만들어줘` / `발표용 슬라이드를 만들어줘` / `Marp 슬라이드로 만들어줘` / `앱 랜딩 페이지를 만들어줘`

**個人品牌偏好設定**（可選）

建立 `~/.config/kami/brand.md` 儲存個人偏好、品牌主色、預設習慣與寫作語氣。完整範例參見 [brand.example.md](skills/kami/references/brand.example.md)。

頂部為 YAML 格式欄位（姓名、職位、信箱、品牌色、語言、紙張尺寸、文風），內文為自由格式 Markdown。當使用者未指定排版參數時，Kami 會優先採用設定中的偏好；使用者在對話中的明確指令始終保持最高優先級。

## 設計規範

預設採用溫暖的米色底（`#f5f4ed`）、油墨藍強調色（`#1B365D`）與經典襯線字型。範本依靠字級階層與留白節奏區分標題、內文與標註。

- **範本體系**：8 款出版級文件範本：一頁紙、長文件、信件、作品集、履歷、簡報、研報與更新日誌，以及配套的多語言落地頁系統（支援 EN、CN、KO）。
- **專業圖表**：18 種行內原生 SVG 圖表，包含研報級系統架構圖。循序圖、類別圖與實體關係圖可直接寫 Mermaid 原始碼：由 [beautiful-mermaid](https://github.com/lukilabs/beautiful-mermaid) 渲染為 SVG，並透過 `skills/kami/scripts/mermaid_normalize.py` 自動調整為 Kami 墨藍配色，無需本機安裝 Node 環境。
- **簡報**：支援 3 條交付路徑：預設 WeasyPrint HTML 轉高精度 PDF；按需透過 python-pptx 匯出可二次編輯的 PPTX；以及位於 `skills/kami/assets/templates/marp/` 的 Markdown 優先 Marp 方案。
- **程式碼高亮**：安裝 Pygments 後自動支援語法著色；未安裝時依然可正常產生純黑灰程式碼區塊。
- **嚴格檢查**：JSON Schema 先行校驗輸入資料完整性；覆蓋率檢測防止關鍵內容在排版時遺漏；交付前透過頁面圖片逐頁檢驗節奏、孤行與排版平衡。
- **本機 MCP 服務**：內建零外部依賴的 MCP 伺服器（`skills/kami/scripts/mcp_server.py`），提供環境自檢、渲染、檢查與截圖工具，任何相容 MCP 的 Agent 均可直接呼叫。
- **白底列印模式**：淺米底色是螢幕閱讀的最佳預設；同時支援一鍵白底模式，適合家庭與辦公室印表機列印，依然保留卡片與表格的溫暖底色。完整配方見 [production.md](skills/kami/references/production.md)。

**字型約定**：每份文件全頁僅使用單一襯線字型。中文：倉耳今楷（TsangerJinKai02）；日文：游明朝（YuMincho）；韓文：思源宋體（Source Han Serif K）；英文：Charter。詳見 [授權條款](#授權條款)。

完整設計手冊：[design.md](skills/kami/references/design.md)。快速備忘單：[CHEATSHEET.md](skills/kami/CHEATSHEET.md)。

## 不止於文件

同一套排版規則不僅能輸出印刷級文件，也同樣適用於產品官網搭建與 AI 繪圖模型的提示詞引導。

<table>
<tr>
  <td align="center" width="25%" valign="top">
    <a href="https://kami.tw93.fun"><img src="site/assets/showcase/kami-landing.png" alt="Kami 落地頁" height="150"></a>
    <br><b>Kami</b> · 產品落地頁
    <br><sub>設計系統官方網站</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <a href="https://mole.fit"><img src="site/assets/showcase/mole-landing.png" alt="Mole 落地頁" height="150"></a>
    <br><b>Mole</b> · 產品落地頁
    <br><sub>macOS 系統清理工具</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-spatialvla.png" alt="SpatialVLA 架構重繪" height="150">
    <br><b>架構圖重繪</b> · 英文
    <br><sub>SpatialVLA 論文圖 1 重構</sub>
  </td>
  <td align="center" width="25%" valign="top">
    <img src="site/assets/illustrations/travel-tesla-optimus.png" alt="Tesla Optimus 專利圖" height="150">
    <br><b>專利圖排版</b> · 中文
    <br><sub>Tesla Optimus 專利圖一覽</sub>
  </td>
</tr>
</table>

落地頁範本支援直接部署為輕快的多語言官網。在支援圖像生成的用戶端中，Kami 會呼叫繪圖能力；在純文字模型中，Kami 也會給出完整的構圖提示詞供繪圖模型使用：

```text
Redraw this as a clean editorial diagram. Background: warm parchment (#f5f4ed), never pure white. One accent only, ink blue (#1B365D); everything else in warm gray with a yellow-brown undertone, no other colors. Thin single-line geometric strokes and simple flat icons. No gradients, no drop shadows, no 3D. Labels in a serif typeface. Generous whitespace, calm and composed, like a figure in a well-typeset report.
```

<sub>上圖由 ChatGPT Images 單次生成完成，無任何人工後期修圖。Kami 負責給出精細要求，繪圖模型負責落筆繪製。</sub>

## 背景

我喜歡美股投資，經常讓 Claude 寫研究報告。每次出來的成果都是同一種預設文件的樣子：灰撲撲的，結構不清晰，格式老舊，換個對話就換一套排版，沒有一份讓人想讀下去。於是我開始一條一條地調字型、配色、間距，直到報告變成一份自己真正願意閱讀的頁面。

後來要去進行《你不知道的 Agent：原理、架構與工程實踐》分享，手邊已有文件，不想再做 PPT，就用 Claude Design 按自己的設計風格來排版，反覆調了許多輪，最後慢慢滿意了。再後來加入 SVG 圖表，統一配色與間距，逐漸用在常寫的各種文件上，再把範本與規則整理成了現在的 Kami。

## 支持作者

- 購買我做的 Mac 清理工具 [Mole for Mac](https://mole.fit)，是對我最直接的支持。
- 如果 Kami 幫到了你，歡迎給它一個 Star，[在 Twitter 分享](https://twitter.com/intent/tweet?url=https://github.com/tw93/kami&text=Kami%20-%20A%20quiet%20design%20system%20for%20professional%20documents.)，或提交 Issue 和 PR。
- 我有兩隻貓：湯圓、可樂。如果 Kami 讓你順手，歡迎<a href="https://cats.tw93.fun?name=Kami" target="_blank">請她們吃罐頭 🥩</a>。

<details>
<summary>這些可愛的朋友已經請過啦 🐱</summary>
<br/>
<a href="https://cats.tw93.fun?name=Kami"><img src="https://cdn.jsdelivr.net/gh/tw93/sponsors@main/assets/sponsors.svg" width="1000" loading="lazy" /></a>
</details>

## 授權條款

Kami 核心程式碼與範本遵循 MIT 授權條款開源，歡迎自由使用與貢獻。

**字型授權**：倉耳今楷（TsangerJinKai02）個人非商用免費，商用授權請洽 [tsanger.cn](https://tsanger.cn)；Charter、游明朝（YuMincho）、思源宋體（Source Han Serif K）遵循 OFL 開源授權條款，相關 CJK 回退字型為系統自帶或開源授權。
