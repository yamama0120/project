new project
--
小農吉米_農產品訂購管理系統!!! #吉米小舖
--
>for賣家更方便&長輩們不要在群組訂餐了!!  
>先記錄下想法,必要功能,**知識**


#### database schema

>customer(**customer_id**,name,cellphone)  
>goods(**goods_id**,items,stock,)  
>trade(**trade_id**,date,customer_id,goods_id,quantity,Receive,Pick_up_time)  

#### 前端UI

1. 賣家相關介紹(fb.line,phone,address,open_time)
2. 取貨時間,取貨方式
3. 商品卡片.介紹.數量 (商品卡片-分三類:蔬菜.水果.other自製農產品)
  
*  (訂購流程)
  4. 選數量後放購物車
  5. 確認訂單頁(1234+個人資料)----->按確認傳後端
  6. 後端確定後傳前端----->訂購成功頁(簡要1234+基本資料修改+訂單修改)


 #### 後端 
* 各種買家(個人資料,歷史訂單_增刪改)----------->買家ㄉ訂購資料_增刪改 須同步
* 各種買家(個人資料,歷史訂單_查)----------->調資料庫 須同步
  
* 賣家面(補貨,銷貨,銷毀異動_增刪改)----------->賣家ㄉ庫存數量_增刪改 須同步
* 賣家面(庫存,待出貨清單,銷貨明細,分析報表_查)----------->調資料庫 須同步

>重點在同步：訂購鍵/確認更改鍵按下時-->調閱商品即時數量，**確保可下訂+同時傳送訂購資料**至資料庫，異動庫存數量

其他附加功能：

1. dream：可以的話從line導來---->訂購---->再導回line(+簡要訂單訊息)
2. 搜尋功能
3. 



前端入門
---
>前端語言(html/CSS/js),瀏覽器
* [學習該如何開發Web](https://developer.mozilla.org/zh-TW/docs/Learn)
* [金魚都懂的網頁學習路徑懶人包](https://ithelp.ithome.com.tw/articles/10228708)
* [网站构建 初级教程](https://www.w3school.com.cn/web/index.asp)
* [初心者的前端路線學習指南](https://medium.com/i-am-mike/%E5%88%9D%E5%BF%83%E8%80%85%E7%9A%84%E5%89%8D%E7%AB%AF%E8%B7%AF%E7%B7%9A%E5%AD%B8%E7%BF%92%E6%8C%87%E5%8D%97-895de088257f)

後端入門
---
>伺服器（Web Server）與資料庫（Database）
>
