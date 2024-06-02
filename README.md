# 我的搜索脚本-文档

我的搜索是一个可自定义内容搜索的脚本应用，比如你收集了很多的网站、软件，想要快速检索它，这也是这个脚本应用的初心！

1、基本使用
------

1、首先需要安装浏览器油猴插件。

2、安装我们的脚本：[我的搜索](https://greasyfork.org/zh-CN/scripts/457020-%E6%88%91%E7%9A%84%E6%90%9C%E7%B4%A2)

3、使用，随便打开一个网页，按Ctrl+Alt+S, 呼出搜索框 （有内置数据可搜索）

![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150202105.png)  
![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150204449.png)  
![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150207254.png)  
![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150216422.png)  
![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150218733.png)

它不仅支持URL/还支持文本内容。  
![image](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150225147.jpeg)

2、编写自己的订阅文件
-----------

首先你需要知道github它是一个代码或说文件托管平台。

### 1）打开 [github](https://github.com/) 注册一下账号

### 2）创建一个仓库

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150227062.png)

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150324943.png)

 这里你的github仓库就创建好了。并且默认打开了这个仓库

### 3）创建订阅文件

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150229232.png)

 内容都不写，然后创建这个文件

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150329500.png)

文件创建好后，打开创建来的文件

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150241152.png)

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150336448.png)

###  **4）获取订阅**

点击下载获取文件的链接（我们说的订阅链接）：上面示例获取到的订阅地址

**https://raw.githubusercontent.com/18476305640/mysearch-zhuangjie/master/%E6%88%91%E7%9A%84%E6%90%9C%E7%B4%A2%E8%AE%A2%E9%98%85%E6%96%87%E4%BB%B6.txt**

订阅格式：

**<tis::https://raw.githubusercontent.com/18476305640/mysearch-zhuangjie/master/%E6%88%91%E7%9A%84%E6%90%9C%E7%B4%A2%E8%AE%A2%E9%98%85%E6%96%87%E4%BB%B6.txt />**

然后将之放到订阅管理上。

### **5）配置订阅**

打开订阅管理

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150245788.png)

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150247318.png)

### **6）添加订阅内容/可检索内容**

**继续向之前创建的仓库中再创建一个文件，资源/内容文件：**

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150311905.png)

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150309193.png)

 跟之前一样的方式获取上面“**收藏的脚本.md**”文件链接，将这个文件链接以下面的格式配置到上面“**我的搜索订阅文件.txt**”中：

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150307065.png)

 然后保存。

**7）查看新加入的可搜索内容**

清理一下缓存（当我们打开一个页面时，如果没有数据会自动请求订阅中的文件并解析为可搜索数据）

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150302627.png)

打开一个页面（比如百度），然后再呼出搜索框，搜索"new"：

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150258161.png)

###  8）详细说明资源定义方式

资源定义的基本方式是由我们内置的“提取函数”来支持的，内置的提取函数有两种：

**单行的处理函数：sLineFetchFun**

**多行的处理函数：mLineFetchFun**

对应的基本格式如下：

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150255177.png)

[内容书写格式视频讲解（blibli）](https://www.bilibili.com/video/BV1Xx4y1o7ps)

### 9）将编写的订阅分享到公共仓库TisHub

TisHub其它就是我们创建的Github仓库，用户想要提交自己的订阅到TisHub，只需要点击“**共享我的订阅到TisHub**”即可，注意该按钮的右边数字表示可共享的订阅个数，当大于0时，只要点击提交到TisHub仓库。

可提交的共享个数，脚本会本地订阅 + 远程公共TisHub中的订阅比较得出的结果。 

提交需要您的github Token,token只会在本地操作与保存。

非常欢迎各位将自己的订阅共享，让我们一起让脚本内容更加丰富。

![](https://cdn.jsdelivr.net/gh/18476305640/typora@master/images/2024/06/02/20240602150344767.png)



