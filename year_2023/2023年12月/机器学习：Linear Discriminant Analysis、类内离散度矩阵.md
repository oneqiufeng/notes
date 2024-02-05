# 机器学习：Linear Discriminant Analysis、类内离散度矩阵

### 目录

- [LDA概念](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_1)
- [线性判别分析（LDA）-二分类](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_6)
- [LDA二分类过程](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_33)[举个例子](https://blog.csdn.net/qq_43738932/article/details/109328870#_44)
- [线性判别分析-多分类](https://blog.csdn.net/qq_43738932/article/details/109328870#_73)
- [LDA多分类过程](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_78)
- [Experiment 3: Linear Discriminant Analysis](https://blog.csdn.net/qq_43738932/article/details/109328870#Experiment_3_Linear_Discriminant_Analysis_81)
- [LDA二分类讲解](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_82)[LDA二分类代码](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_92)[LDA多分类讲解](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_161)[LDA多分类代码](https://blog.csdn.net/qq_43738932/article/details/109328870#LDA_170)

# LDA概念

线性判别分析（Linear Discriminant Analysis）是一种有监督学习的降维方法，用于找到分隔两个或多个对象类的特征的线性组合。

也就是给定有标签的数据集，利用LDA实现一个较好的分类。谈及分类，那么就说一说特征提取： 特征提取（维数约简/特征约简）是指将原始高维数据映射到低维空间。而LDA就是给定数据集，将训练样本投影到一条直线上。使得类间距离最大化，同时使得类内距离最小化。

# 线性判别分析（LDA）-二分类

> 给定两个类中的一组点(2-d)，我们希望将它们投影到一条可以很好地分离它们的行。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/18c130cc-2557-4de4-bf20-0e8696d8db82/20201028111521681.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/18c130cc-2557-4de4-bf20-0e8696d8db82/20201028111521681.png)

> 最大化类间距离Maximize the between-class distance (means)
> 
> 最小化类内距离Minimize the within-class variability (scatter)
> 
> 若只考虑如上第一个标准，仍然无法得到一个好的效果。如左图。使用以上两个标准，我们就能得到如下图右边这样的效果。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/d66518f6-8706-4331-b93c-40484e2c1ea4/20201028112149603.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/d66518f6-8706-4331-b93c-40484e2c1ea4/20201028112149603.png)

**那么我们具体怎样计算出那条投影直线呢？**

> 假设我们有一个d维的样本集，{x1,x2,x3,···，xd}，C1有n1个样本点，C2有n2个样本点，那么我们求一个转换，将d维投影到一条线上，实现降维。那么它的公式如下。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ac72f905-81af-4c4d-b474-92e9b477ff32/20201028112802345.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ac72f905-81af-4c4d-b474-92e9b477ff32/20201028112802345.png)

`θ代表将x投影到y的投影向量`

**那么我们又怎么计算类内距离和类间距离呢？**

首先计算每个类的均值：

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/06a0cd4f-d74a-4b52-b8d1-d1d47c20fe68/20201028113519905.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/06a0cd4f-d74a-4b52-b8d1-d1d47c20fe68/20201028113519905.png)

使得投影间距离最大化：

计算类间散度矩阵：

计算类内散度矩阵：

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/e705fa4a-fcaa-469a-ad21-7634511997db/20201028114217875.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/e705fa4a-fcaa-469a-ad21-7634511997db/20201028114217875.png)

最小化投影

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/75693c6c-40d2-4330-8b87-586c1f692758/20201028115332401.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/75693c6c-40d2-4330-8b87-586c1f692758/20201028115332401.png)

## LDA二分类过程

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1f288061-20b8-4297-aed9-9eac9c992da5/20210127133509363.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1f288061-20b8-4297-aed9-9eac9c992da5/20210127133509363.png)

