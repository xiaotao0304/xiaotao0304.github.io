# HEXO：一个简单的个人博客

## 了解HEXO

### 官网介绍：快速、简洁且高效的博客框架

HEXO官网：[HEXO.io](https://hexo.io/zh-cn/)

### 官网界面

![](https://pngs.yanyujiangnan.site/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-07-17%20223840.png)

### 部署前的准备：

#### NodeJS：[下载链接](https://alist3.xtstudy.site/d/alist/hexo%E6%96%87%E4%BB%B6/node-v20.13.1-x64.msi?sign=tsRRazQlWt11V7kuQKjTrrwotRifAvF749YJ-xMJ0go=:0)

#### Git：[下载链接](https://alist3.xtstudy.site/d/alist/hexo%E6%96%87%E4%BB%B6/Git-2.45.1-64-bit.exe?sign=uNg8sV4hx_764UovO4WDRd2F6fvraAwy6G8XcRIKKR8=:0)

#### 创建一个GitHub仓库

#### 创建一个ssh用于远程登陆

输入以下内容（按顺序），即可完成配置文件的获取
`git config --global user.name "yourname" `

`git config --global user.email "youremail"`

**yourname，就是你的GitHub用户名，email即注册GitHub的邮箱**

## 开始部署

### 安装NodeJS和Git

在1.3部分下载好后，直接安装即可

### 创建一个GitHub仓库，和ssh

在1.3部分已做出说明

### 获取sshkey填入GitHub

打开终端，输入**ssh-keygen -t rsa -C "你的邮箱"**，连续打三个回车，完成这个步骤

这时就会生成ssh文件夹，文件目录一般在 **C:\Users\你的用户名\ .ssh**里

**打开后有一个公钥，一个私钥。id_rsa.pub是公钥，我们需要打开它，复制里面的内容。**

**然后进入github**

### 文字详解

1. **进入GitHub，点击右侧头像，点击Settings**
2. **点击左侧SSH keys的选项，进入设置页面**
3. **找到右侧栏目中SSHKeys的一项，点击NewKeys**
4. **在弹出的框中输入你在文件中复制的keys**
5. **点击左下方AddKeys即可完成 2.4部分的步骤**

### 本地创建一个文件夹，作为博客的主目录

如我在D盘创建一个HEXO文件夹，作为她的主目录

创建完成后，进入这个目录，打开终端

`hexo init` 输入这个命令开始初始化你的hexo

随后进入第三部分，开始部署

## 部署hexo

要修改主目录下的config文件

默认的部分不修改，要找到这里：

> deploy:  
>
> type: git  
>
> repo: 你的GitHubSSH地址
>
> branch: main

每一行的英文冒号后面都要加上一个空格

### repo变量的获取

**打开的你GitHub仓库，默认在Code页面，你会在你用户名的附近看到Code按钮**

**点击她，会看到SSH的字样，下方ssh@开头的地址就是你的repo地址了**

### 部署前安装必要的插件，才能完成部署

代码如下

`npm install hexo-deployer-git --save`

### 安装完成后执行命令

1. `hexo clean`
2. `hexo g`
3. `hexo d`

### 命令解释

#### `hexo clean`

用来清除hexo博客的缓存

#### `hexo g`

生成我们的博客内容

#### `hexo d`

把我们的博客文件部署到GitHub

### 提示

每次写好新的文章，都要依次执行这三个命令，来完成内容的上传

## 成品展示

![主界面](https://pngs.yanyujiangnan.site/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-07-17%20231843.png)

![文章展示页面](https://pngs.yanyujiangnan.site/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-07-17%20231946.png)

![阅读界面](https://pngs.yanyujiangnan.site/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-07-17%20232041.png)