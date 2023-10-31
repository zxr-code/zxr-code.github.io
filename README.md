# zxr-code.github.io

此项目用于记录latex排版的各种问题，Windows 11。


2023.8.7 中文论文模板使用CCT&TEX编译
（安装CTEX3.0和WinEdit10.2的过程很顺利，但是编译不出pdf，后来卸载了CTEX3.0，安装了CTEX2.9.2.167，使用PDFTeXify编译，即可得到pdf，而且速度也还可以。）

**1. 安装 CTEX2.9.2.167：**https://ctex.org/ctex/download/
   注意事项：此处取消勾选![image](https://github.com/zxr-code/zxr-code.github.io/assets/64823727/c9d7eede-a143-4777-b4b2-42bb6106b05c)
**2. 安装 WinEdit10.2：**http://www.winedt.com/download.html
   注意事项：此处要勾选![image](https://github.com/zxr-code/zxr-code.github.io/assets/64823727/484950ed-dd84-4418-80c6-ad0029c1b08e)

PS：中文论文模板使用CCT&TEX编译，无法使用OverLeaf，看网上说是目前好多中文期刊提供的模板只能使用CCT&Latex进行编译，需要下载CTex+WinEdt进行编辑。



2023.8.8 记录中文论文模板使用CCT&TEX编译的问题
1.数学公式：
*行内公式：`${y_i} = {({y_{i1}},{y_{i2}},\ldots,{y_{i{d_i}}})^'}$`这个公式无法编译，结果是因为`^'`，去掉`^`即可成功编译。
*编号公式：使用`\begin{equation}\label{}     \end{equation}`无法编译成功，看了看模板的公式样例，使用`\begin{eqnarray}    \end{eqnarray}`即可编译成功。





**介绍latex的基本内容**
这里以paper为基准，一篇paper包含的几个关键要素是Title、Author、Abstract、Keywords、正文、参考文献。
**1.Title、Author、Abstract、Keywords：**这几个信息期刊模板会给定好内容，直接找到相应位置替换就行。有时候Author Information会根据实际情况调整一下，比如谁是通讯作者、作者单位等等，这种情况这里先不详细介绍。
**2.正文：**正文部分一般包含段落文本、数学符号、数学公式、表格、算法、图片。
  （1）段落文本：
   ①结构：
   \section{} 一级标题
   \subsection{} 二级标题
   \subsubsection{} 三级标题
   ②段落之间一般采用空行进行分割段落，如下图。
   ![image](https://github.com/zxr-code/zxr-code.github.io/assets/64823727/176baa90-32cc-4570-b921-775dc2e4da0f)
   （2）数学符号：
   

\usepackage{cuted}
\begin{strip}
    \centering
    \begin{align}	   
        Mx(t+1) = A_{0}\left(r_{t}\right) x(t) + B_{0}(r_{t}) x(t-t_{d}) + N_{0}(r_{t}) u(t) + \sum_{k=1}^{m} \{ A_{k}\left(r_{t}\right) x(t) + B_{k}(r_{t}) x(t-t_{d}) + N_{k} \}
    \end{align}
\end{strip}

![image](https://github.com/zxr-code/zxr-code.github.io/assets/64823727/d0aca4e5-4a2a-41ca-a5c5-1ef3a12c552c)
