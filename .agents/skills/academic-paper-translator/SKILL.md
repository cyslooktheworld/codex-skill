---

name: academic-paper-translator
description: >-
Translate academic papers, PDFs, LaTeX, Markdown, abstracts, methods,
experiments, related work, and technical literature into accurate Chinese.
Export translated results as DOCX and PDF while preserving structure,
terminology, equations, citations, original figures, tables, and formatting.
---

# Academic Paper Translator

## 目标

将英文论文、技术文献、PDF、LaTeX、Markdown、实验报告、技术文档等内容翻译为准确、自然、正式的简体中文，并在翻译完成后导出为：

1. Word 文件：`.docx`
2. PDF 文件：`.pdf`
3. Markdown 中间文件：`.md`

翻译时必须尽量保留原文的：

* 章节结构
* 标题层级
* 段落顺序
* 公式
* 变量名
* 引用编号
* 图表编号
* 表格结构
* 原始图片
* 图片位置
* 算法编号
* 参考文献格式

---

## 默认任务行为

当用户要求翻译论文、文献、PDF 或技术资料时，应默认执行以下流程：

1. 读取原始文献内容。
2. 识别论文结构。
3. 提取原文中的图片、表格、公式和引用。
4. 翻译正文为简体中文。
5. 翻译图注、表题和必要说明。
6. 将原论文图片真实嵌入翻译后的 Word 文件中。
7. 检查术语一致性和是否漏译。
8. 生成中文翻译版 Word 文件。
9. 由包含原图的 Word 文件转换生成 PDF 文件。
10. 在最终回复中说明导出的文件位置。

如果用户没有指定输出格式，也应默认导出：

* `.docx`
* `.pdf`
* `.md`

---

## 翻译语言

默认翻译为：

```text
简体中文
```

除非用户明确要求其他语言。

---

## 翻译风格

翻译风格应符合中文学术论文表达习惯。

要求：

1. 准确表达原文含义。
2. 语言正式、清晰、自然。
3. 不要过度口语化。
4. 不要随意省略原文内容。
5. 不要加入原文没有的信息。
6. 不要擅自扩写作者观点。
7. 不要改变论文中的实验结论。
8. 不要改变作者原有的逻辑顺序。
9. 对复杂长句可适当拆分，但不能改变含义。
10. 对术语翻译要保持前后一致。

---

## 翻译准确性要求

如果用户说：

```text
翻译要确切
```

则必须优先采用逐句准确翻译，不进行大幅意译或文学化润色。

对于专业论文，应优先保证：

1. 技术含义准确。
2. 实验方法准确。
3. 算法描述准确。
4. 公式解释准确。
5. 结论表述准确。
6. 术语翻译一致。
7. 引用和编号不丢失。
8. 图表和图片不丢失。

---

## 论文结构识别

翻译前应尽量识别原文中的结构，包括但不限于：

* Title
* Abstract
* Keywords
* Introduction
* Related Work
* Background
* Methodology
* Method
* Approach
* System Design
* Implementation
* Experiments
* Evaluation
* Results
* Discussion
* Limitations
* Conclusion
* Acknowledgements
* References
* Appendix

对应翻译建议：

| 英文结构             | 中文译法 |
| ---------------- | ---- |
| Title            | 标题   |
| Abstract         | 摘要   |
| Keywords         | 关键词  |
| Introduction     | 引言   |
| Related Work     | 相关工作 |
| Background       | 背景   |
| Methodology      | 方法论  |
| Method           | 方法   |
| Approach         | 方法   |
| System Design    | 系统设计 |
| Implementation   | 实现   |
| Experiments      | 实验   |
| Evaluation       | 评估   |
| Results          | 结果   |
| Discussion       | 讨论   |
| Limitations      | 局限性  |
| Conclusion       | 结论   |
| Acknowledgements | 致谢   |
| References       | 参考文献 |
| Appendix         | 附录   |

---

## 专业术语处理

遇到专业术语时，应遵循以下规则：

