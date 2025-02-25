请根据以下要求，输出一份详细的 LaTeX 格式学习笔记，遵循 IEEE Conference 模板，内容应当分为以下几个部分：

## 0. 背景需求
- 课程采用过程式评价体系，笔记需完整呈现7个评估维度：
  1. 知识获取（52%）：体现知识体系的完整性与深度联系
  2. 项目执行（8%）：展示知识应用过程
  3. 动机（8%）：反映学习主动性
  4. 责任心（8%）：体现任务完成质量
  5. 沟通（8%）：展示交流协作能力
  6. 思维技巧（8%）：呈现批判性思考
  7. 动手能力（8%）：包含实践操作记录

## 1. 结构规范
1.1. **知识架构图**
   - 使用Mermaid mindmap，根据PPT绘制课程知识拓扑图
   - 标注知识点关联箭头并注明逻辑关系

1.2. **Latex文档架构**
```latex
% 知识架构图
\section{课程内容回顾}
\begin{figure}[htbp]
\centering
% 此处插入mermaid代码生成的知识架构图
\caption{课程内容思维导图}
\end{figure}

% 主体内容
\section{课堂知识精要}
   \subsection{核心概念}
   \subsection{理论框架}
   \subsection{典型应用}

\section{自学与拓展}
   \subsection{理论延伸} % 体现知识获取深度
   \subsection{创新思考} % 展示思维技巧
   \subsection{跨学科联系} % 反映动机维度

\section{实践记录}
   \subsection{实验报告} % 动手能力
   \subsection{项目日志} % 项目执行
   \subsection{协作记录} % 沟通能力

\section{问题与反思}
   \subsection{课后习题解析}
   \subsection{难点突破记录}
   \subsection{改进计划} % 责任心体现
```

## 2. 内容生成要求
嵌入多媒体规范：

2.1. 在笔记中合适的位置插入相关的表格，用于总结知识、对比数据或展示关键内容。表格应该简洁且具有良好的可读性。示例如下：
```latex
\begin{table}[htbp]
\caption{表格类型样式}
\begin{center}
\begin{tabular}{|c|c|c|c|}
\hline
\textbf{表头}&\multicolumn{3}{|c|}{\textbf{表列头}} \\
\cline{2-4} 
\textbf{表头} & \textbf{\textit{表列副标题}}& \textbf{\textit{副标题}}& \textbf{\textit{副标题}} \\
\hline
内容& 更多的表格内容$^{\mathrm{a}}$& &  \\
\hline
\multicolumn{4}{l}{$^{\mathrm{a}}$表格脚注示例。}
\end{tabular}
\label{tab1}
\end{center}
\end{table}
```

2.2. 在适当的地方插入图片，并为每张图片添加简洁且有意义的注释。图片应当能够直观地解释或补充文章内容。在图片的caption下给我一个latex注释，这个注释是这张图片的Google关键词。

```latex
\begin{figure}[htbp]
\centerline{\includegraphics{fig/fig1.png}}
% 这里放上用来google图片的的关键词
\caption{图的标题示例}
\label{fig}
\end{figure}
```

2.3. 如果课程涉及编程或技术性内容，插入相关的代码片段，展示如何使用具体的工具或方法。确保代码注释清晰，能够帮助理解。

2.4. 如果课程涉及数学或技术公式，确保公式排版美观且易于理解。

## 3. 格式要求

