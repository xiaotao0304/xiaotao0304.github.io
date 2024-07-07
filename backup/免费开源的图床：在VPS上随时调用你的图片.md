# 今天来介绍一款开源项目，可以为大家制作自己的私人定制图床！
## 啰嗦几句
- 1：图床是干什么的？
- 图片存储和管理：图床提供了一个免费或付费的平台，让用户可以上传、存储和管理图片文件。这些图片可以通过链接在网页上显示，而无需直接存储在网站的服务器上，节省了服务器空间和带宽。

加速网页加载速度：使用图床上的图片链接替代直接上传图片到网页，可以加快网页的加载速度。因为图床通常会使用CDN（内容分发网络）技术，能够快速地将图片内容分发到全球各地的用户。

方便的分享和发布：上传到图床的图片可以通过生成的链接方便地分享给他人，比如在社交媒体、论坛、博客等平台上发布内容时使用。

节省成本：对于个人用户和小型网站，使用免费的图床服务可以节省存储和带宽成本。对于大型网站和应用，选择付费图床服务可以提供更稳定和专业的服务。

保障图片资源：一些图床提供备份和长期存储功能，确保用户上传的图片资源不会丢失或被删除，提供了一定的安全性和稳定性保障。
- 本期用到的开源项目：[开源图床](https://github.com/osuuu/LightPicture)
- 成品展示：
- ![25a735c0a014f750.png](http://light.xtstudy.site/LightPicture/2024/07/25a735c0a014f750.png)
- 2免费的图床有哪些？
1. cloudflare：[CF官网](https://www.cloudflare-cn.com/)
2. 国内各大云厂家的存储桶服务

- 3：CF免费图床需要准备一个自定义域名即可开始使用，搭建较为简单，后续会单独出内容
-  ## 开始教程
1. 用到的项目：[Github开源项目](https://github.com/osuuu/LightPicture)
2. 需要准备的环境：一个VPS或者国内的云服务器。本期教程以VPS为主
3. VPS推荐1：最适合入门小白的年费10刀VPS—— [注册链接](https://my.racknerd.com/aff.php?aff=11799)   
![8dd917b4ae19720e.png](http://light.xtstudy.site/LightPicture/2024/07/8dd917b4ae19720e.png)
5. VPS推荐2：艾云——价格便宜并且带宽高，适合入门来玩 [艾云注册链接](https://iaclouds.com/aff.php?aff=1878)
![dbb2f74426aebd5d.png](http://light.xtstudy.site/LightPicture/2024/07/dbb2f74426aebd5d.png)
6. 宝塔服务器面板：[宝塔面板](https://github.com/Closty/happpyBT)
7. 因为我的服务器是Ubuntu，所以选择Ubuntu的安装指令：（具体根据happyBT的作者文档内容选择）
`curl -sSO https://52bt.cn/install/new_install.sh && bash new_install.sh`
好的，说完了准备内容，我们直接进入实战环节吧！
首先进入你的宝塔面板，因为我已经提前安装了面板，进入后看到如下界面
![45138e423a833ab6.png](http://light.xtstudy.site/LightPicture/2024/07/45138e423a833ab6.png)
## 开始部署
1. 服务器第一次安装BT面板会有一个部署运行环境阶段，一定要在这个阶段后开始，本期教程的VPS已经完成全部步骤，可以直接开始
![b67cb58929be0ed4.png](http://light.xtstudy.site/LightPicture/2024/07/b67cb58929be0ed4.png)
3. 面板地址一般为：你的VPSIP:端口号，信息会在安装完面板告诉你
4. 进入面板看到如下界面
![45138e423a833ab6.png](http://light.xtstudy.site/LightPicture/2024/07/45138e423a833ab6.png)
6. 点击网站，创建一个站点，域名已在本频道有所涉及，可回看往期内容
7. 以这个域名为例，首先在CF配置好，A类型，名字任意，地址写VPSIP
![46ce374942b08920.png](http://light.xtstudy.site/LightPicture/2024/07/46ce374942b08920.png)
然后再宝塔创建域名，按以下界面输入即可。被遮挡部分即你的域名
![8ad91f78e895c147.png](http://light.xtstudy.site/LightPicture/2024/07/8ad91f78e895c147.png)
8.复制以下链接，在网站目录一栏，选择远程下载，如图所示
![be3b0456463acaf6.png](http://light.xtstudy.site/LightPicture/2024/07/be3b0456463acaf6.png)
下载源码链接为 ：`https://github.com/osuuu/LightPicture/archive/refs/tags/v1.2.2.zip`。输入后确定即可，自动下载
下载后，解压文件，在网站的界面点击域名
设置目录为公开。
配置网站默认：
```
index.html
index.php

```

伪静态规则设置为ThinkPHP
配置好后，即可访问域名/install，如我写的域名的a.com，那么访问时就要带上a.com/install，即可看到安装界面
按说明完成即可
你就得到了一个自己的图床网站！安装完成后默认账号为admin 密码123456
视频正在制作中，后续会发布到YouTube上面
