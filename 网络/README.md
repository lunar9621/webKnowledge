# 网络知识

## [Ajax](Ajax.md)

## [HTTP](HTTP.md)

## [TCP](TCP.md)

## [UDP](UDP.md)

## [跨域](./跨域.md)

## [缓存](缓存.md)

## [cookie和session](cookie和session.md)

## [从输入URL到页面加载完成的过程](从输入URL到页面加载完成的过程.md)

## [HTTPS](HTTPS.md)


### OSI 七层协议
 - 应用层
   - 为应用提供通信服务 Http、tftp、ftp、nfs、wais、smtp
 - 表示层
   - 定义数据格式以及加密 telnet、riogin、snmp、gopher
 - 会话层
   - 定义了如何开始、控制、结束一个会话，包括对多个双向消息的控制和管理 smtp dns
 - 传输层
   - 选择差错恢复协议还是无差错恢复协议
   - TCP、UDP
 - 网络层 ip、icmp、arp、rarp、akp、uucp
   - 端到端包传输。
   - 路由选择、包分解成更小的包
 - 数据链路层  fddi、ethernet、arpanet、pdn、slip、ppp
   - 定义单个链路上如何传输数据
 - 物理层  IEEE 802.1A IEEE 802.2
   - 传输介质相关

### OSI 五层协议
 - 应用层
 - 传输层
 - 网络层
 - 数据链路层
 - 物理层
 在四层模型中数据链路层和物理层合称为网络接口层


### DNS解析
DNS 的作用就是通过域名查询到具体的 IP。

1. 操作系统会首先在本地缓存中查询
2. 没有的话会去系统配置的 DNS 服务器中查询
3. 如果这时候还没得话，会直接去 DNS 根服务器查询，这一步查询会找出负责 com 这个一级域名的服务器
4. 然后去该服务器查询 google 这个二级域名
5. 接下来三级域名的查询其实是我们配置的，你可以给 www 这个域名配置一个 IP，然后还可以给别的三级域名配置一个 IP

以上介绍的是 DNS 迭代查询，还有种是递归查询，区别就是前者是由客户端去做请求，后者是由系统配置的 DNS 服务器做请求，得到结果后将数据返回给客户端。


### 前后端如何通信
 - Ajax
 - WebSocket
 - CORS



### websocket
在单个 TCP 连接上进行全双工通讯的协议。在 WebSocket API 中，浏览器和服务器只需要完成一次握手，两者之间就直接可以创建**持久性**的连接，并进行**双向**数据传输。

 - Socket.onopen	连接建立时触发
 - Socket.onmessage	客户端接收服务端数据时触发
 - Socket.onerror	通信发生错误时触发
 - Socket.onclose	连接关闭时触发