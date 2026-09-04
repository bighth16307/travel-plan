# travel-plan

給同行團員線上瀏覽的旅遊行程表，單檔 HTML（樣式與 JS 內嵌，無外部相依）。
用 GitHub Pages 發布：Settings → Pages → Deploy from a branch → `main` → `/ (root)`。

## 行程

| 行程 | 日期 | 路徑 |
|---|---|---|
| 釜山 4 天 3 夜（圖文版） | 2026/10/01–10/04 | [`busan-2026-10/photo.html`](busan-2026-10/photo.html) |
| 釜山 4 天 3 夜（完整行程） | 2026/10/01–10/04 | [`busan-2026-10/`](busan-2026-10/) |

兩版是同一趟行程的兩種用途：**圖文版**傳給團員產生期待，**完整行程**出發當天現場查。
根目錄 `index.html` 一張卡兩個入口，兩版內頁互相有切換連結。
文字版吃 `#d1`–`#d4`、`#kit` 錨點直接開對應分頁，圖文版每天結尾就是靠這個連過去，
**改動分頁 id 會讓那些連結一起壞掉**。

## 說明

- 頁面內容已脫敏：不寫團員姓名、飯店門牌、療程細節。**站台是公開的**，加什麼進去就等於公開什麼。
- 每頁帶 `noindex,nofollow`，根目錄有 `robots.txt`，減少被搜尋引擎收錄。擋得住爬蟲，擋不住拿到連結的人。
- `.nojekyll` 讓 GitHub Pages 原樣輸出，不跑 Jekyll。
- 出發前一週要重對一次門票價格與店家營業時間，改完記得更新頁尾的「最後更新」。

## 外部連結的做法

- **地圖**一律用 Google Maps 搜尋連結（`maps/search/?api=1&query=<韓文關鍵字>`，關鍵字要百分比編碼）。不用 Naver／Kakao 深連結，因為沒裝 app 的人會看到全韓文頁或被丟到商店頁；代價是 Google Maps 在韓國不能導航，頁面裡有一張卡片說明這件事。
- **票務**優先連 KKday／Klook 的搜尋頁而非單一商品頁，商品下架不會讓連結壞掉。唯一的例外是 Klook 的 SPA LAND 商品頁。
- KKday、Klook、樂天百貨／免稅店的站台會擋 bot（curl 403、headless 吃 Cloudflare 挑戰），**改連結後沒辦法用指令驗證**，只能靠搜尋引擎索引過的 URL，或自己用瀏覽器點一次。
- App 連結用 App Store 數字 ID（已確認台灣區都有上架）配 Google Play 搜尋連結。

## 圖片

`busan-2026-10/img/` 放 Wikimedia Commons 的 CC 授權照片，`credits.json` 記錄每張的來源、作者、授權與原始頁面，**頁面上必須標作者與授權**（目前用的都是 CC BY / CC BY-SA / Public domain，沒有 NC 或 ND）。

- 下載後一律用 `sips -Z 1100` 壓到 1100px 寬再進 repo。
- **每張都要親眼看過再用**：檔名對不代表內容對。實際踩過的例子——`Haedong Yonggungsa Temple 20200522 001.jpg` 是入口步道沒有海，`Hanu 5.jpg` 是一頭活牛不是烤肉。
- 找不到合法好圖的地點（滑車、李載茂披薩、Centum City、田浦咖啡街）走 inline SVG，不要為了湊圖去用來路不明的照片。
