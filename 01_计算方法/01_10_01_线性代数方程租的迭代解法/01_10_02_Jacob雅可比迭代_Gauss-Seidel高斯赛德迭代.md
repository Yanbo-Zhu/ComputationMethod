

# 1 雅可比迭代Jacob 

![](image/Pasted%20image%2020260408161158.png)

![](image/Pasted%20image%2020260408141823.png)


![](image/Pasted%20image%2020260408141929.png)



## 1.1 迭代公式中的矩阵J的分量表达形式 

![](image/Pasted%20image%2020260408142026.png)


![](image/Pasted%20image%2020260408142059.png)



![](image/Pasted%20image%2020260408142418.png)


![](image/Pasted%20image%2020260408161242.png)


## 1.2 Jacob迭代的收敛条件 


![](image/Pasted%20image%2020260408142238.png)

![](image/Pasted%20image%2020260408161345.png)

---

## 1.3 A为严格对角占优矩阵, 则Jacob迭代一定收敛 

![](image/Pasted%20image%2020260408144042.png)


![](image/Pasted%20image%2020260408144121.png)


## 1.4 例子 


![](image/Pasted%20image%2020260408142738.png)


![](image/Pasted%20image%2020260408142825.png)



# 2 Gauss-Seidel高斯赛德迭代

## 2.1 从jokob迭代进化到Gauss-Seidel高斯赛德迭代

![](image/Pasted%20image%2020260408161740.png)

因为从第一个式子已经啊知道了 x_1 的k+1 次迭代的值, 那么  在第二个式子中 用 a_21 乘上  x_1 ^ k+1, 而不用 乘上 x_1 ^k 的迭代值了 


![](image/Pasted%20image%2020260408162043.png)


---

得到综合的心得迭代公式 
列数 小于j 用 k+1 次 迭代的值,  大于j , 用第k次迭代的值 

![](image/Pasted%20image%2020260408162145.png)



## 2.2 Gauss-Seidel高斯赛德迭代公式

L 为 负的下三角矩阵,   U为正的上三角矩阵 

![](image/Pasted%20image%2020260408161158.png)

---


![](image/Pasted%20image%2020260408162145.png)


(A) x = b,   A =  D-L-U
得到 
![](image/Pasted%20image%2020260408162435.png)


![](image/Pasted%20image%2020260408162600.png)



## 2.3 收敛的条件 



![](image/Pasted%20image%2020260408173913.png)


# 3 两种收敛方式的比较 


Gauss-Seidel高斯赛德迭代 和 雅可比迭代Jacob  的收敛速度之间没有任何联系 
Gauss-Seidel高斯赛德迭代 和 雅可比迭代Jacob  的收敛性 之间没有任何联系 

当 Gauss-Seidel高斯赛德迭代 和 雅可比迭代Jacob  的收敛, 那么 Gauss-Seidel高斯赛德迭代 和 雅可比迭代Jacob  的收敛速度的两倍 

# 4 例题 

## 4.1 ##

![](image/Pasted%20image%2020260408174140.png)

1 
![](image/Pasted%20image%2020260408174153.png)

2   雅可比迭代 

2.1 
![](image/Pasted%20image%2020260408174211.png)

2.2 
![](image/Pasted%20image%2020260408174231.png)

![](image/Pasted%20image%2020260408174326.png)


---

高斯赛德迭代 


分量的形式 
![](image/Pasted%20image%2020260408174412.png)


![](image/Pasted%20image%2020260408174420.png)


或者  用这种方式写
![](image/Pasted%20image%2020260408174434.png)



谱半径 

![](image/Pasted%20image%2020260408174501.png)


![](image/Pasted%20image%2020260408174538.png)


## 4.2 


![](image/Pasted%20image%2020260408175252.png)


1 雅可比迭代
![](image/Pasted%20image%2020260408175520.png)

![](image/Pasted%20image%2020260408175536.png)


![](image/Pasted%20image%2020260408180016.png)


什么情况下速度最快 

谱半径    必须小于1 大于0 

![](image/Pasted%20image%2020260408180134.png)



----


2 高斯迭代


![](image/Pasted%20image%2020260407180727.png)


---

A为严格对角占优的时候, 两种 迭代都收敛 
得到的  a 值 的区间更小. 说明 "A为严格对角占优的时候, 两种 迭代都收敛 "  约束更强 
![](image/Pasted%20image%2020260408180330.png)


---

