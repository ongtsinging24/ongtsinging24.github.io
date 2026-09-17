# command_set/

命令列子站，線上位址：<https://ongtsinging24.github.io/command_set/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `shell_find_rm_ref.html` | Shell 參考卡：`find` / `rm` 批次刪檔的三種正確寫法——glob 何時由 shell 展開、`--` end-of-options 的必要性、`-exec +` vs `rm -- *glob` vs `xargs -0` 的取捨與實測紀錄 | 內嵌 `<style>`，淺色獨立主題，不吃站台共用樣式 |

## 注意

- 新增文章時要同步改三處：本目錄 `index.html`（卡片 + `count`）、站台首頁 `../index.html`（卡片 + `count`）、以及本表。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。
