# 机械制造技术基础课程大作业

本项目为《机械制造技术基础》课程大作业，主题为 CA6140 车床杠杆零件的机械加工工艺分析与工艺路线设计。

## 文件说明

- `require.md`：作业要求。
- `template.md`：报告模板。
- `task1.md`：步骤一已完成内容。
- `report.tex`：完整 LaTeX 报告源文件。
- `report.pdf`：已编译生成的 PDF 报告。
- `杠杆（CA6140车床）831009.png`：零件工作图。

## 如何编译 PDF

本项目使用 `xelatex` 编译，原因是报告包含中文内容和中文字体设置。

### 环境要求

- 已安装 TeX 发行版，例如 TeX Live 或 MacTeX。
- 命令行可用 `xelatex`。

可先用下面命令检查：

```bash
xelatex --version
```

### 编译命令

在项目根目录执行：

```bash
xelatex -interaction=nonstopmode -halt-on-error report.tex
xelatex -interaction=nonstopmode -halt-on-error report.tex
```

说明：

- 第一次编译生成目录、引用等辅助文件。
- 第二次编译用于刷新目录和交叉引用。

编译完成后，会在当前目录生成：

```text
report.pdf
```

## 重新生成报告

如果修改了 `report.tex`、`task1.md` 中转写内容，或者替换了工作图，建议重新执行两次 `xelatex` 编译命令，以确保目录、页码和引用正确。

## 备注

- 当前 `report.tex` 默认通过 `xelatex` 编译。
- 若本机缺少对应中文字体，可能需要根据本机字体环境调整 `report.tex` 中的字体设置。
