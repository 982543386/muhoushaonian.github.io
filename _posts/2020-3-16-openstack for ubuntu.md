---
layout: post
title: OpenStack For Ubuntu
description: 善睐产品开发相关[互联网+比赛]
tag: 云计算
---

### 先导知识

最初的云计算便是由Google与Amazon分别提出,核心理念之一就是通过云计算服务降低用户对资源拥有的成本.

最为普遍接受云计算的定义是NIST的定义:
    云计算是一种按使用量付费的服务模式,这是一种能够提供可用的、便捷地、按需求的网络访问模式
    计算共享池能够快速的为用户提供网络、服务器、存储、应用软件及其他服务，并且只需要花费很少的管理时间

云计算三个服务层次:
    laas:提供云计算基础设施
    paas:提供云计算中的开发和分发应用的解决方案
    Saas:提供云计算基础设施上的应用程序

![](/images/post_image/云计算服务类型.png)

### 概括

    The OpenStack project is an open source cloud computing platform that supports all types of cloud environments. The project aims for simple implementation, massive scalability, and a rich set of features. Cloud computing experts from around the world contribute to the project.

OpenStack通过各种补充服务[Compute/Networking/Object Storag/...]来提供服务(Infrastructure-as-a-Servicce: laas)

![](/images/post_image/openstack服务类型.png)

在对基础openstack服务安装、配置、操作和故障诊断熟悉后,使用生产架构部署时需考虑如下步骤:

    确定并实施必要的核心和可选服务，以满足性能和冗余要求
    使用诸如防火墙，加密和服务策略的方式加强安全
    使用自动化工具，如Ansible,Chef,Puppet或者Salt实现自动部署和管理生产环境

TODO: 深入了解产品架构 <https://docs.openstack.org/arch-design/>

**硬件需求**
控制节点运行身份认证服务、镜像服务、管理部分计算和网络服务/需要最少两块网卡

计算结点要求最少两个网络接口

块设备存储和对象存储可选

**网络**
TODO: 深入理解

### 环境
在这个part里面主要配置控制节点和一个计算节点

**安全**
TODO: 待补充

**主机网络**
在按照选择的架构，完成各个阶段操作系统安装以后，必须配置网络接口

TODO: 待补充

**网络时间协议**
利用Chrony完成在不同节点同步服务实现[NTP:网络时间协议，用来同步网络设备的时间]


### 参考

《Linux就该这么学》
