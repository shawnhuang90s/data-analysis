[TOC]

## 准备工作

1、安装虚拟环境包

```bash
pip install virtualenv
pip install virtualenvwrapper-win
```

2、新建虚拟环境

```bash
mkvirtualenv data-analysis
```

3、Pycharm 新建项目 data-analysis 并配置刚才新建的虚拟环境

4、根目录下新建 Jupyter Notebook 格式的文件：numpy_test

5、安装 NumPy 包及 Jupyter Notebook 包

```bash
pip install numpy scipy matplotlib -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install jupyter -i https://pypi.tuna.tsinghua.edu.cn/simple
```

6、Pycharm 终端运行 Jupyter，点击提示的链接会自动打开浏览器（最好设置谷歌浏览器为默认浏览器）

```bash
jupyter notebook
```

7、点击 numpy_test.ipynb 开始测试

8、将 Jupyter 文件转换成 PDF 的两种方法

**第一种：[官方教程](https://nbconvert.readthedocs.io/en/latest/install.html#installing-tex)**

这里展示的在 Windows 上需要安装的内容

安装 nbconvert

```bash
pip install nbconvert -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install nbconvert[webpdf] -i https://pypi.tuna.tsinghua.edu.cn/simple
```

安装 Pandoc 和 TeX（安装包已放在百度网盘，官网下载慢或下载失败的可联系我）

重启电脑（前提是转换成 PDF 失败的话...）

**PS**：缺点是不能显示中文，查了资料很复杂，故弃之

**第二种：利用谷歌浏览器**

安装 Jupyter 目录相关的包

```bash
pip install jupyter_contrib_nbextensions -i https://pypi.tuna.tsinghua.edu.cn/simple
jupyter contrib nbextension install --user
pip install jupyter_nbextensions_configurator -i https://pypi.tuna.tsinghua.edu.cn/simple
```

Pycharm 终端停止运行 Jupyter 并重启它

发现 Jupyter 页面中上面选项栏会出现 `Nbextensions` 的选项

点开 Nbextensions 的选项，并勾选 `Table of Contents`

打开一个 `.ipnb` 文件，右上角的工具栏就会出现目录选项，点击就会生成目录

**注意：有可能点了后看不到左侧的目录，只需用鼠标在左边空白区域点击往下拉一下即可，这是个 BUG!!!**

转成 PDF 之前先关掉目录，不然会与正文内容叠在一起！！！

前面第 6 步提到最好设置谷歌浏览器为默认浏览器，转换 PDF 就是其中一个目的

在 Jupyter 页面选择谷歌浏览器的【打印...】

目标打印机选择【另存为PDF】，布局选择【横向】

然后查看预览效果，主要查看是否有代码内容显示不全，若无，则按【保存】即可

否则，继续选择下面的【缩放】，直到预览的结果满意为止，最后点击【保存】即可

9、Jupyter 主题设置

安装

```bash
pip install jupyterthemes -i https://pypi.tuna.tsinghua.edu.cn/simple
```

列出可用的主题

```bash
jt -l

# 运行结果：
   chesterish
   grade3
   gruvboxd
   gruvboxl
   monokai
   oceans16
   onedork
   solarizedd
   solarizedl
```

选择某个主题

```bash
jt -t onedark
```

重启 Jupyter 查看页面主题效果

恢复默认主题（要导出 PDF 感觉还是默认主题看着舒服一点...）

```bash
jt -r
```

