# [首页查询更多项目](https://github.com/GraduationProject-weixin) 包安装运行


# 50470wxapp基于的物流管理系统-小程序

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1NvtMeFEiw?p=122)


# 系统概述
物流管理系统的设计与开发是指对该系统的各个功能模块进行详细设计，力求每个模块都能够满足用户的要求，系统开发完成后还需对系统进行单元测试和系统测试，发现系统中存在的问题并解决，确保系统正常稳定的运行。物流管理系统工作原理图如图4-1所示：

![](/md/blog.011.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统结构设计必须要满足用户的业务需求，系统结构设计完成后要形成系统结构设计文档，开发人员就可根据模块接口说明进行接口开发，接口开发完需进行功能测试，目的是发现并解决系统漏洞，同时还得保证系统的可扩展性和稳定性，满足用户对系统的要求。系统设计需满足以下要求：

1. 安全性
1. 易用性
1. 柔软性
1. 柔软性
1. 扩展性

物流管理系统的整体结构设计主要分为三大部分：管理员、用户和员工。整体结构设计如图4-2所示。

![](/md/blog.012.png)

图4-2 整体结构设计图
## 4.3 数据库设计
本系统依赖于MySQL数据库来储存信息，系统完成后，所有需要的数据都要从数据库中读取，这也意味着无论是插入、更新还是删除操作，只要对数据有改动的操作都需要与数据库交互，因此，系统的全部数据都要储存在数据库，必须保证数据库在未经授权情况下不得进行删除表结构等危险操作，而且要保证表中字段的准确性。
### 4.3.1 数据库设计原则
1. 从上而下
1. 从下至上
1. 逐渐扩大
1. 结合方法
### 4.3.2 数据库实体
E-R图，即实体-联系图，它是一种通过对实例进行抽象，以可视化的方式来描述现实世界的概念模型。根据需求分析绘制出数据库的E-R图，能够直观地映射出各个表之间的关系。

本系统的实体属性图如下图所示：

1、仓储信息实体图如图4-3所示：

![](/md/blog.013.png)

图4-3仓储信息实体图

2、物流信息实体图如图4-4所示：

![](/md/blog.014.png)

图4-4物流信息实体图

3、物流公司实体图如图4-5所示：

![](/md/blog.015.png)

图4-5物流公司实体图
### 4.3.3 数据库表设计
数据库的主要作用是储存和管理整个系统的数据。数据库中的数据在保证一定的独立性和安全性的前提下，也要有某种程度的共享，在一定条件范围内可以共享某些数据。必须保证数据库中每张表里存储的数据是安全的，如果没有经过身份认证，就无法查阅及使用。在进行数据库设计时，应根据具体情况，进行有针对性的数据库开发和设计。下面列举主要数据库表结构。

表4-1：配送信息

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|peisongshijian|datetime||配送时间|||
|peisongyuan|varchar|200|配送员|||
|yuangongxingming|varchar|200|员工姓名|||
|bumen|varchar|200|部门|||
|wuliuxinxi|longtext|4294967295|物流信息|||
|yunshuluxian|varchar|200|运输路线1|||
|crossuserid|bigint||跨表用户id|||
|crossrefid|bigint||跨表主键id|||

表4-2：物流资讯

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|title|varchar|200|标题|||
|introduction|longtext|4294967295|简介|||
|picture|longtext|4294967295|图片|||
|content|longtext|4294967295|内容|||

表4-3：装卸搬运

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|zhuangxieshijian|datetime||装卸时间|||
|zhuangxieyuan|varchar|200|装卸员|||
|yuangongxingming|varchar|200|员工姓名|||
|bumen|varchar|200|部门|||
|wuliuxinxi|longtext|4294967295|物流信息|||
|yunshuluxian|varchar|200|运输路线3|||
|crossuserid|bigint||跨表用户id|||
|crossrefid|bigint||跨表主键id|||

表4-4：运输信息

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|yunshushijian|datetime||运输时间|||
|yunshuyuan|varchar|200|运输员|||
|yuangongxingming|varchar|200|员工姓名|||
|bumen|varchar|200|部门|||
|wuliuxinxi|longtext|4294967295|物流信息|||
|yunshuluxian|varchar|200|运输路线2|||
|crossuserid|bigint||跨表用户id|||
|crossrefid|bigint||跨表主键id|||

表4-5：员工

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|yuangonggonghao|varchar|200|员工工号|||
|mima|varchar|200|密码|||
|yuangongxingming|varchar|200|员工姓名|||
|bumen|varchar|200|部门|||
|xingbie|varchar|200|性别|||
|nianling|int||年龄|||
|shoujihao|varchar|200|手机号|||
|shenfenzhenghao|varchar|200|身份证号|||
|zhaopian|longtext|4294967295|照片|||
|jiatingzhuzhi|varchar|200|家庭住址|||
|sfsh|varchar|200|是否审核||待审核|
|shhf|longtext|4294967295|审核回复|||

表4-6：仓储信息

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|daodashijian|datetime||到达时间|||
|cangchuyuan|varchar|200|仓储员|||
|yuangongxingming|varchar|200|员工姓名|||
|bumen|varchar|200|部门|||
|wuliuxinxi|longtext|4294967295|物流信息|||
|yunshuluxian|varchar|200|运输路线4|||
|crossuserid|bigint||跨表用户id|||
|crossrefid|bigint||跨表主键id|||

表4-7：物品分类

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|wupinfenlei|varchar|200|物品分类|||

表4-8：物流信息

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|gongsimingcheng|varchar|200|公司名称|||
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|jijianshijian|datetime||寄件时间|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|ispay|varchar|200|是否支付||未支付|

表4-9：物流公司

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|gongsimingcheng|varchar|200|公司名称|||
|fuzeren|varchar|200|负责人|||
|lianxidianhua|varchar|200|联系电话|||
|youxiang|varchar|200|邮箱|||
|gongsidizhi|varchar|200|公司地址|||
|gongsitupian|longtext|4294967295|公司图片|||
|clicktime|datetime||最近点击时间|||

表4-10：收货信息

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|kuaididanhao|varchar|200|快递单号|||
|yonghuzhanghao|varchar|200|用户账号|||
|yonghuxingming|varchar|200|用户姓名|||
|shouji|varchar|200|手机|||
|wupinmingcheng|varchar|200|物品名称|||
|wupinfenlei|varchar|200|物品分类|||
|shuliang|int||数量|||
|zhongliang|float||重量kg|||
|feiyong|float||费用|||
|shoujianren|varchar|200|收件人|||
|shoujiandizhi|varchar|200|收件地址|||
|lianxishouji|varchar|200|联系手机|||
|quhuofangshi|varchar|200|取货方式|||
|zhifuleibie|varchar|200|支付类别|||
|daodashijian|datetime||到达时间|||
|shouhuozhanghao|varchar|200|收货账号|||
|shouhuoxingming|varchar|200|收货姓名|||
|shouhuoriqi|date||收货日期|||
|crossuserid|bigint||跨表用户id|||
|crossrefid|bigint||跨表主键id|||

表4-11：用户

|字段名称|类型|长度|字段说明|主键|默认值|
| :-: | :-: | :-: | :-: | :-: | :-: |
|id|bigint||主键|主键||
|addtime|timestamp||创建时间||CURRENT\_TIMESTAMP|
|yonghuzhanghao|varchar|200|用户账号|||
|mima|varchar|200|密码|||
|yonghuxingming|varchar|200|用户姓名|||
|touxiang|longtext|4294967295|头像|||
|xingbie|varchar|200|性别|||
|nianling|int||年龄|||
|shouji|varchar|200|手机|||


# 5界面设计与功能实现
5.1小程序端实现

5.1.1注册登录界面的实现

第一次使用本小程序的使用者，首先是要进行注册，点击“注册”，然后就会进入到注册的页面里面，将用户信息录入注册表，确认信息正确后，系统才会进入登录界面，用户登录成功后可使用本小程序所提供的所有功能。注册界面如图5-1所示。

![](/md/blog.016.png)

图5-1 注册界面

首先双击打开小程序客户端，连上网络之后会显示出本系统的登录界面，这是进入小程序的初始页面“登录”，能成功进入到该登录界面则代表小程序的开启是成功的，接下来就可以操作本系统所带有的其他所有的功能。登录界面如图5-2所示。

![](/md/blog.017.png)

图5-2 登录界面

5.1.2 小程序首页功能的实现

小程序首页是用户注册登录后进入的第一个界面，在这里，人们能够看到小程序的导航条，内容包括物流公司、我的等。小程序首页界面如图5-3所示。

![](/md/blog.018.png)

图5-3 小程序首页界面图

物流公司：在物流公司界面可以查看到公司名称、图片、负责人、联系电话、邮箱、公司地址等详细信息；并根据需要进行寄件操作；物流公司详情如图5-4所示。

![](/md/blog.019.png)

图5-4物流公司详情界面图

5.1.3用户功能

用户登录成功后，点击“我的”进入我的页面，在我的页面可以对个人中心、物流信息、配送信息、运输信息、装卸搬运、仓储信息等进行详细操作。用户功能界面如图5-5所示。

![](/md/blog.020.png)

图5-5用户功能界面图

5.2 小程序后台功能的实现

后台登录，管理员和员工通过填写用户名和密码等信息进行登录操作，如图5-6所示。

![](/md/blog.021.jpeg)

图5-6后台登录界面图
### 5.2.1 管理员功能的实现
管理员登录进入小程序可以查看到个人中心、用户管理、员工管理、部门管理、物品分类管理、物流公司管理、物流信息管理、配送信息管理、运输信息管理、装卸搬运管理、仓储信息管理、系统管理等功能进行详细操作，如图5-7所示。

![](/md/blog.022.png)

图5-7管理员功能界面图

用户管理；在用户页面输入用户账号进行查询，新增或删除用户列表，并对用户详细信息进行详情、修改或删除操作；如图5-8所示。

![](/md/blog.023.png)

图5-8用户管理界面图

员工管理；在员工页面输入员工工号、员工姓名、选择部门和是否通过进行查询，新增或删除员工列表，并对员工详细信息进行详情、修改或删除操作；如图5-9所示。

![](/md/blog.024.png)

图5-9员工管理界面图

物流公司管理；在物流公司页面输入公司名称进行查询，新增或删除物流公司列表，并对物流公司详细信息进行详情、修改或删除操作；如图5-10所示。

![](/md/blog.024.png)

图5-10物流公司管理界面图

物流信息管理；在物流信息页面输入快递单号、用户姓名和选择物品分类进行查询、新增或删除物流信息列表，并对物流详细信息进行详情、安排配送、修改或删除操作；如图5-11所示。

![](/md/blog.025.png)

图5-11物流信息管理界面图

配送信息管理；在配送信息页面输入快递单号、用户姓名、物品分类和员工姓名进行查询或删除配送信息列表，并对配送详细信息进行详情、安排运输、修改或删除操作；如图5-12所示。

![](/md/blog.026.png)

图5-12配送信息管理界面图

运输信息管理；在运输信息页面输入快递单号、用户姓名、物品分类和员工姓名进行查询或删除运输信息列表，并对运输详细信息进行详情、安排装卸、修改或删除操作；如图5-13所示。

![](/md/blog.027.png)

图5-13运输信息管理界面图

装卸搬运管理；在装卸搬运页面输入快递单号、用户姓名、物品分类和员工姓名进行查询或删除装卸搬运列表，并对装卸搬运详细信息进行详情、仓储、修改或删除操作；如图5-14所示。

![](/md/blog.028.png)

图5-14装卸搬运管理界面图

仓储信息管理；在仓储信息页面输入快递单号、用户姓名、物品分类和员工姓名进行查询或删除仓储信息列表，并对仓储详细信息进行详情、修改或删除操作；如图5-15所示。

![](/md/blog.029.png)

图5-15仓储信息管理界面图

系统管理；在物流资讯页面输入标题进行查询、新增或删除物流资讯列表，并对物流资讯详细信息进行详情、修改或删除操作；还可根据需要对轮播图管理、关于我们和系统简介进行详细操作；如图5-16所示。

![](/md/blog.030.png)

图5-16系统管理界面图
### 5.2.2 员工功能的实现
员工登录进入小程序可以查看到个人中心、配送信息管理、运输信息管理、装卸搬运管理、仓储信息管理等功能进行详细操作，如图5-17所示。

![](/md/blog.031.png)

图5-17员工功能界面图















