
#Generative_Design #Parametric_Design #Revit #BIM #CIM #Dynamo

---

# **_Website_**

> https://www.generativedesign.org/

---

# 0 Welcome

Welcome to the **_Generative Design Primer_**, which aims to introduce **AEC** practitioners of all experience levels to **_an exciting new approach to design using generative design workflows._**

![[../2023年/attachments/A generative design workflows 1.gif]]

## About

This primer will help you:

- **understand** what generative design is by defining the base concepts and terminology you need to know.
- **explore** how these techniques can be used to solve practical challenges commonly found in AEC design projects.
- **learn** how to use Autodesk’s newest generative design tools such as Generative Design for Revit and Dynamo, through practical workflows.

## Why Make a Primer?

Autodesk is working to **democratize technologies** that can help designers in the AEC industry automate the creation of design options and optimise those designs to achieve better outcomes.

![[../2023年/attachments/democratize technologies.webp]]

Using these technologies requires new skills and new ways to think about design. We created this primer to explain the terminology, ideas, and methods you will need to understand to begin using generative design workflows and tools that support this new approach to design.

_Note: there are many different applications of generative design/art, and this primer does not aim to cover them all. This primer is focused on AEC methodologies and how these apply to both Generative Design/Dynamo_

**matterlab** was commissioned to kick-start the development of this primer, we thank them for all their efforts in establishing this valuable resource.

![[../2023年/attachments/matterlab logo.jpg]]

## Open-Source

This primer is an open source project initiated by the **AEC Generative Design Team** at Autodesk and we are dedicated to providing high-quality content on generative design in this primer.

Contributions are of course welcomed. You can contribute to the primer in the following ways:

