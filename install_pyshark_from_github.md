在windows上从github检出python 模块pyshark的代码并安装

1、在windows上安装命令行工具

根据https://www.jianshu.com/p/122f5bf8749e
的方法，照着做完，看到类似如下的界面：

![](images/media/document_image_rId7.png){width="5.768055555555556in"
height="3.6452712160979877in"}

2、检出代码

a\. 假设要把代码放到 d:\\src下，那么要建立d:\\src这个目录。

b\. 运行git bash，用cd命令切换到想用来放源代码的目录/d/src里：

cd /d/src

c\. 从github.com克隆（检出）代码

git clone <https://github.com/md11235/pyshark.git>

3、卸载已有的pyshark，安装从github拿到的代码

1.  运行anaconda prompt

![](images/media/document_image_rId9.png){width="3.9270833333333335in"
height="6.59375in"}

2.  如果之前安装过pyshark，先卸载

pip uninstall pyshark

![](images/media/document_image_rId10.png){width="5.768055555555556in"
height="2.977626859142607in"}

3.  从检出的源代码安装pyshark

用如下命令切换到d:\\src ：

d:

cd d:\\src

然后运行 python setup.py install

![](images/media/document_image_rId11.png){width="5.768055555555556in"
height="3.047825896762905in"}
