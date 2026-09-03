# travel-plan

給同行團員線上瀏覽的旅遊行程表，單檔 HTML（樣式與 JS 內嵌，無外部相依）。
用 GitHub Pages 發布：Settings → Pages → Deploy from a branch → `main` → `/ (root)`。

## 行程

| 行程 | 日期 | 路徑 |
|---|---|---|
| 釜山 4 天 3 夜 | 2026/10/01–10/04 | [`busan-2026-10/`](busan-2026-10/) |

## 說明

- 頁面內容已脫敏：不寫團員姓名、飯店門牌、療程細節。**站台是公開的**，加什麼進去就等於公開什麼。
- 每頁帶 `noindex,nofollow`，根目錄有 `robots.txt`，減少被搜尋引擎收錄。擋得住爬蟲，擋不住拿到連結的人。
- `.nojekyll` 讓 GitHub Pages 原樣輸出，不跑 Jekyll。
- 出發前一週要重對一次門票價格與店家營業時間，改完記得更新頁尾的「最後更新」。
