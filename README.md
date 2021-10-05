# GitHub 搜索案例

## 概要

```
使用"https://api.github.com/search/users?q=xxx"的API來寫一個搜索GitHub使用者的小案例
```

### 使用技術

```
1. 拆分靜態頁面分為兩個組件(Search,List)實現組件化開發 並從index中引入bootstrap
2. 用v-model來雙向綁定關鍵字(keyWord), 並給搜尋按鈕綁定一個點擊事件
3. 在Search組件裡引入axios並在點擊事件的methods中發送一個get請求來獲取用戶資料
4. 為了將資料傳遞給兄弟組件(List), 使用全局事件總線（$bus）來完成組件間的通信
5. 在List中把接收到的數據用v-for的方式將資料呈現在頁面上
```

### 畫面優化

```
加入起始頁面歡迎語､ 讀取提示､ 錯誤訊息提示 並以v-show來決定什麼時候顯示

```
