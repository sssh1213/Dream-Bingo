# Dream Bingo 發布包

這個資料夾是 Dream Bingo 的靜態發布版本。

主要檔案：

- `index.html`：網站首頁，直接上傳即可瀏覽
- `FIREBASE_SETUP.md`：正式收學生資料的 Firebase 設定說明
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

這版是單一 HTML 檔，已預留 Firebase Firestore 收資料功能。
填入 Firebase 設定後，學生送出的資料會寫入 `bingoSubmissions`。
