# RS

igraph作为图计算和社交分析的常用包，在使用Python进行高级数据分析中是大家经常使用到的。

但很多初学者在安装igraph时由于错误的安装方式，导致在Python中加载igraph包(from igraph import *)出现igraph包重复，请升级jgraph的错误信息。

报错信息如下：

“DeprecationWarning: To avoid name collision with the igraph project, this visualization library has been renamed to 'jgraph'. Please upgrade when convenient.”

报错原因分析：

\ \ \ \ 通过pip list发现Python安装的有igraph包有两个：igraph、python-igraph，导致加载igraph包时候系统无法判断加载哪一个。实际上，我们需要的包只有python-igraph。

解决办法：

    第一步：卸载包igraph(pip2 -m pip uninstall igraph)

    第二步：重新安装包python-igraph(python3 -m pip install python_igraph)

完成以上操作，验证Python中能否成功加载igraph包（from igraph import *）

--

python3 -m pip install python_igraph