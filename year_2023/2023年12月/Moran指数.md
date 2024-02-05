空间自相关：[空间自相关—莫兰指数 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/387342753)
https://mp.weixin.qq.com/s/QtymA6nrW9rpdMJYCjCZww

莫兰指数分为全局莫兰指数（Global Moran's I）和局部莫兰指数（Local Moran's I），前者是Patrick Alfred Pierce Moran开发的空间自相关的度量；后者是美国亚利桑那州立大学地理与规划学院院长Luc Anselin 教授在1995年提出的。在**Arcgis**里分别是“**空间自相关**”与“**聚类和异常值分析**”工具。

通常情况，先做一个地区的全局莫兰指数，全局指数告诉我们空间是否出现了集聚或异常值。如果全局有自相关出现，接着做局部自相关，局部Moran'I会告诉我们哪里出现了异常值或者哪里出现了集聚。

![[../../归档/picture/中间黄色部分为随机分布，右侧为集聚分布，左侧为离散分布.webp]]

Geoda下载地址：[Windows | Download | GeoDa on Github (geodacenter.github.io)](https://geodacenter.github.io/download_windows.html)

Moran’s I is used to identify the global degree of spatial association (how much the magnitude of the variable of interest at one location influences its magnitude at a nearby area).43,44 Given the existence of a significant spatial autocorrelation in the data, we aimed to identify where the hotspots formed by spatially autocorrelated units were located. We used for this purpose a local indicator of spatial association (LISA).44 This statistic specifically identifies units with a high incidence that are significantly associated with surrounding units also of high incidence. We could therefore identify malaria hotspots and assess whether they were maintained over time.[[Quantifying climatic and socioeconomic drivers of urban malaria in Surat  India  a statistical spatiotemporal modelling study]]

Moran I用于识别空间关联的全局程度(在一个位置上感兴趣变量的大小对其在附近区域的大小有多大影响). 鉴于数据中存在显著的空间自相关性，我们旨在识别由空间自相关单元形成的热点位置。
使用空间关联的局部指标( **[[LISA_Local indicators of spatial association]]** )。该统计量特别确定了具有高发病率的单元，这些单元与周围具有高发病率的单元显著相关。因此，我们可以识别疟疾热点，并评估它们是否随着时间的推移而保持下去。