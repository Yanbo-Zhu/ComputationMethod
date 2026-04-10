

# 1 Householder阵 H

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


## 1.3 定理 
ab 为两个 等长的非0向量 
![](image/Pasted%20image%2020260410012430.png)

![](image/Pasted%20image%2020260410170044.png)

u 为单位矩阵 
![](image/Pasted%20image%2020260410012628.png)


![](image/Pasted%20image%2020260410011628.png)


## 1.4 推论

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


