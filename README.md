# PhotoView 图片浏览缩放控件

和普通的ImageView一样的使用方法



# 效果图



#使用
1.Gradle添加依赖 (推荐)
```gradle
dependencies {
    compile 'com.bm.photoview:library:1.4.1'
}
```


2.xml添加
```xml
 <com.bm.library.PhotoView
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
// 从一张图片信息变化到现在的图片，用于图片点击后放大浏览，具体使用可以参照demo的使用
photoView.animaFrom(info);
// 从现在的图片变化到所给定的图片信息，用于图片放大后点击缩小到原来的位置，具体使用可以参照demo的使用
photoView.animaTo(info,new Runnable() {
       @Override
       public void run() {
           //动画完成监听
       }
   });
// 获取/设置 动画持续时间
photoView.setAnimaDuring(int during);
int d = photoView.getAnimaDuring();
// 获取/设置 最大缩放倍数
photoView.setMaxScale(float maxScale);
float maxScale = photoView.getMaxScale();
// 设置动画的插入器
photoView.setInterpolator(Interpolator interpolator);
```


