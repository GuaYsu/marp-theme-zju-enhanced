---
theme: zju
marp: true
paginate: true
math: latex
---

<!-- _class: lead -->

# ZJU Marp 主题演示

**你的名字**  
00114514 
2026.4.9

---

<!-- _header: 目录 -->

1.  引言与脚注
2.  代码块
3.  数学公式
4.  新功能：多栏布局
5.  图片排版
6.  结语

---

<!-- _header: 1. 引言与脚注 -->


- Marp 是一款用于使用 **Markdown** 创建 **幻灯片** 的软件。
  - 它支持基本的 Markdown 语法，如列表、加粗和斜体。
  - 本主题的设计灵感和基础来源于 [CouesF/marp-theme-zju](https://github.com/CouesF/marp-theme-zju) 主题。
  - `marp-theme-zju` 主题本身基于 [kaisugi/marp-theme-academic](https://github.com/kaisugi/marp-theme-academic)。
- 在 Markdown 中只需插入 `---` 分隔线，就能跳转到下一页。

本主题将 `<blockquote>` 样式重定义为页脚注释，适合引用参考文献或进行补充说明。¹

> ¹ 这是一个页脚注释的例子。它会自动放置在页面底部，并带有虚线上边框

---

<!-- _header: 2. 代码块 -->

```python
import torch

# 检查 CUDA 是否可用
if torch.cuda.is_available():
    print("CUDA is available! Running on GPU.")
else:
    print("CUDA not available. Running on CPU.")
```

可以这样编写代码块，并支持语法高亮。

```python
from transformers import pipeline

# 使用 pipeline 快速进行文本填充
unmasker = pipeline('fill-mask', model='bert-base-uncased')
result = unmasker("Hello I'm a [MASK] model.")
print([r['token_str'] for r in result])
# >> ['fashion', 'role', 'new', 'super', 'fine']
```

代码块的宽度和字体大小会自动调整，以适应幻灯片页面。

---

<!-- _header: 3. 数学公式 -->
支持$\LaTeX$公式

**行间公式：**
$$p(X|\omega_k) = \frac{1}{(2\pi)^{B/2}|\Sigma_k|^{1/2}} \exp\left[-\frac{1}{2}(X-\mu_k)^T \Sigma_k^{-1}(X-\mu_k)\right]$$

**行内公式：**
爱因斯坦的质能方程是 $E=mc^2$。

顺便一提，也可以使用表情符号 :smile:。

---

<!-- _header: 4.新功能：多栏布局 -->

这是本主题最强大的功能之一。它允许您轻松创建复杂的页面布局。

- **等宽双栏**: `.columns`
- **等宽三栏**: `.columns-3`
- **不等宽比例**:
  - `7:3` -> `.columns-73`
  - `3:7` -> `.columns-37`
  - `2:1` -> `.columns-21`
  - `1:2` -> `.columns-12`
- **垂直居中**: 在任何 `columns` 类上追加 `.center`

接下来我们将通过实例来展示。

---

<!-- _header: 多栏布局 - 等宽双栏 -->

使用 `<div class="columns">` 来创建一个 50:50 的双栏布局，非常适合图文并排。

<div class="columns">
<div>

#### 特点介绍

- **简洁高效**: 用 Markdown 写幻灯片。
- **功能强大**: 支持多栏布局和数学公式。
- **品牌定制**: 集成 ZJU 视觉元素。
- **跨平台**: 可导出为 PDF, HTML, PPTX。

</div>
<div>

![](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

</div>
</div>

---

<!-- _header: 多栏布局 - 不等宽与垂直居中 -->

使用 `<div class="columns-73 center">` 创建一个 7:3 的布局，并让两栏内容垂直居中。

<div class="columns-73 center">
<div>

#### 应用场景
这种左宽右窄的布局非常适合放置大段的文字说明，并在右侧配以一个关键的图表、Logo 或小尺寸图片作为补充视觉元素。

</div>
<div>

![](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

</div>
</div>

---

<!-- _header: 图片排版 -->
除了在多栏布局中放置图片，您还可以控制单张图片在页面上的对齐方式。


**左对齐:** `![center](...)`
![left h:300px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

---
<!-- _header: 图片排版 -->
除了在多栏布局中放置图片，您还可以控制单张图片在页面上的对齐方式。


**居中对齐:** `![center](...)`
![center h:300px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

---
<!-- _header: 图片排版 -->
除了在多栏布局中放置图片，您还可以控制单张图片在页面上的对齐方式。

**右对齐:** `![right](...)`
![right h:300px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

---
<!-- _header: 图片排版 -->
调节图片大小？多张图片？同样不在话下。
使用`![h:xxx](...)`调节图片高度，`![w:xxx](...)`调节图片宽度。
图片间如果不换行则在同一行显示
![h:100px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)![h:200px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)![h:300px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)![h:400px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

---
<!-- _header: 图片排版 -->
如果换行，则图片也换行
![h:100px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)![h:200px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)
![h:300px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)![h:400px](https://patchwiki.biligame.com/images/arknights/5/51/mcykogoq3phi70qshmt51bajjf5fblq.png)

---

<!-- _class: lead -->

# 谢谢！
