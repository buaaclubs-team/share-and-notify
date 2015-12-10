
文件结构
.git* git相关
.jsHintrc 一个hint工具
package.json 就是Hint的配置文件
.js javascript文件
.less（less style sheet） 扩展的css
.tpl html文件
Webpack.config.js，webpack配置文件，设置入口，输出，加载器以及其他设定

Vuechat
-----Src
-------------Card—js less tpl 卡片组件，用来布局
-------------List—js less tpl  列表组件，用来搜索
-------------Message—js less tpl 消息组件，发送消息
-------------Text—js less tpl 文本组件，保存聊天文本
-------------Chat：template模版，watch监视，当sessionList改变的时候保存到localStorage中；filters：获取时间，components：各个组件
-------------Store 包括登录用户，用户列表（名字，头像 ），会话列表，初始的text。localStorage
存储聊天记录
-----build
-------------images 存储图片来源
------------ script.js  webpack打包后的js
-------------script.js.map  渲染
-------------vue.min.js  vue的生产版本

浏览器渲染过程:

每个组件都有相应的tpl模版，less和js。还有chat主体部分和store存储部分。通过webpack组织这些内容。

Vue.js对数据和dom进行双向的绑定，并对模版进行渲染，渲染为常规的html并展示在页面之中。

Source map是源代码和最终浏览器执行的代码之间的关联。里面储存着位置信息，转换前后代码的位置是对应的，通过sourcemap，可以显示原始代码的位置

Webpack：将所有的东西模块化，通过commonjs的语法把所有浏览器段需要发布的静态资源准备好，资源的合并和打包等等。

