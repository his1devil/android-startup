#### 6. 小测试应用


##### 资源编号
AAPT : 应用编译的时候，appt会产生Class R, R.java，包含所有res/目录下的资源IDs
对于添加的所有资源都有一个ID，ID都有一个基于资源类型的格式
对于所有Java图像资源，都会遵循R.drawable格式
对于所有String资源，都会遵循R.string格式 R.string.hello

也就对应着两种读取resource的方式
* java code

```
R.string.hello // string是资源类型，hello是资源名称
```
* xml

```
@string/hello // 
```

##### 从xml文件到Java文件

+ 应用打开 MainActivity 初始化
+ onCreate自动调用, activity会被创建
+ 
 ```
 onCreate(...){...;  setContentView(R.layout.activity_main); ...;}
```
+ 指定resource ID后，Android会开始解析XML布局文件
+ 从头解析，e.g. 遇到LinearLayout，会找出一个Java对象来代表LinearLayout
+ 然后依次构造出hierarchy of Java Objects
+ 一旦获取Java对象的所有视图层级结构，就能进行操作，改变属性，调用方法

##### 创建对象

+ with Factory Method

```
MediaPlayer player = MediaPlayer.create(context, R.raw.song);
Toast toastMessage = Toast.makeText(context, "Hi", duration);
```