3.1. 整篇文章使用中文，遵循 LaTeX 格式，确保论文结构完整、规范。
3.2. 使用 IEEE Conference 模板，排版符合标准。
3.3. 在合适的位置添加相关的参考文献链接，确保文献的格式符合 IEEE 引用要求。
3.4. IEEE Conference 模板如下：
```latex
\documentclass[conference]{IEEEtran}
\IEEEoverridecommandlockouts
% 以上一行仅在需要在脚注中标识资金来源时使用。如果不需要，请将其注释掉。
\usepackage[UTF8]{ctex} 
\usepackage{cite}
\usepackage{amsmath,amssymb,amsfonts}
\usepackage{algorithmic}
\usepackage{graphicx}
\usepackage{textcomp}
\usepackage{xcolor}
\def\BibTeX{{\rm B\kern-.05em{\sc i\kern-.025em b}\kern-.08em
    T\kern-.1667em\lower.7ex\hbox{E}\kern-.125emX}}
\begin{document}
\title{基于LLM的学习笔记生成*\\

\thanks{在此标识相关的资金来源。如果没有，请删除此段。}
}

\author{
\IEEEauthorblockN{曹正阳}
\IEEEauthorblockA{南方科技大学\\
中国深圳\\
Email: caozy2021@mail.sustech.edu.cn}
}

\maketitle

\begin{abstract}
本文提出了一种通过深度学习摄像头实现机器人手臂模仿图像轨迹的图像跟踪方法。
本文的最基本目的是让机器人手臂能够模仿人类的书写。
\end{abstract}

\begin{IEEEkeywords}
组件，格式化，样式，造型，插入
\end{IEEEkeywords}

\section{介绍}
本文档是用于 \LaTeX 的模型和说明。
请注意会议页面的字数限制。

\section{使用方便}

\subsection{保持规范的一致性}

IEEEtran 类文件用于格式化您的论文和设置文本样式。所有边距、列宽、行间距和文本字体均已预设；请勿更改它们。您可能会注意到一些特殊之处。例如，页眉边距比通常情况比例更大。这种测量和其他测量都是有意为之的，采用的规范是为了将您的论文作为整个会议论文集的一部分，而不是独立文档。请勿修改当前的任何设计标识。

\section{在设置样式前准备您的论文}
在您开始格式化论文之前，首先将内容编写并保存为单独的文本文件。在格式化之前，完成所有内容和组织编辑。请参阅以下各节 \ref{AA}--\ref{SCM} 以获取更多关于校对、拼写和语法的信息。

在文本格式化和样式设置完成之前，请将文本和图形文件分开。请勿编号标题——{\LaTeX} 会自动为您完成。

\subsection{缩写和首字母缩略词}\label{AA}
在文本中首次使用缩写和首字母缩略词时进行定义，即使它们已经在摘要中定义过。缩写如 IEEE、SI、MKS、CGS、ac、dc 和 rms 不必定义。除非无法避免，请勿在标题或小标题中使用缩写。

\subsection{单位}
\begin{itemize}
\item 主要使用 SI（MKS）或 CGS 单位制。（鼓励使用 SI 单位制。）可以将英制单位作为次要单位（用括号括起来）。例外情况是贸易中使用英制单位作为标识符，如“3.5 英寸磁盘驱动器”。
\item 避免混合使用 SI 和 CGS 单位，例如以安培为单位的电流和以奥斯特为单位的磁场。这通常会导致混淆，因为方程式在维度上不平衡。如果必须使用混合单位，请明确说明每个量在方程中使用的单位。
\item 不要混合单位的完整拼写和缩写形式：“Wb/m\textsuperscript{2}” 或“每平方米韦伯”，而不是“每平方米韦伯”。当单位出现在文本中时，请拼写出来：“……几个亨利”，而不是“……几个 H”。
\item 小数点前加零：“0.25”，而不是“.25”。使用“cm\textsuperscript{3}”，而不是“cc”。
\end{itemize}

\subsection{方程}
依次编号方程。为了使方程更紧凑，可以使用斜线（~/~）、exp 函数或合适的指数。变量和量用斜体的罗马字母表示，但不适用于希腊字母。用长破折号代替短破折号作为减号。当方程式作为句子的一部分时，应使用逗号或句号标点符号，如：
\begin{equation}
a+b=\gamma\label{eq}
\end{equation}

请确保方程式中的符号在方程之前或之后立即定义。使用“\eqref{eq}”，而不是“Eq.~\eqref{eq}”或“equation \eqref{eq}”，除非在句子开头：“方程式 \eqref{eq} 是……”

\subsection{\LaTeX 特定建议}

请使用“软”（例如 \verb|\eqref{Eq}|）交叉引用，而不是“硬”引用（例如 \verb|(1)|）。这样可以在合并部分、添加方程或更改图形或引用的顺序时，无需逐行修改文件。

请勿使用 \verb|{eqnarray}| 方程环境。请使用 \verb|{align}| 或 \verb|{IEEEeqnarray}| 代替。 \verb|{eqnarray}| 环境会在关系符号周围留下不雅的空隙。

请注意， {\LaTeX} 中的 \verb|{subequations}| 环境即使没有显示方程编号，也会增加主方程计数器。如果忘记了这一点，您可能会写出一个方程编号从（17）跳到（20）的文章，这可能会让编辑人员怀疑您是否发现了新的计数方法。

{\BibTeX} 并非凭空运作。它并不是从空中获取文献数据，而是从 .bib 文件中获取的。如果使用 {\BibTeX} 生成参考文献，必须发送 .bib 文件。

{\LaTeX} 不能读懂您的心思。如果您将相同的标签分配给一个小节和一张表，可能会发现表 I 被引用为表 IV-B3。

{\LaTeX} 没有预知能力。如果您在更新计数器的命令之前放置了一个 \verb|\label| 命令，标签将拾取最后一个被交叉引用的计数器。特别是， \verb|\label| 命令不应放在图或表标题之前。

在 \verb|{array}| 环境中不要使用 \verb|\nonumber|。它不会阻止 \verb|{array}| 内部的方程编号（无论如何都不会有），但可能会阻止周围方程中的所需编号。

\subsection{一些常见错误}\label{SCM}
\begin{itemize}
\item “data” 是复数，不是单数。
\item 真空磁导率 $\mu_{0}$ 的下标以及其他常见的科学常数下标是零，而不是小写字母“o”。
\item 在美式英语中，逗号、分号、句号、问号和感叹号仅在引用完整思想或名称时位于引号内，如标题或完整引用。当使用引号而不是粗体或斜体来突出显示单词或短语时，标点符号应放在引号外。在句末的括号短语或句子外加标点（如这样）。 （完整的括号句子内的标点应在括号内。）
\item 图中嵌套的图为“inset”，而非“insert”。“alternatively” 优于“alternately”（除非您真的指的是交替发生的情况）。
\item 请勿使用“essentially” 表示“approximately”或“effectively”。
\item 在论文标题中，如果单词“that uses”可以准确替代“using”，则将“u”大写；否则，请保持小写。
\item 注意同音异义词的不同含义，如“affect”和“effect”、“complement”和“compliment”、“discreet”和“discrete”、“principal”和“principle”。
\item 不要混淆“imply”和“infer”。
\item 前缀“non”不是一个单词；它应与所修饰的单词结合，通常无需连字符。
\item 在拉丁语缩写“et al.”中，"et" 后没有句点。
\item 缩写“i.e.” 意为“that is”，“e.g.” 意为“for example”。
\end{itemize}
科学写作的优秀风格手册请参考 \cite{b7}。

\subsection{作者和单位}
\textbf{类文件设计用于最多六位作者，但不限于六位作者。} 所有会议文章至少需要一位作者。作者姓名应从左到右列出，然后移到下一行。这是未来引用和索引服务中使用的作者顺序。请勿按单位将姓名分组。请尽量简洁地列出您的单位信息（例如，不区分同一组织的不同部门）。

\subsection{标识标题}
标题是指导读者浏览论文的组织工具。标题有两种类型：组件标题和文本标题。

组件标题标识论文的不同组成部分，它们在主题上互不从属。示例包括致谢和参考文献，对于这些部分，正确的样式是“标题 5”。图形标题应使用“figure caption”，表格标题应使用“table head”。跑题标题，如“摘要”，需要您在下拉菜单中选择样式之外，还需应用样式（在这种情况下为斜体），以区分标题和正文。

文本标题按照关系和层次结构组织主题。例如，论文标题是主要文本标题，因为所有后续材料都与此主题相关并进一步展开。如果有两个或更多子主题，则应使用下一级标题（大写罗马数字），相反，如果没有至少两个子主题，则不应引入子标题。

\subsection{图和表}
\paragraph{图和表的位置} 将图和表置于列的顶部或底部。避免将它们放在列中间。较大的图和表可以跨越两个列。图题应置于图下方；表头应置于表格上方。在正文中引用图和表后插入它们。即使在句子开头也使用缩写“Fig.~\ref{fig}”。

\begin{table}[htbp]
\caption{表格类型样式}
\begin{center}
\begin{tabular}{|c|c|c|c|}
\hline
\textbf{表头}&\multicolumn{3}{|c|}{\textbf{表列头}} \\
\cline{2-4} 
\textbf{表头} & \textbf{\textit{表列副标题}}& \textbf{\textit{副标题}}& \textbf{\textit{副标题}} \\
\hline
内容& 更多的表格内容$^{\mathrm{a}}$& &  \\
\hline
\multicolumn{4}{l}{$^{\mathrm{a}}$表格脚注示例。}
\end{tabular}
\label{tab1}
\end{center}
\end{table}

\begin{figure}[htbp]
\centerline{\includegraphics{fig1.png}}
\caption{图的标题示例。}
\label{fig}
\end{figure}

图标签：图标签使用 8 点 Times New Roman 字体。编写图轴标签时，尽量使用单词而非符号或缩写，以免读者感到困惑。例如，使用“磁化强度”或“磁化强度，M”，而不仅仅是“M”。如果在标签中包含单位，请将其括在括号中。不要仅用单位标记坐标轴。例如，写“磁化强度（A/m）”或“磁化强度 \{A[m(1)]\}”，而不是仅写“A/m”。不要使用数量与单位的比率标记坐标轴。例如，写“温度（K）”，而不是“温度/K”。

\section*{致谢}

美国英语中，“acknowledgment” 一词的拼写不带 “e”。避免使用“one of us (R. B. G.) thanks $\ldots$”这样的表达。可以改为“R. B. G. 感谢$\ldots$”。将资助单位的致谢放在第一页的未编号脚注中。

\section*{参考文献}

请在方括号内按顺序编号引用文献 \cite{b1}。句子的标点符号应跟在方括号之后 \cite{b2}。直接引用参考文献编号，如 \cite{b3}——不要使用“Ref. \cite{b3}”或“reference \cite{b3}”，除非在句子开头：“Reference \cite{b3} 是第一个 $\ldots$”

脚注应分别编号为上标。将实际的脚注放在引用所在列的底部。不要在摘要或参考文献列表中添加脚注。表格脚注用字母表示。

除非有六位或更多作者，否则列出所有作者的姓名；不要使用“et al.”。尚未发表的论文，即使已提交出版，也应引用为“未出版” \cite{b4}。已接受出版的论文应引用为“印刷中” \cite{b5}。除专有名词和元素符号外，论文标题中仅首字母大写。

对于翻译期刊中发表的论文，请首先给出英文引用，然后给出原文引用 \cite{b6}。

\begin{thebibliography}{00}
\bibitem{b1} G. Eason, B. Noble, and I. N. Sneddon, ``On certain integrals of Lipschitz-Hankel type involving products of Bessel functions,'' Phil. Trans. Roy. Soc. London, vol. A247, pp. 529--551, April 1955.
\bibitem{b2} J. Clerk Maxwell, A Treatise on Electricity and Magnetism, 3rd ed., vol. 2. Oxford: Clarendon, 1892, pp.68--73.
\bibitem{b3} I. S. Jacobs and C. P. Bean, ``Fine particles, thin films and exchange anisotropy,'' in Magnetism, vol. III, G. T. Rado and H. Suhl, Eds. New York: Academic, 1963, pp. 271--350.
\bibitem{b4} K. Elissa, ``Title of paper if known,'' unpublished.
\bibitem{b5} R. Nicole, ``Title of paper with only first word capitalized,'' J. Name Stand. Abbrev., in press.
\bibitem{b6} Y. Yorozu, M. Hirano, K. Oka, and Y. Tagawa, ``Electron spectroscopy studies on magneto-optical media and plastic substrate interface,'' IEEE Transl. J. Magn. Japan, vol. 2, pp. 740--741, August 1987 [Digests 9th Annual Conf. Magnetics Japan, p. 301, 1982].
\bibitem{b7} M. Young, The Technical Writer's Handbook. Mill Valley, CA: University Science, 1989.
\end{thebibliography}
\vspace{12pt}
\color{red}
IEEE 会议模板包含撰写和格式化会议论文的指导文字。请确保在提交会议论文之前删除所有模板文字。未能删除模板文字可能导致论文无法发表。

\end{document}
```

## 4. 输出规范
4.1. 生成顺序：
   (1) 完整mermaid架构图（含CSS样式定义）
   (2) 符合IEEE模板的完整Latex源码

```
请严格按照此模板生成完整的学习笔记文档，并确保所有技术要素符合IEEE会议论文格式规范。
