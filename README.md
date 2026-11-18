# ongtsinging24.github.io

GitHub Pages 站台原始碼。線上位址：<https://ongtsinging24.github.io/>

## 拓樸

本目錄是 `ongtradingsys` 底下的**巢狀獨立 repo**（非 submodule），父 repo 已用 `.gitignore` 忽略 `webpage/`。

| Remote | 位址 |
| --- | --- |
| `GHRemote` | https://github.com/ongtsinging24/ongtsinging24.github.io |

分支：`main`（Pages 從 `main` 根目錄建置）。

## 內容

| 目錄 | 說明 |
| --- | --- |
| `option/` | 期權分類頁，見 [`option/README.md`](option/README.md) |
| `command_set/` | 命令列分類頁，見 [`command_set/README.md`](command_set/README.md) |
| `trading/` | 交易分類頁（財報季日曆、量價背離證偽講義、全球交易時段台北時間對照），見 [`trading/README.md`](trading/README.md) |
| `802.11_802.3/` | 網路分類頁（A-MSDU 接收處理：802.11→802.3 收包路徑） |
| `Microwave_Theory/` | 微波原理分類頁（主波諧波與互調、WiFi 封包為何算進 noise、發射端寬頻底噪與雜散、ADC 取樣混疊） |
| `IT/` | IT 分類頁（Microsoft Defender for Endpoint：EDR 與防毒差別、收集範圍、被動模式、關機 7043；公司電腦管控盤點：BeyondTrust PM、TrustView；CrowdStrike Falcon：RTR、隔離、Device Control、WSL 外掛） |
| `outdoor/` | 戶外分類頁（急流泳渡與救援、日月潭泳渡分析、八仙山與虎山健行分析、日月潭馬拉松賽前備忘錄與賽後分析、登山腿力與心肺訓練） |
| `health_care/` | 保健分類頁（Test X180 睪固酮增強劑成分拆解、B6 上限、補充成分證據排行） |
| `utility/` | 工具分類頁（Claude Code 使用筆記：statusline 設定與讀法、高用量成本成因與試算、session 協調機制） |
| `movies/` | 電影分類頁（《全面啟動》解析：夢境層級、柯柏對茉兒的植入、陀螺解讀） |

首頁 `index.html` 以卡片列表彙整各分類文章；新增/移除文章時，`index.html` 與各分類頁自己的 `index.html` 都要同步改（卡片 + `count`）。

## 新增文章：視覺風格（Visual Style）要與既有頁一致

新加入的 html 不可自帶另一套配色/版型（例：深色底＋金色的獨立樣式），一律對齊既有文章頁。樣板：`health_care/test-x180-testosterone-booster-analysis.html`、`movies/inception_analysis.html`。

| 項目 | 規格 |
| --- | --- |
| 配色 | 淺色紙感底（`--bg/--ink/--muted/--rule`），`--accent` 用該分類主色（見 `assets/style.css` 的 `.g-*`）；新分類先在 `style.css` 加色票＋`.g-<分類>` |
| 深色模式 | `@media (prefers-color-scheme:dark)` 以 `:root:not([data-theme="light"])` 守門，另加 `:root[data-theme="dark"]` 同組值 |
| 字型 | Noto Sans TC（內文）＋ JetBrains Mono（編號/縮寫/標記） |
| 版面 | `.wrap` 兩欄 grid：麵包屑 `nav.crumb` 橫跨 → 左 `nav.toc` sticky 目錄 → 右 `main`（max 78ch）；≤860px 收成單欄 |
| 麵包屑 | `<a href="../">筆記與教學</a> / <a href="./">分類</a> / 文章短名` |
| 標題 | `h1` ＋ `.lede` 導言；`h2` 前置 `<span class="n">N</span>`，0 號節為縮寫說明（`dl.abbr`） |
| 元件 | 提示框用 `.note-box` / `.warn` / `.ok` / `.bad-box`（左邊框＋淡底）；表格包 `.scroll` |
| 驗收 | 淺色、深色、手機寬（390px）各看一次，無橫向捲動 |

外部素材（如別處生成的 html）落地後先改樣式再上卡片，不要原樣上架。

## 發佈

```bash
git -C ~/ongtradingsys/webpage add -A
git -C ~/ongtradingsys/webpage commit -m "..."
git -C ~/ongtradingsys/webpage push GHRemote main
```

推上去後 Pages 約 1 分鐘內重建。**不納入 `gh_sync.sh` 自動流程，手動 push。**

## 注意

- 根目錄有 `.nojekyll` → Pages 不跑 Jekyll，純靜態原樣送出。要改用 Jekyll 就把它刪掉。
- ⚠️ **此 repo 與站台皆為 public**。任何持倉、策略、券商資料都不要放進來。
