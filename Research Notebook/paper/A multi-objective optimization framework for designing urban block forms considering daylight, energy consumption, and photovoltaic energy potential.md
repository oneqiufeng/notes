# 考虑日照、能耗和光伏能源潜力的城市街区形态设计的多目标优化框架

[A multi-objective optimization framework for designing urban block forms considering daylight, energy consumption, and photovoltaic energy potential - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0360132323006121)

[徐小东 (seu.edu.cn)](https://arch.seu.edu.cn/2022/1110/c42982a426558/page.htm)

本文基金项目：
- 51978144： [杨慧-中国矿业大学资源与地球科学学院 (cumt.edu.cn)](https://sres.cumt.edu.cn/info/1293/9935.htm)
	- （5）主持国家自然科学面上基金“基于智能算法的城市形态与能源绩效耦合机理及模式研究（51978144）”（2020.1-2023.12，与东南大学建筑学院联合申请，矿大合作单位负责人，在研，15万）
- 52208011 ？

Urban form significantly influences building energy consumption. However, most research has primarily focused on quantifying the relationship between the two factors, with limited exploration of optimizing urban form to enhance building energy performance. Moreover, studies often fail to consider multiple performance objectives simultaneously. This study proposes a multi-objective optimization framework for early urban design stage to improve energy and environmental performance in residential block layouts. The performance objectives include energy consumption, photovoltaic energy potential, and sunlight hours. The framework is implemented using the parametric platform Rhino & Grasshopper, where a parametric model controls the layout of blocks. Ladybug Tools plugin is employed for performance simulation, and Wallacei is used for optimization. An ideal residential block in Jianhu City, China, is taken as a case study. The study generates a total of 1896 valid solutions, including 58 Pareto solutions. The performance of the Pareto solutions demonstrates considerable improvements, indicating the effectiveness of optimizing urban form for enhancing energy and environmental performance. Compared to the initial solution, a typical Pareto solution showcases a 1.5% reduction in energy consumption, a 52.7% increase in photovoltaic energy potential, and a 50% increase in sunlight hours. These findings underscore the pivotal role of urban block morphology in influencing energy consumption, photovoltaic potential, and daylighting. The proposed multi-objective framework in this study enhances and facilitates sustainable block form design, which is expected to provide technical support for energy-efficient or low-carbon urban design.

城市形态对建筑能耗有重大影响。然而，大多数研究主要集中于量化这两个因素之间的关系，而对优化城市形态以提高建筑能耗性能的探索却很有限。此外，这些研究往往未能同时考虑多种性能目标。本研究为早期城市设计阶段提出了一个多目标优化框架，以提高住宅区布局的能源和环境性能。性能目标包括能源消耗、光伏能源潜力和日照时间。该框架使用参数化平台 Rhino 和 Grasshopper 实现，其中参数化模型控制街区布局。瓢虫工具插件用于性能模拟，Wallacei 用于优化。研究以中国建湖市的一个理想住宅区为案例。研究共生成了 1896 个有效解，其中包括 58 个帕雷托解。帕累托方案的性能有了显著改善，表明城市形态优化在提高能源和环境性能方面的有效性。与最初的解决方案相比，典型的帕累托解决方案可减少 1.5%的能源消耗，增加 52.7%的光伏发电潜能，以及增加 50%的日照时间。这些发现强调了城市街区形态在影响能源消耗、光伏发电潜力和日照方面的关键作用。本研究提出的多目标框架增强并促进了可持续街区形态设计，有望为节能或低碳城市设计提供技术支持。

# 研究区域

研究区域为中国江苏省建湖市。建湖市位于中国东部沿海地区。面积 1160 平方公里，人口 60 万。根据中国建筑规范 GB 50176-2016，建湖位于夏热冬冷气候区（HSCW）[82]，是炎热地区和寒冷地区之间的过渡区域。该区具有夏季气温高、冬季气温低、全年湿度大的气候特征。建湖的年平均气温为 14 ◦C，最热月和最冷月的平均气温分别为 27.1 ◦C 和 1.6 ◦C。因此，建湖市对供热和制冷的能源需求很大，对建筑节能的要求也很高。

本研究选择了住宅小区作为案例。图 2 显示了建湖城区的位置和案例街区的分布。研究人员对建湖的一些实际居住小区进行了调查，并获得了一些形态信息，为随后创建理想小区参数奠定了基础和提供了参考。

# 城市街区形态的参数建模

## 典型建筑类型的提取和简化

最近，在对街区形式的研究中广泛使用了建筑类型学方法 [45,83]。这种方法通过对街区形式的研究，简化并提取出最具代表性的建筑类型。这些建筑类型被认为充分反映了实际街区形态的几何特征[41]。本研究参考以往的研究[37,42,84]，从建湖实际街区中**提取了典型的住宅建筑类型**，并将其分为**点式、板式和庭院式**三类。

如图 3 所示，点式建筑有四种，分别为 **P-1、P-2、P-3 和 P-4**；板式建筑有三种，分别为 S-1、S-2 和 S-3；庭院式建筑有两种，分别为 C-1 和 C-2。表 1 列出了拟议建筑类型的详细信息。根据日照规定，随着建筑高度的增加，建筑间距也需要增加。本研究考虑了这一关系，并为不同建筑类型定义了相应的建筑高度变化区间。据观察，楼间距较小的建筑类型表示建筑密度较高，其高度往往较低。相反，楼间距较大的建筑类型往往高度较高。建筑高度间隔分为三段。具体来说，P-1、S-1 和 C-1 为低层建筑，高度变化范围为 1-3 层；P-2、S-2 和 C-2 为中层建筑，高度变化范围为 4-12 层；P-3、P-4 和 S-3 为高层建筑，高度变化范围为 13-30 层。此外，为了简化街区面积的计算和随后的比较分析，本研究规定高度变化相同的建筑类型具有相等的建筑密度和屋顶面积。

>典型的民居建筑类型

![[典型的民居建筑类型.png]]

>九种简化建筑类型的说明

![[九种简化建筑类型的说明.png]]

## 生成策略

本研究中生成的所有街区的建筑面积均为 2.5。在此基础上，区块中的八个土地单元被用来放置建筑物，另一个土地单元被用作空地。Grasshopper 平台可根据设计变量生成三维街区模型（图 5）。本研究采用 NSGA-II 优化算法来控制形态设计变量的取值和组合。根据块体模型的性能评估结果，该算法会改变设计变量的输入，以找到性能更好的块体模型。更多详情将在第 3.5 节中介绍。

>理想城市街区示意图

![[理想城市街区示意图.png]]

## Urban block form design variables.

城市地块形态设计变量
- 建筑类型（Building types）
- 楼层数（Number of floors）
- 开放空间位置（Open space location）

>区块形式方案生成示例

![[区块形式方案生成示例.png]]

# 城市建筑块体的性能模拟

Performance simulation of block forms

在完成街区形式的参数建模后，接下来的步骤是评估它们各自的性能。城市街区形式应努力减少能源需求，提高现场可再生能源的利用率，并促进宜居性。

因此，本研究从能源使用、太阳能光伏发电和日照时间三个方面对生成的街区形式进行了性能评估。**相应地引入了三个性能指标，分别是建筑物总能源使用强度（EUIt）、月平均负荷匹配指数（Av. LM）和最冷天首层朝南的平均日照时数（SH）**。

## 建筑能耗 Building energy consumption

在本研究中，建筑物总能源使用强度（EUIt）作为代表街区能源使用情况的指标。EUIt 是建筑物年总耗电量与街区总建筑面积之比。

众所周知，气候对建筑能耗有重大影响。典型气象年（TMY）数据通常被用作一般能耗模拟的边界条件。然而，典型气象年数据反映的是郊区在更长时期内的平均气候特征[85]。因此，建筑能耗模拟通常不会考虑小气候的影响。本研究采用 UWG 工具[86]，通过蜻蜓模拟街区的微气候。然后，以模拟天气数据为边界条件，使用 Honeybee 对能耗进行模拟。

根据城市景观几何和城市土地使用情况，UWG 可计算出当地城市冠层每小时的空气温度和湿度[87]。在巴塞尔、图卢兹等不同气候条件的城市和地区，UWG 的准确性已得到验证 [86,88]。要运行 UWG，必须输入参数块的建筑和城市参数。建筑功能、围护结构规格和建造日期都包含在建筑参数中。本次分析将建筑用途定义为新建中型住宅公寓，同时保持表 3 中的围护结构规格不变。气候区被设置为 3A 区，但包括交通、路基材料和道路反照率在内的城市特征则保持其通常的系统设置。

>Table 3. The parameter configurations for energy simulation in EnergyPlus.

| Parameter |  | Setting (for Residential buildings) |
| ---- | ---- | ---- |
| Weather data |  | EPW files modified based on simulated microclimate results of UWG |
| Simulation period |  | From Jan.1 to Dec. 31 |
| Constructions | Wall | U value = 0.8 W/m2·K |
|  | Roof | U value = 0.5 W/m2·K |
|  | Floor | U value = 1.5 W/m2·K |
|  | Window | U value = 2.70 W/m2·K, SHGC = 0.78 |
| Window-to-wall ratio | North and south-facing | 0.4 |
|  | West and east-facing | 0.1 |
| Internal loads | People | Occupant density: 0.03 People/m2  <br>Activity level: 100 W/person |
|  | Lighting | 5 W/m2 |
|  | Equipment | 1.9 W/m2 |
| HVAC System | Outdoor air | 30 m3/(h·person) |
|  | Heating/cooling range and setpoints | Heating: Dec. 1 to Feb. 28, 26 °C;  <br>Cooling: Jun. 15 to Aug. 31, 18 °C. |
|  | Infiltration | 1 ACH |

The EnergyPlus engine is employed by the Honeybee plugin to simulate the blocks' energy demand. With the guidance of the US Department of Energy, the comprehensive building energy simulation program EnergyPlus was created, and it is now widely used in engineering and academics [[29](https://www.sciencedirect.com/science/article/pii/S0360132323006121?via%3Dihub#bib29)]. Each building floor was separated into a thermal zone in order to maintain a reasonable simulation time, and the annual building energy intensity was computed for the entire block ([Fig. 6](https://www.sciencedirect.com/science/article/pii/S0360132323006121?via%3Dihub#fig6)(a)). In order to facilitate a comparison of energy performance across multiple blocks, each block was assigned a uniform function of residential, and the same template and simulation parameters were applied throughout the entirety of the block. The main guiding principles for the simulation parameters were the Chinese building codes JGJ 134–2010 and GB 50736–2012. The settings and parameters used for the building energy simulation in EnergyPlus are shown in [Table 3](https://www.sciencedirect.com/science/article/pii/S0360132323006121?via%3Dihub#tbl3).

翻译：蜜蜂插件采用 EnergyPlus 引擎来模拟街区的能源需求。在美国能源部的指导下，综合建筑能源模拟程序 EnergyPlus 应运而生，目前已广泛应用于工程和学术领域。为了保持合理的模拟时间，每个建筑楼层都被划分为一个热区，并计算了整个街区的年建筑能耗强度。为了便于比较多个区块的能源性能，每个区块都分配了统一的住宅功能，整个区块采用相同的模板和模拟参数。模拟参数的主要指导原则是中国建筑规范 JGJ 134-2010 和 GB 50736-2012。表 3 列出了 EnergyPlus 中用于建筑能耗模拟的设置和参数。

![[1-s2.0-S0360132323006121-gr6_lrg.jpg]]

>Fig. 6. Illustration of performance simulation of a block form. (a) Simulation of the total energy use intensity of buildings; (b) Simulation of the annual solar radiation on building roofs; (c) Simulation of the south-facing first-floor sunlight hours on the coldest day (January 20th).
>
>图 6. 街区形式性能模拟图示。(a) 模拟建筑物的总能源使用强度；(b) 模拟建筑物屋顶的年太阳辐射量；(c) 模拟最冷一天（1 月 20 日）朝南一楼的日照时间。

在本研究中，建筑物总能源使用强度（EUIt）作为代表街区能源使用情况的指标。EUIt 是建筑物年总耗电量与街区总建筑面积之比。

众所周知，气候对建筑能耗有重大影响。典型气象年（TMY）数据通常被用作一般能耗模拟的边界条件。然而，典型气象年数据反映的是郊区在更长时期内的平均气候特征[85]。因此，建筑能耗模拟通常不会考虑小气候的影响。

本研究采用 UWG 工具[86]，通过蜻蜓模拟街区的微气候。然后，使用 Honeybee 对模拟天气数据进行能耗模拟，即边界条件。基于城市景观几何和城市土地使用情况，UWG 可计算出当地城市冠层每小时的空气温度和湿度[87]。

在巴塞尔、图卢兹等不同气候条件的城市和地区，UWG 的准确性已得到验证[86,88]。要运行 UWG，必须输入参数块的建筑和城市参数。建筑功能、围护结构规格和建造日期都包含在建筑参数中。本次分析将建筑用途定义为新建中型住宅公寓，同时保持表 3 中的围护结构规格不变。

气候区被设置为 3A 区，但包括交通、路基材料和道路反照率在内的城市特征则保持其通常的系统设置。Honeybee 插件采用 EnergyPlus 引擎模拟街区的能源需求。在美国能源部的指导下，综合建筑能源模拟程序 EnergyPlus 应运而生，目前已广泛应用于工程和学术领域[29]。

为了保持合理的模拟时间，每个建筑楼层都被划分为一个热区，并计算了整个街区的年建筑能耗强度（图 6(a)）。为了便于比较多个区块的能源性能，每个区块都分配了统一的住宅功能，整个区块采用相同的模板和模拟参数。模拟参数的主要指导原则是中国建筑规范 JGJ 134-2010 和 GB 50736-2012。表 3 列出了 EnergyPlus 中用于建筑能耗模拟的设置和参数。

## 太阳能光伏潜力 Solar PV energy potential

鉴于太阳能光伏发电利用的本质是减少街区对外部能源的需求。本研究采用**月平均负荷匹配指数**（Av. LM）来表示街区的光伏能源潜力。**该指标是一个街区一年内每月太阳能光伏发电量与总能耗的平均比率**。指标值越高，意味着能源生产与能源消耗的比率越大，说明离能源自给自足的目标越近。

其中，g 表示地区楼宇的太阳能光伏年发电量（千瓦时），l 表示地区楼宇的总能耗（千瓦时），N 表示月数，t 表示时间间隔（月）。与能源供应总量与能源需求总量的年度比率相比，该指标的月度测量能更全面地反映能源平衡状况。

## 日照时长  Sunlight hours

关于街区日照性能的评估，本研究采用最冷天建筑首层朝南日照时数（SH）作为指标（图 6(c)）。目前，SH 是中国建筑规范（GB 50180-2018）中的一项强制性指标，用于确保住宅建筑的日照性能。例如，住宅建筑在最冷天（1 月 20 日）的首层朝南日照时间在 HSCW 区域必须至少达到 2 小时。在计算日照时数时，使用了 Ladybug 插件的日照时数分析计算器，并考虑了天气文件、模拟时段等输入因素。在本研究中，模拟时段设定为 1 月 20 日（最冷的一天）8:00 至 16:00。在街区内每栋建筑朝南的一楼窗台上，每隔 1 米放置一个参考点，测量距离地面 0.9 米高度的日照时数。最后，计算街区内所有参考点的平均日照时数，以评估街区的整体日照性能。

# Results and discussion

## Overall optimization trend analysis

该研究在 Windows 计算机上进行了所有计算、模拟和优化，该计算机的 CPU 为英特尔酷睿 i7-9700 处理器，主频为 3.00 GHz，内存为 32 GB。优化过程需要近 305 小时和 100 次迭代才能收敛到稳定状态。总共生成了 4000 个解决方案，其中包括 10 个无效解决方案和 2094 个重复解决方案，最终得到 1896 个有效解决方案。在有效解中，有 58 个被确定为帕累托最优解。

在优化过程中，研究中的三个目标都有明显改善，并最终在后面的迭代中达到稳定的波动阶段。这表明优化算法已成功收敛，且算法参数配置合理，确保了所得结果的可靠性。

## Trend analysis of the evolution of block forms 区块形式演变趋势分析

为了直观地显示模块形式的演变，本研究选取了 20 个流程方案并进行了编号，其中包括每个优化目标的最高值和最低值，如图 8 所示。

>Selected block form scenarios.

![[Selected block form scenarios.jpg]]

说明了在优化过程初期，**街区内的建筑高度如何逐渐偏离统一性**。在优化的后期阶段，**地块内的建筑高度明显出现两极分化**，高层和低层建筑占主导地位，中层建筑相对较少。此外，**高层建筑最初在地块内均匀分布，但逐渐向北移动**，优化过程结束后，大部分高层建筑位于地块单元的北侧。在建筑类型方面，优化初期，街区内的建筑类型较为多样，**随着优化的深入，建筑类型逐渐减少**。最终，只有高大的点式建筑和低矮的板式建筑仍占主导地位。至于空地，最初分布在不同的土地单元，但后来主要集中在 0 单元或 1 单元。此外，优化目标在整个优化过程中都有显著增加。

## 帕累托最优解的分布

所有优化解决方案的三维空间分布见图 9(a)。**解决方案空间中的灰色点代表可行解决方案**。此外，**红色点代表帕累托方案**。这些点的位置可以说明各自块体形式的三个性能优缺点。如图 9(a)所示，**帕累托解决方案位于可行解决方案空间的最前沿**。它们的位置靠近坐标交点，表明帕累托最优解优于其他可行解。

>Fig. 9. Distribution of Pareto and feasible solutions. (a) 3D spatial distribution of solutions; (b) 2D spatial distribution of solutions: Av.LM and EUIt; (c) 2D spatial distribution of solutions: Av.LM and SH; (d) 2D spatial distribution of solutions: EUIt and SH.

![[Distribution of Pareto and feasible solutions.jpg]]

>图 9. 帕累托方案和可行方案的分布。(a) 解的三维空间分布；(b) 解的二维空间分布： Av.LM 和 EUIt； (c) 解的二维空间分布： (d) 解的二维空间分布： EUIt 和 SH。

如图 10（a）所示，可行解的 Av.LM 主要分布在 0.245-0.352 之间。这些解的 Av.LM 的中值和均值分别为 0.305 和 0.308。同时，帕累托方案的 Av.LM 主要分布在 0.278-0.354 之间，中位数和平均值分别为 0.317 和 0.314。

可行方案和帕累托方案的 EUIt（kWh/m2/y）分布如图 10（b）所示。可行解决方案的 EUIt 范围主要集中在 68.1 至 71.9 之间，平均值为 69.7，中位数为 69.4。方框图显示了许多能耗超过 72.0 的异常值。相比之下，帕累托解决方案的数据分布高度集中，EUIt 主要在 68.1 至 69.1 之间，中位数和平均值分别为 68.5 和 68.7。值得注意的是，离群点的最大 EUIt 也低于 70.0，这表明帕累托方案比可行方案更节能。

图 10(c) 显示，可行解决方案的 SH (h) 中值和均值分别为 6.7 和 6.5，其分布范围主要在 5.2-7.4 之间。在方框图中，许多离群点都低于可行方案的下限，这表明可行方案的平均日照时数数据分布较为分散，且变化较大。相比之下，帕累托方案的 SH 范围主要分布在 6.7 至 7.4 之间，中位数和平均数分别为 7.0 和 6.9。帕累托方案的数据分布高度集中，表明采光性能更好。

根据前面的数据分析，本次优化中各目标的帕雷托方案性能普遍优于可行方案，且各项性能均有较为明显的提升。

# 块状设计变量分析

---
# 结论

本研究建立了一个优化城市街区形式的框架，优先考虑能源和环境性能。该方法通过最小化 EUIt、最大化 Av.LM 和 SH 来平衡能源和环境性能，并将其作为案例应用于中国建湖市的一个理想住宅小区。本研究选择了城市形态设计变量来生成参数化街区形态。优化共获得 1896 个有效解，其中 58 个为帕累托最优解。

研究结果表明，在建湖地区，具有特定形态特征的城市街区具有更优越的环境性能和更高的能效。南低北高的布局、形式简单的建筑类型以及街区西南角的开放空间是这些街区的一些显著特征。

此外，研究结果表明，城市街区的形态对建筑能耗、光伏发电和日照都有至关重要的影响。街区形态优化可以极大地改善街区各方面的性能，是创建可持续节能街区的重要工具。总之，所提出的优化框架可以为城市设计提供有价值的支持，有助于实现可持续和节能型城市发展的目标。这项工作存在局限性。不过，这些局限性突出了可在未来研究中进一步探索和改进的领域。

首先，本研究选择了一些设计变量来控制参数化街区形式的生成。在今后的研究中，可以考虑加入更多的设计变量，如方向，使生成的最优解具有更多的可能性。

其次，在本研究中，模拟城市街区的性能花费了大量的时间和运算能力。这将是一个不可避免的挑战，尤其是在模拟更大规模的区域时。因此，有必要采用机器学习预测算法等新方法，帮助缩短街区性能评估时间，加快优化速度。

最后，需要指出的是，本研究是一项理论探索，采用模拟方法分析了相同条件下各种区块形式的性能优缺点。尽管如此，在实际项目中检验模拟结果的准确性和研究结论的实用性仍是当务之急。
