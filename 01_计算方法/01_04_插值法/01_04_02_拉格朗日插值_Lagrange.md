

# 1 内插interpolation 和外插 extrapolation

点不包含在 两个 x 值内 就是外插
一般内插的精度 高于 外插的精度 



# 2 线性插值 

![](image/Pasted%20image%2020260209205300.png)




# 3 抛物线插值


![](image/Pasted%20image%2020260209205955.png)


 ![](image/Pasted%20image%2020260209210147.png)

![](image/Pasted%20image%2020260209210213.png) 

---


![](image/Pasted%20image%2020260209210345.png)


# 4 n次拉格朗日插值多项式

![](image/Pasted%20image%2020260209210613.png)



 ![](image/Pasted%20image%2020260209211834.png)

![](image/Pasted%20image%2020260209211928.png)



# 5 拉格朗日插值基函数


![](image/Pasted%20image%2020260209212418.png)


选择的基函数不同， 则空间不同 ， 空间中的每一项的为基函数


# 6 例子


![](image/Pasted%20image%2020260209215619.png)


![](image/Pasted%20image%2020260209215645.png)


# 7 误差 : 插值余项以及估计

属于截断误差 （由于算法的引入）： 算法的解 - 真实值

余项 R_n(x) = f(x) - L_n(x) 为插值的截断误差

![](image/Pasted%20image%2020260209220139.png)

1  插值在节点上不存在误差 （因为 求出来的公式就是根据节点算出来的）
2 x_i 为 R_n(x) 的零点， 因此 可以设 R_n(x) = (x-x_0)(x-x_1)(x-x_n)
3 设 w_(n+1) (x) = (x-x0)(x-x1)(x-xn) 的次数不超过 n+1次多项式 
![](image/Pasted%20image%2020260209220502.png)


==注意辅助函数中 phi， f, L_n 中为 t,。  k 和 w 中为x ==
![](image/Pasted%20image%2020260209220838.png)


 ---

![](image/Pasted%20image%2020260209221430.png)
为什么都等于零

因为 x0, x1, xn都是节点 
因为 f(x0) - Ln(x0) =0  因为在节点上，真实值 f(x0)  和拉格朗日插值公式求出来的值 Ln(x0)  肯定相等 

k(x)w_n+1(t):   w_(n+1) (x) = (x-x0)(x-x1)(x-xn) ,在 x=x0 时候   w_(n+1) (x)  肯定等于0


---

phi(x) 也恒等于零 
![](image/Pasted%20image%2020260209221901.png)


---

这样的话 我们就有 n+2 个点上  我们都有 phi(x) 等于0 

---

鲁尔定理：  当两个函数的值相等的时候， 至少存在一点， 他的导数值为0， 条件是他是连续函数 

![](image/Pasted%20image%2020260209222239.png)
这样我们可以推导得出， 当有 n+2 个点上  我们都有函数 ) 等于0 ， 那他至少存在一点， 使得他的函数的 n-1阶的导数为0


![](image/Pasted%20image%2020260209222319.png)


---

Phi 函数的对t求导，
Ln(t) 的最高项是 x的n次方， Ln(t)  对 t 进行 n+1 次求导 得到 为0 
w_n+1(t) 的最高项是 x的n+1次方， Ln(t)  对 t 进行 n+1 次求导 得到 为(n+1)!

==注意辅助函数中 phi， f, L_n 中为 t,。  k 和 w 中为x ==
![](image/Pasted%20image%2020260209222427.png)


![](image/Pasted%20image%2020260209223302.png)


从而得到误差 
==注意辅助函数中 phi， f, L_n 中为 t,。  k 和 w 中为x ==
![](image/Pasted%20image%2020260209223349.png)

![](image/Pasted%20image%2020260209223401.png)

![](image/Pasted%20image%2020260209223446.png) 
这个为 x0, x1, xn 中的某一个 x值， 不知道那个x值， 但是和这个x 值一定存在 使得

![](image/Pasted%20image%2020260209223551.png)


# 8 例子


## 8.1 

![](image/Pasted%20image%2020260210120144.png)


## 8.2 


![](image/Pasted%20image%2020260210131754.png)


![](image/Pasted%20image%2020260210154846.png)




