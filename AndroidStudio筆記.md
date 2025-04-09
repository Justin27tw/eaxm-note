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

更新時間：25/4/7
