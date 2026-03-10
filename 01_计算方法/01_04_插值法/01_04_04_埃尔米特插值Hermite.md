
# 1 不同插值公式的 基函数

![](image/Pasted%20image%2020260308133653.png)


![](image/Pasted%20image%2020260308133847.png)


---

求误差 ， 就是余项
求误差限 就是 对 f(x) 的 n+1 求导  作估计 ， 
![](image/Pasted%20image%2020260308155705.png)



# 2 多项式插值的提法

![](image/Pasted%20image%2020260308160613.png)



# 3 埃米尔特插值 

==埃米尔特插值公式 不光要给出是节点上的函数值， 还必须给出节点上的导数值 ==

埃米尔特插值多项式的意义： 
要求 插值多项式 在 插值节点上与被插值函数的函数值相等， 
还要求插值多项式的导数在这些点上被插函数的导数值相等。 
![](image/Pasted%20image%2020260308132652.png)


可导节点 
函数值与导数值

![](image/Pasted%20image%2020260308161120.png)

![](image/Pasted%20image%2020260308161143.png)

第一行 有 m1+1 个等式， 就代表着 一共给出了 m1+1 个条件 

![](image/Pasted%20image%2020260308161335.png)


# 4 三次埃米尔特插值


![](image/Pasted%20image%2020260308161601.png)


4个等式 （就是四个条件） 能够得到 三次多项式 
给出两个点， 这两个点上即给出函数值， 也给出他的一阶导数值 ， 这样的话 就凑够了 4个条件 

![](image/Pasted%20image%2020260308162116.png)

---

用 alpha 和 beta 来代表基函数 

![](image/Pasted%20image%2020260308162541.png)



![](image/Pasted%20image%2020260308162616.png)


![](image/Pasted%20image%2020260308162647.png)

