# seeSCNUZone
存放SCNUZone的最新代码，文件已加密

### 华师同校SCNUZone小程序码（长按扫描小程序码查看示例）
<center>
 <img src="/images/scnuzone.png" margin=20% width=30% />
</center>

### 以下是主要功能页面的截图。

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/index.png" width=30% />
 <img src="/images/my.png" width=30% />
 <img src="/images/find.png" width=30% />
</div>

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/delegate.png" width=30% />
 <img src="/images/team.png" width=30% />  
 <img src="/images/mall.png" width=30% />
</div>

<center>
 <img src="/images/personcard.png" margin=20% width=30% />
</center>

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
1.这次提交是一个未完成版的大改动。首先功能上引入了华师圈，二手闲置两个大版块。将校园委托，二手闲置，比赛组队，发现四个板块作为一级入口方在上方，下部的tabbar是首页，华师圈，消息，我的。<br>
2.委托分了委托、他能提供两个部分来展示内容，而闲置则是出售、求购。<br>
3.闲置的教材书籍板块加了一个根据学院、年级筛选的模块。<br>
4.队伍的部分添加了招募人员情况，以及是否已经截止。并准备改成报名，队长确认是否接受入队的形式，而不是直接联系队长。<br>
5.我的界面增加了我的集市，我的反馈两个部分。<br>
6.比赛组队部分根据小程序比赛老师的反馈增加了比赛简介的部分。<br>
7.美化了比赛组队部分的UI，比如跳转进对应比赛下的队伍列表或者比赛简介的时候，上方navigationbar会根据其比赛类型进行颜色的变化。<br>
8.修复了聊天界面的bug，现在每次打开会自动滚动到最下方，当发送了新的消息时，也会自动滚到最下，并且发送完后会清空输入框。

#### 2018年8月21日 星期二
1.完善了二手闲置板块的UI<br>
2.将first的登陆页去掉，改用了用户体验更好的授权方式，兼容用户拒绝授权的情况<br>
3.即时聊天功能完成，每5s轮训一次是否有新消息的，使用了```setInterval```<br>

#### 2018年8月26日 星期天
1.美化了first欢迎页，本来是准备去掉的，但是因为有token的原因，有个时间差，不然index的api还没拿到token就申请了，就会出问题，所以还是得要一个欢迎页面<br>
2.较大幅度的换了一套UI界面，包括颜色，icon等<br>
3.比赛组队部分 申请入队、管理队伍这一块的功能全部完成<br>
4.完善了反馈的提交，申请添加新比赛的添加<br>
5.闲置的添加<br>

#### 2018年9月3日 星期一
1.完善了闲置&求购部分<br>
2.修复了一些用户体验的部，较为琐碎，不提<br>

#### 2018年9月26日 星期三
比较长时间没写更新日志了哈哈，大概就<br>
1.组队增加了上传群聊二维码的图片，为了方便委托和闲置的支付，增加了上传收款码以及展示的功能<br>
2.增加了“找人委托”的模块，与“寻找队友”一起，前者提供委托技能分类检索，后者提供想参加的比赛分类检索，大幅度提升用户体验<br>
3.聊天界面可以快速打开对方的收款码并保存<br>
4.增加了公众号关注的提醒部分，引流到公众号上，并提供消息提醒<br>

#### 2018年9月29日 星期六
1.增加了首页比赛banner轮播图，点击可跳转进对应的组队模块内，并可以查看模块简介等<br>

#### 2018年11月24日 星期六
1.将入口提前了一级，用户刚进来就可以在四个板块切换查看信息，用户体验更好<br>
2.增加了委托修改功能<br>
3.完善了实名制权限限制以及提示引导，用户体验更佳<br>

<center>
 <img src="/images/newindex.png" margin=20% width=30% />
</center>
