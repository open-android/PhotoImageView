# PhotoView 图片浏览缩放控件

和普通的ImageView一样的使用方法



# 效果图

![](http://upload-images.jianshu.io/upload_images/4037105-6cda332626d46f8e.gif?imageMogr2/auto-orient/strip)


#使用
1.Gradle添加依赖 (推荐)
```gradle
dependencies {
     compile 'com.github.open-android:PhotoImageView:0.1.0'
}
```


2.xml添加
```xml
 <com.itheima.library.PhotoView
     android:id="@+id/img"
     android:layout_width="match_parent"
     android:layout_height="match_parent"
     android:scaleType="centerInside"
     android:src="@drawable/bitmap1" />
```

3.java代码
```java
PhotoView photoView = (PhotoView) findViewById(R.id.img);
// 启用图片缩放功能
photoView.enable();
// 禁用图片缩放功能 (默认为禁用，会跟普通的ImageView一样，缩放功能需手动调用enable()启用)
photoView.disenable();
// 获取图片信息
Info info = photoView.getInfo();
// 从普通的ImageView中获取Info
Info info = PhotoView.getImageViewInfo(ImageView);
```


