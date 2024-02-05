![[../../归档/picture/基于GNN的剪力墙结构布梁设计方法.png]]

# 结构案例的结构与建筑布局
![[../../归档/picture/结构案例的结构与建筑布局.png]]

 [[Beam layout design of shear wall structures based on graph neural networks]]

#参数化设计 #剪力墙结构 #GNN #Graph_Neural_Networks 

## Highlights

- •   
    An approach for designing beam layouts in shear wall structures that can account for topological features is presented.
    
- •
    A graph representation method for beam layout scenarios of shear wall structures is proposed.
    
- •
        A method for generating potential beam layout scenarios is presented.

梁的布置是剪力墙结构设计的关键环节。现阶段已经提出了基于生成对抗算法(GAN)的剪力墙结构梁布置设计方法并取得了一定的成功。

直接基于剪力墙的布置去预测梁在剪力墙上的布置形式，会面临几乎无限的梁布置的可能性空间，这无疑极大增加了图的复杂度，增加了预测的难度。因此，本研究提出了考虑结构和建筑构件的空间布置以及工程师经验的潜在梁布置场景生成方法，以有效减少梁布置场景的可能性空间。测试案例表明，本研究所提出方法布置的梁和工程师设计相比具有高相似性。

![[../../归档/picture/剪力墙梁布置GNN_研究难题和关键科学问题.jpg]]

本研究提出的剪力墙结构的GNN梁布置智能设计方法，如图2所示，包括以下三个部分。

**（1）数据准备阶段：潜在梁布置方案图的生成**

直接基于剪力墙的布置去预测梁在剪力墙上的布置形式，会面临极大的梁布置方案的可能性空间。不仅数据量大，而且不能很好的考虑隔墙、门窗等建筑构件布置的影响以及工程师的设计经验。因此，本研究提出耦合结构构件和建筑构件的空间布置以及工程师设计经验的潜在梁布置方案生成方法。

**（2）模型训练阶段：GNN模型训练**

本研究提出了梁布置方案的图表征方法及GNN模型，并基于预设的潜在梁布置方案数据进行神经网络模型的训练。

**（3）AI设计阶段：基于GNN模型实现剪力墙结构的梁布置设计。**

![[../../归档/picture/基于GNN的剪力墙结构梁布置方案设计方法.jpg]]

## 核心技术

### **潜在梁布置方案的生成**

在工程实际中，剪力墙结构中梁的布置往往和剪力墙的布置以及隔墙、门窗等建筑构件布置相关。因此，在生成潜在梁布置方案时，本研究主要参考剪力墙的布置以及隔墙、门窗等建筑构件的布置。此外，工程师的经验对梁布置也是至关重要的，因此，本研究在生成潜在梁布置方案时，定义了一些有望使梁布置方案更合理的规则，如图3所示，具体规则详见论文。

![[../../归档/picture/潜在梁布置方案的生成规则.jpg]]

在进行主梁的潜在梁布置方案生成中，主要考虑三类布置方案，即：  

Scenario-NB（No Background），不考虑隔墙、门窗等非结构构件（即“建筑布置背景”）对梁布置的影响；

Scenario-WB（With Background），考虑“建筑布置背景”对梁布置的影响，仅在填充墙、门窗等构件的位置布置梁；

Scenario-HR（Hybrid Rule），混合考虑“建筑布置背景”的影响。

这三类布置方案的示意如图4所示，综合考虑建筑非结构构件布置的影响，可以综合另外两种的优势。

![[../../归档/picture/主梁的潜在梁布置方案.jpg]]

###  **潜在梁布置方案的图表征**
...

ai-structure.com

## 生成式智能结构设计

![[../../归档/picture/生成式智能结构设计.jpg]]
