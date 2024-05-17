# 介绍

本项目主要提供了如下：
- 中、英文 `content.tex` 以测试不同主题
- 基于 [metropolis](https://github.com/matze/mtheme) 主题(`mytheme.tex`)，添加一些自己的元素
- 提供一个 clean 主题（十分简陋）

# 使用方法

## 测试不同主题

clone 本项目后，创建 `test.tex` 文件，例如：

```latex
% \documentclass[compress, aspectratio=169]{beamer}
\documentclass[compress, aspectratio=169]{ctexbeamer}
\usetheme{metropolis}

% 宏包
\usepackage{fancyhdr} % 标题，页脚
\usepackage{graphicx} % 图
\usepackage{algorithm2e}
\usepackage{booktabs} % 定义表格的画线命令
\usepackage{xcolor}
\usepackage{fontawesome5} % 小图标


% title page
\author{Your Name}
\title{Beamer Theme}


\begin{document}
    \input{content_zh.tex}
\end{document}
```

## 使用 `mytheme.tex`

在 `\begin{document}` 前 `\input{mytheme.tex}` 即可。

一些需要注意的是：
- `mytheme.tex` 为 frametitle 自定义一个命令 `\frametitlelogo{your title}` ，使用该命令可以在标题栏右侧添加自己的 logo（文件名为 `logo-w.png`），推荐使用白色透明图片，否则可能会显示异常。
- 在 title page 标题的右方添加一个 logo（文件名为 `logo.pdf`），该 logo 无特殊要求，根据自身需要调整大小即可。
- 主题配色可参考[网站](https://www.colorhunt.co/)。一般而言，`pri`, `sec`, `ter` 颜色应当逐渐变淡。