1. 第一次出现时，使用：

```text
中文术语（English Term）
```

例如：

```text
大语言模型（Large Language Model, LLM）
```

2. 如果术语有常见缩写，应保留缩写。

例如：

```text
检索增强生成（Retrieval-Augmented Generation, RAG）
```

3. 后续再次出现时，可以只使用中文术语或英文缩写。

例如：

```text
大语言模型
```

或：

```text
LLM
```

4. 对没有稳定中文译法的术语，可以保留英文，并在第一次出现时给出中文解释。
5. 同一篇文献中的同一个术语必须保持一致，不能前后翻译不同。
6. 如果论文领域不是人工智能或计算机领域，应根据论文具体内容重新建立术语表。

---

## 常见术语翻译建议

| 英文术语                           | 推荐中文译法      |
| ------------------------------ | ----------- |
| Large Language Model           | 大语言模型       |
| LLM                            | LLM         |
| Prompt                         | 提示词         |
| Prompt Engineering             | 提示词工程       |
| Fine-tuning                    | 微调          |
| Pre-training                   | 预训练         |
| Dataset                        | 数据集         |
| Benchmark                      | 基准测试        |
| Evaluation                     | 评估          |
| Framework                      | 框架          |
| Method                         | 方法          |
| Approach                       | 方法          |
| Model                          | 模型          |
| Training                       | 训练          |
| Inference                      | 推理          |
| Token                          | 词元          |
| Embedding                      | 嵌入          |
| Transformer                    | Transformer |
| Attention Mechanism            | 注意力机制       |
| Retrieval-Augmented Generation | 检索增强生成      |
| RAG                            | RAG         |
| Code Generation                | 代码生成        |
| Sensitive Information          | 敏感信息        |
| Information Leakage            | 信息泄露        |
| Privacy                        | 隐私          |
| Security                       | 安全性         |
| Vulnerability                  | 漏洞          |
| Mitigation                     | 缓解          |
| Baseline                       | 基线方法        |
| Ablation Study                 | 消融实验        |
| Case Study                     | 案例研究        |

---

## 公式处理

对于数学公式、变量、函数、符号，应遵循以下规则：

1. 不翻译公式本身。
2. 不修改变量名。
3. 不改变公式编号。
4. 不删除公式上下文说明。
5. 公式前后的解释文字需要翻译。
6. LaTeX 公式应尽量保持原始格式。
7. 如果公式无法转换为 Word 原生公式，应至少保留为清晰可读的文本或图片。
8. 不能因为公式识别困难而删除公式。

例如：

原文：

```text
The loss function is defined as:
L = -Σ y_i log(p_i)
```

翻译：

```text
损失函数定义如下：
L = -Σ y_i log(p_i)
```

---

## 代码、变量和文件名处理

以下内容不应翻译：

* 代码片段
* 函数名
* 类名
* 变量名
* 文件名
* 路径
* 命令行指令
* API 名称
* 数据集名称
* 模型名称
* 软件包名称

例如：

```text
getUserInput()
```

不能翻译成：

```text
获取用户输入()
```

应保持：

```text
getUserInput()
```

---

## 引用处理

必须保留原文中的引用格式，包括：

* `[1]`
* `[2, 3]`
* `[4–7]`
* `(Smith et al., 2024)`
* `Smith et al. [12]`

翻译时不能删除引用编号，也不能改变引用编号顺序。

例如：

原文：

```text
Recent studies have shown that LLMs may memorize sensitive information [12].
```

翻译：

```text
近期研究表明，大语言模型可能会记忆敏感信息 [12]。
```

---

## 图表处理

### 核心原则

论文中的原始图片、图表、流程图、架构图、截图、实验结果图等，必须尽量从原文中提取并嵌入到翻译后的 Word 和 PDF 文件中。

不得默认使用图片占位符代替原图。

图片占位符只能在图片提取或嵌入失败时作为临时错误说明使用，并且必须在最终回复中明确说明哪些图片未能成功嵌入以及失败原因。

