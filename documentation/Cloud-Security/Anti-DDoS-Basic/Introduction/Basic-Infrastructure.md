# 基础架构

    DDos基础防护架构主要由管理中心设备、检测设备和清洗设备三个模块组成。
    
## 业务架构

基础防护业务架构如下图所示：

![创建实例](https://github.com/jdcloudcom/cn/blob/edit/image/Basic%20Anti-DDos/Infrastructure01.png)

备注：1、镜像流量到检测设备 2、检测设备检测到攻击，向管理中心通告攻击信息
      3、管理中心收到攻击信息后通知清洗设备开启清洗
      4、引流到清洗设备进行流量清洗，并回注清洗后的干净流量
      5、正常流量

|名称|描述|
| - | - |
|管理中心|主要负责接收攻击信息，并发送清洗策略到清洗设备，指导清洗设备进行流量清洗。
|清洗设备|主要依据管理中心下发的清洗策略，对攻击流量进行清洗，并将清洗后的干净流量进行回注。
|检测设备|主要对流量成分进行分析，以确定是否有攻击发生。如果有攻击发生就发送攻击信息到管理中心。

## 相关参考

- [什么是DDoS基础防护](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Overview.md)
- [核心概念](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Core-Concepts.md)
- [应用场景](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Application-Scenarios.md)
- [基本功能](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Functions.md)
- [使用限制](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Restrictions.md)
