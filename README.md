# Dream Bingo 發布包

這個資料夾是 Dream Bingo 的靜態發布版本。

主要檔案：

- `index.html`：網站首頁，直接上傳即可瀏覽
- `firebase.json`：Firebase Hosting 設定
- `vercel.json`：Vercel 靜態網站設定

## 最簡單發布方式

### GitHub Pages

1. 建立一個新的 GitHub repository。
2. 上傳這個資料夾內的所有檔案。
3. 到 repository 的 Settings → Pages。
4. Source 選 `Deploy from a branch`。
5. Branch 選 `main`，資料夾選 `/root`。
6. 儲存後等待 GitHub 產生網址。

### Vercel

1. 到 Vercel 新增專案。
2. 匯入放了這些檔案的 GitHub repository。
3. Framework Preset 選 `Other`。
4. Build Command 留空。
5. Output Directory 留空或填 `.`。
6. Deploy。

### Firebase Hosting

1. 在 Firebase 建立專案。
2. 在這個資料夾執行 `firebase deploy`。
3. 如果第一次使用 Firebase CLI，先執行 `firebase login`。

## 備註

這版是單一 HTML 檔，適合先讓學生或老師用手機測試流程。
如果之後要加入登入、學生資料同步、教師後台資料庫，再發布完整 Next.js + Firebase 版本會更合適。
