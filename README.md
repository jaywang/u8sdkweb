# u8sdkweb
u8sdk网页版在线打包
这里共分为两个版本，一个是客户端的，一个是网页版的。
网页版的由于个人原因还不是很完善，希望各位大佬们有什么意见可以反馈。

如果仅仅想要手动简洁的请直接本地打包就好，如果想要追求耿刚更强，请移步到webscripts目录，里面的web.py为启动文件，使用flask编写.

============操作步骤===========
1.配置打包参数（游戏参数，渠道参数，后台参数）
2.收集打包需要的信息如（渠道参数，游戏参数）
3.上传sdk包，上传游戏母包以及关联的目录（这个功能现在还没做）
4.指定签名管理（这个功能也没有做）
5.把需要打包的信息保存到数据库
+++++++++++++++++++++++++++++


===========打包流程=========
1.把从数据库取到的参数组合成字典
2.根据字典参数判定母包 or 渠道sdk文件是否存在
3.调用主程序core.py
4.把母包复制到临时目录
5.使用apktool解包
6.把sdk资源复制到临时目录
7.把解包后的通用资源写入sdk目录内
8.编译R
9.打包
10.zip对齐
11.apk包签名
12.把打包好的安装包以及日志复制到可访问目录
13.把数据库表内的信息修改，并写入可访问链接
============================================
