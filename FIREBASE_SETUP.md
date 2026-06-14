# Firebase 收資料設定

這版 Dream Bingo 已經有 Firestore 收資料程式。
你只需要建立 Firebase 專案，然後把網站設定貼到 `index.html`。

## 1. 建立 Firebase 專案

1. 到 Firebase Console
2. 建立新專案
3. 進入專案後，新增 Web App
4. Firebase 會給你一段 `firebaseConfig`

## 2. 貼上 firebaseConfig

打開 `index.html`，找到這段：

```js
const firebaseConfig = {
  apiKey: "",
  authDomain: "",
  projectId: "",
  storageBucket: "",
  messagingSenderId: "",
  appId: ""
};
```

把 Firebase 給你的值貼進去。

## 3. 建立 Firestore

1. 在 Firebase Console 左側選 Firestore Database
2. 建立資料庫
3. 測試期間可以先用測試模式
4. 系統會寫入 collection：`bingoSubmissions`

## 4. 測試

學生送出後，Firestore 裡會出現：

- 姓名
- 班級
- 座號
- Email
- 25 格目標
- XP
- 完成狀態
- 完成率
- Bingo 數

## 重要提醒

測試模式適合短期測試。
正式給學生長期使用前，建議再加登入或安全規則，避免外人修改資料。
