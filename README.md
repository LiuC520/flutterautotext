# flutterautotext

flutter 插件

根据宽度自动缩放字体

![flutter_custom_bottom_tab_bar](/screenshot.png)

### 属性：

*   **```text```**,    //String 要显示的文字
*   **```width```**, //doule 指定text的父容器的宽度，必须制定宽度
*   **```minTextSize```**, //double 最小的字体大小   默认最小是6
*   **```textSize```**, //double 正常的字体大小，默认值是14
*   **```textColor```**, //Color 正常的字体颜色
*   **```textStyle```**,//TextStyle  textStyle文字样式，上面的textSize和textColor可以不用单独写，写这个也行，同样用这个也可以设置字体粗体啊，斜体啊啥的，功能更强大些

```
提示：
 width 这个是必须的属性，因为在build之前无法拿到宽度，必须指定宽度，才能根据宽度进行适配
 其实原理很简单，就是给一个动画，然后在动画结束拿到text的宽度是否大于给定的宽度，
 如果大于给定的宽度，做一个循环来缩小字体，然后重新判断字体的宽度，直到宽度小于等于给定的宽度为止。
```

# Example

1、首先在pubspec.yaml中添加依赖
```

dependencies:
  flutter:
    sdk: flutter
  flutterautotext:
    git: https://github.com/LiuC520/flutterautotext.git
```


```
    import 'package:flutterautotext/flutterautotext.dart';



    FlutterAutoText(
        width: 50, //这个是必须的
        text: "我是刘成" ,
        textSize: 12,
    ),

```
