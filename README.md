单变量线性回归是机器学习中最基础简单也是最重要的问题，解决此问题主要有两种常见方法。一是基于梯度下降算法的机器学习方法，一是直接基于矩阵求解的正规方程解法。
  
#### 1.基于梯度下降算法的机器学习方法：
  
  - **模型:**_单变量线性函数_<p align="center"><img src="https://latex.codecogs.com/gif.latex?h_&#x5C;theta%20=%20&#x5C;theta_0%20+%20&#x5C;theta_1x"/></p>  
  
  - **策略:** _最小二乘法_<p align="center"><img src="https://latex.codecogs.com/gif.latex?J(&#x5C;theta_0,&#x5C;theta_1)%20=%20&#x5C;frac{1}{2m}&#x5C;displaystyle&#x5C;sum_{i=1}^m(h_&#x5C;theta(x^i)%20-%20y^i)^2"/></p>  
  
  <p align="center"><img src="https://latex.codecogs.com/gif.latex?minimizeJ(&#x5C;theta_0,&#x5C;theta_1)"/></p>  
  
  - **算法:** _随机梯度下降(SGD)_
　　　<p align="center"><img src="https://latex.codecogs.com/gif.latex?repeat　until　convergence&#x5C;{
%20%20%20%20&#x5C;theta_j%20:=%20&#x5C;theta_j%20-%20&#x5C;alpha&#x5C;frac{&#x5C;partial}{&#x5C;partial&#x5C;theta_j}J(&#x5C;theta_0,&#x5C;theta_1)　　for%20(j%20=%200　and　j%20=%201)%20
%20%20%20%20&#x5C;}"/></p>  
  
  
#### 2.正规方程：
  
<p align="center"><img src="https://latex.codecogs.com/gif.latex?h_&#x5C;theta(x)%20=%20&#x5C;theta^TX"/></p>  
  
<p align="center"><img src="https://latex.codecogs.com/gif.latex?&#x5C;theta%20=%20(X^TX)^{-1}X^Ty"/></p>  
  
  
  
#### 3.梯度下降与正规方程的比较：
  
梯度下降 | 正规方程
------------ | -------------
需要选择学习率 | 不需要
需要进行多次迭代 | 一次矩阵运算得出
当特征数量n大时也能较好适用 | 需要计算(X^T^ X)^-1^,如果特征数量较大则运算代价大，因为矩阵逆运算的时间复杂度为O(n^3^),通常来说，当n小于10000时，还是可以接受的。
适用于各种类型的模型 | 只适用于线性模型 
  
