# 03统计相关

- np.amin(a[, axis=None, out=None, keepdims=np._NoValue, initial=np._NoValue, where=np._NoValue])  如果不指定axis的话，就是返回**最小值**；axis=0，取每列的**最小值**然后返回；axis=1，取每行的**最小值**然后返回；
- np.amax(a[, axis=None, out=None, keepdims=np._NoValue, initial=np._NoValue, where=np._NoValue])  如果不指定axis的话，就是返回**最大值**；axis=0，取每列的**最大值**然后返回；axis=1，取每行的**最大值**然后返回；
- np.ptp(a, axis=None, out=None, keepdims=np._NoValue)   如果不指定axis的话，就是返回**极差**；axis=0，取每列的**极差**然后返回；axis=1，取每行的**极差**然后返回；
- numpy.percentile(a, q, axis=None, out=None, overwrite_input=False,interpolation='linear',keepdims=False)   如果不指定axis的话，就是返回**百分位q数**；axis=0，取每列的**百分位q数**然后返回；axis=1，取每行的**百分位q数**然后返回；

    注：百分位数是统计中使用的度量，表示小于这个值的观察值占总数q的百分比。

- numpy.median(a, axis=None, out=None, overwrite_input=False, keepdims=False) 如果不指定axis的话，就是返回**中位数**；axis=0，取每列的**中位数**然后返回；axis=1，取每行的**中位数**然后返回；
- numpy.mean(a[, axis=None, dtype=None, out=None, keepdims=np._NoValue)]) 如果不指定axis的话，就是返回**平均数**；axis=0，取每列的**平均数**然后返回；axis=1，取每行的**平均数**然后返回；
- numpy.average(a[, axis=None, weights=None, returned=False])  如果不指定weights的话，就是计算平均数，否则是计算加权平均数，如果不指定axis的话，就是返回**加权平均数**；axis=0，取每列的**加权****平均数**然后返回；axis=1，取每行的**加权****平均数**然后返回；
- numpy.var(a[, axis=None, dtype=None, out=None, ddof=0, keepdims=np._NoValue]) 如果不指定axis的话，就是返回**方差**；axis=0，取每列的**方差**然后返回；axis=1，取每行的**方差**然后返回；

    ddof=0：是“Delta Degrees of Freedom”，表示自由度的个数 ，关于自由度可以参考：[如何理解统计学中「自由度」这个概念？](https://www.zhihu.com/question/20983193)

- numpy.std(a[, axis=None, dtype=None, out=None, ddof=0, keepdims=np._NoValue])   计算标准差，基本同方差
- numpy.cov(m, y=None, rowvar=True, bias=False, ddof=None, fweights=None,aweights=None)  计算**协方差**



$$cov(X,Y) = E((X-E(x))*(Y-E(Y)))=E(XY)-E(X)E(Y)$$<br />  $$cov(X,Y) = \frac{\sum_{i=1}^n(X_i-\bar X)(Y_i-\bar Y)}{n-1}$$

- numpy.corrcoef(x, y=None, rowvar=True, bias=np._NoValue, ddof=np._NoValue)  计算相关系数，协方差描述的是两个向量协同变化的程度，它的取值可能非常大，也可能非常小，这就导致没法直观地衡量二者协同变化的程度。相关系数实际上是正则化的协方差， n 个变量的相关系数形成一个 n 维方阵


<br />$$\rho  = \frac {cov(X,Y)}{\sqrt{D(X)} \sqrt{
D(Y)}}$$

- numpy.digitize(x, bins, right=False)    返回每个值属于的bins的index
   - x：numpy数组
   - bins 一维单调数组，必须是升序或者降序
   - right：间隔是否包含最右，也就是区间是不是右闭区间的
   - 返回值：x在bins中的位置


<br />





