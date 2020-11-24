# 01输入输出
## numpy二进制文件

- numpy.save(file, arr, allow_pickle=True, fix_imports=True)  将数组arr保存到file文件中，文件格式为.npy二进制文件,默认情况下，数组是以未压缩的原始二进制格式保存在扩展名为 .npy 的文件中。以二进制的方式存储文件，在二进制文件第一行以文本形式保存了数据的元信息（ndim，dtype，shape等），可以用二进制工具查看内容。
- numpy.savez(file, *args, **kwds)  将几个数组保存到文件file中，默认情况下，数组是以未压缩的原始二进制格式保存在扩展名为 .npz 的文件中。输出的是一个压缩文件（扩展名为npz），其中每个文件都是一个 save() 保存的npy文件，文件名对应于数组名。 load() 自动识别npz文件，并且返回一个类似于字典的对象，可以通过数组名作为关键字获取数组的内容。可以给数组起名字，默认的话会自动起名为 arr_0, arr_1, …　

## 文本文件
savetxt() ， loadtxt() 和 genfromtxt() 函数用来存储和读取文本文件（如TXT，CSV等）。genfromtxt() 比 loadtxt() 更加强大，可对缺失数据进行处理。

- np.savetxt(fname, X, fmt='%.18e', delimiter=' ', newline='\n', header='', footer='', comments='# ', encoding=None) 将数组保存到文件中
   - fname：文件路径
   - X：存入文件的数组
   - fmt：写入文件中每个元素的字符串格式，默认'%.18e'（保留18位小数的浮点数形式）
   - delimiter：分割字符串，默认以空格分隔
- np.loadtxt(fname, dtype=float, comments='#', delimiter=None, converters=None,<br />skiprows=0, usecols=None, unpack=False, ndmin=0, encoding='bytes', max_rows=None) 从文本文件中加载数据
   - fname：文件路径。
   - dtype：数据类型，默认为float。
   - comments: 字符串或字符串组成的列表，默认为# ， 表示注释字符集开始的标志。
   - skiprows：跳过多少行，一般跳过第一行表头。
   - usecols：元组（元组内数据为列的数值索引）， 用来指定要读取数据的列（第一列为0）。
   - unpack：当加载多列数据时是否需要将数据列进行解耦赋值给不同的变量。
- genfromtxt() 是面向结构数组和缺失数据处理的

## 文本格式选项

- numpy.set_printoptions(precision=None,threshold=None, edgeitems=None,linewidth=None,<br />suppress=None, nanstr=None, infstr=None,formatter=None, sign=None, floatmode=None,<br />**kwarg) 设置打印选项
   - precision ：设置浮点精度，控制输出的小数点个数，默认是8。
   - threshold ：概略显示，超过该值则以“…”的形式来表示，默认是1000。
   - linewidth ：用于确定每行多少字符数后插入换行符，默认为75。
   - suppress ：当 suppress=True ，表示小数不需要以科学计数法的形式输出，默认是False。
   - nanstr ：浮点非数字的字符串表示形式，默认 nan 。
   - infstr ：浮点无穷大的字符串表示形式，默认 inf 。



