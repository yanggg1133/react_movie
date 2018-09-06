# 基于react的影院购票应用

相关介绍：[基于react的影院购票应用](https://github.com/Aaaaaaaty/Blog/issues/3)
> 技术栈：react redux sass webpack es6

## Directory

```
│  .gitignore
│  index.html         入口页面
│  package.json
│  README.md
│  webpack.config.js  webpack配置
│
├─dist                打包目录
│     
└─src
    │  App.js        项目入口
    │
    ├─container      容器组件
    │
    ├─components      子组件
    │
    │
    ├─redux          redux状态管理
    │  ├─action
    │  ├─reducer
    │  ├─store
    │     
    ├─router          路由
    │
    │
    ├─utils            通用文件
    │
    │
    └─styles           通用样式文件

```


## Setup

``` 
git clone https://github.com/Aaaaaaaty/react_movie 

cd react_movie 

cnpm i || npm i

将./data及./src/images 文件 拷贝进dist //项目依赖的图片及假数据

npm start

```

## 效果预览
### 区域选择组件
![区域选择](https://dn-mhke0kuv.qbox.me/bbd349f5eea3aaf661ae)
### 电影列表组件
![电影列表](https://dn-mhke0kuv.qbox.me/48d55570a6113a5c74bf)
### 电影详情组件
![电影详情](https://dn-mhke0kuv.qbox.me/8a548a80b0f4a1d9ac36)
### 电影排期组件
![电影排期](https://dn-mhke0kuv.qbox.me/4e113ca5799e239c89f8)
### 电影选座组件
![选座组件](https://dn-mhke0kuv.qbox.me/247556ed695bcbdb2b91.gif)



===========================

webpack不是内部命令问题
2016年04月10日 18:41:37 阅读数：31952 标签： webpack 环境变量  更多
个人分类： webpack
版权声明：本文为博主原创文章，未经博主允许不得转载。	https://blog.csdn.net/u013446264/article/details/51114276
在帮别人安装webpack的时候遇到了这个问题！！自己没遇到过。。有点慌了 
在网上百度似乎也没有什么人遇到这样的问题。看到一个帖子虽然错误和我的不一样，但是他提到了他是因为环境变量的设置问题啊，然后我突然觉悟！！这应该也是环境变量的问题啊！于是百度了“安装webpack 修改环境变量”的关键词找到了一篇有用的文章。http://www.cnblogs.com/ChengWuyi/p/5020160.html 
但是他有一步没有讲清楚，我决定重新写一遍解决方法。

安装webpack首先检查下自己是否有npm（nodejs自带）,在命令行输入npm，看到版本号说明安装成功： 
这里写图片描述

然后按照网上webpack的教程尝试安装（汇智网有），安装完后按照教程检测是否安装完毕，如果出现不是内部命令的报错可以尝试一下解决方法：

1.在命令行里输入path命令查看nodejs是否安装成功（这一步在我上面提到的博文里面有写）；

2.然后配置npm路径， 
配置全局路径：npm config set prefix “d:\nodejs\node_global” 
配置缓存路径：npm config set cache “d:\nodejs\node_cache”

3.通过npm全局安装webpack，输入命令 npm install webpack -g，安装完后会显示安装路径；

4.修改环境变量：在系统变量中增加NODE_PATH变量（图片来源于上面提到的博文） 
这里写图片描述

然后在PATH变量中添加一个相同的路径（PS：这里的路径都和第2步配置的路径有关系）；

5.（图片来源于上面提到的博文） 
这里写图片描述

到此就成功啦！！终于把项目跑起来！！感觉要上天~~~

==============================

npm报错This is probably not a problem with npm. There is likely additional logging
使用webstorm开发时，遇到npm 报错，于是尝试了如下所有的方法，不完全统计。

https://blog.csdn.net/liu305088020/article/details/79182391

https://segmentfault.com/q/1010000004560187/a-1020000004560356

https://segmentfault.com/a/1190000012729790

https://blog.csdn.net/ink_if/article/details/790158

 

但是都没有用

最终解决方案：卸载node  重新下载并在安装时，勾选add path选择框

然后perfect!!!!!
