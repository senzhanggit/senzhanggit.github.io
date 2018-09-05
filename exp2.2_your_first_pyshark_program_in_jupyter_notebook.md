# 运行Jupyter Notebook

如果是用Anaconda安装的，那么很简单，在开始菜单里找到Anaconda 3菜单项并展开，然后点击Jupyter Notebook即可。

如果是用Miniconda安装的，那么稍微复杂些。打开anaconda prompt命令行窗口，在里面输入

```shell
jupyter notebook
```

然后回车

稍等一阵，会看到有黑色的命令行窗口出现，里面滚动显示日志；并且不出意外的话，会看到有浏览器（系统上的默认浏览器）自动打开新页面，展示一个jupyter notebook，这个页面的URL类似：

```
http://localhost:8888/?token=ac43389c852fab50170ad48922c9495cf42f9571059b4fc2
```

如果看不懂上面的地址的构成，那么本门课更值得你继续。

但是这时还不能直接写代码，你看到的是一个类似文件管理器的界面。在这个界面的右上角，有一个名为`New`的按钮，点击它，里面看到有一个条目叫做：

```
notebook：
Python 3
```

点击这个条目，此时才会打开一个notebook，里面默认有了一个单元格，此时才可以开始下一步，往里面写代码。


# 开始写你的代码

在前面安装配置正确的情况下，终于，我们来到了这里。先下载一个已经用wireshark抓好的数据包， [http-ethereal-trace-1](wireshark-traces/http-ethereal-trace-1)，然后放到比如D盘下，那么这个文件在后续编程时，引用（找到）它的路径是`d:/http-ethereal-trace-1`。

```python
import pyshark

cap = pyshark.FileCapture("d:/http-ethereal-trace-1", display_filter='http')

print(cap[0])
```

如果你看到类似如下输出：
```
Packet (Length: 698)
Layer ETH:
        Destination: aa:bb:cc:dd:ee:ff
        Source: 00:de:ad:be:ef:00
        Type: IP (0x0800)
Layer IP:
        Version: 4
        Header Length: 20 bytes
        Differentiated Services Field: 0x00 (DSCP 0x00: Default; ECN: 0x00: Not-ECT (Not ECN-Capable Transport))
        Total Length: 684
        Identification: 0x254f (9551)
        Flags: 0x00
        Fragment offset: 0
        Time to live: 1
        Protocol: UDP (17)
        Header checksum: 0xe148 [correct]
        Source: 192.168.0.1
        Destination: 192.168.0.2
        ...
```

那么恭喜你，你基本完成了第一个pyshark程序。

# 更多参考资料

[Pyshark作者写的教程页面](https://kiminewt.github.io/pyshark/)
