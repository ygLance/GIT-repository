# 最短路与Dijkstra算法
(单源最短路,无负权边)

[博主nb](https://www.cnblogs.com/godfray/p/4077146.html)

例题[农场问题]()

(快啊,至少比floyd快)

**找min的时候不能一边找一边写true**(还不是真的min)

### 要素
**1.** dis[maxn] 最短路
**2.** vis[maxn] 是否已经确定(flase/true)
**3.** woe[maxn][maxn] 存边(注意重边!!)


### 初始化
* woe:主对角线写0,其它写INF
* dis:直接读woe[1][j]
* vis:除了1,全写false//这里按1位置为源

### 基本思路
初始化完成后,
找到最近的那个点(已经无法优化),
写vis为true,

尝试以该点为中继点,
能不能通过这点让别的点变得更近
(相比于从1直接走,很多都是INF来说)
```
即dis[i]=min(dis[i],min+woe[pos][i])
//比较的二者是,此前以为的最近,和现在以pos为中继点能到的最近路(即dis[pos]+woe[pos][i]//1到pos加pos到i
```
做完一次,
再找最近(无法优化)的点,对其它点优化
直到做完
