<p align="center">
	<img src="./dc3/images/iot-dc3-logo.png" width="400">
</p>
<p align="center">
	<strong>DC3是一个开源的、分布式的物联网(IOT)平台,用于快速开发物联网项目和管理拓展。</strong>
</p>
<p align="center">
	<a>
		<img src="https://img.shields.io/github/stars/pnoker/iot-dc3.svg"></img>
	</a>
	<a>
	    <img src="https://img.shields.io/github/forks/pnoker/iot-dc3.svg"></img>
    </a>
    <a>
    	<img src="https://img.shields.io/github/issues/pnoker/iot-dc3.svg"></img>
    </a>
	<a target="_blank" href="https://github.com/pnoker/iot-dc3/blob/master/LICENSE">
		<img src="https://img.shields.io/github/license/pnoker/iot-dc3.svg" ></img>
	</a>
</p>

 ## 什么是DC3 IOT平台？
 
 DC3致力于：
 
 * 设备端代码一键生成，快速接入设备；
 * 多协议、多设备连接与管理；
 * 物联设备数据采集、处理与数据存储；
 * 分析传入的遥测和复杂事件处理触发警报；
 * 控制设备使用远程过程调用(RPC)；
 * 构建工作流基于设备生命周期事件,REST API,RPC请求,等等。

DC3设计为：

* 可伸缩:水平可伸缩的平台,构建使用领先的开源技术；
* 容错:没有单点故障弱,集群中的每个节点是相同的；
* 健壮和高效:单一服务器节点可以处理甚至数百成千上万的设备根据用例。DC3集群可以处理数以百万计的设备；
* 可定制:添加新的设备协议，并注册到服务中心；
* 数据加密传输。
 
## DC3 IOT平台架构？

DC3平台是基于Spring Cloud架构开发的，是一系列松耦合、开源的微服务集合。
微服务集合由4个微服务层和两个增强的基础系统服务组成，提供从物理域数据采集到信息域数据处理等一系列的服务。

spring-eurake、spring-zuul、spring-hystrix、spring-ribbon、spring-cloud-config、spring-cloud-bus等微服务模块。

### 模块

* 设备微服务层:用于提供标准或者私有协议连接物理设备的SDK；
* 核心微服务层:用于提供微服务注册中心、配置管理中心、设备指令接口、设备注册与关联配对、数据管理中心，是所有微服务交互的核心部分；
* 支持微服务层:用于提供规则引擎、任务调度、报警与消息通知、日志管理、数据清理；
* 开放微服务层:用于提供数据开放等服务...

### 架构设计

* 功能架构

![iot-dc3-architecture](dc3/images/iot-dc3-architecture1.jpg)

* 技术架构

![iot-dc3-architecture](dc3/images/iot-dc3-architecture2.jpg)