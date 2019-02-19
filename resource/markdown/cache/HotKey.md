<h3 style="padding-bottom:6px; padding-left:20px; color:#ffffff; background-color:#E74C3C;">Redis热点Key</h3>

在一定时间内，被频繁访问的key称为 **热点key** 。比如突发性新闻，微博上常见的热搜新闻，引起千千万万人短时间内浏览；在线商城大促活动，消费者比较关注的商品突然降价，引起成千上万消费者点击、购买。热点key所在服务器的压力骤然上升，如果超出物理机器的承载能力，则缓存不可用，进而诱发缓存击穿、缓存雪崩的问题。

![缓存击穿](https://i.loli.net/2019/02/19/5c6b968d1e946.png)



#### 解决方案

**1. 读写分离:** 读写分离比较适用于写少读多的情景，