本次练习使用 鸢尾属植物数据集iris，在这个数据集中，包括了三类不同的鸢尾属植物：  Iris Setosa，Iris Versicolour，Iris Virginica。 

每类收集了50个样本，因此这个数据集一共包含了150个样本，以下四个特征的单位都是厘米（cm）。
- sepallength：萼片长度
- sepalwidth：萼片宽度
- petallength：花瓣长度
- petalwidth：花瓣宽度

完成以下任务：

- 1. 导入鸢尾属植物数据集
- 2. 求出鸢尾属植物萼片长度的平均值、中位数和标准差（第1列，sepallength）

- 3. 创建一种标准化形式的鸢尾属植物萼片长度，其值正好介于0和1之间，这样最小值为0，最大值为1（第1列，sepallength）

- 4. 找到鸢尾属植物萼片长度的第5和第95百分位数（第1列，sepallength）

- 5. 把iris_data数据集中的20个随机位置修改为np.nan值

- 6. 在iris_data的sepallength中查找缺失值的个数和位置（第1列）

- 7. 筛选具有 sepallength（第1列）< 5.0 并且 petallength（第3列）> 1.5 的 iris_data行

- 8. 选择没有任何 nan 值的 iris_data行

- 9. 计算 iris_data 中sepalLength（第1列）和petalLength（第3列）之间的相关系数。

- 10. 找出iris_data是否有任何缺失值

- 11. 在numpy数组中将所有出现的nan替换为0

- 12. 找出鸢尾属植物物种中的唯一值和唯一值出现的数量

- 13. 将 iris_data 的花瓣长度（第3列）以形成分类变量的形式显示。定义：Less than 3 --> 'small'；3-5 --> 'medium'；'>=5 --> 'large'

- 14. 在 iris_data 中创建一个新列，其中 volume 是 (pi x petallength x sepallength ^ 2）/ 3 。

- 15. 随机抽鸢尾属植物的种类，使得Iris-setosa的数量是Iris-versicolor和Iris-virginica数量的两倍

- 16. 根据 sepallength 列对数据集进行排序

- 17. 在鸢尾属植物数据集中找到最常见的花瓣长度值（第3列）

- 18. 在鸢尾花数据集的 petalwidth（第4列）中查找第一次出现的值大于1.0的位置

