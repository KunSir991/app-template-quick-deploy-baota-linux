# 快速部署宝塔运维面板

## 概述

宝塔运维面板是提升运维效率的服务器管理软件，支持一键LAMP/LNMP/集群/监控/网站/FTP/数据库/JAVA等100多项服务器管理功能。

宝塔面板官方网站：[https://www.bt.cn](https://www.bt.cn)

本服务支持在已有的ECS实例（Linux）上部署和新建ECS实例（Linux或Windows）部署。

## 计费说明

宝塔Linux面板在计算巢上的费用主要涉及：

- 所选vCPU与内存规格
- 磁盘容量
- 公网带宽

计费方式：按量付费（小时）

预估费用在创建实例时可实时看到。

## 部署架构

宝塔Linux面板社区版是单机部署架构。

## RAM账号所需权限

宝塔面板服务需要对ECS、VPC等资源进行访问和创建操作，若您使用RAM用户创建服务实例，需要在创建服务实例前，对使用的RAM用户的账号添加相应资源的权限。添加RAM权限的详细操作，请参见[为RAM用户授权](https://help.aliyun.com/document_detail/121945.html)
。所需权限如下表所示。

| 权限策略名称                          | 备注                         |
|---------------------------------|----------------------------|
| AliyunECSFullAccess             | 管理云服务器服务（ECS）的权限           |
| AliyunVPCFullAccess             | 管理专有网络（VPC）的权限             |
| AliyunROSFullAccess             | 管理资源编排服务（ROS）的权限           |
| AliyunComputeNestUserFullAccess | 管理计算巢服务（ComputeNest）的用户侧权限 |
| AliyunCloudMonitorFullAccess    | 管理云监控（CloudMonitor）的权限     |

## 选择ECS实例部署

选择ECS实例部署支持Linux操作系统。

### 前提条件
1. 所选ECS实例可以访问公网并且安全组已打开8888端口
2. 所选ECS实例没有装过其它环境如Apache/Nginx/php/MySQL 
3. 系统兼容性：Centos7.x/Alibaba Cloud Linux2 > Debian10 > Ubuntu 20.04 > Centos8 stream/Alibaba Cloud Linux3 > Ubuntu 18.04

### 操作步骤
1. 单击[部署链接](https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceId=service-8b13e60726a64ffbabc9)，进入服务实例部署界面。
2. 选择目标ECS实例，点击下一步：确认订单。
    <img src="1.jpg" width="100%" align="bottom"/>
3. 点击立即创建，等待服务实例创建完成。
    <img src="2.jpg" width="100%" align="bottom"/>
4. 服务实例创建成功后，进入服务实例详情页。在概览页可获取宝塔面板登录信息。 
    <img src="5.png" width="100%" align="bottom"/>
5. 点击外网面板地址，登录宝塔面板。
    <img src="6.jpg" width="100%" align="bottom"/>


## 新建ECS实例部署

新建ECS实例部署支持Linux和Windows两种操作系统。

### 操作步骤
1. 单击[部署链接](https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceId=service-8b13e60726a64ffbabc9)，进入服务实例部署界面。
2. 选择新建ECS实例并根据界面提示配置参数，配置完成后点击下一步：确认订单。
    <img src="3.jpg" width="100%" align="bottom"/>
3. 点击立即创建，等待服务实例创建完成。
    <img src="4.jpg" width="100%" align="bottom"/>
4. 服务实例创建成功后，进入服务实例详情页。在概览页可获取宝塔面板登录信息，点击外网面板地址，登录宝塔面板。
    <img src="6.jpg" width="100%" align="bottom"/>
