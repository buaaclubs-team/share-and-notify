13061196
Github:fusluv  270509985@qq.com


##浏览器渲染过程:

每个组件都有相应的tpl模版，less和js。还有chat主体部分和store存储部分。通过webpack组织这些内容。
Vue.js对数据和dom进行双向的绑定，并对模版进行渲染，渲染为常规的html并展示在页面之中。

Source map是源代码和最终浏览器执行的代码之间的关联。里面储存着位置信息，转换前后代码的位置是对应的，通过sourcemap，可以显示原始代码的位置

Webpack：将所有的东西模块化，通过commonjs的语法把所有浏览器段需要发布的静态资源准备好，资源的合并和打包等等。

##文件结构
.git* git相关
.jsHintrc发现错误和潜在问题的工具
package.json 就是Hint的配置文件
.js javascript文件
.less（less style sheet） css预处理语言，扩展了css，和原来css的功能类似
.tpl template模版文件，和html基本相同。
Webpack.config.js，webpack配置文件，设置入口，输出，加载器以及其他设定


Vuechat
-----Src  
-------------Card—js less tpl  
-------------List—js less tpl  
-------------Message—js less tpl  
-------------Text—js less tpl  
-------------Chat  
-------------Store  
-----build  
-------------images  
------------ script.js  webpack打包后的js  
-------------script.js.map    
-------------vue.min.js vue的生产版本  



Store:存储部分，包括登录用户，用户列表（名字，头像 ），会话列表，并设置初始的text。聊天记录存在localStorage里面  
Chat:主体部分  template模版，watch监视，当sessionList改变的时候保存到localStorage中；filters：获取时间，components：各个组件  
##组件：
card：卡片组件，卡片展示.  
list：列表组件，搜索；  
message：消息组件，和用户名和头像对应起来；发送消息滚动到底部  
text：文本组件，ctrl+回车输出并存下来  
