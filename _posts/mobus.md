---
layout:default
title: mobus 
---

sb输入法

莫比乌斯反演感觉就是一种无聊且套路的傻逼知识

很多人讲的时候都不想说出来

首先我们那需要一些前置技能

1.线性筛

我们需要通过线性筛来筛出来一些积性函数（不知道请百度）

通常情况下埃氏筛能及其容易的筛出，其和线性筛的速度相差可以是常数级别。

2.积性函数

我们需要认识几种积性函数（感觉不会用latex）

#### 欧拉函数

${\phi}(i)$表示小于i中和i互质的数

一些性质

如果p是质数，那么${\phi}(p)= p-1$

**欧拉定理**

$a^{\phi(p)}\equiv 1 (mod p)$

具体证明百度

p是质数时是费马小定理

#### 莫比乌斯函数

一听就是重点

死都打不出来


[![](http://latex.codecogs.com/png.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%7B%5Cmu%7D%28i%29%3D%20%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%201%20%28i%3D1%29%20%5C%5C%20%28-1%29%5Er%20%28i%3D%5CPi%20\_%7Bi%3D1%7D%5Er%20p\_i%2C%5Cforall%20i%2Cj%20%2Cp\_i%5Cneq%20p\_j%20%29%5C%5C%200%5Cend%7Bmatrix%7D%5Cright.)](http://http://latex.codecogs.com/png.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%7B%5Cmu%7D%28i%29%3D%20%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%201%20%28i%3D1%29%20%5C%5C%20%28-1%29%5Er%20%28i%3D%5CPi%20\_%7Bi%3D1%7D%5Er%20p\_i%2C%5Cforall%20i%2Cj%20%2Cp\_i%5Cneq%20p\_j%20%29%5C%5C%200%5Cend%7Bmatrix%7D%5Cright.)

$p_i$之类的都是质数

不懂什么意思不重要

两个简单的积性函数

1函数。1（i）=1

id函数 id（i）=i

$\xi (1)=1$ 当i时其他数时值都为0


------------


重要的前置知识2

dirichle卷积

首先很多人都不理解卷积，建议先将卷积的定义搞懂，不需要深刻理解

那么dieichle是数论上的重要卷积（针对数论函数）

我们定义

$f(n) \times g(n)= \sum_{ d\mid n}f(d)*g(\frac{n}{d})$



------------


重要的前置知识

$\mu \times 1 = \xi$

随便想想就知道是对的

$\phi \times 1= id$

随便想想就知道是对的

想不通无所谓不重要


------------

我们要试图证明

$\mu \times id= \phi$

$\phi(n)=\sum_{1}^n\xi(gcd(i,n))$

$\because \mu \times id = \xi$

[![](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Csum\_i%5En%5Csum\_%7Bd%5Cmid%20gcd%28i%2Cn%29%7D%20%5Cmu%28d%29)](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Csum\_i%5En%5Csum\_%7Bd%5Cmid%20gcd%28i%2Cn%29%7D%20%5Cmu%28d%29http://)

然后我们考虑枚举gcd

将d提前

[![](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29%5Csum\_%7Bd%5Cmid%20i%7D%3D%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29\*%5Cfrac%7Bn%7D%7Bd%7D%3D%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29\*id%28%5Cfrac%7Bn%7D%7Bd%7D%29%3D%5Cmu%20%5Ctimes%20id)](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29%5Csum\_%7Bd%5Cmid%20i%7D%3D%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29\*%5Cfrac%7Bn%7D%7Bd%7D%3D%5Csum\_%7Bd%5Cmid%20n%7D%5Cmu%28d%29\*id%28%5Cfrac%7Bn%7D%7Bd%7D%29%3D%5Cmu%20%5Ctimes%20id)

那么我们发现

[![](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Cmu%20%5Ctimes%20id%20%3D%20%5Cphi%20%5CLeftrightarrow%20%5Cphi%20%5Ctimes%201%20%3D%20id)](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Cmu%20%5Ctimes%20id%20%3D%20%5Cphi%20%5CLeftrightarrow%20%5Cphi%20%5Ctimes%201%20%3D%20id)

那么我们考虑推广

[![](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Cmu%20%5Ctimes%20f%20%3D%20g%20%5CLeftrightarrow%20g%20%5Ctimes%201%20%3D%20f)](http://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5Clarge%20%5Cmu%20%5Ctimes%20f%20%3D%20g%20%5CLeftrightarrow%20g%20%5Ctimes%201%20%3D%20f)

那么我们简单的证明一下

从左到右

然后建议根据从左到右尝试推导出从右到左

这是做所有题的**关键**

一定要熟练

为了我的室友晚上不饿我决定给他看些好吃的

[![](https://ss2.bdstatic.com/70cFvnSh\_Q1YnxGkpoWK1HF6hhy/it/u=418466229,3629394713&fm=27&gp=0.jpg)](https://ss2.bdstatic.com/70cFvnSh\_Q1YnxGkpoWK1HF6hhy/it/u=418466229,3629394713&fm=27&gp=0.jpg)

[![](http://img4.imgtn.bdimg.com/it/u=2498279644,2340462214&fm=27&gp=0.jpg)](http://img4.imgtn.bdimg.com/it/u=2498279644,2340462214&fm=27&gp=0.jpg)

[![](http://img5.imgtn.bdimg.com/it/u=3478548860,3870032797&fm=27&gp=0.jpg)](http://img5.imgtn.bdimg.com/it/u=3478548860,3870032797&fm=27&gp=0.jpg)

[![](http://img0.imgtn.bdimg.com/it/u=2841007535,1570197587&fm=27&gp=0.jpg)](http://img0.imgtn.bdimg.com/it/u=2841007535,1570197587&fm=27&gp=0.jpg)

[![](http://img3.imgtn.bdimg.com/it/u=1887715588,335063087&fm=27&gp=0.jpg)](http://img3.imgtn.bdimg.com/it/u=1887715588,335063087&fm=27&gp=0.jpg)

[![](http://img0.imgtn.bdimg.com/it/u=3512898448,871646892&fm=27&gp=0.jpg)](http://img0.imgtn.bdimg.com/it/u=3512898448,871646892&fm=27&gp=0.jpg)

是不是感觉很饱 啊

那么我们继续学习

那么我们假设已知

$\mu \times f= g$

试着推出

$g \times 1 = f $


那么其实好像推这些只是锻炼一下技巧，其实莫比乌斯反演作为一种很套路的只是点你只要记住四个式子就好

1.$\phi \times 1 = id$

2$\mu \times id = \phi$

3.$\mu \times 1 =\varepsilon$

4.$\varepsilon \times 1= 1$

注意n/d向下取整最多只有sqrt（n）种取值

$d \mid gcd(a,b) \Leftrightarrow d\mid a $且$d\mid b$

举个经典的例子

$\sum_{i=1}^n\ sum_{j=1}^b gcd(i,j)$

由于id（x）=x

所以gcd（i，j）=id（gcd（i，j））

$=\sum_{i=1}^n\sum_{j=1}^b\sum_{d \mid gcd(i,j)} \phi(d) \times  1\left (  n/d  \right  )$

乘1相当于不乘，且我们将d提前就是枚举两个数的gcd

[![](http://latex.codecogs.com/svg.latex?%24%3D%5Csum\_%7Bd%3D1%7D%5En%20%5Cphi%28d%29%20%5Csum\_%7Bd%20%5Cmid%20i%7D%5En%5Csum\_%7Bd%20%5Cmid%20j%7D%5En%201%24)](http://latex.codecogs.com/svg.latex?%24%3D%5Csum\_%7Bd%3D1%7D%5En%20%5Cphi%28d%29%20%5Csum\_%7Bd%20%5Cmid%20i%7D%5En%5Csum\_%7Bd%20%5Cmid%20j%7D%5En%201%24)

那么后面那两个求和显然直接就向下取整然后求和就好了。

所以说其实很简单对不对


