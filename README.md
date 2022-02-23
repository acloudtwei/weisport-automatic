# weisport-automatic
**介绍**

这是小米刷步数自动版，每天下午六点准时将存储在数据库的用户自动刷步数，步数大小是在【30000-50000】之间随机刷，目前暂不支持手动选择步数，期待下一个版本更新吧!

**数据库**

因为我是个菜鸡，所以用了数据库。用的是mysql，数据库使用的账号是**weisport**

密码是**acloudtwei**，因此如果需要查看数据表的情况可以将数据库的3306端口映射出来，然后再用数据库管理工具连接即可。以后会考虑写一个后台！

**使用**

1. 方法1（需要有docker环境）：首先将这个源代码git clone下来，之后直接在这个项目的目录下通过docker-compose up -d命令部署
2. 方法2（要有python3.5以上的环境）：也是将这个项目直接clone下来，之后使用编译器比如pycharm将automatic.py这个文件打开，之后就直接修改那个连接数据库的代码，也就是将要连接数据库的主机、用户名、密码以及数据库名修改即可；**除此之外，也要将“填写你的token”这里将你的推送token填写进去，可以在推送网站http://pushplus.hxtrip.com/ 上申请一个token，将token填写进去就可以完成推送！！！**
3. 方法3（需要docker环境）：直接在我的docker镜像里面操作也是可以的[docker镜像](https://hub.docker.com/r/acloudtwei/weisport-automatic)

**原因**

为什么要写这个呢？

主要原因还是因为这些天学了docker，然后就行学以致用，然后看到网上很多的这种刷步数都是有广告，而且部分也不安全。并且自动版刷步数的还是要付费，个人感觉明明很简单的功能商业化，感觉不爽。然后之前看到了pywebio，可以通过写py代码构建网页，然后因为这个pywebio部分界面不太好看，我就去美化了一下，也就是二开了。由于时间有限以及没怎么看懂pywebio的代码，所以二开的也没改啥，希望以后有时间再去看看改改吧。个人觉得这个pywebio是十分不错的开源库的！

**演示站**

这个演示站用的服务器是比较low一点的，不过只要不攻击问题就不大。大家可以直接在演示站输入自己小米运动的账号密码即可，成功之后会有一个推送二维码，只需要微信扫描这个二维码即可，之后就会在每天6点自动刷30000-50000的步数了，十分的方便，目前暂不支持自己添加步数，下一个版本会添加此功能，如果需要删除账户的话那只能联系作者本人了

[演示站](http://120.78.219.248:8081/)

**作者联系方式**

如果要删除账号或者其他的问题可以加作者的微信：Acloudtwei

如果觉得项目不错的话可以给个小start⭐嘛？

