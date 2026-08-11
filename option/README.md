# option/

期權子站，線上位址：<https://ongtsinging24.github.io/option/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `option_teach_Phase1-2.1.html` | 期權教學講義 Phase 1–2.1：權利金組成 → Black-Scholes 直覺 → Delta/Gamma/Vega → Dealer 對沖行為 | 引用 `../assets/style.css` |
| `fn_risk_pivot_ref.html` | ROMA_SYS 參考卡：FN Risk Pivot vs 傳統 TA S/R | 內嵌 `<style>`，深色獨立主題，不吃站台共用樣式 |

## 注意

- ⚠️ `fn_risk_pivot_ref.html` 尚未加入 `index.html` 的卡片列表，站內導覽找不到、只能靠直接 URL 存取。若要公開收錄，需在 `index.html` 補一張卡並更新 `count`。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。
