# option/

期權子站，線上位址：<https://ongtsinging24.github.io/option/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `greeks_dealer_gamma_lesson.html` | 期權教學講義（原 `option_teach_Phase1-2.1.html`）：卷首縮寫與術語表 →權利金組成 → Black-Scholes 直覺 → Delta/Gamma/Vega → Dealer 對沖行為 → 2.2 GEX 的組裝 → 2.3 GEX 曲線與 ZG → 2.4 DN/DR/GR 機械效應 → 2.5 Vanna/Charm → Phase 3 CW/PW、KGS/LVP/HVP/HW、Pin 與 OE、Skew → Phase 4 決策表、150 股情境的四結構到期損益、自檢清單；玩具鏈數字皆 BS 實算；Chart.js CDN | 引用 `../assets/style.css` |
| `fn_risk_pivot_ref.html` | ROMA_SYS 參考卡：FN Risk Pivot vs 傳統 TA S/R | 內嵌 `<style>`，深色獨立主題，不吃站台共用樣式 |
| `put_insurance_lesson.html` | 期權入門：80 put 在股價 90 時算不算保險——自付額/保費比喻、價外 put 的內含 vs 時間價值、履約價取捨；含 Black-Scholes 互動計算器與到期損益圖（Chart.js CDN） | 內嵌 `<style>`，淺色獨立主題，不吃站台共用樣式 |
| `gamma_levels_cross_day_lesson.html` | 參考卡：跨日水位表怎麼讀——HW/KGS/PW/CW/DR/GR/IVR/SkewR 四組判讀順序、機械效應與單場噪音、三個五日實例（範例一、SOXX、KLAC）走讀與自檢清單 | 內嵌 `<style>`，淺/深色自動切換，不吃站台共用樣式 |
| `flowpatrol_reading_lesson.html` | 講義：SpotGamma FlowPatrol 怎麼讀——買賣軸（greek 優先、BTO/STO 不可信）、開平倉軸（只有 ΔOI 能定、留倉率、逐 strike OI ladder 補 ΔOI）、聚合層（只看 p9）、AI 文字段的用法；AMZN 10-20 實例走讀、前瞻力實測、官方揭露管道與自檢清單 | 內嵌 `<style>`，淺/深色自動切換，不吃站台共用樣式 |
| `field_notes_price_alerts.html` | 實戰經驗：價格警示與期權水位——推播不是訊號（以 ET 收盤判定、跳空不觸發）、VIX 單日大跌拆解、警示汰換準則、跌破 PW＝超賣該買凸性（機制＋自行回測＋適用邊界）、觸發後檢查順序與自檢清單 | 內嵌 `<style>`（同 flowpatrol 版型），淺/深色自動切換，不吃站台共用樣式 |
| `theta_carry_cost_lesson.html` | 實戰經驗：Long Call 的持有成本——盤前損益估算（Δ 線性 vs BS 全重估、Γ 貢獻、基準價陷阱）、θ 逐部位細算、put-call parity 把 θ 拆成利息＋保險、三把年化量尺與融資買股比較；虛構示範組合（數字皆 BS 實算）＋互動計算器 | 內嵌 `<style>`（同 flowpatrol 版型），淺/深色自動切換，不吃站台共用樣式 |

## 注意

- `put_insurance_lesson.html` 依賴外部 CDN：Chart.js（cdnjs）與 Google Fonts；離線開啟會退化成無圖表、系統字。
- 新增文章時要同步改三處：本目錄 `index.html`（卡片 + `count`）、站台首頁 `../index.html`（卡片 + `count`）、以及本表。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。
