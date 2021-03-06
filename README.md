单变量线性回归是机器学习中最基础简单也是最重要的问题，解决此问题主要有两种常见方法。一是基于梯度下降算法的机器学习方法，一是直接基于矩阵求解的正规方程解法。

####1.基于梯度下降算法的机器学习方法：
  - **模型:**_单变量线性函数_$h_\theta = \theta_0 + \theta_1x$
  - **策略:** _最小二乘法_$J(\theta_0,\theta_1) = \frac{1}{2m}\displaystyle\sum_{i=1}^m(h_\theta(x^i) - y^i)^2$ 
  $minimizeJ(\theta_0,\theta_1) $
  - **算法:** _随机梯度下降(SGD)_
 $repeat　until　convergence\{\newline
           　　\theta_j := \theta_j - \alpha\frac{\partial}{\partial\theta_j}J(\theta_0,\theta_1)　for (j = 0　and　j = 1) 
    \newline\}$

####2.正规方程：
$h_\theta(x) = \theta^TX$
$ \theta = (X^TX)^{-1}X^Ty$


####3.梯度下降与正规方程的比较：
梯度下降 | 正规方程
------------ | -------------
需要选择学习率 | 不需要
需要进行多次迭代 | 一次矩阵运算得出
当特征数量n大时也能较好适用 | 需要计算(X^T^ X)^-1^,如果特征数量较大则运算代价大，因为矩阵逆运算的时间复杂度为O(n^3^),通常来说，当n小于10000时，还是可以接受的。
适用于各种类型的模型 | 只适用于线性模型 
