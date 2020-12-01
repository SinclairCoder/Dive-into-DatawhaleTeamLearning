# 04 线性代数
## 矩阵乘积

- numpy.dot(a, b[, out]) 计算两个矩阵的乘积，如果是一维数组则是它们的内积 ；

## 特征值特征向量

- a,b= numpy.linalg.eig(a) 计算方阵的特征值和特征向量,a为特征值，b为特征向量；
- numpy.linalg.eigvals(a) 计算方阵的特征值；

## 奇异值分解

- u, s, v = numpy.linalg.svd(a, full_matrices=True, compute_uv=True, hermitian=False) **奇异值分解 **
   - a 是一个形如(M,N)矩阵
   - full_matrices 的取值是为False或者True，默认值为True，这时 u 的大小为(M,M)， v 的大小为(N,N)。否则 u 的大小为(M,K)， v 的大小为(K,N) ，K=min(M,N)；
   - compute_uv 的取值是为False或者True，默认值为True，表示计算 u,s,v 。为False的时候只计算 s ；
   - 总共有三个返回值 u,s,v ， u 大小为(M,M)， s 大小为(M,N)， v 大小为(N,N)， a = u*s*v ；
   - 其中 s 是对矩阵 a 的奇异值分解。 s 除了对角元素不为 0 ，其他元素都为 0 ，并且对角元素从大到小排列。 s 中有 n 个奇异值，一般排在后面的比较接近0，所以仅保留比较大的 r个奇异值。
   
## QR分解

- q,r = numpy.linalg.qr(a, mode='reduced') 计算矩阵 a 的QR分解。
   - a 是一个(M, N)的待分解矩阵
   - mode = reduced ：返回(M, N)的列向量两两正交的矩阵 q ，和(N, N)的三角阵r （Reduced QR分解）。
   - mode = complete ：返回(M, M)的正交矩阵 q ，和(M, N)的三角阵 r （Full QR分解）。
   
## Cholesky分解

- L = numpy.linalg.cholesky(a) 返回正定矩阵 a 的 Cholesky 分解 a = L*L.T ，其中 L 是下三角。

## 范数

- numpy.linalg.norm(x, ord=None, axis=None, keepdims=False) 计算向量或者矩阵的范数。

- ![image.png](https://cdn.nlark.com/yuque/0/2020/png/1184496/1606812184944-135e7e08-9963-44d5-829a-014354762081.png#align=left&display=inline&height=196&margin=%5Bobject%20Object%5D&name=image.png&originHeight=391&originWidth=836&size=103195&status=done&style=none&width=418)

## 方阵的行列式

- numpy.linalg.det(a)  计算行列式

## 矩阵的秩

- numpy.linalg.matrix_rank(M, tol=None, hermitian=False)  返回矩阵的秩

## 矩阵的迹

- numpy.trace(a, offset=0, axis1=0, axis2=1, dtype=None, out=None) 方阵的迹就是主对角元素之和；

## 矩阵的逆

- numpy.linalg.inv(a) 计算矩阵 a 的逆矩阵（矩阵可逆的充要条件： det(a) != 0 ，或者 a 满秩）；

## 求解线性方程组

- numpy.linalg.solve(a, b) 求解线性方程组或矩阵方程；