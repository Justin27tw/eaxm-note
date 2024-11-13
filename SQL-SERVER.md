SQL-SERVER

#### 。認識資料庫系統：

。**資料庫管理系統DBMS**：是介於<u>應用程式</u>或<u>一般的查詢語言</u>和<u>資料庫</u>之間的操作介面。

。資料庫綱要：描述整個資料庫儲存資料的定義資料。

#### **小結**

- 一個資料庫系統中可以有多個資料庫， 每個資料庫都是經過整理的資料集合​

- 一般會將資料庫想像成是一個存放資料的容器(電子文件檔案櫃)，但其真實型態其實是一個個的電子檔案(file)​

- **資料庫管理系統**則是指<u>管理資料庫的軟體​</u>

- **應用程式**是指自行開發的使用者介面​

#### 。資料庫的類型：

- 階層式資料庫​ 
  
  =>階層式資料庫是採用樹狀的結構
  
  優點：資料結構類似金字塔。
  
  缺點：關係變得複雜，管理、維護不便，資料重複出現機率高。

- 網狀式資料庫
  
  ​=>網狀式資料庫其實就是階層式資料庫的擴充
  
  優點：避免了階層式資料庫中資料重複的問題
  
  缺點：關聯比較複雜

- 關聯式資料庫​
  
  =>2維的矩陣來儲存資料 (可以說是將資料儲存在表格的欄、列之中)​，儲存在欄、列裡的資料必會有所 "關聯" ，儲存資料的表格則稱為"資料表"。
  
  。舉例：通訊錄資料表的每一欄可以劃分為 『姓名』、『地址』、『電話』​
  
  ![](https://cdn.discordapp.com/attachments/1293405178409779201/1305860509576331295/image.png?ex=673490df&is=67333f5f&hm=3d4abed8f71ddf130ffcf44b83a38759146fcc123dae243b957efcf138ad51f3&=)
  
  圖片Link： https://meee.com.tw/hGdEgAZ
  
  -------------------------------------------------------------------------------------------
  
  。這種方式的優點是可以從一個<mark>資料表中的欄位</mark>， 透過<mark>資料表的關聯</mark>， 而<mark>找到另一個資料表中的資料</mark>
  
  。關聯式資料庫必須由資料庫設計者來設計、建立、及管理關聯​
  
  ![](https://cdn.discordapp.com/attachments/1293405178409779201/1305861854488432736/image.png?ex=6734921f&is=6733409f&hm=aa19001ad7b936dad9300e80a9f4c1dd90d45896aba496af5c548395a17b3dca&=)
  
  圖片Link： https://meee.com.tw/fbALqZr
  
  ----------------------------------------------------------------------------------

- 物件導向資料庫
  
  =>以物件導向的方式來設計資料庫， 其中包含了<mark>物件</mark>的<mark>屬性、方法、類別、繼承</mark>等特性。
  
  <mark>物件導向式資料庫</mark>中， 物件和物件之間的連繫， 是因其<mark>屬性</mark>而必然發生的​
  
   ![](https://cdn.discordapp.com/attachments/1293405178409779201/1305862990871920680/image.png?ex=6734932e&is=673341ae&hm=971499b02160d9597f55066ac699f38295af866ff95d575ae034e28631d61f1e&=)
  
  圖片Link： https://meee.com.tw/PAX3nlT
  
  ===============================================================

##### 資料庫系統架構

- 單機架構​
  
  - 將所使用的<u>應用程式以及資料庫</u>，<mark>全部儲存在每一位使用者的電腦內​</mark>
  
  - 電腦之間的<mark>資料完全獨立​</mark>
  
  - **相同的資料重複**出現在很多部電腦內​
  
  - 無法達到資料的正確性、安全性以及共同分享的目的

- 主/從式架構(Client / Server)​
  
  - - 資料庫管理系統獨立成一部『<mark>資料庫伺服器</mark>』
    
    - 使用者可以利用**本機​的應用程式**，並透過**​網路連線**向『資料庫​伺服器』進行資料的**​存取操作​。**
    
    - 優點：資料可集中管理，資料一致性、資料共享。
    
    - 缺點：使用者須安裝應用程式才能連線。

- 三層式架構( 3-Tier )​
  
  - - 將使用者端的應用程式，獨立成一部『應用伺服器』
    - 所有的<mark>應用程式或稱商業邏輯</mark>獨立存放於『應用伺服器』​

- 分散式架構
  
  - 較為**複雜的方式​**
  
  - 分散式架構是***<u>利用數台資料庫伺服器來分別處理</u>***使用者的連線

#### SQL 語言主要分為三大類型

- 資料<mark>定義</mark>語言(Data Definition Language， DDL)​
  
  。針對不同物件的結構定義
  
  - CREATE，建立物件​
  
  - DROP，刪除物件​
  
  - ALTER，更改物件

- 資料<mark>操作</mark>語言(Data Manipulation Language， DML)​
  
  。針對於<mark>資料表/檢視表內的資料進行存取</mark>的操作
  
  - SELECT，查詢或擷取資料​
  
  - INSERT，新增資料​
  
  - UPDATE，更新資料​
  
  - DELETE，刪除資料​

- 資料<mark>控制</mark>語言(Data Control Language， DCL)​
  
  。針對<mark>資料庫管理系統的安全</mark>進行控制
  
  - GRANT，授予使用權​
  
  - DENY，禁止使用權​
  
  - REVOKE，將以前面所授予或禁止的動作撤銷

##### 。資料庫系統的相關角色

- **應用程式的專案開發**，可分**為四個階段**​

- 規劃階段(plan phase)​

- 分析階段(analysis phase)​

- 設計階段(design phase)​

- 實作階段(implementation phase)​

------------------------------------------------------------

- <mark>與資料庫系統有互動的人員​</mark>
  
  - 資料庫管理師(Database Administrator)​
    
    - 資料庫的安全管理、授權管理、效能調整管理、資料庫的備份/還原。
  
  - 資料庫設計師(Database Designer)​
    
    - **瞭解使用者的需求**​，將資料庫的結構設計並建立。
  
  - 系統分析師(System Analyst，簡稱SA)​
    
    - **訪談、問卷調查及觀察來進行瞭解企業的需求分析**來建立程式規格書​
  
  - 程式設計師(Programmer)​
    
    - 將程式實作出來，進行不同的程式測試，並將文件化
  
  - 終端使用者(End Users)

=================================================================

#### 。SQL Server服務與連線的網路協定

- Shared Memory : 此種通訊協定讓本機的應用程式可以直接連至本機的SQL SERVER​

- 具名管道 : 此種通訊協定可以提供給外部使用者(必須屬於同一個區域網路)，透過SQL SERVER的主機名稱來連線​

- TCP/IP : 此種通訊協定可以提供給外部使用者(包括整個Internet)，透過IP位址或是FQDN的方式連線​

- FQDN(Fully qualified domain name)：完整網域名稱，由主機名稱與母網域名稱兩部份所組成​

======================================================================

## <mark>。 關聯式資料庫</mark>

。由資料表(Table)、紀錄(Record)、欄位(或稱資料行Field)以及資料(Data)

。因爲資料具有相互關聯的特性，不同的資料表間，可以透過特定的欄位(資料行)將資料串起來

。盡量避免重複的資料存在不同的資料表中

。正規化(Normalization)

![](https://cdn.discordapp.com/attachments/1293405178409779201/1305871660477448256/image.png?ex=67349b41&is=673349c1&hm=9463b2cdbeb37e42a79560c934fda84d9b6f6ba9ab996ea29c7cc9d07711fe0d&=)

圖片Link： https://meee.com.tw/AJ5BPpE

-----------------------------------------------------------------------------------------

##### 。關聯式資料庫：

"關聯"必須經由二個資料表中。<mark>相同的意義及資料類型的欄位來實現</mark> (欄位名稱不一定要相同)​，也就是先將<mark>一堆複雜的資料分類存放</mark>，然後再 "<mark>建立關聯性</mark>" 將資料連接起來，並靈活應用

![](https://cdn.discordapp.com/attachments/1293405178409779201/1305872424142901319/image.png?ex=67349bf7&is=67334a77&hm=54f00e46944b3013eb96fbe495ea41fde461751b4b40a19ba6c4c3b56175673f&=)

圖片Link： https://meee.com.tw/oU1ssz3

### ⓵Key的種類

##### ．主鍵 (Primary Key 主索引鍵)

特性：唯一性

表示方式：資料表中會在主鍵的詞前加上*作為標記

說明：非重複性的資料類別可作為主鍵的類別，主鍵的欄位可為一個或是多個欄位所組成，

但是一個資料表中只會有一個類別作為主鍵。

##### ．連外鍵 (Foreign Key 外部索引鍵)

說明：一個資料表中只會有一個主鍵類別，但在一個資料表中可以有多個連外鍵。

舉例：

下圖用書籍編號如：A表中的B0001作為連外鍵代替書籍名稱，則A表的B0001會去尋找B表的B0001，而B表的B0001為B資料表中的主鍵。

所以圖示會像： A表連外鍵-----尋找----->B表主鍵

<img src="https://cdn.discordapp.com/attachments/1293405178409779201/1293408762538885212/20241009_110422.jpg?ex=6719b947&is=671867c7&hm=8eb40685b1ec7864e209d3d6016f2b494ed41b37eb739fe0e204601b7376eea2&" title="" alt="" width="627">

圖片LINK： https://drive.google.com/file/d/19QtsbZf5e6scToJSPqi_WPBy-15PU2uc/view?usp=drive_link

========================================

### ⓶關聯式資料庫

特色：資料完整性

###### 一、實體完整性：

        特性：確保資料表中的記錄是唯一

        說明：設定主鍵就是為了達成實體完整性，如果主鍵的資料重複就不符合實體完整性。

###### 二、區域完整性：

        特色：在允許範圍中

        舉例：如限制數值欄位的範圍為0~999，而資料表中填入的數值欄位為1000時，就不府和區域完整性。

###### 三、參考完整性：

        特色：確保相關資料表間的資料一致

        舉例：A表中的FF003去尋找其他資料表中的FF003，結果尋找不到FF003，就不符合參考完整性。

###### 四、使用者定義的完整性：

        特色：使用者自行定義

=========================================

### ⓷不同的關聯性

##### 壹、 一對一關聯

**說明：**

            甲一筆資料 ----對應到---> 乙一筆資料

![](https://cdn.discordapp.com/attachments/1293405178409779201/1293414242543865926/1293413909985886260remix-1728444382448.png?ex=6722f8e1&is=6721a761&hm=b02eb2cad50fa757e3c63afd751fd37ea143ff104ce33cd198b13f62afc74dc6&=)

圖片LINK： https://drive.google.com/file/d/1mSm6kbQRGKB9gRZevz37yHevaxC7j9eO/view?usp=drive_link

##### 貳、一對多關聯

**說明：**

            甲一筆資料 ---對應到---> 乙多筆資料

![](https://cdn.discordapp.com/attachments/1293405178409779201/1293414718219747358/20241009_112730.jpg?ex=6722f953&is=6721a7d3&hm=22ee534bdee4c0d00236ce6b9c4e9af26b8decd455302ac337fcd94d6c4907f4&=)

圖片LINK： https://drive.google.com/file/d/1l_LCZ06bH-c9iuXSpaIlLj8PBj-JEnSe/view?usp=drive_link

##### 參、多對多關聯

**說明：**

            甲一筆資料 ---對應到---> 乙多筆資料，乙一筆資料 ---對應到---> 甲多筆資料

![](https://cdn.discordapp.com/attachments/1293405178409779201/1293415889064169563/20241009_113244.jpg?ex=6722fa6a&is=6721a8ea&hm=f2f5da99ecd2f7cfa415558e8c87547561aad97fc50055c306d5c764c1ceb3c1&=)

圖片LINK：  https://drive.google.com/file/d/1pLrXXw8Og43UbSQei8b-Rv9XB7getrUG/view?usp=drive_link

======================================

### ⓸ 實體關係模型

主要要素：**

。實體(Entity)

。關係(Relationship)

。屬性(Attribute) 

--------------------------------------------------

橢圓形：實體屬性

菱形：實體與實體之間的關係

方形：實體

![](C:\Users\88697\AppData\Roaming\marktext\images\2024-10-30-13-33-29-image.png)

圖片LINK：  https://drive.google.com/file/d/140dF6RV8Uq8D5YTK_q5F-LGAYCO7BkF4/view?usp=drive_link

#### 。 實體(Entity)

**說明：** 可從真實世界的資料中識別出來的東西。

**舉例：** 人、客戶、產品、地方、物件、事件、一個觀念。

#### 。 實體集合

**說明：** 在實體關係模型中，會將同一類型的實體集合起來成為<mark>實體集合</mark>，具有<mark>相同的特性</mark>

**舉例：** Randy 、Admads、George都是學生都是相同類型的實體，集合起來成為實體集合，因為都具有相同特性有：學號、姓名、性別....等

#### 。實體類型、實例

**說明：** 為了明確的區別每一個實體集合，依照特性不同，給予識別名稱。

**舉例：** Randy 、Admads、George都為學生，而<mark>學生</mark>就是<mark>實體類型</mark>，而Randy 、Admads、George{<mark>姓名</mark>}是學生實體類型中的<mark>實例</mark>。

==========================================

### ⓹弱實體、一般實體

##### 弱實體

**說明：** 必須依靠其他實體才能存在。

**舉例：** 學校的學生為一個實體，而<mark>學生家長為弱實體</mark>。必須依靠學生實體才能存在，如果學生從學校畢業後，該學生的家長就孜然的刪除了。

![](C:\Users\88697\AppData\Roaming\marktext\images\2024-10-30-14-05-20-image.png)

圖片LINK：  https://drive.google.com/file/d/1OjssVA51St6gaZrcGOyVFrWeGrvg9fKc/view?usp=drive_link

##### 一般實體

**說明：** 除了弱實體外其他都是一般實體。

**舉例：** 學生、書籍。

================================================

### ⓺屬性Attribute

###### 一、鍵屬性

**說明：** 可做唯一識別該實體的實例，**<u>要畫底線</u>**。

**舉例：** 學號作為識別學生的實例。

<u>**弱實體中鍵屬性虛底線**</u>

###### 二、推導屬性

**說明：** 某些屬性可以由其他屬性而推算出來，以**虛線的橢圓形**表示。

###### 三、複合屬性

**說明：** 有些屬性可以再攜分為多個小屬性。

**舉例：** 地址可以分開、姓氏名字分開。

###### 四、多值屬性

**舉例：** 專長不只有一個。

====================================================

#### ⓻實體-關係圖

實體的資料用<mark>**屬性**</mark>轉為資料表的<mark>**欄位**</mark>

<mark>鍵屬性=>主鍵</mark>

複合屬性中，所有屬性轉為資料表中、欄位

#### **弱實體的轉換**

    弱實體的存在需依附在其他實體才能存活。

    弱實體需依賴實體的鍵屬性加入作為連外鍵。

<img src="https://cdn.discordapp.com/attachments/1293405178409779201/1298474563796996106/image.png?ex=6729842c&is=672832ac&hm=de4129db6f6e5d311a91f5929f34a2ff1dbe0f129c137f8316459562699e7e9a&=" title="" alt="" width="341">

圖片LINK： https://drive.google.com/file/d/1xAF9soLGlxMPY0nqw9WirkWt8GBwpwKl/view?usp=drive_link

#### 多值屬性的轉換

    實體中的屬性為多值屬性需為該屬性另外建立資料表    ![](https://cdn.discordapp.com/attachments/1293405178409779201/1298475218750148699/image.png?ex=672984c8&is=67283348&hm=a9e06d0bd3ecf3edae2f29d6f02bb8f0ae5d0d90720c0065ec39603923357073&=)

圖片LINK：  https://drive.google.com/file/d/1lI0iJj13UcV5tq0HPhmMT1h6oK7u5MQw/view?usp=drive_link

#### 「一對一」關係的轉換

將部分參與實體的主鍵放入部參與的實體中做為連外鍵

舉例：公司為了獎勵員工給予每位員工汽車，在這中員工是全部參與，汽車是部分參與，會多買汽車當作備案，如果車壞了可以馬上更換。

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298476637150642236/image.png?ex=6729861a&is=6728349a&hm=f13c6c06f66a574cf2959ff1d4c24f9463ad8648f20ef1241940f1ce7222ab8f&=)

圖片LINK： https://drive.google.com/file/d/1FvVG6Yr6XbckMuSo7zdVJrL_taSlnxY6/view?usp=drive_link

#### 「一對多」的轉換

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298478060370264114/image.png?ex=6729876e&is=672835ee&hm=a6a776bb5ceca1f4ae946035757ffd6da1066de040a70a5eeb49813542db8e3e&=)

圖片LINK： https://drive.google.com/file/d/1JCiMf8iu5Lrvwf8EyfpaI0gZ0DqjY_eq/view?usp=drive_link

#### 「多對多」關係轉換

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298478335768395857/image.png?ex=672987af&is=6728362f&hm=545c512d113a830aea3e41fe109ecc45759422931eaa4604e3fa13b0466b0672&=)

圖片LINK： https://drive.google.com/file/d/1-3dLZUXw9ztakHk0pS2Va029mMpji5n7/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298479152558768140/2024-10-23_105014.png?ex=67298872&is=672836f2&hm=6a551daa0e31859d294f450478c528309959d201f945af62a856908495ff4496&=)

圖片LINK：  https://drive.google.com/file/d/198sNneBxmntbugJt85NIPOZlZ9hvMuE2/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298479985849536512/image.png?ex=672adab9&is=67298939&hm=7d53e18188b215539571aad7624cdaa3df76a06ac5800dc418da3edcc7b9c67f&=)

圖片LINK：  https://drive.google.com/file/d/1qY8uaYMpfRQPes1GLRHTeaMZuI_cxt7m/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298480144763060316/image.png?ex=672adadf&is=6729895f&hm=9ba1ab66a07f595fe0eeedff58e51d47e01ebcd6730705a86fdc47246bc2136f&=)

圖片LINK： https://drive.google.com/file/d/1Drww0m8Dp9OwPvUpYLqoSxOAQtQ0icpY/view?usp=drive_link

客戶 =>客戶編號 主鍵 copy to 訂單 => 客戶編號  連外鍵

=============================================================

#### ⓼ 資料庫正規化

1、不當設計所造成的異動操作

**處理**做出適當切割後，可方便查詢且不容易出錯

***正規化 * 可為資料完整性、隱私性、容易維護 、資料不易重複、查詢容易**

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298488428911923290/image.png?ex=672ae296&is=67299116&hm=68387f1abb8a33280dd42ba92b3efe3ccefa9cb095ac037664d1e42fd5ba19ba&=)

圖片LINK：  https://drive.google.com/file/d/1BiH59P2kjuZPrgJDJaV-b2tW4taAGfZ0/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298488500357959781/image.png?ex=672ae2a7&is=67299127&hm=c4eefa86791925098de79556aa604675edf7298d478fb7303eb3c02a7422f56b&=)

圖片LINK：  https://drive.google.com/file/d/1nR8i2MlkTo-wiMr4CqkFW3DpPQ9FfvCh/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298488549439574047/image.png?ex=672ae2b2&is=67299132&hm=a9a2d291b2aca27c6ad8a2e352c7eac71c1ce4c185662de7590cd50eaced1abc&=)

圖片LINK：  https://drive.google.com/file/d/1HNA1UVERyDCcLM3EYIPIHhy6iOuuEMWc/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298493812368474162/image.png?ex=672c3919&is=672ae799&hm=3ae04f0c6e640e242cfcf5e509875b676353d0b0b0e019fbf55d0354c473bc7f&=)

圖片LINK： https://drive.google.com/file/d/1DcWRozxkBMcdfXKMCDzthhAuLYrNs7tE/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298495920446505023/image.png?ex=672c3b10&is=672ae990&hm=61bc0550d75934d93824a574489f91b984ff984a0d9e7a83e02cad0289ae3346&=)

圖片LINK： https://drive.google.com/file/d/1jbQ8hAiqGjrlsyiAyMN-nRRsZCRZJaeD/view?usp=drive_link

相依性 ：產品編號 =>產品名稱 

相依性：供應商編號+產品編號 => 單價

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298497497236242515/image.png?ex=672c3c88&is=672aeb08&hm=eb9f366582515c6b97f8c484bc344f8d1de229166201af4cc22b4c7481472ec9&=)

圖片LINK： https://drive.google.com/file/d/1id2ND3vR75XbBvlU3Lo9p5G8gYlq9uv4/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1293405178409779201/1298498062452523069/image.png?ex=672c3d0f&is=672aeb8f&hm=8e5d260fee2dfdbd52297c62460c729c4711243961ecc7ddd723ba0969b7c682&=)

圖片LINK： https://drive.google.com/file/d/18MV3Ht-tBBXEChfTuNCYaKegZ_-4qWZd/view?usp=drive_link

#### 。正規化

- 『第一正規化』(First Normal Form，1NF)​
  
  - 不允許資料表當中，具有『<mark>多值屬性</mark>』或『<mark>組合屬性</mark>』的存在，讓關聯表只擁有單元值屬性​
  
  - 第一階正規化型式是在處理關聯表本身，並沒有解決任何關聯表存在功能相依所造成的資料重複或操作異常等問題​

- 『第二正規化』(Second Normal Form，2NF)​
  
  - 滿足1NF且關聯表沒有部分相依（Partial Dependency）​
  
  - 不是主鍵的屬性，需要完全相依於主鍵​
  
  - 部分相依只有在主鍵是由多個欄位組成時才會發生​
  
  - 它是指某些欄位只與主鍵中的部分欄位有相依性，而與另一部分的欄位沒有相依性

- 『第三正規化』(Third Normal Form，3NF)​
  
  - 滿足2NF，而且關聯表沒有遞移相依（Transitive Dependency）​
  
  - 移除哪些不是直接功能相依於主鍵的屬性

#### **<mark>功能相依</mark>** 是描述<mark>關聯表中屬性間的相依關係</mark>

![](https://cdn.discordapp.com/attachments/1293405178409779201/1305880442662031401/image.png?ex=6734a36f&is=673351ef&hm=0580525940ba53f2cd4563ef787600438b05d7b89f9f080d7c0d8e1d8c997fba&=)

上圖為R關聯表

圖片Link： https://meee.com.tw/16cbzic

- 若關聯表R擁有屬性A與B​

若屬性 B 功能相依於A，或 A 功能決定B​  
可寫成：R.A => R.B​  
或簡寫成：A => B​

=======================================================================

### **SQL Server的相關資料庫**

系統資料庫：系統層級 

AdventureWorks：範例 

ReportServer：報表服務 

使用者自建資料庫：CHXX範例資料庫 

master： 系統層級、核心 =======================================================================**<mark>msdb：</mark>**

**功能：**

讓<mark>SQL Server Agent 服務使用</mark>，讓代理程式，記錄：排程警告、排程作業、其他相關作業

SQL Server Agent 執行排程管理工作
核心資料庫，如果資料庫損毀、SQL Server將無法正常啟動
記錄：登入帳號、被管理的端點server、分散式處理的server，以及SQL Server 系統中所有的設定項目。
master資料庫記錄所有SQL Server所有的資料庫資訊，包含資料庫的實體檔案位置、SQL Server初始資訊
<mark>Model：</mark>

目的：當成所有新建資料所參考的一個樣版資料庫
so新增一個資料庫時系統會參考此model資料庫。

<mark>tempdb :</mark>

全域性、<mark>暫時性儲存資料</mark>，使用者在經過龐大資料計算時暫時儲存的一個資源暫存性，如果系統重新啟動之後，全部被清除掉

=======================================================================

#### <mark>建立資料庫 DDL語法</mark>

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304061620259127387/image.png?ex=672e0586&is=672cb406&hm=dde96a2a5a935e748efdd3cf64aa894cf184108acb4f71b9770ae922acc5c7d9&=)

圖片LINK： https://drive.google.com/file/d/1QQNKBN4_IPj6pV1xYtglkWr-8zu-jeFF/view?usp=drive_link

<img src="https://cdn.discordapp.com/attachments/1303971581025980426/1304060412911685683/image.png?ex=672e0466&is=672cb2e6&hm=8c376a7f1a376fed09334ad941ae8db06df71450f7359e092d08a4ca49717aa8&=" title="" alt="" width="686">

圖片LINK： https://drive.google.com/file/d/1QR4oU24_DkAMZhkTSaPsxX2xJ8aYYtci/view?usp=drive_link

<img src="https://cdn.discordapp.com/attachments/1303971581025980426/1304065950999511133/image.png?ex=672e098f&is=672cb80f&hm=eeb0a7714fe3334bdc9955a860c4e7da24bd9d8647e641f2a3dba7fac268a319&" title="" alt="" width="670">

圖片LINK： https://drive.google.com/file/d/1UJAf2vJpcYEBWfPZ4GNuUS1IllejP1sd/view?usp=drive_link

CREATE DATABASE {資料庫名稱}

[ ON [PRIMARY] 資料檔規格清單]

[ LOG ON 交易記錄檔規格清單]

**ON：** 資料庫儲存資料的磁碟檔案

**PRIMARY：** 後面承接PRIMARY群組內的資料檔案定義

。**<filespec>：** 定義檔案的詳細規格，包括項目如下：
​===========================================
**。SIZE=size：** 
指定初始建立的檔案大小，可加上檔案大小的單位，包括KB、MB(預設單位)、GB和TB。
沒有設定此項目時，資料檔的預設初始大小為8MB​

==========================================

**。MAXSIZE=maxsize | UNLIMITED：** 
設定該檔案能自動成長的最大容量的上限。可使用的單位包括KB、MB(預設單位)、GB和TB，例如：MAXSIZE=20或MAXSIZE=20MB是相同意義。亦可不限制上限大小，直到整個儲存空間存滿為止，可以設定成MAXSIZE=UNLIMITED

===========================================

。FILEGROWTH=grow_increment：
當檔案容量已經發生不足現象(快超過SIZE)，且該檔案的容量尚未超過MAXSIZE所設定的大小時

**=>設定方式有以下三種：**
**。不自動成長：** 直接設成0即可，FILEGROWTH=0​
**。以指定大小成長**，給定成長大小的數值並加上單位，可用單位為KB、MB(預設單位)、GB和TB​。
**。以百分比成長**，給定成長大小的數值並加上百分比的符號%​
若此項目被省略不設定時，預設情形下，資料檔會以1MB成長，記錄檔會以10% 成長​

=======================================================================

。<filegroup>：定義PRIMARY以外的檔案群組，包括檔案群組名稱，以及該檔案群組下的所有檔案定義​

=======================================================================

。LOG ON：後面承接的是該資料庫儲存記錄檔(log file)的檔案定義

=======================================================================

##### 注意 ! !

用DML建立 資料庫名稱​，舉例：

**CREATE DATABASE [圖書借閱管理5-1]**

----------------------------------------------------------------------------------------------------------------------------

凡是<u>資料庫名稱、資料表或資料列</u>使用到<mark>**特殊符號或中間有空白時**</mark>，該名稱必須加上[ ]。在此例中，因為 **<u>資料庫名稱使用特殊符號『-』</u>**，所以在資料庫的名稱前後要使用中括弧 [ ] 前後括起來，否則會發生語法上的錯誤​。

=======================================================================

用語法建立資料庫

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304070351872852011/241107_1.png?ex=672e0da8&is=672cbc28&hm=8fb079a82cdd99d3a371f6793106c22879ea890ee2a893f90fd2f521205d5d29&=)

圖片LINK： https://drive.google.com/file/d/16uXFmPrPA-xNRwyaZLJB3FZcRvdSqcqx/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304072049286840350/image.png?ex=672e0f3d&is=672cbdbd&hm=58a924fff204681e09780ee7a888cfa466eb8eae666d76d57c8ff33af408f2b1&=)

圖片LINK： https://drive.google.com/file/d/1EsqHZxeu0w169LuF7ZQ1iqLJBSbGbocf/view?usp=drive_link

。請依上圖建立資料庫依語法建立：

<img src="https://cdn.discordapp.com/attachments/1303971581025980426/1304076063672111124/image.png?ex=672e12fa&is=672cc17a&hm=1fb366f8383f77cfad8c5cb489a50c3cc62144e05d5f3913b69f7f14d3232bb4&=" title="" alt="" width="723">

圖片LINK：  https://drive.google.com/file/d/1im8pUTtSkUvIi6FM77eIliJmSn0QOScx/view?usp=drive_link

#### **注意如果是建立新的資料庫!!!!**

#### **記得回到左側「物件總管」最上層點擊後「重新整理」**

<img src="https://cdn.discordapp.com/attachments/1303971581025980426/1304078053177298974/image.png?ex=672e14d4&is=672cc354&hm=b847bb3d2c7e78b2883ae722f725b4c27fdb41e9e3507ebba39158de2d5a4f67&=" title="" alt="" width="698">

圖片LINK：  https://drive.google.com/file/d/1kz-cgUvCe0zLgl_KsWhf72hutpg2pb6i/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304082879982338098/image.png?ex=672e1953&is=672cc7d3&hm=810a1fb759948070f1815f237e87d03cbcb44fa56ec63ca068e0cd082e547294&=)

圖片LINK：  https://drive.google.com/file/d/1H1oGPpry2xeCA0qsBIB3SC4A97-QMU1Q/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304082078006251562/image.png?ex=672e1894&is=672cc714&hm=08bebe5706a05d8e08aa7e1fa3bc4a5db3b06f516d76320dbd921f9731d14ea2&)

圖片LINK：  https://drive.google.com/file/d/1LQ01tMschK31D9D0RDifBCJRMWrNStYz/view?usp=drive_link

====================================================================

##### 新增群組：

**若是要再擴建兩個群組G1 與G2，分別各有兩個檔案G11、G12 以及G21、G22**

<mark>步驟：</mark>

Step1點擊「屬性」

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304084063803670578/image.png?ex=672e1a6d&is=672cc8ed&hm=8caa5776bd0816e04a7f57e9df38aafd4cc5a3378532f88821cd76e3b245075c&)

圖片LINK： https://drive.google.com/file/d/1FB_4DTU6ggV9waWHyKTetDFzANppoJBQ/view?usp=drive_link

Step2 檔案群組=>新增檔案群組 並輸入G1、G2

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304084273111765184/image.png?ex=672e1a9f&is=672cc91f&hm=43b54f6bdab8045e65f08b8b17ee3a9f6a75ef44cc8847b212609b6e2cc0d449&=)

圖片LINK： https://drive.google.com/file/d/1cqCKUE3weLoxwcI24X5cJutYrpgt9cMF/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304084780576538738/image.png?ex=672e1b18&is=672cc998&hm=a52642a13bbe585d775cb2bd3a2e9fc078a5bfc37e56d40d986b1fa2ba030efd&=)

圖片LINK： https://drive.google.com/file/d/1E0M5YbEO_-o2v319RtKndrQHTCSz3nit/view?usp=drive_link

Step3 回到檔案 =>

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304085920986697809/image.png?ex=672e1c28&is=672ccaa8&hm=418399debebb1e641393974cd51455a73c55974eee69747b8fb4f1acd4a6f88a&)

