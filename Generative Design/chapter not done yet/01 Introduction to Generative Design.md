# Introduction to Generative Design

In this chapter, we’ll look at key concepts that are essential to understanding generative design and how Generative Design for Revit and Dynamo works.

![[../../2023年/attachments/CUBE.webp]]

In this section, we will explore the following topics:

- **the fundamental concepts needed to understand generative design**
- **a definition of generative design in the context of AEC**
- **an introduction to Generative Design for Revit and Dynamo**
- **examples of using generative design to solve design problems**
- **common approaches used**
- **related concepts**

Let’s start by looking at something you are likely to be familiar with and already using today: computational design.

# 1.1 Computational Design

_`Computational design`_ is not any one algorithm or off-the-shelf process you can utilize. Rather, we describe it as an approach whereby a designer defines a series of instructions, rules and relationships that precisely identify the steps necessary to achieve a proposed design and its resulting data or geometry.

Crucially, these steps must be computable, meaning they can be understood and calculated by a computer.

![[../../2023年/attachments/compdesign_Above Image of an NURBS manipulations from Martin Stacey.gif]]

> _Above: Image of an NURBS manipulations from Martin Stacey - UCL._

Put simply, computers are very good at performing calculations and executing pre-defined steps.

When approaching a design computationally, the designer would focus on developing the procedure that would create a design - not the design itself. The process of iterating through options and data are offloaded to a computer. This saves time, money and effort, and lets the designer focus on the creativity of the design process.

# 1.2 Generative Design

In this section, we’ll look at what the term 'generative design' means in relation to the AEC industry.

We will look at the following:

- What is Generative Design?
- Why Should I Use Generative Design?
- What Goes into a Generative Design Process?
- Examples of Generative Design

![[../../2023年/attachments/Massing analysis - Alkmaar Housing Commission - The Living.webp]]

> Massing analysis - Alkmaar Housing Commission - The Living

# What is Generative Design?

You may have encountered the term 'generative design' in the context of producing design permutations, creating geometry from some simple inputs, or even just building computational graphs using Dynamo or Grasshopper.

We see generative design (**/ gen·er·a·tive de·sign /** noun) as:

> A collaborative design process between humans and computers. During this process, the designer defines the design parameters and the computer produces design studies (alternatives), evaluates them against quantifiable goals set by the designer, improves the studies by using results from previous ones and feedback from the designer, and ranks the results based on how well they achieve the designer’s original goals.

![[../../2023年/attachments/Some generated alternatives - Mars Innovation District - The Living.gif]]

> Above: Some generated alternatives - Mars Innovation District - The Living

Generative design is a specific application of the computational design approach, with the following distinctions:

- The designer defines goals to achieve a design (rather than the exact steps).
- The computer helps the designer to explore the design space and generate multiple design options (not just one).
- The computer enables the designer to find a set of optimal solutions that satisfy multiple competing goals.
- The designer compares multiple design scenarios to find a set of design options that fits the design goals.