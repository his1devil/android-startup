### 6. 小测试应用

#### 资源编号
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
