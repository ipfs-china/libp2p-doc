# libp2p-doc

> 此文档介绍libp2p，一个现代化、可拓展的网络技术栈，可以用来克服在点对点应用时面对的挑战。libp2p被IPFS作为其网络库。

## 简介

这是IPFS的网络层协议描述。 网络层提供了在两个IPFS节点(可信或不可信) 中点对点的传输。

此文档定义的规范在libp2p中实施。

## 目录

- [介绍](https://github.com/libp2p/specs/blob/master/1-introduction.md)
    - [愿景](https://github.com/libp2p/specs/blob/master/1-introduction.md#11-motivation)
    - [目标](https://github.com/libp2p/specs/blob/master/1-introduction.md#12-goals)
- [网络堆栈技术现状分析](https://github.com/libp2p/specs/blob/master/2-state-of-the-art.md)
    - [客户端(C)/(S)服务端模型](https://github.com/libp2p/specs/blob/master/2-state-of-the-art.md#21-the-client-server-model)

    - [按解决方案对网络分类](https://github.com/libp2p/specs/blob/master/2-state-of-the-art.md#22-categorizing-the-network-stack-protocols-by-solutions)
    - [目前的缺点](https://github.com/libp2p/specs/blob/master/2-state-of-the-art.md#23-current-shortcomings)
- [要求](https://github.com/libp2p/specs/blob/master/3-requirements.md)
    - [匿名传输](https://github.com/libp2p/specs/blob/master/3-requirements.md#34-transport-agnostic)
    - [多路复用](https://github.com/libp2p/specs/blob/master/3-requirements.md#35-multi-multiplexing)
    - [加密](https://github.com/libp2p/specs/blob/master/3-requirements.md#33-encryption)
    - [NAT遍历](https://github.com/libp2p/specs/blob/master/3-requirements.md#31-nat-traversal)
    - [中继](https://github.com/libp2p/specs/blob/master/3-requirements.md#32-relay)
    - [启用多个网络拓扑](https://github.com/libp2p/specs/blob/master/3-requirements.md#36-enable-several-network-topologies)
    - [资源发现](https://github.com/libp2p/specs/blob/master/3-requirements.md#37-resource-discovery)
    - [消息](https://github.com/libp2p/specs/blob/master/3-requirements.md#38-messaging)
    - [命名](https://github.com/libp2p/specs/blob/master/3-requirements.md#38-naming)
- [架构](https://github.com/libp2p/specs/blob/master/4-architecture.md)
    - [节点路由](https://github.com/libp2p/specs/blob/master/4-architecture.md#41-peer-routing)
    - [集群](https://github.com/libp2p/specs/blob/master/4-architecture.md#42-swarm)
    - [分布式记录存储](https://github.com/libp2p/specs/blob/master/4-architecture.md#43-distributed-record-store)
    - [发现](https://github.com/libp2p/specs/blob/master/4-architecture.md#44-discovery)
    - [消息](https://github.com/libp2p/specs/blob/master/4-architecture.md#45-messaging)
        - [发布订阅](https://github.com/libp2p/specs/blob/master/4-architecture.md#451-pubsub)
    - [命名](https://github.com/libp2p/specs/blob/master/4-architecture.md#46-naming)
        - [IPNS](https://github.com/libp2p/specs/blob/master/4-architecture.md#462-ipns)
        - [IPRS](https://github.com/libp2p/specs/blob/master/4-architecture.md#461-iprs)
- [数据结构](https://github.com/libp2p/specs/blob/master/5-datastructures.md)
- [接口](https://github.com/libp2p/specs/blob/master/6-interfaces.md)
    - [libp2p](https://github.com/libp2p/specs/blob/master/6-interfaces.md#61-libp2p)
    - [传输](https://github.com/libp2p/specs/blob/master/6-interfaces.md)
    - [链接](https://github.com/libp2p/specs/blob/master/6-interfaces.md)
    - [流多路复用器](https://github.com/libp2p/specs/blob/master/6-interfaces.md)
    - [集群](https://github.com/libp2p/specs/blob/master/6-interfaces.md#63-swarm)
    - [节点发现](https://github.com/libp2p/specs/blob/master/6-interfaces.md#65-peer-discovery)
    - [节点路由](https://github.com/libp2p/specs/blob/master/6-interfaces.md#62-peer-routing)
    - [内容路由](https://github.com/libp2p/specs/blob/master/6-interfaces.md#62-peer-routing)
        - [分布式记录存储](https://github.com/libp2p/specs/blob/master/6-interfaces.md#64-distributed-record-store)
    - [libp2p接口和UX](https://github.com/libp2p/specs/blob/master/6-interfaces.md#66-libp2p-interface-and-ux)
- [特性](https://github.com/libp2p/specs/blob/master/7-properties.md)
    - [通信模型——流](https://github.com/libp2p/specs/blob/master/7-properties.md#71-communication-model---streams)
    - [端口——受限入口](https://github.com/libp2p/specs/blob/master/7-properties.md#72-ports---constrained-entrypoints)
    - [传输协议](https://github.com/libp2p/specs/blob/master/7-properties.md#73-transport-protocols)
    - [非IP网络](https://github.com/libp2p/specs/blob/master/7-properties.md#74-non-ip-networks)
    - [网线](https://github.com/libp2p/specs/blob/master/7-properties.md#75-on-the-wire)
        - [协议复用](https://github.com/libp2p/specs/blob/master/7-properties.md#751-protocol-multiplexing)
        - [多流——自描述协议流](https://github.com/libp2p/specs/blob/master/7-properties.md#752-multistream---self-describing-protocol-stream)
        - [多流选择器——自描述选择器](https://github.com/libp2p/specs/blob/master/7-properties.md#753-multistream-selector---self-describing-protocol-stream-selector)
        - [流复用](https://github.com/libp2p/specs/blob/master/7-properties.md#754-stream-multiplexing)
        - [便携式编码](https://github.com/libp2p/specs/blob/master/7-properties.md#755-portable-encodings)
        - [安全通信](https://github.com/libp2p/specs/blob/master/7-properties.md#756-secure-communications)

- [实现](https://github.com/libp2p/specs/blob/master/8-implementations.md)
- [参考](https://github.com/libp2p/specs/blob/master/9-references.md)