# command_set/

命令列子站，線上位址：<https://ongtsinging24.github.io/command_set/>

站台拓樸與發佈流程見上層 [`../README.md`](../README.md)（同一個巢狀 repo，非獨立 repo）。

## 檔案

| 檔案 | 說明 | 樣式 |
| --- | --- | --- |
| `index.html` | 分類頁，卡片列表入口 | 引用 `../assets/style.css` |
| `shell_find_rm_ref.html` | Shell 參考卡：`find` / `rm` 批次刪檔的三種正確寫法——glob 何時由 shell 展開、`--` end-of-options 的必要性、`-exec +` vs `rm -- *glob` vs `xargs -0` 的取捨與實測紀錄 | 內嵌 `<style>`，淺色獨立主題，不吃站台共用樣式 |
| `shell_find_today_files_ref.html` | Shell 參考卡：列出目錄樹下「今天產生」的檔案——mtime / birth time / git 新增三種口徑的取捨；實測 GNU find 4.9.0 不支援 `-newerBt`，atomic rename 會讓 birth time 失真 | 內嵌 `<style>`，沿用 find/rm 卡的主題 |
| `gh_sync_guide_git_commands.html` | Git 參考卡：多機同步卡住（未提交＋落後）時的排解流程——本機髒檔 ∩ 遠端變更求交集，分人寫成果／機器產出／union 索引三類處理；禁 stash、`add -A`、reset --hard | 內嵌 `<style>`，沿用 find/rm 卡的主題 |
| `find-large-files-gitignore.html` | Shell 參考卡：搜尋大於 20MB 的檔案並排除於版控——`-size +20M` 為 MiB 且進位、`-printf '%P\n'` 寫入 `.gitignore`、`git rm --cached` 移出索引（不縮小歷史）、副檔名規則預防 | 內嵌 `<style>`，自帶淺/深色主題 |

## 注意

- 新增文章時要同步改三處：本目錄 `index.html`（卡片 + `count`）、站台首頁 `../index.html`（卡片 + `count`）、以及本表。
- 與上層 README 同樣的限制：**public repo**，不放持倉/策略/券商資料。