---

### 图片编号

Figure 翻译为“图”。

例如：

```text
Figure 1. Overview of the proposed method.
```

翻译为：

```text
图 1. 所提出方法的总体框架。
```

---

### 表格编号

Table 翻译为“表”。

例如：

```text
Table 2. Experimental results on different datasets.
```

翻译为：

```text
表 2. 不同数据集上的实验结果。
```

---

### 原图保留要求

处理 PDF、论文或技术文献时，必须尽量执行以下操作：

1. 从原始 PDF 或原始文档中提取所有图片。
2. 将提取出的图片保存到输出目录中的图片文件夹。
3. 在翻译后的 Word 文件中，将原图插入到对应图注附近。
4. 在翻译后的 PDF 文件中，也必须包含这些原图。
5. 图片顺序应尽量与原论文保持一致。
6. 图片尺寸应适合 Word 页面宽度，不应过大导致版面混乱。
7. 图片下方或上方应保留并翻译对应图注。
8. 图编号必须与原文一致。
9. 不要重新绘制、修改或美化原图，除非用户明确要求。
10. 不要用文字描述代替原图。
11. 不要只写图片路径而不插入图片。
12. 不要只写“此处保留图片”之类的占位说明。

---

### 图片保存目录

如果论文中包含图片，应默认创建图片目录：

```text
outputs/images/
```

如果用户指定了输出目录，应在用户指定目录下创建图片文件夹，例如：

```text
translated/images/
```

图片文件命名建议：

```text
figure_1.png
figure_2.png
figure_3.png
```

如果一页中有多张图片，可以使用：

```text
page_3_image_1.png
page_3_image_2.png
```

---

### Word 中图片插入要求

生成 Word 文件时，必须将原图真实插入到 `.docx` 文件中，而不是只写图片路径或图片占位符。

推荐结构一：

```text
[这里插入原文 Figure 1 对应图片]

图 1. 所提出方法的总体框架。
```

推荐结构二：

```text
图 1. 所提出方法的总体框架。

[这里插入原文 Figure 1 对应图片]
```

具体顺序应尽量参考原文。

图片插入要求：

1. 图片应可在 Word 中直接显示。
2. 图片宽度应适配页面。
3. 图片不能超出页面边距。
4. 图片不能被压缩到无法阅读。
5. 图片与对应图注之间不能相隔过远。
6. 如果图片很多，应保持原文顺序。

---

### PDF 中图片保留要求

PDF 应优先由包含原图的 Word 文件转换生成。

优先流程：

```text
提取原图
→ 翻译正文
→ 生成包含原图的 Word 文件
→ 将 Word 文件转换为 PDF
```

如果使用 Markdown 或 HTML 作为中间格式，也必须确保图片路径正确，并且最终 PDF 中能够显示原图。

PDF 检查要求：

1. 打开或检查 PDF 文件，确认图片存在。
2. PDF 中不能只显示图片路径。
3. PDF 中不能只显示图片占位符。
4. PDF 中图片顺序应尽量与 Word 文件一致。

---

### 图片提取失败处理

只有在确实无法提取或嵌入图片时，才允许使用临时失败标记。

失败标记格式：

```text
[图 1 原图提取失败：请检查原 PDF 中该图片是否为扫描图、矢量图或受保护内容]
```

禁止使用模糊占位符，例如：

```text
[图 1 保留：原文中的系统架构图]
```

因为这没有真正保留原图。

如果图片提取失败，必须在最终回复中说明：

1. 哪些图没有成功提取。
2. 失败原因。
3. 是否仍然生成了 Word 和 PDF。
4. 用户可以如何补充原图或重新上传更清晰的 PDF。

---

### 图中文字处理

如果图片内部包含英文文字，默认不强制修改原图内部文字。

处理规则：

1. 原图必须保留。
2. 图注必须翻译。
3. 如果图片内部英文能安全识别，可以在图注下方增加“图中文字说明”。
4. 不要破坏原图质量。
5. 不要因为图中文字未翻译就删除原图。
6. 不要为了翻译图中文字而重绘图片，除非用户明确要求。

