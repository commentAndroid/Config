# config

用于设置业务组件的key、页面的主题风格、组件的版本，应为这个需要根据需求进行配置，所有该控件不是进行aar的导入，而是导入整个module这样更加方便的进行配置，此module在不同的项目中都有一份，不进行整体配置，所以这只是一个模板

## 项目结构图

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## 用法
#### 1.统一编辑的版本和第三方支持库
##### 1.1 在根目录的build.gradle中加入
apply from: "config/config.gradle"
##### 1.2 在所要引入的moudel修改为类似的这样
compileSdkVersion rootProject.ext.android["compileSdkVersion"]  
buildToolsVersion rootProject.ext.android["buildToolsVersion"]  
implementation rootProject.ext.support["appcompat-v7"]  
implementation rootProject.ext.dependencies["ktx"]

#### 2.版本风格设置
##### 2.1 主题风格的设置
设置color.xml中的 
```xml
<!--状态栏颜色-->
<color name="colorPrimaryDark">#1338A2</color>
<!--控制各个控件被选中时的颜色-->
<color name="colorAccent">#1338A2</color>
<!--页面背景色-->
<color name="windowBackground">#F6F6F6</color>
<!--底部导航栏颜色-->
<color name="navigationBarColor">#1338A2</color>
<!--Appbar背景色-->
<color name="colorPrimary">#1338A2</color>
<!--ToolBar上的Title颜色-->
<color name="textColorPrimary">#FFFFFF</color>
<!--各个控制控件的默认颜色-->
<color name="colorControlNormal">#999999</color>
```
各个属性的解释  
![alt statusBarColor](https://raw.githubusercontent.com/commentAndroid/Config/master/image/statusBarColor.jpeg)![alt textColorPrimary](https://raw.githubusercontent.com/commentAndroid/Config/master/image/textColorPrimary.png)


