- You can report any issue you may have found on our [issues page](https://github.com/DynamoDS/GenerativePrimer/issues).
- If you’d like to improve, clarify, or add content to the Primer, please head over to our [Github repository](https://github.com/DynamoDS/GenerativePrimer).
- Have an example workflow of generative design? Head over to our [contribution guidelines](https://github.com/DynamoDS/RefineryPrimer/blob/master/CONTRIBUTING.md) and see how you can add it to the Community examples section.

## Contact

Let us know about any issues with this document.

[aecgdfeedback@autodesk.com](mailto:aecgdfeedback@autodesk.com)

## License

Copyright © 2021 Autodesk

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at the following link:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

---

# 1 Introduction to Generative Design

In this chapter, we’ll look at key concepts that are essential to understanding generative design and how Generative Design for Revit and Dynamo works.

![[../2023年/attachments/CUBE.webp]]

In this section, we will explore the following topics:

- the fundamental concepts needed to understand generative design
- a definition of generative design in the context of AEC
- an introduction to Generative Design for Revit and Dynamo
- examples of using generative design to solve design problems
- common approaches used
- related concepts

Let’s start by looking at something you are likely to be familiar with and already using today: computational design.

## 1.1 Computational Design

_`Computational design`_ is not any one algorithm or off-the-shelf process you can utilize. Rather, we describe it as an approach whereby a designer defines a series of instructions, rules and relationships that precisely identify the steps necessary to achieve a proposed design and its resulting data or geometry.

Crucially, these steps must be computable, meaning they can be understood and calculated by a computer.

![[../2023年/attachments/compdesign_Above Image of an NURBS manipulations from Martin Stacey.gif]]

> _Above: Image of an NURBS manipulations from Martin Stacey - UCL._

Put simply, computers are very good at performing calculations and executing pre-defined steps.

When approaching a design computationally, the designer would focus on developing the procedure that would create a design - not the design itself. The process of iterating through options and data are offloaded to a computer. This saves time, money and effort, and lets the designer focus on the creativity of the design process.

## 1.2 Generative Design

In this section, we’ll look at what the term 'generative design' means in relation to the AEC industry.

![[../2023年/attachments/Massing analysis - Alkmaar Housing Commission - The Living.webp]]

> Massing analysis - Alkmaar Housing Commission - The Living

### What is Generative Design?

You may have encountered the term 'generative design' in the context of producing design permutations, creating geometry from some simple inputs, or even just building computational graphs using Dynamo or Grasshopper.

We see generative design (**/ gen·er·a·tive de·sign /** noun) as:

>A collaborative design process between humans and computers. During this process, the designer defines the design parameters and the computer produces design studies (alternatives), evaluates them against quantifiable goals set by the designer, improves the studies by using results from previous ones and feedback from the designer, and ranks the results based on how well they achieve the designer’s original goals.

![[../2023年/attachments/Some generated alternatives - Mars Innovation District - The Living.gif]]

>Above: Some generated alternatives - Mars Innovation District - The Living

Generative design is a specific application of the computational design approach, with the following distinctions:

- The designer defines goals to achieve a design (rather than the exact steps).
- The computer helps the designer to explore the design space and generate multiple design options (not just one).
- The computer enables the designer to find a set of optimal solutions that satisfy multiple competing goals.
- The designer compares multiple design scenarios to find a set of design options that fits the design goals.

### Why should I use Generative Design?

In a nutshell, generative design is a goal-driven approach to design that leverages automation so that designers and engineers can:

- have better insight into their designs;
- make faster, more informed design decisions; and
- explore more options using the power of computers.

#### Better Outcomes and Insight

As the designer, you specify which outcomes you want to achieve for your design and how they are measured. With your guidance, the computer produces sets of optimal designs, along with the data used to prove which design performs best against your goals. By analyzing how the generated designs measure up against the set goals, you can gain valuable insight into which design aspects impact the outcome and how.

![[../2023年/attachments/Maximization of active shared spaces - Mars Innovation District - The Living.webp]]

> Maximization of active shared spaces - Mars Innovation District - The Living

#### Faster, More Informed Design Decisions

Generative design can help you find better designs for your project more quickly by leveraging what computers are good at: computation and repetition.

生成式设计可以利用计算机擅长的计算和重复，帮助你更快地为项目找到更好的设计。

Computers can generate and evaluate a huge number of design variants in only a fraction of the time it would take an individual designer, allowing you to learn what does and doesn't work at an accelerated pace.

计算机只需花费单个设计师的一小部分时间，就能生成和评估大量的设计变体，让你能够快速了解哪些可行，哪些不可行。

![[../2023年/attachments/Design options generated - Mars Innovation District - The Living.gif]]

> Above: Design options generated - Mars Innovation District - The Living
> [MaRS Discovery District (marsdd.com)](https://www.marsdd.com/)

#### A Greater Variety of Options

With a generative design approach, the initial design parameters you input are used to generate your potential design solutions, with the only limitation being how much computer power and time you have.

For example, using traditional computational design techniques, it's feasible for you to explore ten variants (or more, perhaps). However, using generative design, an algorithm can generate thousands of variants in mere minutes.

![[../2023年/attachments/Design options generated - Bionic Partition for Airbus - The Living.webp]]

> Above: Design options generated - Bionic Partition for Airbus - The Living

#### A Collaborative Approach

The aim of a generative design approach is not to replace designers - it is to augment human capability with computation power.

To illustrate this, this about the fact that a good generative design process using several metrics to analyze designs in a study will rarely generate a single output. Instead, it will almost always generate a range of outputs that the designer can choose from, all of which will already have been objectively assessed and ranked. It doesn't choose for you.

### What goes into a Generative Design Process

#### Stages

As previously discussed, a generative design approach allows for a more integrated workflow between human and computer. In Generative Design, this workflow involves the following stages: **generate, analyze, rank, evolve, explore, and integrate**.

正如前面所讨论的，生成式设计方法使人与计算机之间的工作流程更加一体化。在生成式设计中，这一工作流程包括以下阶段：_**生成、分析、排序、演化、探索和整合**_。

##### Generate

The design options are created or generated by the system, using algorithms and parameters specified by the designer.

![[../2023年/attachments/stage Generate.png]]

##### Analyze

The designs generated in the previous step are now measured or analyzed based on how well they achieve goals defined by the designer.

![[../2023年/attachments/stage Analyze.png]]

##### Rank

The design options are ordered or ranked based on the results of the analysis.

![[../2023年/attachments/stage Rank.webp]]

##### Evolve

The process ranks the design options to figure out in which direction they should be further developed or evolved.

![[../2023年/attachments/stage Evolve.png]]

##### Explore

The designer compares and explores the generated designs, inspecting both the geometry and evaluation results.

![[../2023年/attachments/stage Explore.webp]]

##### Integrate

The designer chooses a favorite design option and integrates it into the wider project or design work.

![[../2023年/attachments/stage Integrate.png]]

#### Anatomy of each stage

Each of these stages can be further broken down into _`define`_, _`run`_ and _`results`_ steps. The _`define`_ step is the responsibility of the designer, while the _`run`_ and _`results`_ steps are performed by the computer.

Using this breakdown, let's look at what the_`generate`_ stage would entail.

##### Define

![[../2023年/attachments/详解Define.webp]]

For the _`define`_ step, the designer will need to do the following:

- Establish the generation algorithm - this is the logic that defines how designs are generated, which may include things like constraints and rules.
- Provide the generation parameters - these are the variables or inputs needed for the previously-defined algorithm.

This _`define`_ step is present and vital for all stages of the generative design process, as the validity of outputs relies on the quality of the designer’s contribution in this step.

With clear and concise logic, the computer can provide suitable outputs.

##### Run

![[../2023年/attachments/详解Run.png]]

Once everything is defined in the algorithm and its accompanying parameters, the computer begins to _`run`_, meaning it starts to generate different design options. This process might happen locally on the designer's computer or, for more intensive calculations, it may happen using cloud computing.

##### Result

![[../2023年/attachments/详解Result.webp]]

The things that are generated during the _`run`_ step are the final outputs from each stage. These are then used as inputs or parameters in subsequent phases.

For example, the designs created in the _`generate`_ phase will be used as one of input parameters in the _`analysis`_ phase.

#### Overall Process

We can map these stages and steps together in a single diagram, allowing us to visualize the order of each stage and their dependencies.

![[../2023年/attachments/Stages Overall Process.webp]]

The diagram shows us that:

- Each stage and step is dependent on the previous one.
- The entire study process is repeatable, as each iteration learns from the previous results.

## 1.3 Examples of Generative Design

In this section, we'll look at several examples that illustrate how generative design can help you achieve your design goals.

### MaRs Innovation District of Toronto

To design the new office and research space in the MaRs Innovation District of Toronto, Autodesk used generative design processes. Starting with high-level goals and constraints, the design team used the power of computation to generate, evaluate and evolve thousands of design alternatives. The result was a high-performing and novel work environment that would not have been possible without this approach.

为了设计多伦多 MaRs 创新区的新办公和研究空间，欧特克采用了生成式设计流程。设计团队从高层次的目标和约束条件开始，利用计算的力量生成、评估和演化了数千种设计方案。最终形成了一个高性能、新颖的工作环境，如果没有这种方法是不可能实现的。

#### Generate

![[../2023年/attachments/Design goals - Mars Innovation District - The Living.png]]

>Above: Design goals - Mars Innovation District - The Living

The designers created a geometric system that meant the computer could explore multiple configurations of work neighborhoods, amenity spaces and circulation zones. This work represents the _`define`_ step of the _`generate`_ phase. Using this algorithm, the computer varied the parameters to produce thousands of design options.

设计师创建了一个几何系统，这意味着计算机可以探索工作区、休闲空间和流通区的多种配置。这项工作是生成阶段的定义步骤。利用这一算法，计算机可以改变参数，生成数千种设计方案。

#### Evaluate

![[../2023年/attachments/Design option evaluated and selected- Mars Innovation District.jpg]]

>Above: Design option evaluated and selected- Mars Innovation District - The Living

For this stage, information was collected from employees and managers about work styles and location preferences. Based on this data, six primary and measurable goals were defined:

- work style preference
- adjacency preference
- low distraction
- interconnectivity
- daylight
- views to the outside

The designers then created an algorithm to measure how any given floor plan could be measured against each of the goals above. Known as _`evaluators`_, these algorithms represent the _`analyse`_ and _`rank`_ stages of the generative process.

After the algorithms were formulated, the computer used them to evaluate each of the designs generated in the previous stage against the defined goals.

在这一阶段，我们从员工和管理人员那里收集了有关工作方式和地点偏好的信息。根据这些数据，确定了六个主要的、可衡量的目标：工作方式偏好、邻近性偏好、低分心、互联性、日光、外部景观。然后，设计师们创建了一种算法，用于衡量任何给定平面图如何与上述目标相匹配。这些算法被称为评价器，代表了生成过程中的分析和排序阶段。在制定算法后，计算机使用这些算法，根据确定的目标对上一阶段生成的每个设计进行评估。

#### Explore

![[../2023年/attachments/Design Options - Mars Innovation District - The Living.gif]]

>Above: Design Options - Mars Innovation District - The Living

After the designs were evaluated, the designers looked at the _`solution space`_ to explore the generated designs together with their evaluation results. Taking into account each defined goal, they identified the design that best achieved the goals overall.

在对设计进行评估后，设计人员查看了解决方案空间，以探索生成的设计及其评估结果。考虑到每个既定目标，他们确定了最能实现总体目标的设计。

### Furniture Design

Looking at a simpler example, let's consider the process of designing a typical, four-legged table. Using a standard approach, you as the designer would manually define the length, width, height and material of the table. The resulting output is a single, physical object with a fixed, immutable form. Here, you have the option to test several distinct sets of dimensions and material combinations to end up with three or four prototypes (or however many iterations you wanted).

举个简单的例子，让我们来看看设计一张典型的四脚桌子的过程。使用标准方法，设计者需要手动定义桌子的长度、宽度、高度和材料。最终的输出结果是一个具有固定不变形式的单一物理对象。我们可以选择测试几组不同的尺寸和材料组合，最终得到三到四个原型（或任意多的迭代）。

![[Furniture Design.webp]]

In a generative design approach, you would instead create an algorithm that specifies:

- a range of permissible values for each dimension;
- a series of available materials and their properties (such as cost/m²); 
- a set of goals that measure how successful a table design is.

在生成式设计方法中，您可以创建一种算法，指定

- 每个尺寸的允许值范围；
- 一系列可用材料及其属性（如成本/平方米）； 
- 一组衡量桌子设计成功与否的目标。

#### Generate

Then, you would use a computer to run the algorithm and generate a series of designs that fall within the ranges you previously specified.

Some designs will be short and wide, others will be tall and thin, but each will satisfy the user-defined constraints. This is key, as many designs can be generated very quickly, much more than any human could feasibly examine.

>Let's imagine the computer looked at 20 different values for each of: length, width, height, table/leg material combinations. The resulting solution space would be 20 * 20 * 20 * 20  = 160,000 designs, which is way too many options for a person to reasonably evaluate.

![[Furniture Design Generate.png]]

>Above: Matrix showing 36 generated table designs, varying width, length, and height.

#### Evaluate

The next step is to define how the generated designs are evaluated. This is your opportunity to clearly express your design goals.

![[A range of table designs (sizes), colour-coded based on evaluator function result (cost)..jpg]]

>Above: A range of table designs (sizes), colour-coded based on evaluator function result (cost).

Let's see how different design goals could be expressed in this _`evaluation`_ stage:

|   |   |   |
|---|---|---|
|Design goal|Analysis method|Ranking method|
|lowest cost per desk, with minimum 800mm x 600mm size|desk size: at least 800mm x 600mm in size = _`yes/no`_ and desk cost: area * material cost/m² = currency _`$`_ value)|lowest cost first and only options that satisfy area requirements|
|most profitable (largest desk area with lowest material cost)|desk area = outputs m² and unit cost (area * material cost/m²) = currency _`$`_ value|largest area and lowest cost|

The matrix above exemplifies how you can use this stage in the generative design process to design for wildly different scenarios.

In the first scenario, lowest overall cost is the driving goal, so we can expect small desk sizes and cheap materials while still satisfying the size requirement. This scenario would be relatively simple for humans to replicate, so generative design would only come in handy when the variation or complexity of material costs is high.

For the second scenario, we're aiming to maximize return on investment (ROI) for each desk. This means that we can expect larger, more expensive desks than the first scenario, but that still have the best overall ROI. It wouldn't be unexpected for this process to identify a desk with cheap legs and more expensive tabletop materials as a viable option.

This second scenario is a good illustration of using generative design to work towards multiple and competing goals, which is very hard for humans to replicate.

![[Visualizing evaluator function results as a color range.jpg]]

>Above: Visualizing evaluator function results as a color range.

As you can see, both of these examples follow the same fairly generic process, which is why there are so many possible applications of generative design in areas as diverse as aviation, automotive and building design, manufacturing, and product design.

### A Further Analogy

Let’s now look at generative design through the lens of something most of us do on a daily basis: finding the quickest commute route to work. In this example, let's say you’re looking to go from Brooklyn to Manhattan. You go to your favorite route-comparison website and ask it to find you the quickest route between these two locations.

现在，让我们从我们大多数人日常工作的角度来看看生成式设计：寻找最快的通勤路线。在这个例子中，假设你想从布鲁克林去曼哈顿。您可以访问您最喜欢的路线比较网站，让它为您找出这两个地点之间的最快路线。

![[The Citymapper website showing possible routes between Brooklyn and Manhattan, while also considering multiple modes of transportation.webp]]

>The Citymapper website showing possible routes between Brooklyn and Manhattan, while also considering multiple modes of transportation(Citymapper 网站显示了布鲁克林和曼哈顿之间的可能路线，同时还考虑了多种交通方式)

To help illustrate this analogy, let's make a table comparing the expected activities when searching for the quickest commute route and what their equivalent would be in a generative design process.

为了帮助说明这个类比，让我们制作一个表格，将搜索最快通勤路线时的预期活动与生成式设计流程中的相应活动进行比较。

|   |   |
|---|---|
|Map activity|Equivalent in generative design process|
|Person (you) sets first parameter: go from Brooklyn to Manhattan|Stage: generate Step: set generation parameters|
|Computer generates possible routes from Brooklyn to Manhattan, taking into consideration all the available transportation modes, their operating status and set routes|Stage: generate Step: run generation algorithm|
|Person sets goals: quickest route|Stage: rank<br>Step: define ranking objectives|
|Computer evaluates each of the identified routes based on your goals|Stage: rank<br>Step: run ranking|
|Computer attempts to solve your goals and returns the list of routes, putting most suitable ones first|Stage: evolve<br>Step: run evolution|
|Person evaluates the list of best options and makes a choice more efficiently than if they had to do it themselves|Stage: explore<br>Step: evaluate options|
|Person chooses preferred route and sends travel instructions to their phone|Stage: integrate<br>Step: integrate preferred option|

It's important to note that, because the computer knows about multiple modes of transport (walk, cycle, bus, train, etc.), it can combine them to find the best option. This means the goal we set the computer can have a big effect on the routes that are generated. For example, if we specified that we wanted to travel by car, or that we needed step-free access, the resulting routes would be completely different.

值得注意的是，由于计算机了解多种交通方式（步行、骑自行车、公交车、火车等），因此它可以将这些方式结合起来，找到最佳选择。这意味着我们给电脑设定的目标会对生成的路线产生很大影响。例如，如果我们指定要开车出行或需要无台阶通道，生成的路线就会完全不同。

![[Citymapper website showing routes that have step-free access..png]]

>Above: Citymapper website showing routes that have step-free access.

In this example, we can see that the generated routes take longer than in the first example, as the new goal is to have 'step-free access' instead of 'quickest commute'. Though this example may be stretching the imagination (as a computer doesn't generate new transport modes, it just generates new routes using existing modes), this analogy demonstrates similar steps as those found in a generative design workflow.

在这个例子中，我们可以看到生成路线所需的时间比第一个例子要长，因为新的目标是 "无台阶交通"，而不是 "最快通勤"。虽然这个例子可能有些夸张（因为计算机不会生成新的交通模式，它只是利用现有模式生成新的路线），但这个类比展示了与生成式设计工作流程中类似的步骤。

