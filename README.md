# SJTUBeamer 🤓

欢迎使用 SJTUBeamer! 🥳

SJTUBeamer 是上海交通大学的非官方 Beamer 模版。您可以使用 SJTUBeamer 制作幻灯片，展示您的成果。

这个仓库中包含 SJTUBeamer 所使用的宏包 `sjtubeamer`，以及一个示例文档。

## 快速上手 👋

目前的 `main.tex` 是一个示例文档《如何使用 LaTeX 排版论文》。您可以将里面的内容替换掉。下面是一个最简示例：

<details>

<summary>点击展开代码片段</summary>

```latex
\documentclass[
    % draft,          % 草稿模式
    aspectratio=169,  % 使用 16:9 比例
]{ctexbeamer}
\mode<presentation>

\usetheme[min]{sjtubeamer}
% 使用 maxplus/max/min 切换标题页样式
% 使用 red/blue 切换主色调
% 使用 light/dark 切换亮/暗色模式
% 使用外样式关键词以获得不同的边栏样式
%   miniframes infolines  sidebar* 
%   default    smoothbars split	 
%   shadow     tree       smoothtree
% *siderbar 推荐与 max 一起使用。

\usepackage[backend=biber,style=gb7714-2015]{biblatex}
\addbibresource{thesis.bib}

\institute[SJTUG]{上海交通大学 Linux 用户组} % 组织

\title{SJTUBeamer 幻灯片模板}         % 标题
\subtitle{SJTUBeamer Template}       % 副标题
\author{SJTUG}                       % 作者
\date{\today}                        % 日期  

\begin{document}

\maketitle                           % 创建标题页

\part{第一部分}

% 使用节目录
\AtBeginSection[]{
  \begin{frame}
    % \tableofcontents[currentsection]  % 传统节目录             
    \sectionpage                        % 节页
  \end{frame}
}

\section{第 1 节}

\begin{frame}
  \frametitle{标题}
  \paragraph{列表} 这个\alert{幻灯片}有下面几项：
  \begin{itemize}
    \item 第 1 项
    \item 第 2 项
    \item 第 3 项
  \end{itemize}
\end{frame}

\begin{frame}
  \frametitle{标题}
  \framesubtitle{子标题}
  \begin{equation}
    x^2+2x+1=(x+1)^2
  \end{equation}
\end{frame}

\section{第 2 节}
\begin{frame}
  \frametitle{一些盒子}
  \begin{block}{盒子}
    这是一个盒子\cite{thelegendofjiang}
  \end{block}
  \begin{alertblock}{注意}
    注意内容
  \end{alertblock}
  \begin{exampleblock}{示例}
    示例内容
  \end{exampleblock}
\end{frame}

\begin{frame}[fragile]          % 注意添加 fragile 标记
  \frametitle{代码块}
  % 代码块参数：语言，标题
  % 请减少代码初始的缩进
  \begin{codeblock}[language=c++]{C++代码}
#include<iostream>

int main(){
  // Console Output
  std::cout << "Hello, SJTU!" << std::endl;
  return 0;
}
  \end{codeblock}
\end{frame}

\part{参考文献}
\begin{frame}[allowframebreaks]
  \printbibliography[title=参考文献]
\end{frame}

\makebottom       % 创建结束页

\end{document}
```

</details>

## 使用方法 🧰

普通用户只需编辑 `main.tex` 即可开始使用。

### 模版下载与编译

