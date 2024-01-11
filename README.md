小農吉米_農產品訂購管理系統!!! #吉米小舖
--
>for賣家更方便 & 長輩們不用在賴群訂餐了!  
>先記錄下想法,必要功能,**知識**


#### database schema(至少要有)

>customer(**customer_id**,name,cellphone)  
>goods(**goods_id**,items,stock,)  
>trade(**trade_id**,date,customer_id,goods_id,quantity,Receive,Pick_up_time)  

### 前端UI
(基本資訊)  

1. 賣家相關介紹(fb.line,phone,address,open_time)
2. 取貨時間,取貨方式
3. 商品卡片.介紹.數量 (商品卡片-分三類:蔬菜.水果.other自製農產品)
  
(訂購流程)  

  4. 選數量後放購物車
  5. 確認訂單頁(1234+個人資料)----->按確認傳後端
  6. 後端確定後傳前端----->訂購成功頁(簡要1234+基本資料修改+訂單修改)
  7. 訂單查詢  

(賣家操作)    

  8. 一頁式補貨介面-增刪改
  9. 出貨&預訂清單-確認
  10. 出貨&預訂清單-交易完成/取消
  11. 現場銷貨
  12. 交易紀錄-查.分析  

(訂單狀態)  
已送出.備貨完成.已取貨.訂單取消
  
 ### 後端操作(同步!!)

* 各種買家(個人資料,歷史訂單)
  >5.6.//**增刪改**---->資料庫(1.確認庫存夠嗎? 2.增刪改:異動庫存數量-*暫改* 3.訂單結果:已送出)----->**回傳結果+同時傳送訂購明細---->出貨資料FOR賣家**  
  >7.//**查**--------->資料庫(查)------>**回傳結果**

* 賣家面(補貨)
  >8.//**增刪改**------>資料庫(1.確認庫存是否有誤? 2.增刪改:異動庫存數量)----->**回傳結果**
  
* 賣家面(出貨&預訂清單)
  >9.// 出貨資料備貨確認--->資料庫(訂單結果:備貨完成)----->**回傳結果**  
  >10.//交易完成.取消---->資料庫(1.增刪改:異動庫存數量-*確認更改* 2.訂單結果:已取貨/訂單取消)----->**回傳結果**


* 賣家面(刪-賣出,銷毀) //未經由訂購系統的現場交易
  >11.//**刪改**------->資料庫(1.確認庫存夠嗎? 2.增刪改:異動庫存數量)----->**回傳結果** 


* 賣家面分析(庫存.銷貨明細-報表)
  >12.//**查**-------*按確認傳後端*------>資料庫(查)------>**回傳結果**



其他附加功能：  
1. dream：可以的話從line導來---->訂購---->再導回line(+簡要訂單訊息)
2. 搜尋功能
3. 



學習地圖
---
* 前端(瀏覽器)  [筆記](https://github.com/yamama0120/project/blob/main/forward.md)
1. html:建構網頁內容,賦予其含意.用途
2. CSS:塑造網站的特殊風格
3. RWD(串接):解決多種裝置顯示問題
4. JavaScrip:增加互動功能 函式庫-JQuery
5. 框架-vue/react  

* 後端(伺服器)
1. 精通至少一種語言及框架 (**1. java/Spring** 2. PHP/Laravel 3. JavaScript/Node.js 4. Python/Flask.Django 5. C#/ASP.NET) 6.Ruby
2. Java Restful API串接:解決'不同軟體互傳資料'的相容性
3. 基本的伺服器指令、網路知識、通訊協定(HTTP、TCP、IP、DNS、SMTP、SSH)
4. 資料庫(MySQL、PostgreSQL、Microsoft SQL Server、Oracle Database)

入門資源
---
**0.轉職觀念 架構順序**
* [胡立/學程式，不只是學程式](https://life.huli.tw/2018/10/29/learn-coding-9c572c2fb2/)
* [胡立/先別急著寫 leetcode](https://lidemy.com/p/alg101-leetcode)
* [胡立/程式導師實驗計畫第四期](https://github.com/Lidemy/mentor-program-4th)
* [從教學者的角度看無經驗轉職以及課程選擇](https://www.ptt.cc/bbs/Soft_Job/M.1546655647.A.807.html)

**1. 前端**
* [學習該如何開發Web](https://developer.mozilla.org/zh-TW/docs/Learn)
* [金魚都懂的網頁學習路徑懶人包](https://ithelp.ithome.com.tw/articles/10228708)
* [网站构建 初级教程](https://www.w3school.com.cn/web/index.asp)
* [初心者的前端路線學習指南](https://medium.com/i-am-mike/%E5%88%9D%E5%BF%83%E8%80%85%E7%9A%84%E5%89%8D%E7%AB%AF%E8%B7%AF%E7%B7%9A%E5%AD%B8%E7%BF%92%E6%8C%87%E5%8D%97-895de088257f)

**2. 後端**

* [java備忘筆記](https://yubin551.gitbook.io/java-note/)



