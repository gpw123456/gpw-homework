                               制作HTLM5游戏
     首先 启动Construct 2.单击File按钮，然后选择New，
     新建一个文本。
     1平铺的背景
     我们想要的第一件事是重复的背景图块。该平铺背景对象
     可以为我们做到这一点。首先，这是你的背景纹理 - 右
     键单击​​它并将其保存到你的计算机某处：![在这里插入图片描述](https://img-blog.csdn.net/20181007111132631?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
     2双击布局中的空格以插入新对象。（稍后，如果
     它已满，您也可以右键单击并选择“ 插入新对象”。）
     出现“ 插入新对象”对话框后，
     双击“平铺背景”对象将其插入。![在这里插入图片描述](https://img-blog.csdn.net/20181007111448295?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
     3然后会出现一个十字准线，
     指示放置对象的位置。单击布局
     中间附近的某个位置![在这里插入图片描述](https://img-blog.csdn.net/20181007111647955?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)调整它以覆盖整个布局。
     确保选中它，然后左侧的属性栏应显示对象
     的所有设置，包括其大小和位置。将其位置设置为0,0
     （布局的左上角），并将其大小设置为1280,1024
     （布局的大小适合即可）。
     4为了防止不小心选择平铺的背景，
     除非我们锁定它，使其无法选择。
     让我们使用分层系统来做到这一点。
        布局可以包含多个图层，您可以
        使用这些图层对对象进行分组。
        想象一下像玻璃板堆叠在一起的层，
        每个板上都涂有物体。它允许您轻松
        地排列哪些对象出现在其他对象之上，
        并且可以隐藏，锁定图层![在这里插入图片描述](https://img-blog.csdn.net/20181007112417773?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)背景”旁边的小挂锁图标，
        它将被锁定。这意味着您将无法选择任何内容
  5      现在，确保在图层栏中选择了
      “主”图层，
        所选图层是活动图层。所有新
        插入的对象都插入到活动层中，
        因此如果未选中，我们将意外
        插入到错误的层。活动图层显示
        在状态栏中。
  6  游戏对象插入
       双击以插入新对象
       双击 “Sprite”对象。
       当鼠标变为十字准线时，
       单击布局中的某个位置。工具提示应         
       为“Main”。（请记住这是活动布局。）
       弹出纹理编辑器。单击打开图标，然后
       加载四个纹理中的一个。
        关闭纹理编辑器，保存更改,
        现在应该在布局中看到对象
    7添加行为
      单击播放器以选择它。在属性栏中!
      [在这里插入图片描述](https://img-blog.csdn.net/2018100711330915?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)单击行为对话框中的绿色“添加行为”图标
      9 使用control + drag，单击并拖
      动Monster对象，创建7或8个新怪物。
         ![在这里插入图片描述](https://img-blog.csdn.net/20181007113617972?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
         10  不同对象的活动
         单击顶部的“ 事件表1”
         选项卡以切换到“ 事件”
         表编辑器。事件列表称为事件表
         ，您可以为游戏的不同部分
         或组织设置不同的事件表。
         事件表还可以“包含”
         其他事件表。![在这里插入图片描述](https://img-blog.csdn.net/20181007114103110?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

         简而言之，事件基本上如下所示：
         是否符合所有条件？
         ---> 是：运行所有事件的动作。
        ---> 否：转到下一个事件
        （不包括任何子事件）。
![在这里插入图片描述](https://img-blog.csdn.net/20181007114248150?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)添加          各种活动并且赋予指令
![](https://img-blog.csdn.net/20181007114655351?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI2ODM5Mw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
11  游戏模型基本完成。
