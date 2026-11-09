# OPAT 前端（GitHub Pages）

Release R64（v2.50）Build `02f142f79ecaa8aa`

這個資料夾就是整個網頁。它不含任何資料、名單或密鑰；資料全在院方的 Google 試算表（控制台），由 Apps Script 後端讀寫。

## 一次性設定（約 10 分鐘）

1. 在 GitHub 建立**公開**儲存庫，名稱 `opat`（網址會是 `https://<你的帳號>.github.io/opat/`）。
2. 把本資料夾全部檔案上傳到儲存庫根目錄（含 `.nojekyll`）。
3. 在 GitHub 網頁上編輯 `config.js`：貼上控制台選單「產生前端設定檔內容（config.js）」顯示的整段內容。
4. Settings → Pages → Build and deployment：Source 選 **Deploy from a branch**，Branch 選 **main**、資料夾 **/(root)** → Save。
   GitHub 說明最多約 10 分鐘生效。
5. 開啟網址 → 按「連線測試」→ 顯示「後端連線正常」後，以 Google 帳號登入。

## 更新版本

用新的部署包之 `index.html` 取代舊檔即可（`config.js` 不用動）。

## 安全說明

- GitHub Pages 一律是公開網頁；本頁只有程式，沒有任何資料。後端網址與 Google 用戶端 ID 屬公開資訊，安全不依賴它們保密。
- 登入權杖只存在瀏覽器分頁（sessionStorage），關閉分頁即清除；閒置與有效時數由後端控管（控制台可調）。
- 內容安全政策（CSP）只允許本站、Google 登入與 Apps Script 後端。
