#Urban_Road_Planning #Building_Demolition #Nosie #Air_Pollution #MCDM #GIS 

![[../../归档/画板/可持续道路规划的MCDM-GIS方法.canvas]]

Sustainable road alignment planning in the built environment based on the [[../2023年5月/MCDM-GIS|MCDM-GIS]] method（[https://linkinghub.elsevier.com/retrieve/pii/S2210670722005510](https://linkinghub.elsevier.com/retrieve/pii/S2210670722005510)）
# Abstract 

城市建成区的可持续道路规划力求在有限的建设空间和建成环境的各种限制条件下，综合考虑工程、交通、经济、社会和环境因素，满足社会的交通需求。**与农村地区不同，城市建成区的道路规划会受到周围环境的很大影响，如现有建筑、[[道路网络]]和[[土地利用]]，并应考虑噪音和空气污染对居民的影响。** 此外，道路宽度和道路拓宽也是道路选线规划的重要因素。

基于 **[[../2023年5月/MCDM-GIS|MCDM-GIS]]** 方法，考虑到建筑拆迁和[[土地利用]]、交通拥堵、噪声影响、空气污染影响和建设成本，采用最小成本宽路径算法进行建筑环境中的可持续道路选线规划。同时考虑道路宽度、新道路建设和现有道路拓宽。

本文提出了几种方法，**将各种可持续因素数字化并解析为可理解的表达式**，用于道路选线规划。定义了道路拓宽的禁区和道路缓冲区。所提出的方法已在英国肯特郡达特福德的道路规划中实施。**不同权重的可持续因素可从不同角度产生不同的道路选线，而道路宽度可对道路选线产生显著的局部影响。**

# Introduction & Content Thinking

决策者和规划者致力于提供可持续的道路规划，以应对当前和未来与交通有关的需求，并实现财政、环境和社会目标，同时不损害子孙后代满足其自身需求的能力。

如何选择决策因素，决策者和规划者的方案。确认的影响因素，不可避免地受到有限的剩余空间、现有[[道路网络]]、现有建筑、[[土地利用]]、 交通拥堵等因素的影响。

#道路网络 #土地利用

Factors can be categorised into demands and constraints.

降低拆除成本、土地使用成本和建设成本（成本控制） #成本控制 

道路规划方案应有利于 #区域经济 [[区域经济]]

噪音和空气污染对居民的影响

从生态友好的角度出发，在建成环境中进行道路规划，应尽量减少对环境造成的负面影响，如空气、土壤、水体和噪声污染，以及对绿地和植被的占用。

[[道路线形规划]]方法可分为两类。在第一类中，考虑了根据设计规范由标准线形元素组成的道路线形形状，如直线、缓和曲线、圆曲线等。

# Method Learning

The overall workflow of the method can be described in Fig. 1. First, multi-source data are collected, parsed and digitalised using different methods, such as digital twin, digital image processing, etc., to express various factors, including building demolition and land use, traffic congestion, noise impact, air pollution impact, and construction costs. After that, MCDM methods are employed to evaluate and give weights to various factors to establish cost rasters in the GIS environment. Then, the least-cost path algorithm is updated to the least-cost wide path algorithm to generate the optimal road alignment in the built environment considering road width, new road construction, and existing road widening.

![[../../归档/picture/Overall workflow of road alignment planning in the built environment..png]]

建筑数字孪生的应用和拆迁成本的估计
![[../../归档/picture/建筑数字孪生与拆迁成本估算.png]]

代表**建筑物(高程为零)的二维多边形**可以从矢量地图(图2、3、4)中获得。然后，**从DDM中获得每栋建筑物的二维多边形区域的高程**，并计算出每栋建筑物的这些高程的平均值，称为建筑物的平均高度(图2中5)。

# Thinking

Sustainable road planning in the cities’ [[../2023年5月/Built-Up]] areas strives to meet traffic demands of society within limited spaces available for construction and various constraints in the built environment considering engineering, traffic, economic, social, and environmental factors. **Unlike rural areas, road planning in the built environment can be significantly influenced by the surroundings, such as existing buildings, road network, and land use, and should consider noise and air pollution impact on residents.** In addition, road width and road widening are significant factors for road alignment planning. 

Based on the [[../2023年5月/MCDM-GIS|MCDM-GIS]] method, the least-cost wide path algorithm is employed for sustainable road alignment planning in the built environment, considering building demolition and land use, traffic congestion, noise impact, air pollution impact, and construction costs. Road width, new road construction, and existing road widening are considered simultaneously. Several methods are proposed to digitalize and parse various sustainable factors into understandable expressions for road alignment planning. Forbidden areas and road buffer areas for road widening are defined. The proposed method is implemented in road planning in Dartford, Kent County, UK. 

在[[../2023年5月/MCDM-GIS]]方法的基础上，考虑到建筑拆迁和[[土地利用]]、交通拥堵、噪声影响、空气污染影响和建设成本，采用最小成本的宽路径算法来进行建筑环境中的可持续道路线形规划。道路宽度、新道路建设和现有道路拓宽同时被考虑。提出了几种方法，将各种可持续因素数字化并解析为可理解的表达，用于道路线形规划。定义了道路拓宽的禁区和道路缓冲区。提出的方法在英国肯特郡达特福德的道路规划中得到了实施。

Sustainable factors with different weights can generate various road alignments from different perspectives, and road widths can significantly and locally in­ fluence road alignments. 具有不同权重的可持续因素可以从不同的角度产生各种道路线形，而道路宽度可以显著地和局部地影响道路线形。

# 部分笔记翻译

MCDM（Multiple Criteria Decision Making）多属性决策

**Result & Discussion**

There are ten alignment planning results, as shown in Figs. 27 and 28. All the alignments do not touch the forbidden areas and try to avoid widening A282 and A2 highways. For alignments considering traffic congestion, they try to go through the areas less distant from congested areas. There are some newly built sections and road widening sections. In the road widening section, the road is always on one side and tries to avoid occupying existing old roads because the sections occupying existing old roads represent the section without road widening or new road construction, which cannot help ease traffic congestion.

有十个对齐规划结果，如图所示。第27和28段。所有路线均不接触禁区，并尽量避免拓宽A282和A2高速公路。对于考虑交通拥堵（图27和图28中的（1）和（2））的路线，它们试图穿过距离拥堵区域较不远的区域。有一些新建路段和道路拓宽路段。在道路拓宽路段中，道路始终在一侧，尽量避免占用现有的旧道路，因为占用现有旧道路的路段代表没有道路拓宽或新道路建设的路段，无助于缓解交通拥堵。