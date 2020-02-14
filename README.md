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
##### 在根目录的build.gradle中加入
apply from: "config/config.gradle"
##### 在所要引入的moudel修改为类似的这样
compileSdkVersion rootProject.ext.android["compileSdkVersion"]  
buildToolsVersion rootProject.ext.android["buildToolsVersion"]  
implementation rootProject.ext.support["appcompat-v7"]  
implementation rootProject.ext.dependencies["ktx"]

##### 修改版本号升级  
PUBLISH_VERSION = '0.0.2'

## 引用方法 
##### 在根目录的build.gradle中加入
allprojects {
        repositories {
            ...
            maven { url 'https://jitpack.io' }
        }
    }
##### 在所要引入的moudel加入
implementation 'androidx.core:core-ktx:1.1.0'

