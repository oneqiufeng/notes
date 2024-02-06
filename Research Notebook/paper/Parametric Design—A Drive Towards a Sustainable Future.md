# 参数化设计——迈向可持续发展的未来

## Abstract

Traditionally, design involves the development of ideas within a static environment. Identifying the optimal solution can be a time-consuming and highly iterative process, with numerous variables which could be altered and investigated.

传统上，设计是在静态的环境中进行思想的发展。确定最优解可能是一个耗时且高度迭代的过程，其中有许多变量可以被改变和研究。

Due to time constraints, the full breadth of combinations is rarely assessed, and the ﬁnal solution is usually identiﬁed using experience and design judgement. The result is often a reproduction of tried and tested designs without exploration of innovative and new ideas, with potentially beneﬁcial options remaining untested.

由于时间限制，很少对各种组合进行全面评估，通常是根据经验和设计判断来确定最终解决方案。这样做的结果往往是重复那些经过试验和测试的设计，而没有对创新和新想法进行探索，潜在的有益方案仍然没有经过测试。

Parametric design allows a more dynamic approach. Using parametric software, key project parameters can be identiﬁed and rapidly altered to allow different solutions to be tested with relatively little effort. Combined with optimisation algorithms, the design outcomes of each option can be understood and evaluated. In its basic form, parametric design can bring about considerable design efﬁciency on projects across the built environment.

参数化设计是一种更加动态的方法。使用参数化软件，可以确定并快速改变项目的关键参数，从而以相对较少的工作量测试不同的解决方案。结合优化算法，可以了解和评估每个方案的设计结果。就其基本形式而言，参数化设计可以为整个建筑环境项目带来相当大的设计效率。

At a deeper level, however, questions can be asked on materiality, minimisation of waste and optimisation of the construction process itself. The key for unlocking and driving sustainable design across the built environment may therefore lie in the ability to understand the variability of design and drive positive outcomes through the use of parametric tools. This chapter will overview the basic principles of parametric design and present a selection of case studies into the practical application of the technology to achieve positive project outcomes. Addressing key lessons learnt, the opportunities to drive the future of design to achieve sustainable outcomes will be outlined.

然而，在更深的层面上，还可以就材料性、最大限度地减少浪费和优化施工过程本身提出问题。因此，在整个建筑环境中开启和推动可持续设计的关键可能在于了解设计的可变性并通过使用参数化工具推动积极成果的能力。本章将概述参数化设计的基本原理，并介绍一些案例研究，说明如何实际应用该技术来实现积极的项目成果。在总结主要经验教训的同时，还将概述推动未来设计实现可持续成果的机遇。

## Keywords

#Parametric_Design #Parametric_Modelling #Genetic_Algorithm #Topology_Optimisation

## Introduction

Traditional design methodologies involve the development of geometric options and technical elemental design within a static environment. Whilst, in any given project, there are numerous variables which can be investigated; a full assessment of the potential beneﬁts of differing combinations can be a time-consuming iterative process. Due to time, budget and resource constraints, the full breadth of solutions is rarely assessed, and the ﬁnal solution is often identiﬁed using experience and design judgement. Whilst this tried and tested way of working delivers satisfactory options, potential optimal solutions may remain untested, leaving new and potentially innovative and more sustainable designs unconsidered. With the need to challenge building design to deliver better environmentally sustainable outcomes, historic methods of design will not allow rapid testing of new ideas. These historic methods, with individual elements, be they structural elements, façade components or MEP systems, being designed manually for the geometry which is under consideration, do not allow the full optimisation of key parameters (materials, geometric layout, embodied carbon, etc.), to enable designers to identify the best outcome for future buildings.

传统的设计方法包括在静态环境中开发几何方案和技术要素设计。虽然在任何特定项目中，都有许多变量可以研究，但全面评估不同组合的潜在优势可能是一个耗时的反复过程。由于时间、预算和资源的限制，很少会对各种解决方案进行全面评估，最终的解决方案往往是通过经验和设计判断来确定的。虽然这种久经考验的工作方式能够提供令人满意的方案，但潜在的最佳解决方案可能仍未得到检验，从而使新的创新和更具可持续性的设计未得到考虑。由于需要对建筑设计提出挑战，以实现更好的环境可持续发展成果，历史悠久的设计方法无法对新想法进行快速测试。这些传统的设计方法，无论是结构元素、外墙组件还是 MEP 系统，都是针对正在考虑的几何形状进行人工设计，无法对关键参数（材料、几何布局、隐含碳等）进行全面优化，从而使设计师能够为未来的建筑确定最佳结果。

Parametric modelling and design allow a more dynamic approach to design to rapidly assess multiple options and push the selected design towards a chosen optimal outcome. Through the identiﬁcation of variable parameters across the project, parametric software can be used to rapidly alter key variables to allow different solutions to be tested with relatively little effort and in a compressed timeframe. Each combination can easily be reviewed the impact on other parameters, and the key beneﬁts and drawbacks of multiple options can be collaboratively discussed with design partners to identify the optimal solution.

参数化建模和设计允许采用更动态的设计方法来快速评估多种方案，并将选定的设计推向所选的最佳结果。通过确定整个项目的可变参数，参数化软件可用于快速改变关键变量，从而在相对较短的时间内测试不同的解决方案。每种组合都可以轻松审查对其他参数的影响，并与设计合作伙伴共同讨论多种方案的主要优点和缺点，以确定最佳解决方案。

### Parametric Modelling Versus Parametric Design

Whilst linked, it should be noted that parametric modelling and design are two separate aspects of computational design. Computational design—the use of computational strategies to aid the design process—has been gaining more traction in the last decade. Used as a tool to extend and enhance traditional design skills, the use of computers and more accessible visual programming languages has unlocked opportunities to further optimise and automate the design process across the majority of disciplines in the built environment.

参数化建模和设计是计算设计的两个不同方面，虽然两者相互关联，但应注意的是，参数化建模和设计是计算设计的两个不同方面。计算设计——使用计算策略来辅助设计过程——在过去十年中得到了越来越多的关注。计算机和更易于使用的可视化编程语言被用作扩展和提高传统设计技能的工具，为进一步优化和自动化建筑环境中大多数学科的设计过程提供了机会。

The use of parametric modelling has allowed designers to unlock the optimised possibilities that are available through geometric parametric manipulation. Whilst traditional modelling involves deﬁning static geometry—drawing 3D elements in space, interconnected to form a building massing, parametric modelling involves the deﬁnition of variable parameters to the elements. This allows rapid manipulation of the 3D geometry of the massing through varying the parameters assigned to the building components.

参数化建模的使用使设计师能够通过几何参数化操作释放优化的可能性。传统建模包括确定静态几何图形——在空间中绘制三维元素，相互连接形成建筑体量，而参数建模则包括确定元素的可变参数。这样就可以通过改变建筑构件的参数，快速调整建筑群的三维几何形状。

The next evolution of parametric modelling is parametric design, where the design outcome of the geometric options is automatically altered to suit the new arrangement. Parametric design is about automating the work (Debney, 2020). For static geometry, an engineer will need to design each column. However, if the column height is a variable parameter in a model, designing each iteration of the column height would be a lengthy exercise. Parametric design automates this process, applying algorithms to the model which identify the most appropriate size for the column given its height, allowing an automatically reactive model which self-updates based on the geometric manipulation.

参数化建模的下一个发展方向是参数化设计，即自动改变几何选项的设计结果，以适应新的布置。参数化设计就是将工作自动化（Debney，2020 年）。对于静态几何图形，工程师需要设计每根立柱。但是，如果柱高是模型中的一个可变参数，那么设计柱高的每一次迭代都将是一项漫长的工作。参数化设计将这一过程自动化，将算法应用到模型中，根据柱子的高度确定最合适的尺寸，使模型能够自动反应，并根据几何操作进行自我更新。

This generative design activity allows not only the spatial impacts to be understood, but also a host of other data which can be used to assess options, including material sizes, carbon quantities and net ﬂoor areas. The two differing techniques are discussed in this chapter, with outline case studies discussing the use of both.

通过这种生成式设计活动，不仅可以了解空间影响，还可以利用大量其他数据对方案进行评估，包括材料尺寸、碳量和净室内面积。本章将讨论这两种不同的技术，并通过简要案例研究讨论这两种技术的使用。

### The Future of Parameterisation

In the drive towards an environmentally sustainable future, this ability to assess the variability of key design parameters may be key to unlocking viable building designs which can deliver on both economic and sustainable design principles. Indeed, the most proliﬁc use to date for parametric modelling has been to understand, model and construct complex buildings around the world. This has resulted in some truly fantastic architecture; however, the next generation of parametric designs should aim to push the boundaries of sustainable design, using the tools on offer to optimise our environmental impact of the next generation of building typologies.

