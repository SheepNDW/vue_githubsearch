# GitHub 搜索案例

![image](https://raw.githubusercontent.com/SheepNDW/vue_githubsearch/master/sampleGif/githubsearch.gif)

## 概要

使用`"https://api.github.com/search/users?q=xxx"`API 來寫一個搜索 GitHub 使用者的小案例

## 使用技術

1. 拆分靜態頁面分為兩個組件(Search,List)實現組件化開發 並從 index 中引入 bootstrap
2. 用 v-model 來雙向綁定關鍵字(keyWord), 並給搜尋按鈕綁定一個點擊事件
3. 在 Search 組件裡引入 axios 並在點擊事件的 methods 中發送一個 get 請求來獲取用戶資料
4. 為了將資料傳遞給兄弟組件(List), 使用全局事件總線（\$bus）來完成組件間的通信
5. 在 List 中把接收到的數據用 v-for 的方式將資料呈現在頁面上

### 畫面優化

加入起始頁面歡迎語､ 讀取提示､ 錯誤訊息提示 並以 v-show 來決定什麼時候顯示
