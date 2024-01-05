new project
--
小農吉米_農產品訂購管理系統!!!
==

#### database schema

>customer(**customer_id**,name,cellphone)  
>goods(**goods_id**,items,stock,)  
>trade(**trade_id**,date,customer_id,goods_id,quantity,Receive,Pick_up_time)  

#### 前端UI
* 介面
  1. 賣家相關介紹(fb.line,phone,address,open_time)
  2. 取貨時間,取貨方式
  3. 商品卡片.介紹.數量
  4. 購物車
  5. 確認訂單頁(1234+個人資料)
  6. 訂購成功頁(簡要1234+基本資料修改+訂單修改)

>dream：可以的話從line導來---->訂購---->再導回line(+簡要訂單訊息)
 #### 後端 
* 買家面(個人資料,歷史訂單_增刪改)----------->買家ㄉ訂購資料_增刪改 須同步
* 賣家面(補貨,銷貨,銷毀異動_增刪改)----------->賣家ㄉ庫存數量_增刪改 須同步
* 賣家面(庫存,待出貨清單,銷貨明細,分析報表_查)----------->調資料庫 須同步

>重點在同步：訂購鍵/確認更改鍵按下時-->調閱商品即時數量，**確保可下訂+同時傳送訂購資料**至資料庫，異動庫存數量