在迈向环境可持续的未来的过程中，这种评估关键设计参数的可变性的能力可能是开启可行的建筑设计的关键，它可以实现经济和可持续的设计原则。事实上，迄今为止参数化建模最多产的用途是理解、建模和构建世界各地的复杂建筑。这就产生了一些真正神奇的建筑；然而，下一代参数化设计的目标应该是推动可持续设计的边界，使用提供的工具来优化我们对下一代建筑类型的环境影响。

## Parametric Design Software

There are numerous different software packages which can be used for parametric modelling, each one with different user interfaces and mechanisms for parameterising the design. The commonly used packages can be used across a range of applications, including product and mechanical component design through a building geometry. With a range of plugin’s and differing user interfaces, selecting the best package to use will depend on the intended use and experience in CAD software. Some of the more commonly used packages include those listed below.

有许多不同的软件包可用于参数化建模，每种软件包都有不同的用户界面和参数化设计机制。常用的软件包可用于各种应用，包括产品和机械部件设计以及建筑几何设计。由于有一系列插件和不同的用户界面，选择最佳软件包将取决于 CAD 软件的预期用途和经验。以下是一些比较常用的软件包。

- Rhino 3D with Grasshopper 3D plugin
- Autodesk Dynamo
- Solidworks
- Catia
- Creo Parametric
- FreeCAD
- Siemens NX
- Autodesk Inventor

Whilst a number of packages require previous experience in CAD, there are some which are more tailored towards beginners in the ﬁeld of parametric design. For most packages, there are numerus free online tutorials available, covering introductions to the basics of use, through an advanced application.

虽然许多软件包要求用户有 CAD 方面的经验，但也有一些软件包更适合参数化设计领域的初学者。对于大多数软件包，都有许多免费的在线教程，从基础使用入门到高级应用，一应俱全。

For the purposes of the following examples and case studies, we have used Rhino 3D and Grasshopper, due to the prevalence in the architectural and engineering ﬁelds. Rhino 3D with the Grasshopper Plugin, uses a visual programming language to input the design geometry and alter the parametric values assigned to this geometry. A range of computational plugins are available to allow optimisation algorithms to be run within Grasshopper and visualised in Rhino.

由于 Rhino 3D 和 Grasshopper 在建筑和工程领域的广泛应用，我们在以下示例和案例研究中使用了这两种语言。带有 Grasshopper 插件的 Rhino 3D 使用可视化编程语言输入设计几何体，并更改分配给几何体的参数值。一系列计算插件允许在 Grasshopper 中运行优化算法，并在 Rhino 中实现可视化。

## Basic Principles of Parametric Modelling and Design

Parametric design is widespread in historical designs around us. Perhaps, the most well-known example is the work which was done by Antonio Gaudi during the design of the Sagrada Familia. His use of hanging weights and chains to ﬁnd the most optimal form for the building, and the ability to vary the lengths of the chains and see the resultant form changes is an early form on physical parametric modelling.

参数化设计广泛存在于我们身边的历史设计中。最著名的例子可能是安东尼奥-高迪在设计圣家堂时所做的工作。他利用悬挂的砝码和链条为建筑找到了最理想的形式，并且能够通过改变链条的长度来观察形式的变化，这是物理参数建模的早期形式。

The idea of using hanging chains to derive the idealised form of a catenary arch was ﬁrst proposed by Robert Hooke in 1675, when he postulated that: 

罗伯特-胡克（Robert Hooke）于 1675 年首次提出了利用悬链推导出理想化的悬索拱形的想法： 

> Ut pendet continuum ﬂexile, sic stabit contiguum rigidum inversum 
> As hangs a ﬂexible cable so, inverted, stand the touching pieces of an arch 

The use of this theory to deﬁne a catenary arch led to the design and construction of many of our landmark architectural buildings, including St Paul’s Cathedral in London, designed by Christopher Wren, who consulted with Hooke in the design of the dome at St Pauls to reduce the thickness of the dome itself.

利用这一理论来定义双曲拱桥，设计和建造了我们许多具有里程碑意义的建筑，包括克里斯托弗-雷恩（Christopher Wren）设计的伦敦圣保罗大教堂（St Paul's Cathedral）。

![[Gaudi’s physical parametric model and examples of funicular shapes in 2D.png]]

Fig.1 _Gaudi’s physical parametric model and examples of funicular shapes in 2D_

This theory, of hanging chains to ﬁnd forms, allowed numerous architects and engineers to play with the two key parameters in the physical model—the length of the chain and the width of the supports, to develop stable designs for many historic buildings (Fig. 2).

Whilst we now use computational software to undertake parametric modelling, the principles are still the same as in Hooke and Gaudi’s day. The fundamental principle of parametric modelling is the ability to varying key design parameters to investigate the impact on the holistic design. In a standard design project, the design team will step through a decision tree, making choices on key elements of the design as they progress. The further along the tree the team travels, the more difﬁcult it is to backstep and try different options to see if there is value in change. To back up the tree too far would be costly and time-consuming, and with the typical programme pressures on design teams, this is not often done. This means that potentially value adding options are taken off the table early on during the design process (Fig. 3).

In essence, parametric design involves a dynamic decision tree, where you can ﬂick between differing values of variables throughout the project rather than locking in a decision earlier on. This maintains ﬂexibility during the design process and the ability to rapidly step back up the decision tree to test different options (Fig. 4).

### The Basic Process

The basic process starts with the development of a parametric model and then extends to the inclusion of the required design algorithms to allow generative design outcomes. It is key at this stage to understand what the intended outcome of any parametric study is to be, which allows the model to be set up with the correct interdependencies between design features, known as parameters.

基本流程从开发参数模型开始，然后扩展到包含所需的设计算法，以实现生成设计结果。在这一阶段，关键是要了解参数研究的预期结果是什么，这样才能在模型中设置正确的设计特征（即参数）之间的相互依存关系。

The process therefore begins with the identiﬁcation of key parameters (or design features) and constraints within the design. Typical constraints could be:

- The Site Boundary.
- Planning Constrains building height.
- Material availability.
- Below ground constraints, including buried services or assets.
- Foundation constraints, including capacity or adjacency to waterways or other assets.

