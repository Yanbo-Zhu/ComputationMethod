




# 1 插值型的求积公式 

![](image/Pasted%20image%2020260314174040.png)


# 2 Newton-Costes公式 （等距节点下的插值型求积公式）


![](image/Pasted%20image%2020260314174228.png)



----
求证 所有的c_k 加起来为1

 因为拉格朗日基函数之和 恒为1 
![](image/Pasted%20image%2020260210190812.png)


所以 所有的c_k 加起来恒为 1
![](image/Pasted%20image%2020260314175156.png)


# 3 常用的低阶Newton-Cotes 公式

![](image/Pasted%20image%2020260314175423.png)


## 3.1 n=1   ， 只考虑有两个已知点， 每个配有一个Cotes系数 ， f(x)的求积公式为梯形公式 

这时候 就是只有 i= 0， 1 两个点，  就只有两个 cotes 系数 
又根据 
![](image/Pasted%20image%2020260314175557.png)
得到 c0 = c1
c0+ c1 应该为 1
得到 c0=c1 = 1/2


![](image/Pasted%20image%2020260314175922.png)


![](image/Pasted%20image%2020260314175912.png)



## 3.2 n=2 抛物线公式Simpson公式， 考虑有三个已知点 


![](image/Pasted%20image%2020260314175937.png)



![](image/Pasted%20image%2020260314182203.png)



## 3.3 n=4  Cotes 公式 ， 考虑有5个已知点  

 
![](image/Pasted%20image%2020260314182341.png)




# 4 对于 具有n个节点的Newton-Cotes公式， 如果n为偶数， 则相应公式的代数精度为n+1;  如果n为基数， 则求积公式的代数精度为n 
![](image/Pasted%20image%2020260314182538.png)


证明一下子

n=1, 梯形公式 代数精度为1
![](image/Pasted%20image%2020260314183647.png)



n=2， Simpson 公式, 代数精度为3 
![](image/Pasted%20image%2020260314183753.png)

![](image/Pasted%20image%2020260314183841.png)


# 5 误差公式

![](image/Pasted%20image%2020260314190603.png)


## 5.1 梯形公式的余项

![](image/Pasted%20image%2020260314190701.png)


==两行之间根据拉格朗日余项公式来变换的==
![](image/Pasted%20image%2020260314190802.png)


![](image/Pasted%20image%2020260314190838.png)


和 函数的二阶导数有关 ， 他越光滑， 二阶导数值越小 
和 a,b 区间大小有关




## 5.2 Simpson 公式的余项

![](image/Pasted%20image%2020260314190958.png)

和 函数的5阶导数有关 ， 他越光滑， 5阶导数值越小 
和 a,b 区间大小有关
Simpson 公式的余项 比 梯形公式要小很多 



==两行之间根据拉格朗日余项公式来变换的==
![](image/Pasted%20image%2020260314191257.png)

---

换一种方法， 用 三次 hermite插值公式的余项
![](image/Pasted%20image%2020260314191529.png)



![](image/Pasted%20image%2020260314191614.png)


H3(x)  为 三次 hermite插值公式， 他的最高次项为x的三次方
因为  他的最高次项为x的三次方 n=2 ， 所以 可以用 Simpson求积公式 的值 完全等于 H3(x) 在 ab 区间上的求积后的值 
![](image/Pasted%20image%2020260314192044.png)

可以看到  H3(x) 在 ab 区间上的求积后的值  就是为  n=2 Simpson求积公式 的值

---
则 这两者相减为 误差值
![](image/Pasted%20image%2020260314201018.png)

![](image/Pasted%20image%2020260314201027.png)
 

![](image/Pasted%20image%2020260314201052.png)


# 6 例子 


![](image/Pasted%20image%2020260314202837.png)

---

![](image/Pasted%20image%2020260314203030.png)


---

![](image/Pasted%20image%2020260314203228.png)


![](image/Pasted%20image%2020260314203423.png)






