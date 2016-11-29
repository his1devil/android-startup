### 多屏应用

#### 创建新的Activity

```
Intent i = new Intent(this, newActivity.class);
startActivity(i);
```

#### Intent 类型

+ implicit 隐性intent

当你不知道哪个组件来处理intent的时候，使用implicit，比如相机，分享，发送邮件



+ explicit intent 显性intent

谨慎使用，不知道用户安装了什么第三方应用，导致调用失败，同一应用内可以使用


+ 如何创建事件监听器

1 定义一个事件监听器
```
public class NumbersClickListener implements onClickListener {
  @override
  public void onClick(View view) {
    // do some thing
  }
}
```

2 创建一个事件监听器对象的实例
```
NumbersclickListener clickListener = new NumbersClickListener();
```

3 绑定视图view
```
buttonView.setOnClickListener(clickListener);
```