> 1.从训练集中构造样本 X 1 X_1 X1和有样本 X 2 X_2 X2。即分为2类，分别取两个类别的样本。
> 
> 2.计算每个类别的样本均值 μ 1 \mu_1 μ1和 μ 2 \mu_2 μ2
> 
> 3.计算类内散度矩阵
> 
> 4.计算类内散度矩阵的逆。(矩阵的逆 A A − 1 = A − 1 A = I AA^{-1}=A^{-1}A=I AA−1=A−1A=I， I I I是单位矩阵)
> 
> 5.计算 θ ∗ = S w − 1 ( μ 1 − μ 2 ) \theta^_=S^{-1}_w(\mu_1-\mu_2) θ∗=Sw−1(μ1−μ2),这里的 θ ∗ \theta^_ θ∗是投影向量。
> 
> 6.给出一个测试函数。(就是实际的用于分类的目标函数): y = θ ∗ T x y=\theta^{*T}x y=θ∗Tx,因为是二分类，所以y∈{-1,1}
> 
> 7.计算阈值 γ \gamma γ
> 
> 8.比较阈值γ和y，确定测试点的类别。若 y < γ y<\gamma y<γ,为负类，类别号为-1，反之则为1。
> 
> 9.注意，LDA是用来降维的！不是用来分类的。

## 举个例子

> 计算下列二维数据集的线性判别投影。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1ed41480-dd35-484e-802f-a32c6294d6c0/20201028115439911.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1ed41480-dd35-484e-802f-a32c6294d6c0/20201028115439911.png)

> 由上图，这是一个二分类问题，我们分别计算出每一类的均值。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/109f0609-97e1-42de-83f2-eac46562bce1/20201028115556773.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/109f0609-97e1-42de-83f2-eac46562bce1/20201028115556773.png)

`第一个类别的协方差矩阵`

`第二个类别的协方差矩阵`

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/96b1a2fb-f6c3-4751-8b0e-260db07628df/2020102812352325.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/96b1a2fb-f6c3-4751-8b0e-260db07628df/2020102812352325.png)

> 类内散度矩阵

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/890ca4e3-5abb-4d31-a184-ba33fa3e9ca1/20201028123601434.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/890ca4e3-5abb-4d31-a184-ba33fa3e9ca1/20201028123601434.png)

> 类间散度矩阵

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/506b42a2-ca5e-4a1b-9499-81aed858608b/20201028123629644.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/506b42a2-ca5e-4a1b-9499-81aed858608b/20201028123629644.png)

> 计算特征值

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/b08d6c3c-3db0-48ea-a936-bd024a732dce/2020102812372259.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/b08d6c3c-3db0-48ea-a936-bd024a732dce/2020102812372259.png)

> 最优投影就是最小化的投影

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/d2146bf6-7a95-4e57-8e27-c7ee85774bfd/20201028123808870.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/d2146bf6-7a95-4e57-8e27-c7ee85774bfd/20201028123808870.png)

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8e9fb0b7-33d2-4887-83db-ac3204485a3b/20201028123843776.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8e9fb0b7-33d2-4887-83db-ac3204485a3b/20201028123843776.png)

# 线性判别分析-多分类

多分类与二分类不同的是类间散度矩阵和类内散度矩阵计算公式不同。其余根据概念计算即可。

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/18314803-98ef-4214-87a4-6afb12469427/20201028114434419.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/18314803-98ef-4214-87a4-6afb12469427/20201028114434419.png)

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8c2966da-0e67-4a14-8860-a09c1e57846b/20201028114445741.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8c2966da-0e67-4a14-8860-a09c1e57846b/20201028114445741.png)

## LDA多分类过程

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/588b123c-2803-4a41-9f35-14c52b9497fe/20210127135642139.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/588b123c-2803-4a41-9f35-14c52b9497fe/20210127135642139.png)

# Experiment 3: Linear Discriminant Analysis

## LDA二分类讲解

**1. 数据加载**

下载数据 exe3Data.zip 并解压。在 exe3red、exe3green、exe3blue 中分别有 14 行红色 的点，14 行绿色的点和 14 行蓝色的点。用该数据来实现 LDA 算法。

**2. LDA 的实现过程**

a.两个类别的 LDA 你必须根据课堂上正确的原则自己实现 LDA。不允许直接使用 Matlab 提供的可用 LDA 代码， 这些代码可用于检查结果。 在本节中，需要实现两个类的 LDA。这里我们选择对两个类使用红色和蓝色的点。你应该加 载数据到你的矩阵和绘图:

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/61ead725-3bb5-4879-951a-80dae4835684/20201028115807179.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/61ead725-3bb5-4879-951a-80dae4835684/20201028115807179.png)

