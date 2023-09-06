# .NET反序列化漏洞系列文章

说起反序列化漏洞就不得不提前些年异常火爆的Java和PHP语言，如今网上分析的文章已经很多了，而.Net反序列化攻击相对低调，文章乏善可陈，笔者最近参考多方资料后，整理了如下课程，喜欢的朋友可关注我们的```知识星球```及```dot.Net安全矩阵```公众号，让我们一起探讨.NET安全。

---
# .NET安全矩阵星球

dotNet安全矩阵星球从创建以来一直聚焦于.NET领域的安全攻防技术，定位于高质量安全攻防星球社区，也得到了许多师傅们的支持和信任，通过星球深度连接入圈的师傅们，一起推动.NET安全高质量的向前发展。星球汇聚了各行业安全攻防技术大咖，并且每日分享.NET安全技术干货以及交流解答各类技术等问题，社区中发布很多高质量的.NET安全资源，可以说市面上很少见，都是干货。其中主题包括```.NET Tricks、漏洞分析、内存马、代码审计、预编译、反序列化、webshell免杀、命令执行、C#工具库```等等，后续还会倾力打造专刊、视频等配套学习资源，循序渐进的方式引导加深安全攻防技术提高以及岗位内推等等服务

![](zsxq2.jpg)

---
# .NET安全矩阵公众号

[ dotNet安全矩阵 ] —聚焦于微软.NET安全技术，曾原创连载 .NET十大反序列化漏洞课程 , 关注基于.NET衍生出的各种红蓝攻防对抗技术、分享内容不限于 .NET代码审计、 最新的.NET漏洞分析、反序列化漏洞研究、有趣的.NET安全Trick、.NET开源软件分享、. NET生态等热点话题，愿你能在这里学到实在的干货，共同推动.NET安全氛围卷起来

![](gzh.jpg)

---
# 更新日志

- 2023-08-30 
  - [.NET 序列化生成Ysoserial JavaScriptSerializer链 Payload](https://mp.weixin.qq.com/s/N-8uhhgbvv66kJFBMjRghQ)
- 2023-07-17 
  - [实现Json.NET序列化生成Ysoserial Payload](https://mp.weixin.qq.com/s/wldhQ6vhYSg-RBjy7v0aMQ)
- 2022-07-10 
  - [.NET高级代码审计（第15课）反序列化Gadget之ExpandedWrapper](https://mp.weixin.qq.com/s/9PzATv9AS6UbQK4RUhvzQw)
- 2022-05-27
  - [.NET高级代码审计（第14课）反序列化Gadget之XAML](https://mp.weixin.qq.com/s/8fQNU7i6nqB1kHuL_hhUDw)
- 2022-05-13
  - [.NET高级代码审计（第13课）反序列化Gadget之详解ObjectDataProvider](https://mp.weixin.qq.com/s/IcFnCSN8aCkcWg7HKrLO8g)
- 2022-04-22
  - [.NET高级代码审计（第12课）反序列化Gadget之详解ObjectDataProvider](https://mp.weixin.qq.com/s/sHKR0zlW2CsphGAmv3_KVA)
- 2019-01 -> 2019-05
  - [.NET高级代码审计（第11课）LosFormatter反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484611&idx=1&sn=9a42e5549d4ffca2bba69d440552742d&chksm=fa5aaa2ecd2d2338863416bc51e8d3f9022e20070fd4853f30995d440b13dc3920b485f5487c#rd)
  - [.NET高级代码审计（第10课）ObjectStateFormatter反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484610&idx=1&sn=b74ddabee3bbdcb398b99e75dcbf4766&chksm=fa5aaa2fcd2d23394c0165103ea7e3c69e4031bfcb7258b9029941b208e80e73a77926290bc2#rd)
  - [.NET高级代码审计（第9课） BinaryFormatter反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484609&idx=1&sn=6fbee63bf44616fa7ad8bfca15bd55f6&chksm=fa5aaa2ccd2d233a19349afde3144073d13573b4481e80aa79bbcaf4a220063d0cc9d6060525#rd)
  - [.NET高级代码审计（第8课） SoapFormatter反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484608&idx=1&sn=8c11cdfa296856575ae758db76db78bc&chksm=fa5aaa2dcd2d233b702afe07a4dfeceec3059757ad0737ac506a648561e1b68ed9ac2d385f61#rd)
  - [.NET高级代码审计（第7课） NetDataContractSerializer反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484525&idx=1&sn=e6570b210cac88b4cdda2edd5a9805a0&chksm=fa5aaa80cd2d2396f68d3c83365f318c5614a596edce45c0fa611c84c4e5190abe5b59439fa6#rd)
  - [.NET高级代码审计（第6课） DataContractSerializer反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484502&idx=1&sn=eb4e846cb7735d8d15c6e590bfe91272&chksm=fa5aaabbcd2d23adb6d3fe4d2b52c8ee8c14a31c6d3f2a912a862e058ea137b3500939bda742#rd)
  - [.NET高级代码审计（第5课） .NET Remoting反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484477&idx=1&sn=5dfff6ae438b1921dd246aee64aeb70f&chksm=fa5aaad0cd2d23c63cbdb9573d0dd8cc644c31d3f9944ef106abf507c1372a604ebba7fc34ac#rd)
  - [.NET高级代码审计（第4课） JavaScriptSerializer反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484438&idx=1&sn=8f4ccb0e38cb6caa0af5ce11c25c4b8d&chksm=fa5aaafbcd2d23ed1140b9b6876e43bb52bf70fe62718ee7f613a74d155b439277a879e5bb31#rd)
  - [.NET高级代码审计（第3课） Fastjson反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484373&idx=1&sn=10c80ece04ab280dee39be5e31a534e9&chksm=fa5aad38cd2d242e031b71c5d51e940a9a6d45c888054d43575f5f1437a4ffeeede473d997e5#rd)
  - [.NET高级代码审计（第2课） Json.Net反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484349&idx=1&sn=8b2786bee0cf290b0bc23e140cd093d0&chksm=fa5aad50cd2d24464d83701a02aa54ef393588bd32349e21ec241825a4c9ba73bda3e648ca99#rd)
  - [.NET高级代码审计（第1课） XmlSerializer反序列化漏洞](https://mp.weixin.qq.com/s?__biz=MzUyOTc3NTQ5MA==&mid=2247484252&idx=1&sn=2ca29a090b548f8d5617138a6bce7dea&chksm=fa5aadb1cd2d24a76c7ac24336c750fb21bf91a39e8c1fd3a55299ef20b435b037e26cfbb352&token=263427717&lang=zh_CN#rd)
 
 #经典案例
 
- 2022-04-28 
  - [最新Windows事件查看器.NET反序列化漏洞分析](https://mp.weixin.qq.com/s/A7Z720lavhNSjlNNc3nzng)
