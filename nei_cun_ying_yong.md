#### 成绩单结构


##### 内存是有限的资源

+ 通过ListView和Adapter实现view 重用， 而不必new 很多view占用内存

View Recycling: 重复使用在屏幕上不再可见的视图，放置于scrap views等待使用
ListView + ArrayAdapter


##### 适配器如何应用到每个类别

ListView.setAdapter()方法需要ListAdapter作为参数 ListAdapter是个接口
BaseAdapter是个抽象类
ArrayAdapter是ListAdapter