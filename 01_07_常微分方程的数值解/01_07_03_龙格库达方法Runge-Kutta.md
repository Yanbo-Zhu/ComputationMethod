

![](image/Pasted%20image%2020260319180640.png)


可c 的值 无法找到, 我们就找 y(可c) , 或者 f(可c)
 f 为 y的导数 


k* 取左端点的导数 为 y(x_n+1) - y (n) =  h x f( x_n, y_n) , 为 显式欧拉公式 
k* 取右端点的导数 为 y(x_n+1) - y (n) =  h x f( x_n+1, y_n+1) , 为 隐式欧拉公式  


![](image/Pasted%20image%2020260322114602.png)



# 1 总结 


![](image/Pasted%20image%2020260606155243.png)

![](image/Pasted%20image%2020260606155254.png)


![](image/Pasted%20image%2020260606155310.png)


![](image/Pasted%20image%2020260606155322.png)


![](image/Pasted%20image%2020260606155355.png)


# 2 二阶 Runge-Kutta 龙格库达方法


## 2.1 
在一个区间中 多取几个点 , 把这几个点上的斜率 取平均值 , 从而提高精度   , ==使得 局部截断误差的进度最高(解释 误差阶数达到最大)==
如何找合适的点?   



![](image/Pasted%20image%2020260319180705.png)


![](image/Pasted%20image%2020260322115046.png)

----

 1  注意 下面应该为  lambd_2 x p  =  1/2   而不是  lambd_1  x p  = 1/2  
![](image/Pasted%20image%2020260322115147.png)



![](image/Pasted%20image%2020260322115627.png)



2 
![](image/Pasted%20image%2020260322115736.png)

关于  x的全导数
![](image/Pasted%20image%2020260322120055.png)


![](image/Pasted%20image%2020260322120240.png)




3  
带入 K2

带入 
下面应该为  lambd_2 x p  =  1/2   而不是  lambd_1  x p  = 1/2  
![](image/Pasted%20image%2020260322120614.png)

得到 
![](image/Pasted%20image%2020260322120516.png)



要使得具有最高的精度
p lamdba_2   =  1/2,  则 此时 阶段误差 为 O(H^3 ) . 这时候 方法的  阶数为二阶

故称为 二阶  runge-kutta 方法

## 2.2 几个具体二阶 Runge-kutta 方法



1  
最后结果为 改进的欧拉公式 

![](image/Pasted%20image%2020260322120857.png)


----

2 
![](image/Pasted%20image%2020260322121026.png)



# 3 三阶龙格库达方法  , 要选取三个点  x_n, x_n+p,  x_n+q

![](image/Pasted%20image%2020260322121313.png)



# 4 四阶龙格库达方法

按道理我们要用到四个点
但实际只用到了三个点, 没有用到四个点
x_n+1/2  用到了两次,, 用到的斜率不一样 



![](image/Pasted%20image%2020260322124826.png)


类似的, simpson公式
![](image/Pasted%20image%2020260314175937.png)