示例：

```text
图 2. 模型训练流程。

图中文字说明：图中 “Input” 表示输入，“Output” 表示输出，“Encoder” 表示编码器。
```

---

## 表格处理

表格翻译时应尽量保留原有结构。

要求：

1. 表头需要翻译。
2. 表格编号需要保留。
3. 数值不能改动。
4. 百分比、指标、实验结果不能改动。
5. 方法名称、模型名称、数据集名称通常不翻译。
6. 表格中的注释需要翻译。
7. 如果表格是图片形式，应把原表格图片嵌入 Word 和 PDF，并翻译表题。
8. 如果表格可以被准确解析为可编辑表格，应优先转换为 Word 表格。
9. 如果表格无法准确解析为可编辑表格，应保留原表格图片，并翻译表题和表注。
10. 不得因为表格复杂而删除表格。

---

## 参考文献处理

参考文献部分默认保留原文，不强制翻译。

如果用户明确要求翻译参考文献标题，则只翻译论文标题，不改变作者、期刊、会议、年份、DOI 等信息。

默认处理方式：

```text
参考文献标题可保留英文，引用格式不变。
```

要求：

1. 不要改变参考文献编号。
2. 不要删除 DOI。
3. 不要删除 URL。
4. 不要更改作者姓名。
5. 不要更改会议、期刊名称。
6. 不要更改年份、卷号、页码。

---

## OCR 错误处理

如果输入来自 PDF 识别文本，可能存在：

* 单词断裂
* 多余换行
* 页眉页脚混入正文
* 公式识别错误
* 图表标题断裂
* 连字符错误
* 乱码
* 多栏论文读取顺序混乱

处理规则：

1. 应根据上下文尽量修正常见 OCR 错误。
2. 不确定的地方不要擅自猜测。
3. 对明显无法识别的内容，用标记说明。
4. 多栏论文应尽量按正确阅读顺序翻译。
5. 页眉页脚、页码、版权声明等如果混入正文，应识别后避免干扰正文翻译。

例如：

```text
[此处原文疑似 OCR 错误，无法准确识别]
```

---

## 输出文件要求

翻译完成后，必须生成以下文件：

```text
translated_paper_zh.docx
translated_paper_zh.pdf
translated_paper_zh.md
```

如果原文文件有明确标题或文件名，应使用更具体的文件名。

例如：

```text
Mitigating_sensitive_information_leakage_zh.docx
Mitigating_sensitive_information_leakage_zh.pdf
Mitigating_sensitive_information_leakage_zh.md
```

文件命名规则：

1. 使用英文文件名或拼音文件名。
2. 避免特殊符号。
3. 空格用下划线 `_` 替代。
4. 中文译文文件名以 `_zh` 结尾。
5. Word 文件扩展名为 `.docx`。
6. PDF 文件扩展名为 `.pdf`。
7. Markdown 文件扩展名为 `.md`。

---

## 推荐输出目录

默认将导出文件放在：

```text
outputs/
```

如果仓库中没有 `outputs/` 目录，应自动创建。

推荐结构：

```text
outputs/
  translated_paper_zh.docx
  translated_paper_zh.pdf
  translated_paper_zh.md
  images/
    figure_1.png
    figure_2.png
    figure_3.png
```

如果用户指定其他路径，则必须使用用户指定路径。

例如：

```text
translated/
  word/
    translated_paper_zh.docx
  pdf/
    translated_paper_zh.pdf
  markdown/
    translated_paper_zh.md
  images/
    figure_1.png
    figure_2.png
```

---

## Word 导出要求

生成 Word 文件时，应尽量满足：

