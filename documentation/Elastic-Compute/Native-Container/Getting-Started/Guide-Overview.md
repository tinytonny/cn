
# 入门指南概述

**初始配置**
**注册京东云账户**
若您已有京东云账号，可跳过本步骤进行后续设置。
若您还未注册京东云账号，可在京东云官网进行注册，请参考注册京东云。当您完成账号注册后，需要您激活账号，如下图所示。image.png

认证账号

为了正常使用容器服务，您还需要对您的账号进行认证。

进入实名认证页面，可选择认证类型为个人或企业。请参考实名认证。


**创建私有网络（必选）**

1.打开控制台，选择 网络>>私有网络 ，进入私有网络列表页；

2.选择创建私有网络所属地域，点击“创建”按钮；

3.地域选择：在此步骤仍可以选择创建私有网络的地域，如果所选地域限额已满，可以通过提交工单提升限额；

4.设置私有网络名称：名称不可为空，只支持中文、数字、大小写字母、英文下划线“_”及中划线“-”，且不能超过32字符；

5.设置私有网络的CIDR：设置私有网络的边界，CIDR只能是内网网段，可选范围为10.0.0.0(掩码为16~28)、172.16.0.0~172.31.0.0(掩码为16~28)、192.168.0.0(掩码为16~28)。也可不预设CIDR，此时vpc的边界将随其中子网的网段自动伸缩，建议对网络理解深刻的用户选择无预设CIDR的私有网络。

6.设置私有网络描述：描述可以为空，只支持中文、数字、大小写字母、英文下划线“_”，且不能超过256字符；

7.点击【确定】后即可进入“控制台”查看创建的私有网络；


**创建子网（必选）**

1.打开控制台，选择  网络 >>私有网络>>子网 ，进入子网列表页；

2.选择创建子网所属地域，点击“创建”按钮；

3.地域选择：在此步骤仍可以选择创建子网的地域，如果所选地域限额已满，可以通过提交工单提升限额；

4.选择所属私有网络，子网必须创建在某个私有网络内。

5.创建子网：支持同时创建多个子网，输入子网名称、子网CIDR、关联的路由表、描述等信息。

6.子网的CIDR只能是内网网段，可选范围为10.0.0.0(掩码为16~28)、172.16.0.0~172.31.0.0(掩码为16~28)、192.168.0.0(掩码为16~28)。

7.多个子网的CIDR之间不可重叠，若所属私有网络已预设了CIDR，则子网的CIDR不能超过私有网络的边界。

8.设置子网名称：名称不可为空，只支持中文、数字、大小写字母、英文下划线“_”及中划线“-”，且不能超过32字符；

9.选择子网关联的路由表，每个子网能够关联一张路由表，且必须关联一张路由表。

10.设置子网描述：描述可以为空，只支持中文、数字、大小写字母、英文下划线“_”及中划线“-”，且不能超过256字符；

11.点击【确定】后即可进入“控制台”查看创建的子网；


**创建安全组（可选）**

安全组提供实例级别的网络访问控制。您需要在安全组中添加规则，以便能够使用实现一些访问接入，比如允许SSH 从您本地 IP 地址连接到实例。为方便您使用，京东云为每一个私有网络均提供了三个默认安全组以便您快速选择，分别是默认全开安全组、默认Linux开22端口及默认Windows开3389端口；

1.进入京东云控制台，选择 弹性计算 >>容器服务>>安全组页面，点击【创建】，弹出创建弹框；

TimLine截图20171228152929.png

2.首先您需要选择安全组所在的地域和私有网络，安全组只能应用在相同私有网路下的容器。您可以为当前已创建的私有网络新建安全组，也可以点击“新建私有网络“按钮，跳转到新建私有网络页面，创建新的私有网络。单个私有网络下最多可以创建50个安全组，如所选择的私有网络下安全组数量已达到50个，则会提示“所选私有网络资源安全组限额已达到50个”，您需要重新选择其他私有网络。

3.之后输入安全组名称及描述，描述用于对安全组规则的额外说明，如“开放了入口方向80、443端口和出口方向的”；建议您用安全组的使用场景或功能作为安全组的名称，如“Web服务器集群_开放80端口”。

4.新建安全组默认all drop所有入口、出口流量。



确定实例所在地域
京东云不同地域之间完全隔离，保证不同地域间最大程度的稳定性和容错性。当前覆盖国内华北-北京、华南-广州、华东-宿迁及华东-上海四地域。目前容器在华北-北京、华东-上海开通，未来我们将逐步增加更多服务地域以满足您业务需求。
选择地域时建议考虑以下几点：


实例与其他京东云产品间的部署关系。

不同地域之间的云产品默认不能通过内网通信。

实例默认不可跨地域内网互访，默认不可跨地域访问云数据库及云缓存等

实例绑定公网IP、安全组时仅支持绑定同地域下的公网IP、安全组；实例绑定云硬盘时仅支持绑定同可用区下的云硬盘

上述内网互通是均指同一账户下的资源互通，不同账户的资源内网完全隔离。



选择实例配置

正式部署业务前建议您使用按配置计费实例来进行性能测试，找到与您业务量匹配的实例规格及其他资源配置。可参考

实例配置推荐。