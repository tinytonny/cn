# 创建工作流

前置条件：需确保您已经在‘数据计算服务’的‘数据仓库’中创建数据表并上传数据，工作流运行结果输出到数据仓库，因此还需创建结果表。

**操作步骤：**

1.        选择计算节点地域；

2.        点击‘新建定义’创建工作流：

![创建工作流1](../../../../../image/Data-Factory/create-step1.png)

3.        设置spark任务：

拖拽SPARK模块到中心区，添加spark任务名称、描述、选择类型、补全脚本。脚本类型支持sql、python、scala三种，保存后用鼠标连接工作流。

![创建工作流2](../../../../../image/Data-Factory/create-step2.png)

![创建工作流3](../../../../../image/Data-Factory/create-step3.png)

右键单击SPARK任务，可以对任务进行启动、编辑、查看日志、删除及重试。

4.        设置数据集成任务

拖拽数据集成到屏幕中心，弹出编辑菜单，进行数据同步。

![创建工作流4](../../../../../image/Data-Factory/create-step4.png)

点击‘确定’按钮进行保存：

![创建工作流5](../../../../../image/Data-Factory/create-step5.png)

右键单击数据集成任务，可以对任务进行启动、编辑、查看日志、删除及重试。

5.        选择‘设置’Tab页，对工作流进行保存，根据需求设置执行策略：

![创建工作流6](../../../../../image/Data-Factory/create-step6.png)

6.        设置报警信息：

![创建工作流7](../../../../../image/Data-Factory/create-step7.png)
