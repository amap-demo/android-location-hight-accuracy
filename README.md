# android-location-hight-accuracy
提升定位精度示例

## 前述 ##
- [高德官网申请Key](http://lbs.amap.com/dev/#/).
- 阅读
  [定位SDK参考手册](http://a.amap.com/lbs/static/unzip/Android_Location_Doc/index.html).
- 工程基于高德定位SDK实现

## 使用方法##
###1:配置搭建AndroidSDK工程###
- [Android Studio工程搭建方法](http://lbs.amap.com/api/android-sdk/guide/creat-project/android-studio-creat-project/#add-jars).
- [通过maven库引入SDK方法](http://lbsbbs.amap.com/forum.php?mod=viewthread&tid=18786).

## 扫一扫安装##

 ![Screenshot](https://github.com/amap-demo/android-drive-route-plan/blob/master/resource/download.png)

## 定位结果展示##

 ![Screenshot](https://github.com/amap-demo/android-location-hight-accuracy/blob/master/resource/Screenshot.png?raw=true)
 
## 核心类/接口 ##
| 类    | 接口  | 说明   | 版本  |
| -----|:-----:|:-----:|:-----:|
|AMapLocationClientOption|	setLocationMode()|设置定位模式|V2.0.0|

## 核心难点##
- 打开系统wifi设置界面

```java
        Intent intent = new Intent(android.provider.Settings.ACTION_WIFI_SETTINGS);
        startActivity(intent); // 打开系统设置界面
    
```

- 设置高精度模式
 
 ```java
    private AMapLocationClientOption getDefaultOption() {
        AMapLocationClientOption mOption = new AMapLocationClientOption();
        mOption.setLocationMode(AMapLocationClientOption.AMapLocationMode.Hight_Accuracy);
        return mOption;
    }
 ```
