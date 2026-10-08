# ongtsinging24.github.io

GitHub Pages 站台原始碼。線上位址：<https://ongtsinging24.github.io/>

## 拓樸

本目錄是 `ongtradingsys` 底下的**巢狀獨立 repo**（非 submodule），父 repo 已用 `.gitignore` 忽略 `webpage/`。

| Remote | 位址 |
| --- | --- |
| `GHRemote` | https://github.com/ongtsinging24/ongtsinging24.github.io |
| `GODRemote` | `/mnt/e/GOOG_DESK/webpage_sync_dir/ongtsinging24.github.io.git`（bare，走 Google Drive 跨機同步） |

分支：`main`（Pages 從 `main` 根目錄建置）。

## 內容

| 目錄 | 說明 |
| --- | --- |
| `option/` | 期權分類頁，見 [`option/README.md`](option/README.md) |
| `command_set/` | 命令列分類頁，見 [`command_set/README.md`](command_set/README.md) |
| `trading/` | 交易工具分類頁（財報季日曆），見 [`trading/README.md`](trading/README.md) |
| `802.11_802.3/` | 網路分類頁（A-MSDU 接收處理：802.11→802.3 收包路徑） |
| `outdoor/` | 戶外技術分類頁（急流泳渡與救援） |

首頁 `index.html` 以卡片列表彙整各分類文章；新增/移除文章時，`index.html` 與各分類頁自己的 `index.html` 都要同步改（卡片 + `count`）。

## 發佈

```bash
git -C ~/ongtradingsys/webpage add -A
git -C ~/ongtradingsys/webpage commit -m "..."
git -C ~/ongtradingsys/webpage push GHRemote main
git -C ~/ongtradingsys/webpage push GODRemote main   # 跨機備份，非必要
```

推上去後 Pages 約 1 分鐘內重建。**不納入 `gh_sync.sh` 自動流程，手動 push。**

## 注意

- 根目錄有 `.nojekyll` → Pages 不跑 Jekyll，純靜態原樣送出。要改用 Jekyll 就把它刪掉。
- ⚠️ **此 repo 與站台皆為 public**。任何持倉、策略、券商資料都不要放進來。
