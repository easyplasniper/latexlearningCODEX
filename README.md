# LaTeX / Overleaf 零基础动手练习项目

这个项目是给完全没有 LaTeX 基础的学习者准备的。核心学习方式不是“先看很多理论”，而是“打开一个最小示例，改一点，编译一次，再观察结果”。

项目默认以中文讲解，示例尽量短小，并在 LaTeX 源码里加入了较多中文注释，方便你一边读一边试。

## 适合谁

- 从未接触过 LaTeX
- 会用文本编辑器，但不熟悉排版语法
- 想在 Overleaf 或本地环境里边改边学

## 你会学到什么

1. 第 1 课：第一次成功编译 LaTeX 文档
2. 第 2 课：文档结构、标题、作者、日期
3. 第 3 课：标题层级与基础文本格式
4. 第 4 课：最常见的数学公式写法
5. 第 5 课：图环境、图题、引用
6. 第 6 课：表格环境、列格式、引用
7. 第 7 课：交叉引用与参考文献
8. 第 8 课：完成一个小型技术报告

## 项目结构

```text
latexlearningCODEX/
├─ README.md
├─ main.tex
├─ assets/
│  └─ README.md
├─ bib/
│  └─ references.bib
├─ examples/
│  ├─ lesson01_hello.tex
│  ├─ lesson02_structure.tex
│  ├─ lesson03_sections_text.tex
│  ├─ lesson04_math.tex
│  ├─ lesson05_figures.tex
│  ├─ lesson06_tables.tex
│  ├─ lesson07_refs_bib.tex
│  └─ final_report_template.tex
├─ exercises/
│  └─ final_report_task.md
└─ lessons/
   ├─ lesson01_first_document.tex
   ├─ lesson02_document_structure.tex
   ├─ lesson03_sections_and_text.tex
   ├─ lesson04_math_basics.tex
   ├─ lesson05_figures.tex
   ├─ lesson06_tables.tex
   ├─ lesson07_references_and_bib.tex
   └─ lesson08_final_mini_report.tex
```

## 推荐学习路径

1. 先编译 `main.tex`，看整套课程导航。
2. 再打开对应的 `examples/lessonXX_*.tex` 文件。
3. 先原样编译一次，确认能跑通。
4. 按 `lessons/` 里对应课程的“动手修改任务”一点点改。
5. 每改一次就重新编译，观察 PDF 变化。
6. 第 8 课完成后，继续做 `examples/final_report_template.tex` 和 `exercises/final_report_task.md`。

## 在 Overleaf 中使用

1. 新建一个空白项目。
2. 把整个 `latexlearningCODEX` 文件夹内容上传到 Overleaf。
3. 在菜单中把编译器设为 `XeLaTeX`。
4. 先把主文件设置为 `main.tex`，编译查看课程总入口。
5. 学某一课时，直接打开 `examples/` 里的对应示例文件修改。
6. 如果你想单独编译某个示例，可把该示例设为 Main file。

说明：

- 本项目主要为中文内容设计，推荐始终使用 `XeLaTeX`。
- 第 7 课和最终综合练习使用了参考文献，Overleaf 会自动处理多轮编译；如果第一次看到 `??` 或文献未生成，再点一次 Recompile 即可。

## 本地编译

推荐环境：

- TeX Live
- MiKTeX
- TeXstudio / VS Code + LaTeX Workshop
- 编译引擎：`XeLaTeX`

### 编译课程总入口

在项目根目录执行：

```powershell
xelatex main.tex
```

如果你安装了 `latexmk`，更推荐：

```powershell
latexmk -xelatex main.tex
```

### 编译单个示例

在项目根目录执行，例如：

```powershell
xelatex examples/lesson04_math.tex
```

带参考文献的示例和最终报告，推荐：

```powershell
latexmk -xelatex examples/lesson07_refs_bib.tex
latexmk -xelatex examples/final_report_template.tex
```

如果你的编辑器默认把工作目录切换到 `examples/`，而又找不到 `bib/references.bib`，请把工作目录改回项目根目录再编译。

## 如何边改边学

建议每节课都按下面的节奏来：

1. 先编译原始示例，确认它能成功输出 PDF。
2. 只改一个点，比如标题、文字、公式、表格中的一个单元格。
3. 立刻重新编译。
4. 问自己两个问题：
   - 我刚改的是哪一行？
   - PDF 里哪一块因此变了？

## 常见环境问题

- 中文乱码：通常是因为没用 `XeLaTeX`。
- `Undefined control sequence`：通常是命令拼错，或者少写了反斜杠 `\`。
- `File not found`：通常是图片或 `.bib` 路径写错。
- 看到 `??`：通常是交叉引用或参考文献还没完成第二轮编译。

## 最终综合练习

最终练习位于：

- `examples/final_report_template.tex`
- `exercises/final_report_task.md`

目标是完成一篇小型技术报告，要求至少包含：

- 标题、作者、日期
- 至少 3 个一级标题
- 至少 1 个公式
- 至少 1 个图
- 至少 1 个表
- 至少 1 处交叉引用
- 至少 1 条参考文献

## 使用建议

- 不要一口气学完全部内容。
- 一次只改一处，更容易看懂“语法”和“结果”的对应关系。
- 如果报错，不要慌，先看报错行附近有没有漏掉花括号、反斜杠、环境结束命令。
