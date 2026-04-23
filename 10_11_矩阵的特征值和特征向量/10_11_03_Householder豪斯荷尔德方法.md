

# 1 Householder阵 H

==结论 : 任意两个向量a,b 肯定能找到一个 正交矩阵H, 使得 Ha=b ==


## 1.1 推导

![](image/Pasted%20image%2020260410011628.png)

---

u 为单位矩阵 计算公式如下
x与y垂直, 则x和y 的内积应该为0 , 则x和y^T 的内积应该为0 
![](image/Pasted%20image%2020260410011955.png)

![](image/Pasted%20image%2020260410012124.png)


![](image/Pasted%20image%2020260410012534.png)

----

H为正交矩阵 

u 为单位矩阵 
![](image/Pasted%20image%2020260410012628.png)

![](image/Pasted%20image%2020260410012204.png)

![](image/Pasted%20image%2020260410012249.png)

---

## 1.2 结论 

==结论 : 任意两个向量a,b 肯定能找到一个 正交矩阵H, 使得 Ha=b ==


## 1.3 定理 : 如何求H
ab 为两个 等长的非0向量 
![](image/Pasted%20image%2020260410012430.png)

![](image/Pasted%20image%2020260410170044.png)

u 为单位矩阵 
![](image/Pasted%20image%2020260410012628.png)


![](image/Pasted%20image%2020260410011628.png)


## 1.4 推论1: 如何求H 的第二种方式

根据结论得到的推论 
x=  sigma 乘上 e_1
sigma 取正负值都可以 

e_1 为 `[1,0,0,0..., 0] ` , 则 e_1 的范数 等于1 


![](image/Pasted%20image%2020260410160602.png)

![](image/Pasted%20image%2020260410163056.png)

![](image/Pasted%20image%2020260410170258.png)

---


原本 
![](image/Pasted%20image%2020260410161024.png)

取 
a= x,  
b 等于 - sigma e_1

则可以得到 
![](image/Pasted%20image%2020260410170153.png)

----

==这个推论证明 我们可以通过 Householder 矩阵, 将 x 中除了第一个分量外, 其他的分量都化为0.   因为 e_1 中只有第一个分量有值, 其他的都为0==

做数值运算的时候 我们尽可能要求 sigma 和 x 中第一个分量同号 ,  这样是的 ||x+  sigma e_1 ||\_2 的值尽可能的大, 使得  u的误差尽可能的小

### 1.4.1 例题 

Hx = - sigma 乘上 e_1
根据 题设  sigma 必须为 -3 , 是一定定死的 

![](image/Pasted%20image%2020260410161648.png)


![](image/Pasted%20image%2020260410161717.png)


## 1.5 推论2: 如何求H 的第三种方式

 给定一个 向量x, 找到一个正交矩阵 使得 Hx 的结果 为 
 保留x 的前r半部分, 然后 元素为 -sigma 或者 + signma , 然后的元素都为0 , 但是 Hx 的长度 和 x 一致

其中 sigma 的值为
![](image/Pasted%20image%2020260410203543.png)

---

取 y= ()  , 利用 推论1 , 则一定存在 H矩阵 使得 Hy = - sigma e_1  

![](image/Pasted%20image%2020260410203936.png)

最终 H 的值 为 r阶的单位矩阵,  加上 H welle 

## 1.6 例题 

 x 中 signma 为 正号的

Hx = (x1, x2, - sigma, 0, ..., 0) 
Hx= (-1, 4, -3, 0, 0 )

![](image/Pasted%20image%2020260410205017.png)

![](image/Pasted%20image%2020260410205100.png)

![](image/Pasted%20image%2020260410205111.png)


# 2 对称矩阵的三对角化: 用 Householder矩阵

三对角矩阵是一种特殊的稀疏矩阵，其非零元素只分布在主对角线以及紧邻主对角线的上方和下方两条对角线上，其余位置全为零。

![](image/Pasted%20image%2020260410213810.png)

==若A 为对称矩阵,  A^T = A , 这时候 A 才能化为 三对角矩阵 ==


步骤1
取 H_1 welle 

![](image/Pasted%20image%2020260410211745.png)

---

步骤2 
取得 H_1
![](image/Pasted%20image%2020260410211843.png)


---

步骤3

A1 = H1_welle A1_welle H1_welle 
A1_welle 为  A的 有下角的一块
![](image/Pasted%20image%2020260410212029.png)



![](image/Pasted%20image%2020260410212221.png)


---

上面的 3个步骤 是一个相似变换, 因为 H 为 正交矩阵 和 对称矩阵
(正交阵:  H^-1 = H^T,   对称矩阵: H^T = H^-1)

![](image/Pasted%20image%2020260410212432.png)

## 2.1 例题

给出 Ax=b A 为实对称阵

1 用 正交对称矩阵H 将  A化为3对角矩阵 
2 用追赶方法求解 




## 2.2 例题

![](image/Pasted%20image%2020260410212722.png)


步骤一 算 H_1 wave
![](image/Pasted%20image%2020260410213124.png)

步骤2 算 H1

![](image/Pasted%20image%2020260410211843.png)



![](image/Pasted%20image%2020260410213205.png)


---

步骤三 

算 H_1 A H_1
![](image/Pasted%20image%2020260410213855.png)

![](image/Pasted%20image%2020260410213955.png)


A1 = H1_welle A1_welle H1_welle 
A1_welle 为  A的 有下角的一块
![](image/Pasted%20image%2020260410212029.png)



# 3 对一般的实矩阵的Hessenberg阵

a_11 同一行中 的元素  和 a_11 同一列的元素 不是对称的

![](image/Pasted%20image%2020260410214543.png)


## 3.1 结论 



![](image/Pasted%20image%2020260410215311.png)

HAH 这个矩阵为 上 hesseberg 矩阵 
