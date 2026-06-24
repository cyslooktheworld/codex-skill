---
name: academic-paper-translator
description: Translate academic papers, PDFs, LaTeX, Markdown, abstracts, methods, experiments, related work, and technical literature into accurate Chinese while preserving structure, terminology, equations, citations, figures, and tables.
---

# Academic Paper Translator

## 目标

将英文论文、技术文献、PDF 提取文本、LaTeX 或 Markdown 内容翻译为准确、自然、学术化的中文。

## 翻译要求

1. 默认翻译为简体中文。
2. 保留原文的章节结构、标题层级、公式、引用编号、图表编号。
3. 不翻译代码、变量名、函数名、文件名。
4. 第一次出现专业术语时，使用“中文术语（English term）”格式。
5. 后续术语翻译必须前后一致。
6. 不删减原文信息。
7. 不编造论文中没有的内容。
8. 如果原文存在 OCR 错误或断行错误，应根据上下文修正后再翻译。
9. 如果用户要求“翻译要确切”，应优先逐句准确翻译。
10. 如果用户要求“保留图片”，应保留图片位置或图片占位符。

## 图表处理

Figure 翻译为“图”，Table 翻译为“表”。

例如：

Figure 1. Overview of the proposed method

翻译为：

图 1. 所提出方法的总体框架

## 公式和引用

必须保留：

- 数学公式
- 变量名
- 引用编号，例如 [1]、[2]
- 作者年份引用，例如 Smith et al., 2024
- 图表编号
- 算法编号

不要随意改动公式和引用。

## 默认输出格式

如果用户没有指定格式，默认输出 Markdown。

如果用户要求生成 Word 文件，应输出适合转换为 Word 的结构化内容，并尽量保留标题、段落、图表位置和引用编号。

## 质量检查

翻译完成后检查：

- 是否漏译
- 术语是否一致
- 公式是否被错误改动
- 引用编号是否保留
- 中文是否通顺
- 是否出现原文没有的信息