b.成功完成代码后，LDA 结果应该如下所示:

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/a969868d-81de-4d4e-a3a6-f7e4e9a31d73/20201028115916610.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/a969868d-81de-4d4e-a3a6-f7e4e9a31d73/20201028115916610.png)

c.投影点绘制

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1b1dda12-16cf-49d9-81ef-fcbd71d6b000/20201028115952231.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/1b1dda12-16cf-49d9-81ef-fcbd71d6b000/20201028115952231.png)

## LDA二分类代码

```matlab
%upload data
x1=load('ex3red.dat');
x2=load('ex3blue.dat');
x3=load('ex3green.dat');
figure %first
hold on
plot(x1(:,1),x1(:,2),'ro','markerfacecolor','r');
plot(x2(:,1),x2(:,2),'b*','markerfacecolor','b');
xlabel('x');
ylabel('y');
xlim([0.00 10.00])
ylim([0.00 10.00])
m1=mean(x1);%compute mean value
m2=mean(x2);
%LDA for 2-class
Sb=(m1-m2)'*(m1-m2);%compute Between-class scatter
Sw=(x1-m1)'*(x1-m1)+(x2-m2)'*(x2-m2);%compute Within-class scatter
[V,L]=eig(inv(Sw)*Sb);
[a,b]=max(max(L));
theta = Sw\\(m1-m2)';%left
disp(theta)
figure % second
hold on
plot(x1(:,1),x1(:,2),'ro','markerfacecolor','r');
plot(x2(:,1),x2(:,2),'b*','markerfacecolor','b');
x=linspace(0,10,100);
y=(theta(2)/theta(1))*x;
plot(x,y,'black')
title('LDA for two-classes')
xlabel('x')
ylabel('y')
%compute the projection
k=theta(2)/theta(1);
s1=size(x1,1);
s2=size(x2,1);
x1_tag=[];
x2_tag=[];
for i=1:s1
    y0=x1(i,2);
    x0=x1(i,1);
    xn=(k*(y0-b)+x0)/(k^2+1);
    x1_tag=[x1_tag;xn];
end
y1_tag=k*x1_tag + b;
x1_final=[x1_tag y1_tag];
for i=1:s2
    y0=x2(i,2);
    x0=x2(i,1);
    xn=(k*(y0-b)+x0)/(k^2+1);
    x2_tag=[x2_tag;xn];
end
y2_tag=k*x2_tag + b;
x2_final=[x2_tag y2_tag];
figure%third
hold on
plot(x1(:,1),x1(:,2),'ro','markerfacecolor','r');
plot(x2(:,1),x2(:,2),'b*','markerfacecolor','b');
x=linspace(0,10,100);
y=(theta(2)/theta(1))*x + b;
plot(x,y,'black')
title('LDA for two-classes')
xlabel('x')
ylabel('y')
plot(x1_final(:,1),x1_final(:,2),'ro','markerfacecolor','r');
plot(x2_final(:,1),x2_final(:,2),'bo','markerfacecolor','b');
1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465
```

## LDA多分类讲解

LDA 可以用于多分类实现，这部分，对于 LDA 实现的 N 分类，不妨取 N=3，将所有的红、蓝、 绿点加载到矩阵中并绘制它们。实际上，对于 N 个类实现 LDA 比较困难。完成代码后，看看 结果有多令人满意。

**a. 加载数据集并绘制散点图：**

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ace5ce44-288c-4655-a29c-99da918c431e/20201028122721250.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ace5ce44-288c-4655-a29c-99da918c431e/20201028122721250.png)

**b. 计算类内散度矩阵和类间散度矩阵。绘制直线**

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8d87f550-990d-4b00-b3f5-6015b93d7d9f/20201028122739820.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/8d87f550-990d-4b00-b3f5-6015b93d7d9f/20201028122739820.png)

**c.投影。**

![https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ae9311e7-eddc-4dc4-90a6-00dd01c1734a/20201028122820575.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c924a3ca-aaf7-46b7-be35-676775825d60/ae9311e7-eddc-4dc4-90a6-00dd01c1734a/20201028122820575.png)

## LDA多分类代码