---
对于 alpha_0(x) 
![](image/Pasted%20image%2020260308163954.png)

 1 由右边两个条件 1阶导数为0， 我们可以得到  alpha_0(x） 对于 x=x1 是2阶0点
则 含有因子 $(x-x1)^2$

2 我们要 求 拥有 x的3次方的 hermite 的 多项式
则 alpha_0(x)在含有因子 $(x-x1)^2$ 外，也应该还有 个 ax+b, 这样保证 x 有 三次方的项


3 故而推测 alpha_0(x)  = (ax+b) $(x-x1)^2$ 
![](image/Pasted%20image%2020260308164135.png)


4   左边的那两个条件 
![](image/Pasted%20image%2020260308164209.png)

得到 
![](image/Pasted%20image%2020260308164216.png)

$a(x-x1)^2 + (ax+b)2(x-x1) = 0$, x0-x1 肯定不为0， 故而等式两边 左右两边都除以 x0-x1
得到 $a(x0-x1) + (ax0+b)2 = 0$,



5 最后得到 
![](image/Pasted%20image%2020260308164626.png)


---

对于 alpha_1(x) 
![](image/Pasted%20image%2020260308164825.png)


---

对于 beta_0(x)

通过上面的等式可以判断
x0 是1阶零点， x2 是2阶零点  

![](image/Pasted%20image%2020260308165008.png)


---

对于 beta_1(x)

通过上面的等式可以判断
x0 是1阶零点， x2 是2阶零点  

![](image/Pasted%20image%2020260308165034.png)

---

最终根据 

![](image/Pasted%20image%2020260308162541.png)

得到 三次 hermite多项式 

---

余项 
R3(x) = f(x)  -  H3(x)
H3(x) 为 三次 hermite多项式 ，  就是含有x 的 3次方的项， x 的最高次 为3次
![](image/Pasted%20image%2020260308171837.png)


## 4.1 三次埃米尔特插值多项式的余项 

埃米尔特插值多项式的意义： 
要求 插值多项式 在 插值节点上与被插值函数的函数值相等， 
还要求插值多项式的导数在这些点上被插函数的导数值相等。 

1 
x0 为 已知的点， f(x)  就是根据 x0 , x1 等等的点 构造出来的， 所以  f(x0)  -  H3(x0) 必然为0 
R3(x0) = f(x0)  -  H3(x0)  = 0

2 同理 
R3(x1) = f(x1)  -  H3(x1)  = 0


3 又根据 埃米尔特插值多项式的意义， 得到 
![](image/Pasted%20image%2020260308172658.png)


4 可以得到 x0, x1 分别为H3(x) 二阶零点 
![](image/Pasted%20image%2020260308172808.png)

得到 余项的表达式为 $K(x)(x-x0)(x-x1)^2$

---

如何构造余项公式的基函数

![](image/Pasted%20image%2020260308173639.png)


真实的余项  为 f(x) - H3(x)  
这个真实的余项的近似值 是 $K(x)(x-x0)^2(x-x1)^2$

phi 的四姐导数等于0
 0 =  f(x) 的四阶导数 - H3(x) (H3(x)的四阶导数 为0 因为 H3 的最高项是x的3次方) - 4! K(x)
![](image/Pasted%20image%2020260308183824.png)



## 4.2 罗尔定理 

![](image/Pasted%20image%2020260308173625.png)



# 5 2n+1次的 Hermite多项式

![](image/Pasted%20image%2020260308184334.png)


一共有 n+1 列
则可以构建  2(n+1) -1  的 Hermite多项式 
![](image/Pasted%20image%2020260308184937.png)

x_j 是 alpha_i 的2重零点 ， j 的取值 是 0 到 n, 除了i

![](image/Pasted%20image%2020260308185501.png)


---

余项 

为什么是(x-x0)^2， 为什么2次方。 因为 x0 为 2阶零点。 
为什么 x0 为 2阶零点  ，  见 三次埃米尔特插值  这章 的相关解释和计算 

![](image/Pasted%20image%2020260308191023.png)



# 6 非完全的hermite插值多项式

不是所有点的 函数值都是已知的

![](image/Pasted%20image%2020260308191651.png)


首先构造其 2次插值多项式   langerange 2次插值多项式 
![](image/Pasted%20image%2020260308191802.png)


---

2次 langerange 插值多项式  和 三次 hermite 插值多项式 

H3(x0) 肯定等于 L_2(x0), 那么 说明 H_3(x) = L_2(x)  + xxx 
xxx 中一定含有 （x-x0）

同样的道理 ， xxx 中一定含有 （x-x1） 和 （x-x2）
得到 H_3(x) = L_2(x)  +  A (x-x0)(x-x1)(x-x2)
(x-x0)(x-x1)(x-x2) 已经含有 x 3次方了, 则除了 (x-x0)(x-x1)(x-x2)， 不再含有其他了 

![](image/Pasted%20image%2020260308192538.png)

---

再利用 H_3'(x1) = y_1'

![](image/Pasted%20image%2020260308192659.png)

L_2(x)  已经通过 拉格朗日插值法 在前面求出来了 

## 6.1 余项


x0 应为 1 重零点 
x1 应为 2重零点

![](image/Pasted%20image%2020260308193024.png)


# 7 例子： 请看出下面插值的余项因子

![](image/Pasted%20image%2020260308194840.png)



Hermite 多项式 的 x的最高次项是4次方 ， 因为一共最多能给出5个等式
那他的余项 
- 因为一共最多能给出5个等式。 其中 两个还是 为二阶零点 ， 所以 w(n) 为 (x-x0)^2 (x-x1)  (x-x2)^2 ， 中 x最高项是5.
- f(x)应给是 4+1 次方求导 .   因为 H_4(x) 最高次项是4次方



# 8 例子



## 8.1 

![](image/Pasted%20image%2020260309145548.png)

![](image/Pasted%20image%2020260309163646.png)


![](image/Pasted%20image%2020260309163702.png)

![](image/Pasted%20image%2020260309164953.png)

![](image/Pasted%20image%2020260309165022.png)

## 8.2 