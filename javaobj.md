#### 面向对象

##### 画面滚动

LinearLayout 不能进行scroll，所以使用ScrollView
一般解决方案是把LinearLayout当做ScrollView的子类

ScrollView 只能包含一个item

##### EditText

默认系统会选择聚焦EditText控件，并弹出键盘
解决方法是在上一级父控件添加
```
android:focusable="true";
android:focusableInTouchMode="true";
```

##### intent

应用可以通过intent来调用其他应用, some type of message 来要求其他应用组件完成动作，比如发送邮件，打开相机...

intent类似于一个用来标识某种指定动作的message，主要包含两个主要内容
Action和Data，还可以指定额外的信息比如 Category, Component, and Extras(用来指定额外信息) 所有内容参数由Android框架来制定哪个组件来处理这个intent

比如 Dial intent 包含 ACTION_DIAL and 内容 tel:88888888 URI格式确保intent正确送达，由Android决定谁来处理intent

```
// 判断 intent会被接收的代码 
Intent intent = new Intent(Intent.ACTION_VIEW);
intent.setData(Uri.parse("get:47.6, -122.3"));
if (intent.resolveActivity(getPackageManager()) != null) {
  startActivity(intent);
}
```