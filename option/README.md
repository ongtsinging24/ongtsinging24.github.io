# option/

期權子站，線上位址：<https://ongtsinging24.github.io/option/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `option_teach_Phase1-2.1.html` | 期權教學講義 Phase 1–2.1：權利金組成 → Black-Scholes 直覺 → Delta/Gamma/Vega → Dealer 對沖行為 | 引用 `../assets/style.css` |
| `fn_risk_pivot_ref.html` | ROMA_SYS 參考卡：FN Risk Pivot vs 傳統 TA S/R | 內嵌 `<style>`，深色獨立主題，不吃站台共用樣式 |
| `put_insurance_lesson.html` | 期權入門：80 put 在股價 90 時算不算保險——自付額/保費比喻、價外 put 的內含 vs 時間價值、履約價取捨；含 Black-Scholes 互動計算器與到期損益圖（Chart.js CDN） | 內嵌 `<style>`，淺色獨立主題，不吃站台共用樣式 |

## 注意

- `put_insurance_lesson.html` 依賴外部 CDN：Chart.js（cdnjs）與 Google Fonts；離線開啟會退化成無圖表、系統字。
- 新增文章時要同步改三處：本目錄 `index.html`（卡片 + `count`）、站台首頁 `../index.html`（卡片 + `count`）、以及本表。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。
