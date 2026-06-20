# Firebase 正式版設定

目前版本已完成：

- 學生 Email／密碼註冊與登入
- 老師 Google 白名單登入
- 學生私人 Bingo 資料
- 登入後可查看的公開排行榜摘要
- 正式 Firestore 安全規則

## Authentication

Firebase Authentication 必須啟用：

1. Email／密碼
2. Google

老師白名單帳號：

`sssh1213@sssh.tyc.edu.tw`

## Firestore

資料位置：

- `groups/{group}/settings/public`
- `groups/{group}/bingoSubmissions/{學生 UID}`
- `groups/{group}/leaderboard/{學生 UID}`

學生只能讀寫自己的 `bingoSubmissions` 文件。
排行榜只包含姓名、班級、完成率、XP 與 Bingo 數。
中心目標、公告、群組重置及刪除僅限老師。

## 安全規則

規則保存在 `firestore.rules`，並已發布到 Firebase。
若未來修改規則，請將該檔案內容重新發布到 Firestore「規則」頁。
