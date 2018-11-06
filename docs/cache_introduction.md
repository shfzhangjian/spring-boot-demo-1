# Cache Introduction
---

## 缓存分类和应用场景

一般按照缓存与应用的耦合程度以及缓存是否可以共享可以将常用的缓存分为本地缓存（local cache）和分布式缓存（remote cache）。

### Local Cache    

应用中的缓存组件，也叫做进程缓存或者JVM缓存。

优点：
- 应用和cache是在同一个进程内部，请求缓存非常快速，没有过多的网络开销等，在单应用不需要集群支持或者集群情况下各节点无需互相通知的场景下使用本地缓存较合适；同时，它的缺点也是应为缓存跟应用程序耦合，多个应用程序无法直接的共享缓存，各应用或集群的各节点都需要维护自己的单独缓存，对内存是一种浪费。