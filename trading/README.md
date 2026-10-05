# trading/

交易工具子站，線上位址：<https://ongtsinging24.github.io/trading/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `earnings_calendar/earnings_calendar_q4_2026.html` | 2026 Q3 財報季日曆（10–12 月）：美股科技 / 半導體財報日程、每週家數分布、BMO / AMC、已確認 vs 估計、OpEx / FOMC / 休市事件；可依重點關注 / ETF 重權重篩選 | 內嵌 `<style>`，獨立主題（含深色模式） |

## 注意

- 新增文章時要同步改三處：本目錄 `index.html`（卡片 + `count`）、站台首頁 `../index.html`（卡片 + `count`）、以及本表。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。標色用「重點關注」，不要寫「持倉」。
