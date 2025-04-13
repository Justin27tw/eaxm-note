Android Studio 筆記

頁面分為UI 、 Activity

UI 使用 XML

Activity 使用 Kotlin 或Java

Kotlin的程式碼在MainActivity.kt

XML的程式碼會在activity_main.xml

存放在res/layout資料夾內

<img src="file:///C:/Users/88697/AppData/Roaming/marktext/images/2025-04-05-16-48-50-image.png" title="" alt="" width="685">

相對位置

<img title="" src="file:///C:/Users/88697/AppData/Roaming/marktext/images/2025-04-05-16-57-57-image.png" alt="" width="654">

改背景顏色為backgroundTint的項目



============================== 

parent 容器大小，wrap_context內容一樣大小

buildFeatures{

viewbinding=true

}

private lateinit var  binding:ActivityMainBinding

binding=ActivityMainBinding.inflate(layoutInflater)

setContentView(binding.root)

=============================================

輸入值後按下按鈕並儲存

binding.{按鈕名稱}.setOnClickListener{

var  {值名稱}=binding..{painText id名}.text.toString()

}

課本3-19頁

linearlayout  

vertical 垂直

Horizontal水平

設定照片來源：

binding.{imageView 名稱}.setImageResource(R.drawable.{照片名})

================================

new  Layout的話在res資料夾下，layout按右鍵new Layout

================================

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-16-25-30-image.png)

res=> 為R

drawable換圖片

放圖片於res/drawable的話就是一個id編號

binding.{imageView名稱}.setImageResiurce(R.drawable.{圖片名稱})

============================

 除錯用

Log.d(標籤,訊息)

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-16-44-51-image.png)

若Log為紅字，為系統不認識Log，import class Log 按下 Alt+Enter檢查提示工作

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-16-47-20-image.png)

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-16-49-37-image.png)

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-16-52-06-image.png)

Log會跑迴圈

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-17-52-17-image.png)

課本5-1節

Toast  

binding.{按鈕名稱}.setOnClickListener{

Toast.makeText(context:this,R.string.{物件內容},Toast.{長度}).show()

}

//this在我自己顯示,我要顯示的文字,顯示時間長短

Toast.makeText(顯示位置,顯示內容,顯示時間).show()

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-19-08-09-image.png)

val 不能計算 、(他是物件)不能用show

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-19-47-20-image.png)

變成全域變數用法，可以重複使用 

val myToast=Toasr.makeText(this,{文字},顯示時間長短)

。可以直接這樣使用

binding.{按鈕名稱}.setOnClickListener{

myToast.show()

}

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-19-54-04-image.png)

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-19-54-29-image.png)

設定位置

myToast.setGravity()

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-19-56-48-image.png)



AlertDialog     課本5-2



binding.btnAlert.setOnClickListener{

AlertDialog.Builder(this).apply{

setTitle("標題")

setMessage("內文")

setIcon(R.drawable.{圖示名稱}) //設定圖示

setPositiveButtonIcon(getDrawable(R.drawable.{圖示名稱}) //設定正向的按鈕圖示

setPositiveButton("OK",DialogInterface.OnClickListener{ dialogInterface , i ->

Toast.makeText(this@MainActivity,"已顯示",Toast.LENGTH_LONG).show() //點下OK按鈕後的事件

 })

setNegativeButton("Cancel",DialogInterface.OnClickListener{ dialogInterface , i ->

finish() //點下Cancel後的事件

 })

show()  //顯示出來

}

}

![](C:\Users\88697\AppData\Roaming\marktext\images\2025-04-13-20-45-26-image.png)

內建圖示使用方法：

drawable按右鍵new=> Vector Asset



更新時間：25/4/13 完成80%