1. 标题层级清晰。
2. 一级标题、二级标题、三级标题格式正确。
3. 正文段落清楚。
4. 图表编号保留。
5. 必须将原论文图片真实嵌入 Word 文件中，并尽量放在对应图注附近，不得用占位符代替原图。
6. 表格尽量保持表格形式。
7. 公式尽量保留为可读格式。
8. 引用编号不丢失。
9. 参考文献部分格式不乱。
10. 页面排版整洁。
11. 图片应适配页面宽度。
12. 图片不能只以文件路径形式出现。
13. 图片不能只以 Markdown 图片语法形式留在 Word 中，必须能在 Word 中直接显示。

推荐 Word 样式：

* 正文中文字体：宋体或等效中文字体
* 正文英文字体：Times New Roman 或等效英文字体
* 标题：加粗
* 正文行距：1.15 或 1.5
* 页面边距：普通边距
* 图注和表题：可使用较小字号或居中格式
* 参考文献：保持清晰可读

---

## PDF 导出要求

PDF 应由翻译后的 Word 或 Markdown 转换生成。

优先顺序：

1. 先生成包含原图的 `.docx`
2. 再由 `.docx` 转换为 `.pdf`

如果当前环境无法直接从 Word 转 PDF，可以改用：

1. Markdown 转 PDF
2. HTML 转 PDF
3. LaTeX 转 PDF

无论使用哪种方式，最终 PDF 都应包含原论文图片。

如果 PDF 生成失败，仍然必须保留 `.docx`，并说明 PDF 失败原因。

---

## Markdown 中间文件

建议先生成一个中间 Markdown 文件：

```text
outputs/translated_paper_zh.md
```

然后再转换为：

```text
outputs/translated_paper_zh.docx
outputs/translated_paper_zh.pdf
```

Markdown 中间文件应保留：

* 标题层级
* 段落
* 公式
* 引用
* 真实图片引用路径，例如 `outputs/images/figure_1.png`
* 表格
* 参考文献

Markdown 中间文件中可以使用图片引用语法，例如：

```text
![图 1. 所提出方法的总体框架](images/figure_1.png)
```

但在最终 Word 和 PDF 中，图片必须真实显示，不能只显示路径或占位符。

---

## 图片提取与嵌入实现要求

处理 PDF 时，应优先使用 PyMuPDF、pdfimages、pypdfium2 或其他可用工具提取原始图片。

推荐流程：

```text
1. 从 PDF 中提取图片到 outputs/images/
2. 建立图片与图编号、图注之间的对应关系
3. 翻译正文和图注
4. 生成 Word 文件时插入对应原图
5. 由 Word 文件转换生成 PDF
6. 检查最终 Word 和 PDF 中是否能看到原图
```

如果无法准确建立图片与图注对应关系，应至少按照原 PDF 中图片出现顺序插入，并保留原图编号说明。

处理扫描版 PDF 时：

1. 如果整页都是扫描图片，应尽量保留整页原图或页面截图。
2. 翻译正文可以放在对应页面内容之后。
3. 不要删除扫描页中的原始图片。
4. 如果图片与正文无法分离，应保留页面截图作为原图证据。

---

## 推荐实现方式

Codex 在执行任务时，可以根据当前环境选择合适工具。

优先方案：

```text
PDF / Markdown / LaTeX
→ 提取正文、图片和表格
→ 保存原图到 outputs/images/
→ 翻译为中文 Markdown
→ 生成包含原图的 DOCX
→ 由 DOCX 转换为 PDF
→ 检查 DOCX 和 PDF 中图片是否显示
```

可使用的工具包括但不限于：

* pandoc
* python-docx
* PyMuPDF
* pdfimages
* pypdfium2
* markdown
* wkhtmltopdf
* LibreOffice
* LaTeX
* docx2pdf

如果工具不可用，应优先保证：

1. 翻译内容完整。
2. Word 文件成功生成。
3. 原图尽可能嵌入 Word。
4. PDF 失败时说明原因。

不得因为 PDF 转换工具不可用而放弃生成 Word 文件。

---

## 翻译质量检查

导出文件前必须检查：

