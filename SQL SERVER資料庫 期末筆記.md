### SQL Server

前言：

SQL Server 有一組內定的 **<mark>系統資料型別</mark>** 來定義SQL Server所能使用的所有資料型別​

按ctrl+點擊(註圖)即可跳到該圖

#### 一、系統內定資料型別

1.「精確數值」資料型別：

- 整數型態
  
  - 只可儲存**整數**的資料，包括<mark>正</mark>整數、<mark>零</mark>與<mark>負</mark>整數。[​(註圖1)](https://media.discordapp.net/attachments/1293405178409779201/1311197947589038110/image.png?ex=6747fbbf&is=6746aa3f&hm=b92fbe227b5519cf5a26845b326a3557c510428fc80123562bc65e36bd0aa0f4&=&format=webp&quality=lossless&width=787&height=333)

- 精確小數：具有固定**有效位數**和**小數位數**的資料型態
  
  - 舉例：168.33、1968.00
  
  - 用來定義整數及小數位數的個數，定義方式numeric(p，s)

- 貨幣型態







2.

3.近似數值(浮點數)：不精確小數資料

4.日期和間：資料精確度分為六種：

。datetime、smalldatetime問題，如下：

- 日期與時間合併再一起：容易造成資料篩選上的錯誤

- 時間部份有效位數：datetime秒數的小數點位置會四捨五入為 `.003`或 `.007` 秒的`.000`遞增

![](https://cdn.discordapp.com/attachments/1293405178409779201/1311160880993665084/20241127_104343.jpg?ex=6747d93a&is=674687ba&hm=02900cd99ee3dbf10e779befc89567216c6a57f57a6ea480ae4fbf90089fb991&=)

5.字元字串：「固定長度」、「可變長度」：

。char(n)屬於**固定長度**，一旦宣告n的值之後，他所佔的空間大小就固定，ex：宣告char(10)，則char(10)= 'abc'，則就會佔用10字元大小。

。varchar(n)屬於「可變長度」

。
