# chatbot-Internet-novel-Auto-update  
## chatbot製作動機 ##
相信不少同學有過追更連載中小說的經歷，壹天一章或兩章，有的追了壹年，兩年，三年，五年，甚至十年，追書，是壹種信仰，也可能是這本小說已經融入我們的生活。任何一個人在追更小說之餘都有自己的學習生活，在此同時，每天頻繁的打開網站或者小說app查看連載中小說的更新狀態，除了會讓自己無法專心工作之外，遇到小說沒按時更新的時候更是難免失望。所以趁著這次課程的期末作業，就想著能不能自己做一個小說追更chatbot，來替我監控小說的更新狀態，並且在小說更新的第一時間將最新內容推送到我的手機上。
## 為什麼選擇wechat？ ##  
1.服務完全免費  
2.客戶端和服務端對平台依賴度低，方便移植  
3.wechat公眾號具有模板消息功能，使用手機就可以隨時進行部分內容的編輯  
4.提供專門的測試平台，無需註冊可以即連即用:  
https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login  
5.爬蟲程式fork的大部分為盜版網站，使用wechat推廣中不容易出現嚴重版權糾紛  
## 架構圖，核心組件 ##  
爬蟲程序：定時循環爬取小說源站，監控小說更新。  
微信token服務器：統一獲取並保存微信公眾號的access token，供微信公眾號程序使用。  
微信公眾號服務程序：接收爬蟲程序的更新章節推送，並將更新通過微信消息發送給用戶。

![image](https://github.com/kaobeia/chatbot-Internet-novel-Auto-update/blob/main/frame1.png)
![image](https://github.com/kaobeia/chatbot-Internet-novel-Auto-update/blob/main/frame2.png)
