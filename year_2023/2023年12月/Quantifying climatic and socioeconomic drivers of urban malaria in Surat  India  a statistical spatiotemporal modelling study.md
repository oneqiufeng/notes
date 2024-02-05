#The_Lancet_Planetary_Health #中科院医学一区 #SCI_Q1
# Quantifying climatic and socioeconomic drivers of urban malaria in Surat, India: a statistical spatiotemporal modelling study
## Background
Cities are becoming increasingly important habitats for mosquito vectors of disease. The pronounced heterogeneity of urban landscapes challenges our understanding of the effects of climate and socioeconomic factors on mosquito-borne disease dynamics at different spatiotemporal scales. Here, we quantify the impact of climatic and socioeconomic factors on urban malaria risk, using an extensive dataset in both space and time for reported Plasmodium falciparum cases in the city of Surat, northwest India. （利用印度西北部苏拉特市报告的恶性疟原虫病例的大量时空数据集，**量化了气候和社会经济因素对城市疟疾风险的影响**。）

![[../../归档/picture/Map of the study zones and time series of P falciparum cases in the central zone in 2008–14.png]](#pic_center)

## Methods 
We analysed 10 years of monthly P falciparum cases resolved at three nested spatial resolutions (seven zones, 32 units, and 478 worker units) with a Bayesian hierarchical mixed model that incorporates the effects of population density, poverty, relative humidity, and temperature, in addition to random effects (structured and unstructured). To reduce dimensionality and avoid correlation of covariates, socioeconomic variables from survey data were summarised into main axes of variation using principal component analysis. With model selection, we identified the main drivers of spatiotemporal variation in malaria incidence rates at each of the three spatial resolutions. We also compared observations to model-fitted cases by quantifying the percentage of predictions within five discrete levels of malaria risk. 
- 该模型除随机效应（结构化和非结构化）外，还包含人口密度、贫困、相对湿度和温度的影响。
- 使用主成分分析法将调查数据中的社会经济变量归纳为变异主轴
- **三种空间分辨率下**疟疾发病率时空变化的主要驱动因素
- **量化五个离散疟疾风险等级内的预测百分比**，观测结果与模型拟合案例进行比较

## Findings 
The spatial variation of urban malaria cases was stationary over time, whereby locations with high and low yearly cases remained largely consistent across years. Local socioeconomic variation could be summarised with three principal components accounting for approximately 80% of the variance. The model that incorporated local temperature and relative humidity together with two of these principal components, largely representing population density and poverty, best explained monthly malaria patterns in models formulated at the three different spatial scales. As model resolution increased, the effect size of humidity decreased, whereas those of temperature and the principal component associated with population density increased. Model predictions accurately captured aggregated total monthly cases for the city; in space-time, they more closely matched observations at the intermediate scale, with around 57% of units estimated to fall in the observed category on average across years. The mean absolute error was lower at the intermediate level, showing that this is the best aggregation level to predict the space-time dynamics of malaria incidence rates across the city with the selected model. 

![[../../归档/picture/Quantifying climatic and socioeconomic drivers of urban malaria in Surat,_Mauricio Santos-Vega et al_页面_07.jpg]]

## Interpretation 
This statistical modelling framework provides a basis for development of a climate-driven early warning system for urban malaria for the units of Surat, including spatially explicit prediction of malaria risk several weeks to months in advance. Results indicate environmental and socioeconomic covariates for which further measurement at high resolution should lead to model improvement. Advanced warning combined with local surveillance and knowledge of disease hotspots within the city could inform targeted intervention as part of urban malaria elimination efforts.

## Discussion

![[../../归档/picture/Quantifying climatic and socioeconomic drivers of urban malaria in Surat,_Mauricio Santos-Vega et al_页面_11.jpg]]

# 翻译 - 量化印度苏拉特城市疟疾的气候和社会经济驱动因素：一项**统计时空建模**研究
mosquito vectors of disease：蚊媒疾病
The pronounced heterogeneity of urban landscapes challenges our understanding of the effects of climate and socioeconomic factors on mosquito-borne disease dynamics at different spatiotemporal scales. 城市景观的显著异质性对我们理解气候和社会经济因素在不同时空尺度上对蚊媒疾病动态的影响提出了挑战。
## 一些分析方法
1. 然后，我们对时空系统进行了标准的单变量统计分析，以**评估每1000人中疟疾病例的空间依赖性**。也即是：通过时间(附录p 3).43计算单变量[[Moran指数]]( Moran ' s I)，44 Moran ' s I用于确定全局空间关联程度(**在一个位置上感兴趣变量的大小对其在附近区域的大小有多大影响**).