Static decision tree (author original)
![[Static decision tree (author original.png]]

Dynamic decision tree (author original)
![[Dynamic decision tree.png]]

-  Structural span lengths or depth constraints.
	-  Once the constraints are deﬁned and the building has boundaries for optimisation within, the key design parameters can then be identiﬁed. These could include:
		- Material types and quantities.
		- Structural column grid. 
		- Floor-to-ﬂoor heights. 
		- Service distribution zones. 
		- Loading requirements.

This list of parameters can be used to start developing the base parameters which will be used as the outline for the creation of model (Fig. 5).

![[Model development outline.png]]
Fig.5 _Model development outline_

At this point, it is worth considering the value of varying different parameters and whether constraints should be added to the parameter variation. For instance, if the structural grid is likely going to need to support a unitised façade system on a multiple of 1.5 m centres, then the parameterisation of the structural grid can be linked to this value. The more parameters which are added to the list, the more complex the model will become, and this may result in a more positive outcomes as more options which will be produced for investigation. Conversely, the more complex the model becomes, the more potentially for error in the model and analysis, and the more difﬁcult it may become to set up and manage the model. In some instances, therefore, there is little value in varying certain parameters—for instance if there is a client requirement for a certain ﬂoor-to-ﬂoor height, or certain materials are likely to command a premium in a certain geographic location. One common ﬂaw of parametric modelling is to overcomplicate the parameters. Experience of both parametric modelling and design can help to identify key parameters which drive better outcomes and root out inconsequential parameters. This simpliﬁes the modelling, the analysis run time and overall design process.

此时，值得考虑的是改变不同参数的价值，以及是否应在参数变化中添加限制条件。例如，如果结构网格可能需要在 1.5 米中心的倍数上支持一个单元化的外墙系统，那么结构网格的参数化就可以与这个值联系起来。添加到列表中的参数越多，模型就会变得越复杂，这可能会产生更积极的结果，因为会有更多的方案可供研究。反之，模型越复杂，模型和分析出错的可能性就越大，模型的建立和管理也就越困难。因此，在某些情况下，改变某些参数的价值不大--例如，如果客户要求特定的层到层高度，或者某些材料在特定的地理位置可能会溢价。参数建模的一个常见缺陷是参数过于复杂。参数化建模和设计的经验可以帮助确定关键参数，从而获得更好的结果，并剔除无关紧要的参数。这样可以简化建模、分析运行时间和整体设计过程。

Once the list of parameters is identiﬁed, it is possible to start identifying the interdependencies and the limits of each of the variables and identifying the required calculations which will need to be embedded in the model to allow the implications of key decisions to be overviewed. 

一旦确定了参数清单，就可以开始确定每个变量之间的相互依存关系和限制，并确定需要嵌入模型的必要计算，以便对关键决策的影响进行概述。

Once the key parameters, constraints and interdependencies are identiﬁed, it is possible to begin developing the parametric model to evaluate the outcomes of the various options. 

一旦确定了关键参数、制约因素和相互依存关系，就可以开始开发参数模型，对各种方案的结果进行评估。

With the model now set up, it is possible to begin to add in the feedback loops, and algorithms needed to develop the parametric design aspect of the project. These algorithms will allow iterative design solutions to both update the elemental design due to geometric changes and optimise the design to drive efﬁciencies and idealised solutions.

有了现在建立的模型，就可以开始添加反馈回路和算法，以开发项目的参数化设计方面。这些算法将允许迭代设计解决方案，既能根据几何变化更新元素设计，又能优化设计以提高效率和理想化解决方案。

## Parametric Modelling

The key tools in the parametric modelling process include the deﬁnition of the parameters, their variability, the interdependencies between them and any constraints associated with the design in question. It is perhaps prudent to deﬁne a ‘parameter’ and make a distinction between it and a constraint. The dictionary deﬁnition of parameter is a ‘measurable factor forming one of a set that deﬁnes a system or sets the conditions of a systems operation’. But, it is perhaps best to consider a parameter as a variable design feature which both contributes to and constrains the design. Constraints, which are themselves another type of design feature, are different in that they are ﬁxed design feature. It is also important to recognise parameters, and constraints can sometimes be interchanged. For example, a door width can be a parameter for a room layout if it can go on any position on any wall or be any width. Whereas, a door can be a design constraint if it is ﬁxed in position and width, say it is an existing doorway into an already constructed room. 

参数化建模过程中的关键工具包括参数的定义、参数的可变性、参数之间的相互依存关系以及与相关设计有关的任何约束条件。为慎重起见，应先定义 "参数"，并将其与约束条件区分开来。在字典中，参数的定义是 "可测量的因素，构成确定系统或设定系统运行条件的集合之一"。但是，也许最好将参数视为一种可变的设计特征，它既有助于设计，又对设计构成制约。约束本身是另一种类型的设计特征，但它们的不同之处在于它们是固定的设计特征。同样重要的是要认识到，参数和约束条件有时可以互换。例如，门的宽度可以是房间布局的一个参数，如果它可以位于任何墙壁的任何位置或任何宽度的话。而如果一扇门的位置和宽度是固定的，比如说它是进入一个已建成房间的现有门洞，那么它就可以成为一个设计约束条件。

Deﬁnition of the parameters themselves needs to be accompanied with the limits of their variability. For instance, in their most basic form, this can be simply a numerical range which is applied to the parameter.

在确定参数本身的同时，还需要确定其可变性的限度。例如，在最基本的形式中，这可以是一个适用于参数的简单数字范围。

![[Parameterised column—overview and Grasshopper 3D (author original).png]]

>Figure 6 : Parameterised column — overview and Grasshopper 3D (author original)

By way of simple example, let us assume, we want to allow the variability of the ﬂoor-to-ﬂoor height of a single ﬂoor plate. Figure 6 indicatively deﬁnes a column height, varying the height whilst keeping the base in a ﬁxed location.

举个简单的例子，假设我们想让单个楼板的楼板到楼板的高度发生变化。图 6 给出了柱子高度的示意图，在改变高度的同时，底座保持在一个固定的位置。

Once a key parameter can be identiﬁed and deﬁned, it is then possible to link a number of elements to this parameter. Building on the previous example, this will then allow a whole ﬂoor of column lengths to be varied, in essence varying the ﬂoor-to-ﬂoor height across the project.(Fig.7)

一旦确定并定义了一个关键参数，就可以将多个元素与该参数联系起来。在前一个例子的基础上，这样就可以改变整层楼的柱子长度，从而改变整个项目的楼到楼高度。

![[Linking of elements to the parameter—overview and Grasshopper 3D (author original).png]]

>Figure 7 : Linking of elements to the parameter—overview and Grasshopper 3D (author original)

Building on this example, adding in an additional variable—the number of ﬂoors in the building—can then allow us to play with how many levels we can achieve within the given height. By adding in another variable parameter and linking this to the column heights, it is possible to play with the two variables, or parameters, in order to investigate various options (Fig. 8).

在这个例子的基础上，增加一个额外的变量“建筑物的楼层数”可以让我们在给定的高度内实现多少层。通过添加另一个变量参数并将其与柱高联系起来，我们可以利用这两个变量或参数来研究各种方案（图 8）。

![[Adding the additional variable—overview and grasshopper 3D (author original).png]]

>Figure 8 : Adding the additional variable—overview and grasshopper 3D (author original)

Whilst a simple example, this basic model could be useful to understand the implications of adding an additional ﬂoor, for instance will saving ~100 mm in the servicing zone at each ﬂoor allow an additional storey? This value-added discussion is relatively simply answered using even a basic parametric model.

虽然这只是一个简单的例子，但这一基本模型有助于了解增加一层楼的影响，例如，在每层楼面的维修区节省约 100 毫米是否就能增加一层楼？即使使用基本的参数模型，也可以比较简单地回答这一增值问题。

It is also possible to add in a number of ‘intelligent’ algorithms to the system which can allow some implications of varying the parameters to be seen. The most obvious one would be the structural column size:

此外还可以在系统中加入一些 "智能 "算法，以了解改变参数的影响。最明显的就是结构柱的尺寸：

- As the storey height increases, so too does the effective length of the column. 
- As the number of storeys increases, so will the load applied to the column.

Both of these aspects will affect the design of the column and cause it to increase or decrease in size and tonnage. Using a linked algorithm to calculate the size of the columns in the above model, it is therefore possible to extract the tonnage output and implications of varying the inter-storey height and the number of storey in the building. Whilst this is a simple example, there are further opportunities to optimise the output, covered in more detail in the following section.

这两个方面都会影响支柱的设计，并导致其尺寸和吨位的增减。因此，使用链接算法计算上述模型中支柱的尺寸，可以提取吨位输出以及改变层间高度和建筑物层数的影响。虽然这只是一个简单的例子，但还有更多优化输出的机会，下文将详细介绍。

The above outline gives a ﬂavour of the parametric design process and basic tools; however, this is the tip of the iceberg in terms of capabilities of the various available software packages. Some further examples and recommended exercises for Grasshopper in particular can be found on the below resources.

以上概要介绍了参数化设计流程和基本工具，但这只是各种可用软件功能的冰山一角。有关 Grasshopper 的更多示例和推荐练习，请参阅以下资源：

- Grasshopper 3D Tutorials([Tutorials - Grasshopper (grasshopper3d.com)](https://www.grasshopper3d.com/page/tutorials-1))
- McNeel Wiki Tutorials([Grasshopper Tutorials [McNeel Wiki]](https://wiki.mcneel.com/labs/explicithistory/examples))
- Parametric House([Rhino Grasshopper Tutorials | Parametric House](https://parametrichouse.com/rhino-grasshopper/))
- Black Spectacles([Black Spectacles](https://www.blackspectacles.com/topics/grasshopper-rhino-tutorials-training))

A number of other, paid and more in depth training resources for the varying different parametric software packages can be found on platforms such as Plural- sight([pluralsight.com](https://www.pluralsight.com/)). These resources allow upskilling of organisations and individuals for a rela- tively modest cost and would be a recommended place to start when embarking on the journey into parametric modelling and design.

在 Plural- sight 等平台上还可以找到其他一些付费的、更深入的培训资源，用于不同的参数化软件包。这些资源可以帮助组织和个人提高技能，而且费用相对较低，是开始参数化建模和设计之旅的推荐起点。

## Parametric Design

The next evolution of parametric modelling is parametric design, where the use of built in or bespoke algorithms to generate a design outcome from the parametric model. This technique can be used to further develop the geometric options described in Section 0 to identify efﬁciencies in the overall design. This could include the most efﬁcient use of materials, the most optimal spatial layout and least amount of embodied carbon or any manner of targets which can be linked to the parameters in question. There are various options for undertaking optimisation design, using a variety of plugins to the available software. These can be used individually to target speciﬁc design drivers, or can be linked together to evolve a design in conjunction with other design consultants.

参数建模的下一个发展阶段是参数设计，即使用内置或定制算法从参数模型中生成设计结果。这种技术可用于进一步开发第 0 节中描述的几何选项，以确定整体设计中的优缺点。这可能包括最有效地使用材料、最理想的空间布局、**最少的含碳量**或任何与相关参数有关的目标。利用现有软件的各种插件进行优化设计有多种选择。这些插件可以单独使用，以特定的设计驱动因素为目标，也可以连接在一起，与其他设计顾问共同发展设计。

### Form Finding

Form ﬁnding is the method of ﬁnding an efﬁcient 3-dimensional form for a complex surface, or series of elements. Used frequently in the structural design of organic shapes, the technique uses bespoke algorithms to identify the geometric form which provides the most efﬁcient structural result to a deﬁned set of rules. Often this method is used to deﬁne grid shells and other natural gravity systems, where the elements of the system are in pure axial load rather than under bending. This technique has been well documented and was used by Gaudi to deﬁne the structure of the Sagrada Familia as described in Section 3. This technique aims to identify a certain geometry, bespoke to the particular constraints that removes all bending actions in the elements. This geometry is known as a funicular form and is often the target of the majority of form ﬁnding designs (Fig. 9).

形状确定是一种为复杂表面或一系列元素确定有效三维形状的方法。该技术常用于有机形状的结构设计中，它使用定制算法来确定几何形状，从而为确定的规则集提供最有效的结构结果。这种方法通常用于确定网格壳体和其他自然重力系统，其中系统的元素处于纯轴向载荷而非弯曲状态。高迪曾使用这种技术来确定圣家堂的结构，如第 3 节所述。这项技术旨在确定特定的几何形状，并根据特定的约束条件消除元素中的所有弯曲作用。这种几何形状被称为漏斗形，通常是大多数造型设计的目标（图 9）。

![[Form ﬁnding of rectangular area with uniform loads (author original).png]]

>Figure 9 : Form ﬁnding of rectangular area with uniform loads (author original)

### Manual Optimisation

There are various ways of undertaking manual optimisation within Grasshopper, using manually input algorithms and constructing feedback loops to re-analyse the output until a set of target results are achieved. Through this technique, the implications of geometric alterations can be understood and allow informed decisionmaking. For instance, increasing the column grid will either increase the ﬂoor plate steel tonnages or will increase the depth of the beams. These two options can be assessed to select the most appropriate for the particular project (Fig. 10).

在 Grasshopper 中进行手动优化的方法有很多种，可以使用手动输入算法和构建反馈回路来重新分析输出，直到达到一组目标结果。通过这种技术，可以了解几何改动的影响，从而做出明智的决策。**例如，增加柱格要么会增加楼板钢材吨数，要么会增加梁的深度**。可以对这两种方案进行评估，以选择最适合特定项目的方案（图 10）。

![[Manual optimisation.png]]

> Figure 10 : Manual optimisation

### Genetic Algorithm Optimisation

An extension of manual optimisation is the use of genetic algorithms within the optimisation scripting to automatically ﬁnd the most optimal solution. Based on the theory of natural selection, where stronger traits are identiﬁed and passed down through generations, similarly, genetic algorithms identify and promote the ‘strongest’ and most optimal solutions to a given problem. Using genetic algorithms allows designers to deﬁne a series of target outcomes and then let the script run through, altering the parameters accordingly to identify how closely the target can be achieved.

人工优化的延伸是在优化脚本中使用遗传算法，自动找出最优解。根据自然选择理论，较强的性状会被识别出来并代代相传，同样，遗传算法也能识别并推广特定问题的 "最强 "和最优解决方案。使用遗传算法，设计人员可以确定一系列目标结果，然后让脚本运行，相应地改变参数，以确定可以在多大程度上实现目标。

By way of an example, if designing a ﬂat slab, what is the most optimal column layout to reduce the thickness and reinforcement content in the slab? Using an algorithm to vary the locations of the columns, and recalculating the slab design at each iteration, will allow the optimal location to be identiﬁed. This concept is covered in more detail in one of the case studies outlined in Section 6.

举例来说，如果要设计一个平面板，那么怎样的柱布局才是减少板厚度和钢筋含量的最佳方案？使用一种算法来改变柱子的位置，并在每次迭代时重新计算板的设计，这样就能确定最佳位置。第 6 节中的一个案例研究将详细介绍这一概念。

### Generative Design

Generative design uses analytical formulae to identify the most optimal solution to a given problem. Commonly used with a genetic algorithm process (deﬁned later), this method undertakes numerous iterations of solutions to the problem and assesses each one against a set target to identify the most optimal solution. By way of example, when optimising the form of a truss, a target can be set to minimise the amount of material in each element, using a ratio of axial force/length. This crude design approach ignores buckling, but allows a good approximation to understand the design. Allowing a number of variables to be altered (depth, geometry, etc.) can allow an algorithm to rapidly assess numerous different arrangements to identify the option which best ﬁts the target (Fig. 11).

生成式设计使用分析公式来确定给定问题的最优解。这种方法通常与遗传算法过程（稍后定义）一起使用，对问题的解决方案进行无数次迭代，并根据设定的目标对每个解决方案进行评估，以确定最优解决方案。例如，在优化桁架形式时，可以使用轴向力/长度比来设定目标，以尽量减少每个构件的材料用量。这种粗略的设计方法忽略了屈曲，但却为理解设计提供了一个很好的近似值。允许改变一些变量（深度、几何形状等）可以让算法快速评估众多不同的排列方式，从而确定最符合目标的方案（图 11）。

![[Generative design of a simple truss.png]]

>Figure 11 : Generative design of a simple truss

### Topology Optimisation

``` txt
拓扑结构优化
```

Topology optimisation uses mathematical analysis to optimise the material content within a bound area. In structural engineering, this can be thought of as the process of either removing lazy or underutilised material, or growing or adding material to highly stressed areas. However, it is not limited to structural engineering and can be used to plan water ﬂow systems, trafﬁc networks and city plans. In the case of structural engineering, using a set of input loads and boundary conditions to this area, the optimal material layout can be derived to understand what the most efﬁcient layout would be. Simplistically, material which is not engaged in transferring forces is removed from the 2D surface or 3D volume. In Grasshopper, the **millipede** plugin can be used to optimise a 2D surface when a set of boundary conditions are deﬁned. SOLIDWORKS simulation allows topology optimisation of a 3D volume in a similar manner (Fig. 12).

拓扑优化利用数学分析来优化约束区域内的材料含量。在结构工程中，这可以理解为去除懒惰或未充分利用的材料，或在高度受力区域增加或添加材料的过程。然而，它并不局限于结构工程，还可用于规划水流系统、交通网络和城市规划。在结构工程中，利用该区域的一组输入载荷和边界条件，可以推导出最佳材料布局，从而了解最有效的布局是什么。简单来说，就是将不参与力传递的材料从二维表面或三维体积中移除。在 Grasshopper 中，如果定义了一组边界条件，就可以使用千足虫插件来优化二维表面。SOLIDWORKS 仿真可以类似的方式对三维体积进行拓扑优化（图 12）。

![[Topology optimisation in millipede (author original).png]]

>Fig 12 Topology optimisation in millipede (author original)

## Case Studies

The following case studies outline in more detail where some of the previously outlined parametric design techniques have been used on real-world projects. Applied to both complex geometric challenges and more standard designs, each case study provides, and overview of the method followed and the key outcomes from using parametric design. Whilst the first three case studies outline an individual technique, the final study brings a number of different techniques together to find the optimal design solution as part of a wider design collaboration.  

以下案例研究更详细地概述了前面概述的一些参数化设计技术在实际项目中的应用。每个案例研究都适用于复杂的几何挑战和更标准的设计，并概述了所遵循的方法以及使用参数化设计的主要结果。虽然前三个案例研究概述了一种单独的技术，但最终研究将许多不同的技术结合在一起，以找到最佳设计解决方案，作为更广泛的设计协作的一部分。

### Case Study 1: Form Finding

Our ﬁrst case study concerns a theatre roof structure, which was originally envisaged as an iconic open-span roof to provide a unique identity to not only the theatre, but the wider development as a whole. The original concept featured a ﬂat long-span roof, supported on perimeter columns and creating a column-free space through the majority of the building. The architectural intent involved exposed beams to the underside of the roof that follow a radial arrangement and span from the internal walls to the columns on the outer perimeter. The complex shape of the internal hall and perimeter edge in plan combined with the long spans resulted in a visually and materially heavy and costly structural solution. An alternative approach for the roof geometry looked to use the clear height above the building massing to give curvature to the long-span structure. This option would reduce the bending moments and increase axial forces in the steel roof elements, developing a funicular geometry and resulting in a more efﬁcient structural system. It would also add to interior and exterior building aesthetic. Deﬁning the funicular form is not always straightforward, especially in the 3D environment. As noted earlier, Antonio Gaudi used the concept of the hanging chains for this reason. A chain is a structural element that can only work in tension. Therefore, supporting it from the roof and hanging loads from it, Gaudi was able to ﬁnd a structural layout, where everything worked in tension. Inverting that shape gave the Sagrada Familia concept design, where everything worked in pure compression—perfect for the masonry construction of the time. Nowadays, parametric design techniques in form ﬁnding have allow us to do similar experiments in the digital world, with many more capabilities.

我们的第一个案例研究涉及一个剧院的屋顶结构，最初的设想是采用标志性的大跨度屋顶，不仅为剧院，也为整个开发项目提供独特的标识。最初的设计理念是采用平面大跨度屋顶，由周边柱子支撑，并在建筑的大部分区域形成无柱空间。建筑设计的意图是在屋顶下方设置外露的横梁，横梁呈放射状排列，从内墙一直延伸到外围的柱子上。内部大厅和外围边缘的平面形状复杂，跨度又大，导致结构方案在视觉上和材料上都十分笨重，而且成本高昂。屋顶几何形状的另一种方法是利用建筑体量上方的净高，使大跨度结构具有弧度。这种方案可以减少弯曲力矩，增加钢结构屋顶构件的轴向力，形成一个漏斗状的几何形状，使结构系统更加高效。它还将增加建筑内部和外部的美感。确定缆车的形式并不总是那么简单，尤其是在三维环境中。如前所述，安东尼奥-高迪正是出于这个原因使用了悬挂链条的概念。链条是一种结构元素，只能在拉伸状态下工作。因此，高迪通过从屋顶支撑链条并将负荷悬挂在链条上，找到了一种结构布局，使所有东西都在拉力作用下工作。将这种形状颠倒过来，就形成了圣家堂的概念设计，一切都以纯粹的压缩方式工作，非常适合当时的砖石结构。如今，通过参数化设计技术，我们可以在数字世界中进行类似的实验，而且功能更加强大。

- A planar surface is deﬁned, using the inner/outer edges of the system, depending on the project constraints.
- This surface is converted into a mesh, with a selected element density. This density is usually deﬁned by the target size of the cladding panels. 
- An analytical model is created where all mesh edges are converted into springs, and all mesh nodes are given a mass (or load vector). Certain nodes are used as supports, by restraining their movement in all directions. 
- A physics engine runs iterations, allowing the system to deform as the loads are applied, until it converges to a certain deformed geometry.

- 根据项目限制，使用系统的内/外边缘定义一个平面。
- 然后将该曲面转换为网格，并选定元素密度。这种密度通常是根据覆层板的目标尺寸确定的。
- 创建一个分析模型，将所有网格边缘转换为弹簧，并给所有网格节点赋予质量（或载荷矢量）。某些节点被用作支撑，限制其在各个方向上的移动。
- 物理引擎运行迭代，允许系统在施加负载时变形，直到收敛到一定的变形几何形状。

The main parameters deﬁning the exact shape of the ﬁnal geometry, other than the surface shape and support conditions, are the spring stiffness and nodal loads used in the analytical model. Different values for these result in different curvatures, which in theory, are all funicular systems. However, when real structural elements replace the analytical springs, there is an optimum curvature that minimises the overall energy of the system. Therefore, a ﬁne tuning is required to determine the optimum values for these variables, before arriving on the ﬁnal geometry.

除了表面形状和支撑条件外，决定最终几何形状的主要参数是分析模型中使用的弹簧刚度和节点载荷。不同的数值会产生不同的曲率，从理论上讲，这都是漏斗系统。然而，当实际结构元素取代分析弹簧时，就会出现一个最佳曲率，使系统的总能量最小。因此，在确定最终几何形状之前，需要对这些变量进行一次调整，以确定最佳值。

Another aspect to consider is planarity and repetitiveness. Optimising the structure is not the only driver for reduced costs and material quantities. Especially for free-form roof structures, the planarity of panels is essential for rectangular glass, whilst repetitiveness of both cladding and structural elements is key, due to the large quantities involved in both trades. To account for this, additional constraints can be used in the analytical model, to tweak the funicular geometry to suit standard sections and a practical cladding grid, exchanging partially bending action for practicality.

另一个需要考虑的方面是平面性和重复性。优化结构并不是降低成本和材料数量的唯一驱动力。特别是对于自由形式的屋顶结构，面板的平面度对于矩形玻璃来说至关重要，同时，由于覆层和结构元素的数量都很大，因此重复性也很关键。为了考虑到这一点，可以在分析模型中使用额外的约束条件，调整漏斗的几何形状，以适应标准截面和实用的覆层网格，用部分弯曲作用换取实用性。

In the case of the theatre, applying this method presented a viable alternative roof option for consideration. Using the inner concrete wall supports and a perimeter stiff beam (fabricated box section, working in biaxial bending), the roof plane was allowed to deform to create a funicular shape. The result was a more complex shape with deeper curvature at long spans and almost ﬂat members in the shorter ones, as a direct response to the unique shape of the roof in plan. This not only resulted in a lighter and more sustainable structural system, but also contributed in the architectural vision of an enhanced user experience, with a varying clear height around the theatre terrace.

就剧院而言，采用这种方法提供了一个可供考虑的可行的屋顶替代方案。利用混凝土内墙支撑和外围刚梁（箱形截面制造，双轴弯曲），允许屋顶平面变形，以创建一个漏斗形状。其结果是形成了一个更加复杂的形状，在长跨度处有更深的弧度，而在短跨度处几乎是平面构件，这是对屋顶平面独特形状的直接响应。这不仅使结构系统更轻盈、更可持续，还有助于提升用户体验的建筑愿景，使剧院露台周围的净高各不相同。

### Case Study 2: Slab Optimisation

An example residential development is a multi-storey tower as part of a wider residential development. The tower structure is a post-tensioned ﬂat slab system, with blade columns and a central RC core for lateral stability. To suit the residential layout, the structural layout has been coordinated to hide all blade columns inside the partition walls.

Generally considered ‘as efﬁcient as it can be’ given the coordination constraints, this structural system is commonly used across residential projects, with engineers placing columns to the best of their abilities to optimise the ﬂat slab behaviour, usually based on experience and past projects. However, to drive efﬁciencies in the ﬂat slab design, it was proposed to challenge the position of some columns which appeared to have ﬂexibility in terms of location along internal partition walls. The study targeted columns within the tower layout which could move along the partition lines between units, without affecting the architecture.

Based on an initial inspection, how is it possible to identify the most optimal location for positioning these columns? It is possible to easily check the impact on the structural slab design if a certain column is shifted by a meter and maybe do a similar exercise a few more times. However, if each column has a range of movement of 10–5000 mm (plus and minus) and that we have nine columns, this leads to thousands of possible combinations. Even if symmetry is applied to limit the number of columns to four, this is still in the magnitude of thousands, which practically means it is impossible to exhaust all options, and ensure the most efﬁcient solution has been selected.

This is where computational power through parametric design provides a solution. A parametric model is set up, in which the slab is modelled as a mesh that has two support types:

1. Fixed supports—shown in red and representing all the columns or core walls that are not able to move.
2. Free supports—shown in blue and given the ability to move along the partition walls, within a certain range per column. These are grouped to ensure symmetry and reduce the size of the problem (Fig. 13).

![[Fig 13 Parametric model 2.png]]

>Figure 13 Parametric Model

The design variables here are just four sliders that indicate the position of the free columns under the slab. The mesh is dynamic, and it is adapted in every column move to ensure that the support point is also a mesh node. This geometry is then assigned attributes (loads, cross sections, boundary conditions, etc.), and real-time analysis is performed each time a variable is altered.

The exploration of the design space to ﬁnd the optimum arrangement is accelerated by the use of genetic algorithms. In any optimisation problem, three important aspects need to be deﬁned, namely the input variables, the constraints and the objective function. The ﬁrst two have already been deﬁned as described; however, the third one is not that straightforward. A ﬂat slab can be optimised for reducing deﬂections, maximum bending moment and the sum of bending moments or the strain energy. All of them are desirable targets, but each one of them gives different results. As part of the process therefore, it is necessary to rapidly analyse each generated option and compare it against a set of target criteria. The post-processing of the options allows the objective function to be deﬁned and ‘zero’d’ in on.

With a targeted outcome of reduction in the strain energy in the slab as the criteria, a new location was proposed for the columns, accompanied with a range of movement that resulted in similar results, allowing for any changes by other parties due to unforeseen constraints. The end result provided around 7% less reinforcement material, without creating any implications to architecture or buildability, since there is still the same number of columns positioned inside the partition walls. Whilst not a signiﬁcant saving, the reduction in the reinforcement content, for no impact on the spatial layouts or use of the space, represents an easy win to reduce the embodied carbon and costs of the projects. Given the huge number of similar residential building built around the world, such an approach, if you used industry wide, can play a large part in driving sustainable outcomes on projects (Fig. 14).

![[Optimisation results for the ﬂat slab study.png]]

>Fig. 14 Optimisation results for the ﬂat slab study

### Case Study 3: Generative Design

Can a building structure grow itself, similar to natural microstructures? Maybe not entirely yet, but the latest technological advancements have brought us new methods of investigating efﬁcient structures that allow us to explore a whole new design space. These methods usually sit under the term of generative design—an iterative process that involves an algorithm generating solutions to a well-deﬁned problem and ranking them based on predeﬁned objectives to achieve the target efﬁciency.

An example of using such techniques is the concept design of the Circular Quay tower in Sydney. This tower had a very irregular shape in plan with a ‘bird’s mouth’ feature in the front façade, splitting the tower envelope in two. The purpose of this bird’s mouth was to clearly frame the views out to the Harbour Bridge and Opera house on the two sides of harbour, and provide smaller facades that face these prominent city features to lessen the impact on key city views. After some initial studies on structural systems, an external mega-bracing system was selected over a core with outriggers option, for both structural and architectural reasons. 

A desire for a distinct building identity pushed the team to explore alternative and more efﬁcient bracing layouts that would be unique to the tower shape and constraints. 

The ﬁrst step in the design process involved a method called ‘Topology Optimisation’ (TO). This method allows the structure to use material only in locations that maximise efﬁciency, providing a theoretical optimum solution of a self-designed system. This technique works as follows:

- Solid surfaces of a continuum material are deﬁned. 
- The boundary conditions are deﬁned (extent of material, supports). 
- Loads are applied (only the leading action for this exercise, which was the wind for the bracing elements we are exploring this is dominate case).
- Stress analysis is performed, and areas of high and low stress are identiﬁed.
- Starting with a uniform thickness, material is removed from areas of low stress and added to high stress areas.
- This happens for many iterations until the system converges to a solution with a given material reduction target (for this case 10% of the original uniform surface volume).

This method is given a lot of freedom, and whilst the result is only a theoretical solution, it can be a useful indication of a preliminary layout strategy that will lead to the practical optimum. Therefore, in order to convert this into an optimised ‘stick model’ solution, parametric modelling was used. In this model, the layout of the bracing system follows certain rules and satisﬁes the main architectural constraints (i.e. ﬂoor levels, column locations) but by varying a few design parameters, it is able to produce different layouts. The input parameters have been the number of braced bays, the height of each bay and the inclination of the diagonals as they intersect certain columns. Every time the input parameters are adjusted, a new geometry is generated and then analysed and evaluated based on predeﬁned metrics (tonnage, deﬂections and strain energy) (Fig. 15).

This type of ‘ﬂexible’ modelling allows the exploration of many more alternatives compared to the traditional way of modelling, where manual labour limits the number of options that can be explored. The bracing system was able to change from a conventional single bracing system, to cross-bracing or to a more complicated ‘curved’ arrangement that was similar to the one indicated by the topology optimisation study. In order to select the best option, genetic algorithm optimisation was used to come up with the best combination of input parameters which minimised the objective function (steel tonnage in this case). The output of this exercise was used as a base for the ﬁnal detailed analysis of the structural system, for inclusion of all loading combinations and checks. The selected layout from this was very similar to the initial result of the topology optimisation process, giving more comfort that an option close to the theoretical optimum was selected.

![[Generative design workﬂow.png]]

>Fig. 15 Generative design workﬂow

The images below summarise the process, starting with the topology optimisation model to the left, exploring different bracing arrangements to manually reproduce this layout and then allowing the parametric model to explore thousands of layouts before converging to the ﬁnal option. Plotting the principal stress paths on the tower envelope proves that the selected bracing layout tries to follow them closely. The architectural advantages can also be shown in the renders below, with a unique exoskeleton and minimised visual obstructions towards the top of the tower (Fig. 16).

![[Fig. 16 Design process overview.png]]

>Fig. 16 Design process overview

### Case Study 4: Elizabeth House Arch

The previous case studies present the individual aspects of parametric design; however, it is possible to link these elements together in an evolving design process. This was undertaken in the development of the structural system for Elizabeth House.

Elizabeth House is a commercial ofﬁce development in London, UK and is challenged due to a myriad of below ground constraints. The site is adjacent to Waterloo station and sits above the main London Underground station which connects to the overground train network. Located beneath the site therefore are a number of undergound platform tunnels, train running tunnels and a network of passenger concourse tunnels. Linking these are numerous service tunnels and ventilation shafts (Fig. 17).

![[Fig. 17 Below ground constraints 1.png]]

>Fig. 17 Below ground constraints

The development aspiration for the site was to deliver 1.3 million square feet of commercial ofﬁce space. Whilst the current seven-storey building is founded on a raft foundation, evenly distributing the load form the building on to the below ground assets, this system would not support the building massing required to deliver the require area. With a target building height of 30 storeys, a piled solution would be required to support the new structure. However, with the congested site constraints, the opportunity to install deep-piled foundations was limited to small areas located over 100 m apart. To solve this challenge, a transfer system was required to span the superstructure massing approximately 108 m clear over the below ground assets. However, removing too much weight from the tunnels would also be a problem causing them to move upwards; hence, a transfer of 108 m combined with some weight directly down onto a raft is required to effectively hold the tunnels close to their original position (Fig. 18).

![[Fig. 18 Piled foundation zones.png]]

>Fig. 18 Piled foundation zones

#### Initial Idea Generation—Topology Optimisation

With numerous potential options for the transfer system, the ﬁrst step was to undertake a number of topology optimisation exercises to identify what a natural system would look like and how, in the absence of any other constraints, a structural system would respond to the in ground constraints. Undertaken using the millipede plugin for Grasshopper, a number of different boundary conditions were analysed to gain an understanding of the idealised geometry based on differing foundation solutions (Fig. 19).

![[Fig. 19 Topology optimisation options.png]]

>Fig. 19 Topology optimisation options

#### Design Development—Parametric Optioneering Process

As the design progressed, a number of structural options were investigated for the main transfer structures. All of these options were modelled parametrically using Grasshopper to allow geometric manipulation of the structure within the architectural massing. This allowed rapid evaluation of the various options against a series of criteria, including structural steel tonnages, architectural impacts and constructability issues. Four distinct structural ‘families’ of options were developed, with various options then investigated within the families. All these families shared a common objective—to transfer approximately 70% of the building weight over the tunnels and place back down approximately 30% of the building weight to hold the tunnels in position (Fig. 20).

![[Fig. 20 Structural family options.png]]

>Fig. 20 Structural family options

With each of the options schemed in Grasshopper, it was possible to run an outline design for the main transfer elements which was linked to their geometry. This allowed rapid updates to structural element sizes and tonnages based on geometric changes and enabled the optioneering study to progress much more rapidly, and with informed data, than a traditional design options process. To accomplish this, the following steps were taken:

- A massing option was received by the architect. 
- Floor surfaces were extracted based on levels schedule. 
- The same structural grid (driven by the ground constraints) was projected on these levels. 
- The selected transfer system was adapted to the massing option by ﬁnding the relevant intersection points.
- Manual modiﬁcation of the transfer geometry was allowed by the script (inclination of diagonals, number of them, truss depth, etc.). 
- Real-time analysis was performed by the Grasshopper plugin ‘Karamba’,14 a parametric structural analysis tool for trusses and space frames.
- Metrics were extracted automatically after each geometry change regarding tonnage, deﬂections, ﬂoor area, façade area, etc. 
- Baked structural geometry was sent back to the architects for inclusion in the rendering process for visual impact (Fig. 21).

![[Fig. 21 Design optioneering 1.png]]

>Fig. 21 Design optioneering(设计选项设计)

#### Generative Design Optimisation

As the design progressed, the A-frame option was selected as the most suitable when assessed holistically and was further developed in collaboration with the architects. As the architectural massing evolved to reﬂect planning and spatial drivers, further geometric updates were needed to the transfer systems to continue to integrate the structure into the architecture of the building. This development began to introduce elongated force-paths towards the support points.

To assess the most optimal geometric arrangement for the A-frame, a genetic algorithm was run to iterate numerous different options and zero in on the most efﬁcient system. Key parameters within this iterative process were locked to maintain critical architectural and grid setting out, including.

- Node points within the system were locked to the grid intersections between the ﬂoor plates and the column grid. 
- The ﬂoor-to-ﬂoor heights were locked. 
- The longitudinal column grids were locked. 
- Geometric symmetry was enforced left and right of the apex point of the system— important to enhance the space planning and character of the building, from both an internal and external perspective (Figs. 22 and 23).

![[Fig. 22 Arch algorithm – automated design script.png]]

>Fig. 22 Arch algorithm – automated design script

![[Fig. 23 Arch algorithm – geometric outputs.png]]

>Fig. 23 Arch algorithm – geometric outputs

The algorithm was run using the following steps.

1. Focussing on one gridline at the time, the loads of the given mass were determined.
2. Nodes were deﬁned in the gridline/ﬂoor intersections that were able to change levels during the optimisation.
3. Members connecting these nodes were generated based on predeﬁned rules, ensuring a truss-like transfer system, regardless of the node locations.
4. Real-time analysis and evaluation of metrics were performed by Karamba. Each time a node was changing levels, whilst moving along a certain gridline, a new ﬁnite element analysis was performed, and the efﬁciency of the system was evaluated.
5. Genetic algorithms were used to explore all the possible combinations of node locations.
6. The algorithm converged to node locations that formed a parabolic curve for the main chord of the trusses.

#### Foundation Design Optimisation

One additional discrete challenge which was solved using a parametric design process was the supporting foundation arrangement to the northern edge of the site. Whilst the available piling zones to the south allowed more scope for deep foundations, the planning requirements for the site drove the mass of the building towards the northern end.

The northern pile groups are constrained by a number of train and passenger tunnels and therefore have limited scope for pile sizes and numbers. The initial concept was based on the use of 1500 mm diameter piles; however, this limited the heights of the building, especially to the north-eastern corner where the area for piling was the least. To further optimise the potential load-bearing capacity, a generative design algorithm was run on the north-eastern pile cap to test whether varying the number, size and position of the piles would achieve a higher group capacity. To set up the algorithm, key steps were taken:

1. A comparative table was set up with pile sizes and their respective capacity.
2. The area was then deﬁned within which piles could be placed.
3. Key geometric rules were added, including minimum pile spacing as a function of diameter.
4. Possible pile arrangements that maximise density were explored, resulting in an orthogonal and a hexagonal grid.
5. Regardless of the grid selection, the whole grid was allowed to move in two directions and rotate.
6. A trimming algorithm allowed only piles that were fully inside the allowable area to be accounted for in the design.
7. Genetic algorithms were used to alter pile diameters, grid type, vertical/horizontal location and rotation, with the goal to maximise the pile group capacity (Fig. 24).

![[Fig. 24 Pile optimisation script.png]]

>Fig. 24 Pile optimisation script

The resulting output was that by reducing the pile size to 1200 mm diameter and a best ﬁt position for maximum piles, it allowed an additional two piles to be included in the pile group, which allowed an additional 10% load-bearing capacity from the overall group. This unlocked the restraint on the superstructure above and gave a more viable foundation design.

#### The Final Design

The ﬁnal design for the transfer system, mega tied arches, allowed this complex site to be unlocked and yet retain an efﬁcient and cost-effective structural system. The arch geometry and structural sizes respond directly to the massing of the building, with three distinct systems embedded in on geometric arrangement. These consist of:

1. A symmetric arch to support the lower mass of the building.
2. An asymmetric arch to support the eccentric upper mass of the tower.
3. A propped truss system to resist pattern and out of balance loading (Figs. 25 and 26).

![[Fig. 25 Arch design.png]]

>Fig. 25 Arch design

![[Fig. 26 Arch geometry.png]]

>Fig. 26 Arch geometry

Throughout the design process, parametric modelling and design techniques were used on both the holistic design and on targeted discrete aspects. This allowed the design to be integrated into the architecture of the building, which when complete, will result in an iconic development in the heart of London.

## Lessons Learnt

Parametric modelling and design principles, and their application, are not without disadvantages. The techniques used can incur both design and technical issues which need to be acknowledged throughout the process to achieve the best outcome.

### A Steep Learning Curve

To fully master parametric modelling, with the myriad of plugins and opportunities which the method can provide, is not an easy task. For new users, even those who are familiar with traditional 2D and 3D modelling packages, learning the skills to build through a design parametrically will take time and should not be rushed. Aside from the basic building blocks which are used to develop the models, understanding the interdependencies and relationships between differing variables requires a different way of thinking about design.

Luckily, there are numerous online and in person tutorials and courses available to both new and advanced users and active online forums where questions can be asked to resolve issues. Starting with simple models and growing the complexity and additional capabilities of the model would be the best route into the world of parametric design.

### Black box engineering and design

As with all software, there is an inherent danger of ‘black-box’ design, i.e. an overreliance on the outcome of any particular analysis and design package—in essence believing a solution is correct because ‘the computer says so’. This has the potential to introduce errors into the design, ones which can be costly and time-consuming to rectify later. Whilst this risk is present in most software packages, with the prevalence of open-sourced plugins available to enhance, the basic parametric tools increases the risk of potential errors. Issues can include:

1. Incorrect analysis of stresses in materials (tension vs. compression) during analysis and design optimisation.
2. Incorrect force distribution if boundary conditions are not correctly set.
3. Node rotation issues due to member releases not set.
4. No consideration of second order, but sometimes important affects such as member buckling, global buckling or local buckling or instabilities.
5. Over implementation of optimisation, missing a critical check such as pattern loading.

To mitigate the risks of this, it is important to use technical engineering judgement across all aspects of a particular project. Any solution which is developed parametrically should still be veriﬁed against global force equilibrium and should have easily identiﬁable force-paths. Rough hand calculations can also be used to verify the basic magnitude of forces and verify the fundamental concept behind the more optimised design. Also, geometry and sizing derived through an optimisation and parametric process and simple analysis can be check by more complex analysis and design only software.

### Lack of deﬁned targeted outcomes

With a range of parameters which can be varied across a project, the potential outcomes can be numerous. As you introduce more variables to this already diverging process, it becomes difﬁcult to identify what the ideal solution might be. To avoid endless iteration, it is therefore important to identify what is important to the project outcome. This could be a geometric target, minimisation of material quantities, ﬁnding the lowest embodied carbon solution or identifying the optimal end-user experience. With a solid deﬁnition of the critical metrics against which to test the varied outcomes, it becomes easier to discard the solutions which do not meet these metrics, and dive deeper into the more promising options.

### Slave parameters

One potential pitfall across the generative design aspect is the issue of slave parameters. This is where certain parameters will always be linked to others, either through a geometric requirement or due to base design principles. In this instance, varying certain parameters will always result in the result for any slave parameters. Therefore, numerous iterations will give the same result and can run indeﬁnitely without converging to a solution.

### Constructability—can it be built?

Analysis and design software, whilst burdened by bounds of physics, are unrestrained by the need to construct the ﬁnal design in an efﬁcient and safe manner. With the endless geometric options provided by parametric design and the ability to fully optimise the material quantities in the ﬁnished building, this may not provide the most cost-effective and sustainable solution. Reducing steel tonnages to a bare minimum for instance is potentially counterproductive if the construction phase requires two or three times more temporary works to stabilise the structure until it is complete.

Further, a complex geometric solution may meet an aesthetic requirement, however, could add a number of months to the construction programme, incurring additional cost.

Avoiding a ‘wished-in-place’ design is therefore key to successful use of parametric design software and is essential during the early concept phases of the project, where the overall buildings form and geometry are established. Understanding the basic principles of construction and embedding these as constraints into the design as it develops are therefore important steps.

### Are you asking the right question?

With the fundamental principle of variability of key parameters, one of the critical aspects of the methodology is to make sure that the right parameters are selected to both ﬁx and to vary. In essence—are you asking the right question of the software before the iteration process starts? Do you have a full understanding of the project constraints, below ground risks, likely construction methodologies and budget limitations? Is ﬁxing one variable likely to overly constrain the design? Is varying one parameter going to introduce unnecessary cost. There is not necessarily a right or wrong answer which can be outlined here to these questions, as these questions will need to be answered on a project-by-project basis. However, we would recommend that prior to the development of any models, a collaborative review is undertaken to identify all of the key variables and identify which ones have the potential to add value, which must be ﬁxed (perhaps due to third party inﬂuences).

### Imaginative and design thinking?

One potential drawback to parametric design and modelling is that it can constrain the historic thinking which has produced some of histories ﬁnest design examples. In both conceptual and optimisation design stages, the use of a parametric model will produce a number of different iterations and provide the designers with a number options to choose from—in effect a list of possible solutions to the question which has been asked. However, this has the potential to constrain the creative design process if rigidly adhered to. Across engineering and architecture, there are foundation design principles, be they technical or emotive in nature which are applied to all projects. Whilst the correct use of parametric modelling and design can enhance the creative design process, the designs produced should always be tested against the fundamentals and critiqued by colleagues and design partners to challenge the outputs. This will ensure that the ﬁnal solution is designed as best for project rather than just selecting an option from a software generated list.

### Qualitative Issues

Parametric design is often seen as able to provide a solution to a problem which has presented itself during the design process. However, it is not necessarily always the right tool. Certain design complexities or design development is qualitative in nature. As such, developing a parametric design script to apply to the design will not solve the complexity or develop a solution to provide an optimal outcome. Indeed, it may further complicate the design through adding costly complexity to the project. In these instances, again, design experience is critical to identifying whether or not parametric design is the right solution or whether a more qualitative design process should be applied instead.

### Diving into software too soon

One of the key risks to any design process is diving into the use of software to early on in the project. Even in traditional design processes, if the concept is not fully thought though from the outset, and the fundamental principles laid down, then any early modelling can be abortive or can give incorrect outputs for preliminary design quantities, causing errors in the initial project budgets. With parametric design, this issue can be exacerbated. If the constraints are not fully understood, or the parameters to be optimised are not fully thought through, including the upper and lower bounds for each of these variables, then there is a risk that the outcome of the parametric design process will not provide the intended outcome.

``` txt
任何设计过程的主要风险之一都是在项目初期就开始使用软件。即使在传统的设计过程中，如果没有从一开始就充分考虑概念并制定基本原则，那么任何早期建模都可能会失败，或者为初步设计数量提供不正确的输出，从而导致最初的项目预算出现错误。在参数化设计中，这一问题可能会更加严重。如果没有充分理解制约因素，或者没有充分考虑需要优化的参数，包括每个变量的上下限，那么参数化设计过程的结果就有可能达不到预期效果。
```

## A Parametric Drive to Sustainable Design

As has been mentioned previously, the primary use of parametric design tools to date has been to deﬁne some fantastic geometrically complex buildings, creating landmark developments across the world. However, these tools are not often used in anger on the basic design activities, those bread and butter residential and commercial developments of which hundreds are in design and construction phases around the world at any one time. This is perhaps where there is the most scope for pushing the boundaries on sustainable design—creating more efﬁcient and optimised structures to suit the everyday requirements of our communities. Even an average 5% saving in material quantities across these numerous projects could result in signiﬁcant carbon savings worldwide. There are a number of ways in which the use of parametric design can be used to further advance sustainable design principles—some of which are outlined below.

### Material Optimisation

```txt
材料优化
```

The optimisation techniques available in parametric design tools are outlined above and provide an opportunity to not just optimise the elemental design itself, but also to challenge the materiality of the structural elements which we use to design and build. Through amendments to the geometric form of elements, it is possible to identify more optimal force paths, connection points, spatial layouts and structural forms.

Parametric design also provides an opportunity to test different materials. For instance, what would a concrete frame look like in timber? Varying the design parameters and conceptual design algorithms, it is possible to ﬂick between the two options and identify the carbon quantities in both and indeed understand the spatial implications of switching between the two materials, in affect running two designs in parallel. This might be particularly useful when the optimum outcome might not be known until the project has been tendered, such as looking at two or more alternative materials (steel, concrete, timber) or looking at options such as volumetric modular vs. traditional building construction techniques (Fig. 27).

![[Fig. 27 Material optimisation (author original).png]]

>Fig. 27 Material optimisation (author original)

Whilst this is a simplistic example, using simple concept level calculations and ignores questions around aspects such as ﬁre protection and cost, it demonstrates the potential to rapidly evaluate differing materials against a target outcome for the project.

### Challenging Structural Form

Case study 2 outlines the signiﬁcant beneﬁts of using genetic algorithms to challenge the basic geometry in a residential column layout. Basic building geometry, usually based on experience and design judgement, can be further enhanced through the use of parametric design techniques.

Whilst an initial concept can be developed by hand, this should not preclude the spatial layout of the structure from being challenged. This can either be within the constraints of the architectural layouts, or even outside of them and challenging whether there is a better way to design a building. As demonstrated, the opportunities which are presented by parametric design methods in optimising the structural layouts within a building can result in more efﬁcient design, using less materials, with faster and more concise construction programmes. All of these will contribute to reducing the embodied carbon content of the development and hence its environmental impact.

### Visualisation of Sustainable Targets

As has been noted, as various parameters are optimised or altered through the parametric process, it is important to understand the key targeted outcomes for the project. With better understanding of the embodied carbon in various materials, it is possible to directly link carbon quantities to the parametric design, making the resultant an output of the design process. Various tools exist to accomplish this, including.

1. Whole life carbon assessment for architects([Embodied and whole life carbon assessment for architects sustainable design (architecture.com)](https://www.architecture.com/knowledge-and-resources/resources-landing-page/whole-life-carbon-assessment-for-architects))
2. Inventory of carbon and energy database—V3.0 (10 Nov 2019).([Embodied Carbon Footprint Database - Circular Ecology](https://circularecology.com/embodied-carbon-footprint-database.html))

The above resources provide guidance on calculating the carbon based on material quantities and can be used within parametric software to take the material outputs and convert them into a carbon content.

Using optimisation algorithms, it is then possible to create a feedback loop to optimise for the lowest embodied carbon option across a particular aspect of the project.

A word of warning however—this process needs to be a holistic review across the project—over optimisation of the structure for instance could have knock-on effects on the façade system, negating any carbon savings in steel tonnages for example.

### Modern Methods of Construction and Componentised Design

There have recently been signiﬁcant advances in modern methods of construction, using modular geometry to facilitate more off-site construction and allow faster on-site construction. In addition, the use of componentised design is also growing in certain sectors of the construction industry. Parametric design can allow future development massing and geometric layouts to be linked to certain components or modules. With this, it will be possible to develop unique building typologies using a standard set of modules or components, allowing mass of-site construction of elements and simpler and less constrained on-site delivery. These future methods will reduce material waste on site signiﬁcantly, whilst also de-risking the construction process and speeding up the construction phase. Used intelligently, these methods will therefore have a signiﬁcant impact on the embodied carbon content of new buildings and reduce the environmental impact of new construction.

### Integration of Existing Structure

Parametric modelling is particularly useful to integrate and reuse existing buildings, either wholly or partially. Reusing components of an existing building can signiﬁcantly reduce the embodied and whole life carbon quantities in a new development and the parametric tools which have been outlined above can allow the identiﬁcation of the optimal way of reuse.

Examples include the reuse of foundations—where the existing capacities are set as ﬁxed parameters in the model, and the superstructure is optimised within these bounds. Similarly, reuse of existing buildings to extend them vertically and add ﬂoor plate capacity, again using the existing capacity of the structural systems to bind the parametric modelling process. These methods can help identify the opportunities available on a particular and aid in the decision-making process at the initiation of a project.

Taking this a step further, future opportunities will exist to mine the BIM data from buildings scheduled for demolition. Through limiting the model to only components which are available for reuse from previous projects (be they façade panels, MEP equipment or structural components), the design team is able to develop new and innovative developments without the need for newly fabricated materials—think of Lego building on a macro-scale.

### Future of Materials

Material advances which have occurred over recent years, and indeed those yet to come, can take time to be adopted by the wider industry. Without extensive rework, it is often difﬁcult to demonstrate what an alternative frame and material makeup might look like. The potential pros and cons can be difﬁcult to explain with traditional design methods.

Parametric design, using manual optimisation, can allow options to be tried within a set massing and aspects such as material and embodied carbon quantities, along with geometric impacts such as ﬂoor-to-ﬂoor heights visualised and understood.

The ability to better understand the beneﬁts of new materials will allow more comfort in their use to be gain by developers and contractors and will lead to more use of environmentally sustainable materials in future projects.

## Concluding Thoughts

This chapter has outlined the opportunities, along with some practical examples, of how parametric design can be used to challenge geometry and materiality to drive minimisation of material quantities and more efﬁcient geometric solutions. Whilst we have only outlined the possibilities here, with suggestions on areas to be investigates, we believe that parametric design carries the opportunity to have signiﬁcantly positive impact on the embodied carbon quantities of the next generation of building.

本章通过一些实际案例，概述了如何利用参数化设计来挑战几何形状和材料特性，从而最大限度地减少材料用量，并提供更加高效的几何解决方案。虽然我们在这里只是概述了可能性，并对有待研究的领域提出了建议，但我们相信，参数化设计有机会对下一代建筑的内含碳量产生显著的积极影响。

As designers, we have a duty to drive sustainable design through all our projects, to lessen the environmental impact of the built environment and enhance the cities and towns in which we and our communities live. Parametric design gives us a set of powerful tools and design methods which can be used to challenge projects from the outset to ensure that we are delivering on our obligations to deliver a better world for future generations.

作为设计师，我们有责任在所有项目中推动可持续设计，减少建筑环境对环境的影响，改善我们和我们的社区所居住的城镇。参数化设计为我们提供了一套强大的工具和设计方法，可用于从一开始就对项目提出质疑，以确保我们履行为子孙后代创造一个更美好世界的义务。