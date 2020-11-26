# 02随机抽样
numpy.random 模块对 Python 内置的 random 进行了补充，增加了一些用于高效生成多种概率分<br />布的样本值的函数，如正态分布、泊松分布等。

- numpy.random.seed(seed=None) 


## 离散型随机变量
### 二项分布
$$P\{X=k\} = C_n^kp^k(1-p)^{n-k}$$

- numpy.random.binomial(n, p, size=None) Draw samples from a binomial distribution.

表示对一个二项分布进行采样， size 表示采样的次数也即n次伯努利实验进行的次数， n 表示做了 n 重伯努利试验， p 表示成功的<br />概率，函数的返回值表示 n 中成功的次数。

### 泊松分布
泊松分布主要用于估计某个时间段某事件发生的概率<br />$$P\{X=k\} = \frac{\lambda^k}{k!}e^{-\lambda}$$

- numpy.random.poisson(lam=1.0, size=None) Draw samples from a Poisson distribution.

表示对一个泊松分布进行采样， size 表示采样的次数， lam 表示一个单位内发生事件的平均值，函<br />数的返回值表示一个单位内事件发生的次数

### 超几何分布
假设有限总体包含N个样本，其中质量合格的为m个，则剩余的N-m个为不合格样本，如果从该有限总体中抽取出n个样本，其中有k个是质量合格的概率为：<br />$$P(k,m,n,N) = \frac{C_m^k C_{N-m}^{n-k}}{C_N^n}$$

- numpy.random.hypergeometric(ngood, nbad, nsample, size=None) Draw samples from a<br />Hypergeometric distribution.

表示对一个超几何分布进行采样， size 表示采样的次数， ngood 表示总体中具有成功标志的元素个数， nbad 表示总体中不具有成功标志的元素个数， ngood+nbad 表示总体样本容量， nsample 表示抽取元素的次数（小于或等于总体样本容量），函数的返回值表示抽取 nsample 个元素中具有成功标识的元素个数。

## 连续型随机变量

### 均匀分布

- numpy.random.uniform(low=0.0, high=1.0, size=None) Draw samples from a uniform distribution

### 正态分布

- numpy.random.randn(d0, d1, ..., dn) Return a sample (or samples) from the "standard normal" distribution.
- numpy.random.normal(loc=0.0, scale=1.0, size=None) Draw random samples from a normal (Gaussian) distribution,创建均值为 loc（mu），标准差为 scale（sigma），大小为 size 的数组

### 指数分布
指数分布描述时间发生的时间长度间隔.<br />$$f(x)=\begin{cases}
\lambda e^{-\lambda x},  & \text{x$>0$}\\
0, & \text{x $\le$ 0}
\end{cases}$$

- numpy.random.exponential(scale=1.0, size=None) Draw samples from an exponential distribution, scale = 1/lambda

## 其他随机函数
### 随机从序列中获取元素

- numpy.random.choice(a, size=None, replace=True, p=None) Generates a random sample from a given 1-D array.

从序列中获取元素，若 a 为整数，元素取值从 np.range(a) 中随机获取；若 a 为数组，取值从 a 数组元素中随机获取。该函数还可以控制生成数组中的元素是否重复 replace ，以及选取元素的概率 p 。
### 对数据集进行洗牌操作

- numpy.random.shuffle(x)  对 x 进行重排序，如果 x 为多维数组，只沿第 0 轴洗牌，改变原来的数组，输出为None
- numpy.random.permutation(x) Randomly permute a sequence, or return a permuted range.  permutation() 函数的作用与 shuffle() 函数相同，可以打乱第0轴的数据，但是它不会改变原来的数组。
# 参考

- [np.random.binomial()](https://blog.csdn.net/m0_37393514/article/details/81838308)