圖片LINK：  https://drive.google.com/file/d/1RMvOREs3SZYXV04UIeER5GbRErX7mBDw/view?usp=drive_link

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304086818131546133/image.png?ex=672e1cfe&is=672ccb7e&hm=23deee8602947068cb30bac3d711c92c2a6c892107c9de4b9648de99ac09a07a&)

圖片LINK： https://drive.google.com/file/d/1RqDDYHew7U3oI0jljRoYDJKw6_OVHixn/view?usp=drive_link

###### 解釋：

。FILE 資料列

。LOG FILE 記錄檔

![](https://cdn.discordapp.com/attachments/1303971581025980426/1304089450799824967/image.png?ex=672e1f71&is=672ccdf1&hm=cd5a734750e7093ec12d132b7231022e4a8efdb72348f91f9df07683d0522885&=)

圖片LINK：  https://drive.google.com/file/d/1bkxuIaljl3bcDTHHglZImg8FuqRI7IK-/view?usp=drive_link

```建立資料庫並設定PRIMARY檔案及LOG檔案
。建立資料庫並設定PRIMARY檔案及LOG檔案
CREATE DATABASE [圖書借閱管理5-5]​

ON ​

PRIMARY​

      (name=P1,filename='C:\5-5\P1.MDF',size=5MB,maxsize=5GB,filegrowth=10%) ​

LOG ON​

      (name=Log1,filename='C:\5-5\Log1.LDF',size=5MB,maxsize=5GB,filegrowth=10%)​
```

```新增檔案群組G1​
。新增檔案群組G1​
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILEGROUP G1​
```

```新增檔案群組G2​
。新增檔案群組G2​
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILEGROUP G5​
```

```要移除群組G5
。要移除群組G5
ALTER DATABASE [圖書借閱管理5-5]​

REMOVE FILEGROUP G5
```

```增加檔案群組G2
。增加檔案群組G2
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILEGROUP G2​
```

```同時新增兩個檔案(G11、G12)至群組G1​
。同時新增兩個檔案(G11、G12)至群組G1​
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILE  (name=G11,filename='C:\5-5\G11.NDF',size=5MB,maxsize=10GB,filegrowth=20%),        ​

                  (name=G12,filename='C:\5-5\G12.NDF',size=5MB,maxsize=10GB,filegrowth=20%)​

TO FILEGROUP G1​
```

```同時新增兩個檔案(G21、G22)至群組G2
。同時新增兩個檔案(G21、G22)至群組G2
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILE  (name=G21,filename='C:\5-5\G21.NDF',size=5MB,maxsize=10GB,filegrowth=20%),         ​

                  (name=G22,filename='C:\5-5\G22.NDF',size=5MB,maxsize=10GB,filegrowth=20%)​

TO FILEGROUP G2​
```

```新增一個檔案到PRIMARY群組
。新增一個檔案到PRIMARY群組
ALTER DATABASE [圖書借閱管理5-5]​

ADD FILE (name=P2,Filename='C:\5-5\P2.NDF',size=5MB,maxsize=10GB,filegrowth=20%) ​

TO FILEGROUP [PRIMARY]​
```

**[注意] 由於PRIMARY是保留字，所以要用中括弧 [ ] 前後括起來，否則會發生語法錯誤​**

```新增一個記錄檔
。新增一個記錄檔
ALTER DATABASE [圖書借閱管理5-5]​

ADD LOG FILE  (name=Log2,filename='C:\5-5\Log2.LDF',size=5MB,maxsize=10GB,filegrowth=20%)​
```

```變更原本已建立的檔案格式(maxsize：5變成10、filegrowth：10%
。變更原本已建立的檔案格式(maxsize：5變成10、filegrowth：10% 變成 20%)
ALTER DATABASE [圖書借閱管理5-5]​

MODIFY FILE (name=P1,maxsize=10GB,filegrowth=20%)
​

ALTER DATABASE [圖書借閱管理5-5]​

MODIFY FILE (name=Log1,maxsize=10GB,filegrowth=20%)
```

```更改資料庫庫名稱(5-5變成55)
。更改資料庫庫名稱(5-5變成55)
ALTER DATABASE [圖書借閱管理5-5]​

MODIFY NAME=圖書借閱管理55​
```

關係圖複習：

題目：

1. 請將下列 3 項描述畫出整合後的實體-關係圖：  
   注意：請使用ERDPlus(https://erdplus.com/)，並匯出圖檔上傳至數位學院  
   (1)學生實體和課程實體之間有選修的關係。  
   (2)學生實體有學號、學生姓名、出生年月日、年齡、地址、電話及專長等屬性，其中學號為鍵屬性、年齡需要利用出生年月日導出來，而學生有兩個以上的專長。  
   (3)課程實體有課程編號、課程名稱、學分數等屬性，課程編號為鍵屬性。

![](https://cdn.discordapp.com/attachments/1293405178409779201/1306084170795323492/image.png?ex=6735612c&is=67340fac&hm=17de5645601d006503416a4c7eb2503e95c161d8acbeeed74fcfe5e03cc3fed3&=)

圖片Link：  https://meee.com.tw/RTME8ZC
