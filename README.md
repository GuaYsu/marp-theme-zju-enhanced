# Marp 主题：ZJU-academic-enhenced

这是一个为浙江大学社区量身定制，并经过功能增强和代码优化的 Marp 演示文稿主题，通过引入分栏以便于排版，旨在成为一个功能全面、风格严谨的学术报告解决方案。


## ✨ 核心特性

- **强大的多栏布局系统**:
  - 内置基于 CSS Grid 的多栏布局系统，让复杂的图文混排变得轻而易举。
  - 支持**等宽双栏/三栏** (`.columns`, `.columns-3`)。
  - 支持多种**不等宽比例**，如 7:3, 3:7, 2:1, 1:2 (`.columns-73`, `.columns-12` 等)。
  - 支持列内元素**垂直居中** (`.columns.center`)。

- **专业的排版与风格**:
  - **经典衬线字体**: 正文采用 `Noto Serif SC` 衬线字体，赋予幻灯片经典、正式、易读的学术气质。
  - **便捷的图片对齐**: 可通过 `alt` 文本轻松实现图片的居中或右对齐。

- **代码优化**:
  - 对 CSS 进行了全面的重构和优化，遵循 DRY 原则，减少了代码冗余。
  - 合并网络请求，使用 CSS 变量，提升了主题的性能和可维护性。

## 📥 安装

1.  下载本项目中的 `zju.css` 文件，并将其放置在您的项目文件夹中。
2.  在您 Marp 项目的 YAML front-matter 中声明使用此主题：

    ```markdown
    ---
    marp: true
    theme: zju
    size: 16:9
    paginate: true
    ---
    ```

    **注意**: 如果 `zju.css` 文件不在 Markdown 文件的同一目录下，请提供正确的相对路径，例如 `theme: './themes/zju.css'`。

## 🛠️ 使用指南 (Cheatsheet)

### 1. 封面页 (Title Slide)

使用 `class: lead` 来创建一个居中对齐、引人注目的封面页。

```markdown
---
class: lead
---

# 报告的题目
## 副标题
### 报告人：CouesF
```

### 2. 多栏布局

在幻灯片中使用 `<div>` 标签来创建列。

#### 等宽双栏

````markdown
<div class="columns">
<div>

- 列表项 1
- 列表项 2
- 列表项 3

</div>
<div>

![bg right fit](image.jpg)

</div>
</div>
````

#### 7:3 左宽右窄 (文字 + 图片)

````markdown
<div class="columns-73">
<div>

#### 结论

这是一段详细的文字说明，放置在较宽的左栏。

</div>
<div>

![center](chart.png)

</div>
</div>
````

#### 垂直居中

在任意 `columns` 类上追加 `.center` 即可。

````markdown
<div class="columns center">
<div>

这段文字会垂直居中。

</div>
<div>

这张图片也会垂直居中。

![center](logo.svg)

</div>
</div>
````

### 3. 图片对齐

在图片的 `alt` 文本中加入 `center` 或 `right` 关键词。

```markdown
<!-- 居中对齐 -->
![center](path/to/image.png)

<!-- 右对齐 -->
![right](path/to/image.png)
```

### 4. 页脚注释

使用标准的 Markdown 引用语法即可创建页脚注释。

```markdown
> 参考文献 [1]: CouesF, *et al*. A Study on Marp Themes. 2024.
```

## 📜 鸣谢

- 本主题的设计灵感和部分基础来源于 [zju-academic](https://github.com/CouesF/marp-theme-zju) 主题。
- `zju-academic` 主题本身基于 [kaisugi/marp-theme-academic](https://github.com/kaisugi/marp-theme-academic)。
- 浙江大学 Logo 和品牌指南由浙江大学提供。

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE) 授权。详情请参阅 LICENSE 文件。
