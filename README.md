# 安装环境
## 安装命令工具git
## 打开git bash
## 安装nodejs
<pre>官网下载nodejs的安装包，新版nodejs已经集成npm,所以npm已安装成功。可以用node -V和npm -V来测试是否安装成功。如下图：</pre>
![image](https://raw.githubusercontent.com/Sumahan/vue2.0-/master/screenshot/1.png)
## 基于node.js，利用淘宝镜像安装相关依赖
<pre>npm install -g cnpm --registry=https://registry.npm.taobao.org</pre>
## 安装webpack
<pre>cnpm install webpack -g</pre>
## 安装vue脚手架，用于帮助搭建所需的模板框架
<pre>
cnpm install vue-cli -g
输入vue -V,出现vue信息说明表示安装成功
</pre>
## 创建项目
<pre>
在硬盘上找一个文件夹放工程，在终端中进入该目录：cd 路径
根据模板创建项目：vue init webpack 工程名字<工程名字不能用中文>
之后会有一系列的项目选填：? Project name vue1.0
                        ? Project description A Vue.js project
                        ? Author hanpanpan
                        ? License MIT
                        ? Use sass? (y/N)
</pre>

## 工程目录如图所示
![image](https://raw.githubusercontent.com/Sumahan/vue2.0-/master/screenshot/3.png)

## 安装依赖
<pre>
cd 工程名字
npm install
</pre>
回到项目文件里，会发现目录结构里，多了一个node_modules文件夹（该内容就是之前安装的依赖）
基于脚手架创建的项目默认结构如下：
<pre>
├── build                                       // webpack配置文件
├── config                                      // 项目打包路径
├── src                                         // 源码目录
│   ├── assets                                  // 项目所需公共静态资源，如图片，css等
│   │   ├── images                              // 项目公共图片资源
│   │   └── scss                                // 项目公共样式资源
│   │       └── common.scss                     // 公共样式配置文件
│   ├── common                                  // 项目公共js资源
│   │   └── ajax                                // ajax组件
│   │       ├── ajax.js                         // 根据axios封装出来的Ajax
│   │       └── ajax-config.js                  // axios的默认配置项
│   ├── components                              // 组件
│   │   ├── common                              // 公共组件
│   │   │   └── shoplist.vue                    // msite和shop页面的餐馆列表公共组件
│   │   ├── footer
│   │   │   └── footer.vue                      // 底部公共组件
│   │   └── header
│   │       └── header.vue                      // 头部公共组件
│   ├── page
│   │   ├── error
│   │   │   └── error.vue                       // 错误页面
│   │   ├── login
│   │   │   └── login.vue                       // 登录页
│   │   └── home.vue                            // 项目页面总布局
│   ├── router
│   │   └── router.js                           // 路由配置
│   ├── store                                   // vuex的状态管理
│   │   ├── action.js                           // 配置actions
│   │   ├── getters.js                          // 配置getters
│   │   ├── modules                             // store模块
│   │   ├── mutation-types.js                   // 定义常量muations名
│   │   ├── mutations.js                        // 配置mutations
│   │   └── store.js                            // 引用vuex，创建store
│   ├── App.vue                                 // 页面入口文件
│   └── main.js                                 // 程序入口文件，加载各种公共组件
├── static                                      // 项目公共静态资源，如图片等
│   └──images                                   // 项目公共图片资源
├── index.html                                  // 入口html文件

</pre>

## 测试环境是否搭建成功
<pre>
npm run dev
在浏览器里输入：localhost:8080
</pre>
