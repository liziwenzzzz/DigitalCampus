# DigitalCampus
基于模拟道路状况和出行方式推荐最优路径
通过模拟校园地图对用户选择路径提供帮助。在文本中记录各点之间的路径关系， C++程序利用这些数据实现了最优路线规划、 高峰期道路推荐、 寻找关键道路、 道路
不通重新选路等功能。
1.道路只分为两种：可通汽车的大道（ avenue） 和不可通汽车的小路（ walkway）。 地图参考了校园的实际情况，将主要的道路和地点都罗列了出来。可选地点共有 17 个，道路近 40 条。
2.备选的交通方式有：步行，自行车和汽车。 假设步行正常速度 0.5m/s， 自行车正常速度5m/s, 汽车的正常速度为 10m/s。 这些交通工具高峰路段(部分路径，在图上标有三角形)速
度均减半。显然这里简化的具体各个道路实际的通行流量和实时路况，只分为高峰期和非高峰期。
3.道路被封情况需要用户告知，在用户确定被封道路后程序将重新按照用户的偏好选择最优路径。 任意 A,B 两地之间的路径中如果某些段道路被封则用户用他按他的交通方式无法从
A,B 之一点到达另一点， 则称这样的道路为 A,B 之间的关键道路。
4.本问题是无向图问题，节点之间的道路长度为边的权值， 用邻接矩阵来表示节点之间的信息，两种道路各形成一个矩阵，分别放在 avenue.txt 和 walkway.txt 中， 通过文件操作读
取。