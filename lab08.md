1 开始构建
 当按下左右箭头键时，平台对象左右移动（您可以更改这些键，如果您愿意，可以更改为“A”和“D”，或者在移动设备上使用触摸手势替换它们）。

-当按下“Shift”键时，它们会跳转（您可以再次更改此键或替换触摸手势）。

-当他们没有固体物体时，它们会掉下来。
2 构建播放布局
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174051827.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==,size_16,color_FFFFFF,t_70)  


3 单击项目栏中的PlayerImages对象，然后单击左侧的“动画 - 编辑”
  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174119240.png)


  单击项目栏中的“Flooring”对象，然后单击“属性栏”中的“编辑行为 - 添加/编辑”。给它“稳固”行为(上图，右上角）
  对“Wall”对象执行相同操作。
  单击项目栏中的“播放器”对象，并将其设置为“平台”行为（在“移动”下）
请记住，我们需要将PlayerImages对象固定到Player对象。因此，单击项目栏中的“PlayerImages”对象，并为其指定“Pin”行为（在“General”下）。
a  条件：系统 - > 在布局开始
 行动：PlayerImages - > 输入密码：PIN到对象 - >为对象，选   择播放器对象
b 操作：PlayerImages - > 设置动画 - >为动画，键入“站立”在（休假“发件人”在'开始'）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174140472.png)

c 条件：播放器 - > 平台：移动
动作：PlayerImages - > 设置动画 - > 动画，输入“正在运行”
 
d  条件：键盘 - > 键已关闭 - >按左箭头键
操作：PlayerImages - > 设置镜像（在“ 动画 ”下）

e  条件：键盘 - > 键已关闭 - >按右箭头键
操作：PlayerImages - > 设置镜像 - >这次选择' Not mirrored '

f 条件：玩家 - > 平台：按墙 - > 侧：左
操作：PlayerImages - > 设置动画 - >输入“站立”（离开'从'开始'）
g 条件：玩家 - > 平台：按墙 - > 侧：右
操作：PlayerImages - > 设置动画 - >“站立”

h  右键单击“Platform has wall to left”条件并选择“Add another condition”：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174316500.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==,size_16,color_FFFFFF,t_70)


i   条件：玩家 - > 外部布局（在“ 大小和位置 ”下）
动作：玩家 - > 设置位置 - > X：370，Y：100
首先，添加主要事件：
条件：玩家 - > 平台登陆
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174341805.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==,size_16,color_FFFFFF,t_70)

  更改是PlayerImages运行速度(调整帧数）。
  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174400524.png)

评分标准

添加全局变量：score（将默认类型保留为“Number”，将初始值保留为0）。
添加全局变量：health（将默认类型保留为“Number”，并将初始值设置为3）。
当蒂姆退出布局并退回到顶部时，需要恢复得分的初始值，并且他的健康等级需要降低一个。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181111174414249.png)

游戏基本完成。
