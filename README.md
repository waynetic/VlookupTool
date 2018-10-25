## VlookupTool小工具
excel中自带函数vlookup是很方便使用的，但随着单元格行数逐渐增多时vlookup使用起来会显得很慢，于是利用vba字典写了Vlookup工具加快工作效率。

### 使用方法：

打开vlookup工具，点击“视图”→点击“宏”→选中VlookupTool宏→点击“执行”

然后就可以激活窗口使用啦

### 工具介绍：

窗体设计比较简洁，看图↓

![Image text](https://github.com/StinkCat/VlookupTool/raw/master/img/jiemian.png)

1、其中红色框是必填值，绿色框是选填值；

2、输入索引列和其他列是只能输入字母，假设是A列输入“A”，输入完后下边对应灰色框会提示输入列的第一行内容；

3、“起始行”代表把匹配结果从选择的列中第几个单元格往下写入，通常除去首行就是在第二行开始，默认值为2；

4、绿色框中按需求勾选“替换无结果值”，可以将无法索引的结果替换为特定的值，默认替换值为#N/A；

5、绿色框中按需求勾选“重复结果串联值”，不勾选时遇到当索引有多个结果时取第一个值，勾选时将多个结果连接一起，用特定值相隔，默认替换值为&；

6、勾选绿色框运行时会多了一点运算，所以时间耗费多那么一点点

![Image text](https://github.com/StinkCat/VlookupTool/raw/master/img/jieguo.png)

 测试两边为33万行数据进行索引匹配，只耗费18秒，尝试上面所说勾选绿色框两功能耗费27秒左右，差距不是很大。
 
 ### 已知不足：窗体激活时没关闭状态，再打开一个工作簿进行索引时，复选框中不能读取新打开的工作簿，研究了几个小时没头绪...只能关闭窗体重新激活使用喽
