# 永久免费的节点！免费解锁Netflix、ChatGPT！通过Cloudflare Worker、Pages部署免费的VLESS节点！

# 前言 

zizifn 大佬的一个开源项目 edgetunnel ，使得我们可以免费的在 Cloudflare 上面通过部署 Worker ，来创建一个免费 VLESS 节点！

> 何为 Cloudflare Worker ?
>
> Cloudflare Worker 是 Cloudflare 提供的一种服务，它允许开发者在全球分布的边缘服务器上运行自定义的 JavaScript 代码。
>
> Cloudflare Worker 可以用来处理 HTTP 请求，从而允许开发者通过编写 JavaScript 代码来实现各种功能，例如路由请求、修改请求和响应、执行身份验证、实现缓存策略等。

## 关于注册cf账号，以及域名的托管方法

建议第一次接触的先看这篇文章：**初级教学：**[[教学链接](https://jiaoliu.xtstudy.site/07/)](https://jiaoliu.xtstudy.site/07/)

<!--more-->



## 完成托管之后你要做的

## 第一类方案，简单的部署节点

> 本方法在上一期教学也有涉及到，本期就简单说了
>
> 上期教学文档：**看这里：**[[教学链接](https://jiaoliu.xtstudy.site/07/)](https://jiaoliu.xtstudy.site/07/)

**原作：[GitHub](https://github.com/zizifn/edgetunnel)**

**项目地址：[GitHub](https://github.com/zizifn/edgetunnel)**

**这个要用到CF的Workers服务，看图即可**

## workers部署

来到 Cloudflare 首页，点击 `Workers 和 Pages` ，创建 Work ，自定义名称，然后部署！

## 在线生成uuid[[链接](https://1024tools.com/uuid)](https://1024tools.com/uuid)

在线生成一个 UUID，用于替换下面代码中第七行的 `UUID`

关于 `proxyIPs` ，是用于转发CF的一些流量，所以，若是存在套了CF的一些网站无法打开，请更换其中的其他网址，也就是第九行中的部分网址！

代码地址：[[点击访问](https://github.com/V2RaySSR/Free-VLESS/)](https://github.com/V2RaySSR/Free-VLESS/)

更多 `proxyIP` 列表：

> 1. CM 维护
> 2. proxyip.us.fxxk.dedyn.io 
> 3. IP落地区域: 美国 维护频率: 12小时/次
> 4. proxyip.sg.fxxk.dedyn.io 
> 5. IP落地区域: 新加坡 维护频率: 12小时/次
> 6. proxyip.jp.fxxk.dedyn.io 
> 7. IP落地区域: 日本 维护频率: 12小时/次
> 8. proxyip.hk.fxxk.dedyn.io
> 9. IP落地区域: 香港 维护频率: 12小时/次
> 10. proxyip.aliyun.fxxk.dedyn.io 
> 11. IP落地区域: 阿里云 维护频率: 4小时/次
> 12. proxyip.oracle.fxxk.dedyn.io 
> 13. IP落地区域: 甲骨文 维护频率: 4小时/次
> 14. proxyip.digitalocean.fxxk.dedyn.io 
> 15. IP落地区域: 数码海 维护频率: 4小时/次
> 16. 
> 17. 白嫖哥维护
> 18. workers.cloudflare.cyou
> 19. 
> 20. Mingyu维护
> 21. my-telegram-is-herocore.onecf.eu.org
> 22. sg.ipdb.rr.nu
> 23. nl.ipdb.rr.nu
> 24. hk.ipdb.rr.nu
> 25. jp.ipdb.rr.nu
> 26. us.ipdb.rr.nu
> 27. 
> 28. 小一维护
> 29. hk.cf.zhetengsha.eu.org
> 30. sg.cf.zhetengsha.eu.org
> 31. us.cf.zhetengsha.eu.org
> 32. jp.cf.zhetengsha.eu.org

改好之后，保存并部署，返回（点击左上角箭头）

设置以下自定义域名即可

找到**设置** – **触发器**，**添加自定义域**，输入 没使用过 的 已经托管在 CF 上面 的，二级域名（xxx.xxx.xxx），如图：

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191145.png)

> 博主托管在 CF 上面的域名是 a.com ，随便指定一个二级域名的前缀：vless（名字随意），所以就有了二级域名 vless.a.com

访问通过 **自定义域名/UUID，即可拿到订阅链接**

打开 **clash或v2ray,v2ray，导入订阅即可**

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20192303.png)



# 优选IP的运用

若是速度不理想，可以自行优选 CF IP ，来进行提速！CF 优选 IP Windows 工具：[[点击下载](https://github.com/badafans/better-cloudflare-ip/releases/download/20221201/batch.zip)](https://github.com/badafans/better-cloudflare-ip/releases/download/20221201/batch.zip)

运行 IP 优选的时候，请关闭代理，这样会更准确！记得不要使用 TLS 优选！

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191828.png)

优选完成后，结果会自动复制

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191952.png)

复制替换即可：**替换ip的框内容**

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191254.png)

# 另一种方法

### pages节点

### 项目地址

高级版的部署，其实和初级的部署，大同小异，道理是一样的，只是多了很多功能，比如自动生成 SUB CLASH，SURGE订阅地址、自动优选 IP 等。

[[CM](https://github.com/cmliu)](https://github.com/cmliu) 基于 [[zizifn](https://github.com/zizifn/edgetunnel)](https://github.com/zizifn/edgetunnel) 的项目进行了二次创作，GitHub 地址：[[点击访问](https://github.com/cmliu/edgetunnel)](https://github.com/cmliu/edgetunnel) （功能还是很多的）

### 下载源文件

下载作者的 Worker 文件：点击下载 [[worker.zip](https://raw.githubusercontent.com/cmliu/edgetunnel/main/worker.zip)](https://raw.githubusercontent.com/cmliu/edgetunnel/main/worker.zip)

### Pages 部署 VLESS

登录 CloudFlare ，来到 Workers 和 Pages ，和刚才不一样，我们需要点击 Pages ，点击 使用直接上传创建 – 上传资产。

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20190709.png)

随便起名，上传刚才下载下来的 [[worker.zip](https://raw.githubusercontent.com/cmliu/edgetunnel/main/worker.zip)](https://raw.githubusercontent.com/cmliu/edgetunnel/main/worker.zip) （从计算机中选择 – 上传压缩文件），然后点击 部署站点，继续处理项目！

生成一个UUID之后，保存设置即可，UUID[[在线生成](https://1024tools.com/uuid)](https://1024tools.com/uuid)

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20190943.png)

保存后，重新部署pages

再次按照刚刚的步骤重新部署一次，然后去设置自定义域名

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191145.png)

这样，我们点击上图中的 访问站点，若是有内容出现，证明部署成功

我们可以访问 `https://域/UUID` ，来查看我们的节点。例：刚才生成的 UUID 为 `abcd` ，

按照上图，我们访问 `https://vless.a.com/abcd` ，可以看到详细的节点情况！

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20191045.png)

到这一步，pages节点就部署好了，复制自适应链接导入相应的软件即可

# 测试节点

## chatgpt

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20192719.png)

## YouTube 4K视频

![](https://pngs.xiaotaolive.club/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20192930.png)

## ins

![](https://png1.xiaotaolive.cfd/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-06-08%20193537.png)

其他的节点解锁流媒体的情况就需要大家自行测试了！

本期内容仅用于学习交流，切勿用于非法，请不要传播摄政，造谣，诈骗等内容！