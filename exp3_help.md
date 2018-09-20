# 第三次实验辅助信息

## WiFi 网络连接

WiFi SSID: network_lab，password: 88888888 。 设备太多，未必能连上。可以考虑在教师机上用usb盘拷贝。

## 软件下载

<http://192.168.92.100/>

强烈建议从上述站点安装Firefox浏览器。

该站点还提供 第三次实验样本网络数据包： <http://192.168.92.100/wireshark-traces.zip> 。 提交作业时不能用这个包哈，需要提交你们小组用wireshark抓的包文件。

## 供还未配置好编程环境的同学

下载安装好了pyshark、jupyter notebook的压缩包 <http://192.168.92.100/Anaconda3.rar>
并将该文件直接(不要再创建目录)解压缩到比如D:\下面，然后进行下一步。

打开一个默认的cmd（windows键+r,在弹出的小窗口里输入cmd 回车）

然后输入

`d:\Anaconda3\Scriptsjupyter-notebook.exe`

然后按下 回车 键，即可运行出juputer notebook。这个压缩包解压缩之后的环境里已经包含了pyshark，所以可以直接在jupyter notebook里调用pyshark写实验课要求的代码了。
