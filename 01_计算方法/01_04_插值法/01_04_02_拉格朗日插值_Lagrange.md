


# 1 拉格朗日插值的缺点
拉格朗日插值的缺点
如果新增一个节点，  那所有的基函数都要重新计算 


牛顿多项式插值的优点
增加一个节点， 之前的计算结果  还能用上 

# 2 内插interpolation 和外插 extrapolation

点不包含在 两个 x 值内 就是外插
一般内插的精度 高于 外插的精度 

`[a,b]` 的长度越小， 误差越小 

# 3 线性插值 

![](image/Pasted%20image%2020260209205300.png)




# 4 抛物线插值


![](image/Pasted%20image%2020260209205955.png)


 ![](image/Pasted%20image%2020260209210147.png)

![](image/Pasted%20image%2020260209210213.png) 

---


![](image/Pasted%20image%2020260209210345.png)


# 5 n次拉格朗日插值多项式

![](image/Pasted%20image%2020260209210613.png)



 ![](image/Pasted%20image%2020260209211834.png)

![](image/Pasted%20image%2020260209211928.png)



# 6 拉格朗日插值基函数


![](image/Pasted%20image%2020260209212418.png)


选择的基函数不同， 则空间不同 ， 空间中的每一项的为基函数


# 7 例子


![](image/Pasted%20image%2020260209215619.png)


![](image/Pasted%20image%2020260209215645.png)


# 8 误差 

## 8.1 截断误差：插值余项以及估计


插值余项属于截断误差 （由于算法的引入导致的误差）： 算法的解 - 真实值

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

### 8.1.1 总结



![](image/Pasted%20image%2020260210191219.png)

![](image/Pasted%20image%2020260210191316.png)

![](image/Pasted%20image%2020260210191325.png)


## 8.2 插值方法的绝对误差：插值余项的最大值


![](image/Pasted%20image%2020260210173442.png)


![](image/Pasted%20image%2020260210173546.png)



---

立体

C^2 表示其2阶倒数在`[a,b]` 上连续

![](image/Pasted%20image%2020260210174053.png)


f(a) + xxxx  这一长串， 是 经过 两个点的直线方程 （一阶lagrange 方程 ）   
fx 减这一长串  就是 插值方程的余项
![](image/Pasted%20image%2020260210174247.png)

![](image/Pasted%20image%2020260210174624.png)




# 9 例子


## 9.1 

![](image/Pasted%20image%2020260210120144.png)


## 9.2 


![](image/Pasted%20image%2020260210131754.png)


![](image/Pasted%20image%2020260210154846.png)


# 10 结论

![](image/Pasted%20image%2020260210174935.png)


## 10.1 

f 的 n+1 阶导数一定为0， 因为 x最多是 with power to k 
这样 能够推得 fx 恒等于 L_n(x)

![](image/Pasted%20image%2020260210180054.png)

比说 f(x) = x^4 + 2x+ 1, 然后给你五个节点， 然后得到的拉个朗日插值公式 有x^ 5 , 则这个 拉个朗日插值公式 一定等于 f(x)

![](image/Pasted%20image%2020260210180312.png)


## 10.2 



基函数 的性质 
复合一定的条件， 拉格朗日基函数之和等于1 

![](image/Pasted%20image%2020260210190812.png)


## 10.3 拉格朗日插值公式的缺点

一旦考虑的节点变多， 基函数的公式都变掉了。 就是说之前的基函数对后面的基函数的计算 毫无帮助 

![](image/Pasted%20image%2020260210191353.png)

  
![](image/Pasted%20image%2020260210191345.png)


