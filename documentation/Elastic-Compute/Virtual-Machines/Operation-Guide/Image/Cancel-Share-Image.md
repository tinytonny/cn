# 取消共享私有镜像

## 注意事项
* 取消共享后，原被共享用户将无法再使用该镜像创建实例，同时使用该镜像创建的实例也无法重置为原始系统状态。

## 操作步骤
1. 访问[镜像控制台][1]，或访问[京东云控制台][2]点击左侧导航栏【弹性计算】-【云主机】-【镜像】进入镜像列表页。
2. 选择【私有】TAB，在列表中选定您要取消共享的私有镜像。
3. 您可以在列表操作列点击【共享镜像】操作，从弹窗内显示的已共享账号中，选择要取消共享的账号，点击操作列中的【取消共享】操作，则对应账号对此私有镜像的共享被取消，该镜像会自动从对应账号的“共享镜像”列表中删除。也可以点击镜像名称进入详情页，选择“镜像共享”TAB，查看该镜像已共享的账号，点击【取消共享】来实现。
![](../../../../../image/vm/Operation-Guide-Image-unshare1.png)
![](../../../../../image/vm/Operation-Guide-Image-unshare2.png)



  [1]: ./images/Operation-Guide-Image-unshare2.png "Operation-Guide-Image-unshare2.png"
  [2]: https://cns-console.jdcloud.com/host/compute/list