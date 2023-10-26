# search_wechat_key
## 本程序用来搜索微信数据库的密钥key信息   
** 不用用于非法用途！ **  
** 不用用于非法用途！ **  
** 不用用于非法用途！ **  
  
原理是打开微信进程句柄，遍历微信内存空间。   
找到关键字，比如android或者iphone字样，返回这个地址。   
从这个地址开始往前逐步搜，每次读32字节，然后判断读取的是不是微信sqlite的数据库密钥。   
密钥找到后，可以为后续读取微信聊天记录做准备。   

## 用法类似：
```
C:\Users\Win10\Desktop\pc_wechat\dist>search_wecaht_key.exe  
2023-10-26 13:52:01,281 - search_wecaht_key.py- INFO - wechat version：3.9.7.28  
2023-10-26 13:52:01,583 - search_wecaht_key.py- INFO - db_file:C:\Users\Win10\Documents\WeChat Files\wxid_cpyn7pe119rxxx\Msg\Misc.db  
2023-10-26 13:52:01,699 - search_wecaht_key.py- INFO - phone_addr:713817B8  
2023-10-26 13:52:01,888 - search_wecaht_key.py- INFO - found key pointer addr:71381744, key_addr:7417E70  
2023-10-26 13:52:01,888 - search_wecaht_key.py- INFO - key:eb204727b80a44dea374ee92df27fb06ef7218098ae7473bafc695b9b5a9xxxx  
2023-10-26 13:52:01,888 - search_wecaht_key.py- INFO - eb204727b80a44dea374ee92df27fb06ef7218098ae7473bafc695b9b5a9xxxx  
 ```
