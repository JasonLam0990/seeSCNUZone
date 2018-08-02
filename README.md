# seeSCNUZone
存放SCNUZone的最新代码，文件已加密

#### 2018年7月24日 星期二

1.修复了清除缓存后登陆进来读取不到已填写过的数据的问题<br>
2.将队伍详情页面纯学号的完善成了头像+姓名<br>
3.修改了队伍分享海报的内容<br>
待解决问题：添加队伍时，如果填写的学号还没有注册要提示，得等师兄把api写出来才能做

#### 2018年7月25日 星期三

1.名片页面，默认填写计算机学院时会undefined，已修复<br>
2.扫小程序码进入以后，没有返回到主页的按钮，影响用户体验，已修复<br>
3.按钮可以多次点击问题，所以给每个按钮的点击事件都加了wx.showloading，wx.hideloadinga，点击后锁定用户行动，直至按钮事件完成，已修复<br>
4.修改了证书页面的一些文字<br>
5.修复了“我的收藏”页面“队伍收藏”滑动删除无法使用的bug

#### 2018年7月30日 星期一
1.整合api，将整个项目所有的api都放在api.js中，然后暴露模块。其他页面需要用到时，通过require将api.js引入，然后api.xxxx来使用相应的api，这种方法可以降低耦合度，如果需要改接口，只需要在app.js改一个地方即可，而不用到所有页面的该接口的位置改。<br>
2."我的队伍"，"我的委托"左滑增加了一个修改按钮，并采用bootstrap的按钮配色，函数还没有写，打算集中一些内容以后再让师兄干活，不然一点一点让师兄搞感觉有点繁琐哈哈

#### 2018年8月2日 星期四
1.这次提交是一个未完成版的大改动。首先功能上引入了华师圈，二手闲置两个大版块。将校园委托，二手闲置，比赛组队，发现四个板块作为一级入口方在上方，下部的tabbar是首页，华师圈，消息，我的。
2.委托分了委托、他能提供两个部分来展示内容，而闲置则是出售、求购。
3.闲置的教材书籍板块加了一个根据学院、年级筛选的模块。
4.队伍的部分添加了招募人员情况，以及是否已经截止。并准备改成报名，队长确认是否接受入队的形式，而不是直接联系队长。
5.我的界面增加了我的集市，我的反馈两个部分。
6.比赛组队部分根据小程序比赛老师的反馈增加了比赛简介的部分。
7.美化了比赛组队部分的UI，比如跳转进对应比赛下的队伍列表或者比赛简介的时候，上方navigationbar会根据其比赛类型进行颜色的变化。
8.修复了聊天界面的bug，现在每次打开会自动滚动到最下方，当发送了新的消息时，也会自动滚到最下，并且发送完后会清空输入框。
