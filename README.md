# SpringBoot-ActiveMq
SpringBoot 集成 ActiveMq

1). ActiveMQ
ActiveMQ是Apache所提供的一个开源的消息系统，完全采用Java来实现，因此，它能很好地支持J2EE提出的JMS（Java Message Service,即Java消息服务）规范。JMS是一组Java应用程序接口，它提供消息的创建、发送、读取等一系列服务。JMS提供了一组公共应用程序接口和响应的语法，类似于Java数据库的统一访问接口JDBC,它是一种与厂商无关的API，使得Java程序能够与不同厂商的消息组件很好地进行通信。

2). Java Message Service(JMS)
JMS支持两种消息发送和接收模型。

一种称为P2P(Ponit to Point)模型，即采用点对点的方式发送消息。P2P模型是基于队列的，消息生产者发送消息到队列，消息消费者从队列中接收消息，队列的存在使得消息的异步传输称为可能，P2P模型在点对点的情况下进行消息传递时采用。

另一种称为Pub/Sub(Publish/Subscribe，即发布-订阅)模型，发布-订阅模型定义了如何向一个内容节点发布和订阅消息，这个内容节点称为topic(主题)。主题可以认为是消息传递的中介，消息发布这将消息发布到某个主题，而消息订阅者则从主题订阅消息。主题使得消息的订阅者与消息的发布者互相保持独立，不需要进行接触即可保证消息的传递，发布-订阅模型在消息的一对多广播时采用。

3). JMS术语
Provider/MessageProvider：生产者
Consumer/MessageConsumer：消费者
PTP：Point To Point，点对点通信消息模型
Pub/Sub：Publish/Subscribe，发布订阅消息模型
Queue：队列，目标类型之一，和PTP结合
Topic：主题，目标类型之一，和Pub/Sub结合
ConnectionFactory：连接工厂，JMS用它创建连接
Connnection：JMS Client到JMS Provider的连接
Destination：消息目的地，由Session创建
Session：会话，由Connection创建，实质上就是发送、接受消息的一个线程，因此生产者、消费者都是Session创建的