* Overleaf
  * 下载 [最新版](https://github.com/sjtug/SJTUBeamer/archive/refs/heads/main.zip) 压缩包。
  * 或下载 [v1.5.0](https://github.com/sjtug/SJTUBeamer/archive/refs/tags/v1.5.0.zip) 压缩包。
  * 上传至 Overleaf 使用即可。
  * Overleaf 的设置中需要选择“XeLaTeX”编译器编译。
* 本地使用
  * 安装 TeXLive 套件。
  * 下载 [最新版](https://github.com/sjtug/SJTUBeamer/archive/refs/heads/main.zip) 压缩包。
  * 或下载 [v1.5.0](https://github.com/sjtug/SJTUBeamer/archive/refs/tags/v1.5.0.zip) 压缩包。
  * 或使用 git 克隆仓库 `git clone https://github.com/sjtug/SJTUBeamer/`。
  * 之后通过 `latexmk -xelatex main.tex` 命令进行编译即可。
  * VSCode 用户可以使用 LaTeX Workshop 中的 “Recipe: latexmk (latexmkrc)” 进行编译。

目前模版最新的稳定版是 v1.5.0。您可以在 [发布页](https://github.com/sjtug/SJTUBeamer/releases/tag/v1.5.0) 查看修改日志和更多资料。通常来说，SJTUBeamer 的一个稳定版本包括如下内容：

* `sjtubeamer.pdf`: SJTUBeamer 用户文档。**强烈推荐在使用前阅读一遍 👍👍👍。**
* `sjtubeamerdevguide.pdf`: SJTUBeamer 开发指南。
* `sjtulib-talk-max-red.pdf`: 示例文档《如何使用 LaTeX 排版论文》的 `max,red` 主题版本。
* `sjtulib-talk-maxplus-blue.pdf`: 示例文档《如何使用 LaTeX 排版论文》的 `maxplus,blue` 主题版本。
* `sjtulib-talk-maxplus-red.pdf`: 示例文档《如何使用 LaTeX 排版论文》的 `maxplus,red` 主题版本。
* `sjtulib-talk-min-red.pdf`: 示例文档《如何使用 LaTeX 排版论文》的 `min,red` 主题版本。
* `sample-all-covers.pdf`: 所有配色主题的封面封底。
* `sjtubeamer-ctan.zip`: 包含所有文档和样式的压缩包。
* SJTUBeamer 源代码。

## 使用反馈与贡献代码 👷

* 您可以通过 GitHub Issue 反馈使用时碰到的问题。同时，也欢迎您提交 PR 帮助我们改进。
* 所有对模版的修改应该在 `.dtx` 文件中进行，而后用 l3build 生成 sty 文件。
* 您可以阅读发布页面中的《SJTUBeamer 开发指南》`sjtubeamerdevguide.pdf` 了解模版的实现细节与编译方法。

整个开发流程如下：

* 修改 `.dtx` 文件。
* 运行 `make generate` 将生成的 sty 文件拷贝到根目录下。
* 更新 `main.tex`，运行 `make build` 查看模版修改后的效果。
* 更新开发文档，运行 `make build-dev` 编译所有开发文档，运行单元测试。
* （可选）运行 `make format-dev` 格式化所有文件。
* 发 PR。

新贡献者可以将自己的信息加入 `src/doc/sjtubeamerdevguide.tex` 的 `Developer` 章节。

## 展示 🧐

![cover-0](https://user-images.githubusercontent.com/4198311/131241659-90f0804b-d0b1-4bb9-b45c-7d3c81ace02a.png)
![cover-1](https://user-images.githubusercontent.com/4198311/131241665-2ced7884-7428-4967-8055-6ce47de7f8bd.png)
![cover-2](https://user-images.githubusercontent.com/4198311/131241668-cc47d9fb-14c4-4681-b95d-98400e9b8d77.png)
![cover-3](https://user-images.githubusercontent.com/4198311/131241669-ccf58f17-d35f-492d-8707-2cfdbd613107.png)

## 许可证

SJTUBeamer 仓库同时包含 SJTUBeamer 包和一个示例文档。其中内容的许可证各不相同。您可以阅读各个文件的开头部分，了解该文件所使用的许可证。

* SJTUBeamer 包使用的许可证为 Apache-2.0。
* SJTUBeamer 示例文档使用 CC-BY-SA 4.0 许可。
* sjtuvi 和 sjtucover 库及其附属徽标、图片由上海交通大学持有版权。校属各单位及个人以经营为目的使用视觉形象识别系统，须向学校申请使用许可。校外单位及个人未经许可，不得制作或使用载有视觉形象识别系统的物品。