1. 是否有漏译段落。
2. 是否有英文正文未翻译。
3. 是否有术语前后不一致。
4. 是否有公式被破坏。
5. 是否有引用编号丢失。
6. 是否有图表编号丢失。
7. 是否有表格数据被改动。
8. 是否已将原论文图片真实嵌入 Word 和 PDF，而不是仅使用图片占位符。
9. 是否有明显 OCR 错误未处理。
10. 是否生成了 `.docx`、`.pdf` 和 `.md` 文件。
11. 是否创建了图片目录。
12. 是否保留了图片文件。
13. Word 中图片是否能直接显示。
14. PDF 中图片是否能直接显示。

---

## 最终回复格式

任务完成后，应向用户简洁说明：

```text
已完成论文翻译，并导出以下文件：

1. Word 文件：outputs/xxx_zh.docx
2. PDF 文件：outputs/xxx_zh.pdf
3. Markdown 中间文件：outputs/xxx_zh.md
4. 图片目录：outputs/images/
```

如果 PDF 没有成功生成，应说明：

```text
Word 文件已生成，但 PDF 转换失败，原因是当前环境缺少 PDF 转换工具。
```

如果部分图片没有成功嵌入，应说明：

```text
部分原图未能成功嵌入，失败图片如下：

1. 图 3：原 PDF 中该图无法被图片提取工具识别。
2. 图 5：图片可能是矢量内容或受保护内容。

已在 Word 文件中保留失败说明。
```

---

## 禁止行为

不得执行以下行为：

1. 不得省略原文重要内容。
2. 不得随意总结代替完整翻译。
3. 不得删除公式。
4. 不得删除引用编号。
5. 不得删除图表编号。
6. 不得改变实验数据。
7. 不得编造作者没有提出的观点。
8. 不得把代码、变量名、函数名翻译成中文。
9. 不得擅自改变论文结构。
10. 不得只输出摘要，除非用户明确只要求翻译摘要。
11. 不得用图片占位符代替原论文图片，除非图片提取或嵌入确实失败，并且必须说明失败原因。
12. 不得只在 Word 或 PDF 中写图片路径而不显示图片。
13. 不得删除复杂表格。
14. 不得因为图片内部英文未翻译就删除原图。
15. 不得擅自重绘、修改、美化原论文图片。

---

## 用户常见指令理解

当用户说：

```text
翻译这篇论文
```

应理解为：

```text
完整翻译全文，并导出 Word 和 PDF。
```

当用户说：

```text
翻译要确切
```

应理解为：

```text
逐句准确翻译，不大幅意译。
```

当用户说：

```text
保留图片
```

应理解为：

```text
必须从原文中提取图片，并真实嵌入翻译后的 Word 和 PDF，不能只放占位符。
```

当用户说：

```text
生成 Word 文件
```

应理解为：

```text
至少生成 .docx，并尽量同时生成 .pdf。
```

当用户说：

```text
生成 Word 和 PDF
```

应理解为：

```text
必须同时生成 .docx 和 .pdf。
```

当用户说：

```text
原图不要占位
```

应理解为：

```text
必须把原论文图片真实放入 Word 和 PDF 文件中。
```

---

## 推荐提示词示例

用户可以这样调用本 Skill：

```text
使用 $academic-paper-translator 翻译这篇论文，要求翻译准确，保留原图、公式、引用和图表编号，并导出 Word 和 PDF。
```

也可以这样调用：

```text
使用 $academic-paper-translator 将这个 PDF 论文完整翻译成中文，翻译要确切，保留原文结构和原始图片，最后生成 docx 和 pdf 文件。
```

也可以指定输出路径：

```text
使用 $academic-paper-translator 翻译 input/paper.pdf。

要求：
1. 完整翻译为简体中文。
2. 翻译要确切。
3. 保留原论文图片，不要用图片占位符。
4. 保留公式、引用编号、图表编号和表格。
5. Word 文件输出到 translated/word/
6. PDF 文件输出到 translated/pdf/
7. Markdown 文件输出到 translated/markdown/
8. 图片输出到 translated/images/
```
