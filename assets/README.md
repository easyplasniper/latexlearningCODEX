# assets 目录说明

这个目录用来放你自己的图片资源。

目前仓库没有放入二进制图片文件，目的是让项目保持纯文本、便于直接查看和克隆。

建议你后续把图片放成下面这种形式：

- `assets/figure-01.png`
- `assets/figure-02.jpg`
- `assets/chart-01.pdf`

在 LaTeX 中常见写法是：

```latex
\includegraphics[width=0.7\linewidth]{assets/figure-01.png}
```

如果编译时报 `File not found`，优先检查：

1. 文件名是否写对
2. 扩展名是否写对
3. 图片是否真的放在 `assets/` 目录里
