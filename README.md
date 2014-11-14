#5秒轻游戏android客户端简明概要设计说明书

***
##一、概述
本说明书旨在进一步细化在需求分析阶段得出的软件总体概貌，把它加工成在程序细节上接近于源程序的软件表示


##二、场景视图
![用例图](/images/case.jpg)
![活动图](/images/exercise.jpg)
![活动图](/images/exercise1.jpg)

##三、逻辑视图
![时序图](/images/time.jpg)
![时序图](/images/time1.jpg)

##四、开发视图
###1.包管理

+ 界面相关：
        com.wumiao.games.ui.activity
        com.wumiao.games.ui.fragment
+ 工具相关：
        com.wumiao.games.util
+ 常量、枚举：
        com.wumiao.games.constant
+ 网络相关：
        com.wumiao.games.net
+ 适配器：
        com.wumiao.games.adapter
+ 自定义：
        com.wumiao.games.customcontrol
+ 数据库：
        com.wumiao.games.db
+ 数据实体：
        com.wumiao.games.bean
+ 全局：
        com.wumiao.games.application
+ 服务：
        com.wumiao.games.service
+ js交互：
        com.wumiaogames.jsAndroid


###2.命名规范

#### 文件名命名：
+ **资源文件：**不同的场景相应的前缀，全小写，以“_”连接
例如:
        activity_main.xml
        flagment_game.xml
        dialog_about.xml
        item_gamelist.xml
        main_bt.png
        game_bt.png
        about_textview_bg.png
        gamelist_iv.png

+ **类文件：**不同的场景相应的后缀，首字母大写
例如：
        MainActivtity.java
        BaseFragment.java
        HttpUtil.java
        PersonBean.java
        BaseAdapter.java

####类名，方法名，属性

+ **类名：首字母大写：**
例如：
        MainActivity
        GameActivity
        UserBean

+ **方法名：** 第一个字母小写，其余首字母大写
例如：
        initTextView()
        getGameData()

+ **属性名：**
`常量属性，枚举：`全大写，以下划线连接
例如：
        TAB_GAME
        TAB_SHOW
        ONE_TWO_THREE
`普通属性：`以小写m开头，其余首字母大写
 例如：
        mContext
        mArrayList

 `静态属性：`以s开头，其余首字母大写
例如：
        sSum
        sMoney

 `局部变量：`首字母小写
例如：
        person
        student

![类图](/images/class.jpg)
![组件图](/images/subassembly.jpg)
##五、过程视图
+ **图片加载**
采用第三方SDK imageloader进行异步加载，图片缓存等
+ **拉取数据**
采用第三方SDK unirest 进行get/post/delete/put等网络请求