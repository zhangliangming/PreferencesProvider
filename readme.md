# 简介 #
之前项目使用了SharedPreferences来保存数据，然而项目修改为多进程后，SharedPreferences保存数据却出现了数据没有更新的问题，当然SharedPreferences设置了MODE_MULTI_PROCESS后可以使数据同步，不过官方已经废弃了原先的MODE_MULTI_PROCESS, 并且建议跨进程存取值还是用ContentProvider之类的更靠谱一些，由于ContentProvider提供了对底层数据存储方式的抽象，底层我们可以使用SQLite，MongoDB等等，当然也可以使用SharedPreferences来实现

## v1.0 ##


- 2018-04=30
- ContentProvider封装SharedPreferences功能，解决跨进程存取值的问题

# Gradle #
1.root build.gradle

	`allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}`
	
2.app build.gradle

`dependencies {
	         compile 'com.github.zhangliangming:PreferencesProvider:v1.1'
	}`

# 调用Demo #

链接: [https://pan.baidu.com/s/15SixU_nviX1ppK74gxL3dg](https://pan.baidu.com/s/15SixU_nviX1ppK74gxL3dg)  密码: u8hw

# 调用用法 #

## 继承 ##
![](https://i.imgur.com/72XGw4b.png)
## 声明 ##
![](https://i.imgur.com/daxZdRA.png)
## 相关API ##
![](https://i.imgur.com/wlhdM2O.png)
![](https://i.imgur.com/kcyTksE.png)


# 参考 #

[ContentProvider从入门到精通](https://www.jianshu.com/p/f5ec75a9cfea)

[http://bbs.51cto.com/thread-1070974-1.html](http://bbs.51cto.com/thread-1070974-1.html)


# 捐赠 #
如果该项目对您有所帮助，欢迎您的赞赏

- 微信

![](https://i.imgur.com/e3hERHh.png)

- 支付宝

![](https://i.imgur.com/29AcEPA.png)