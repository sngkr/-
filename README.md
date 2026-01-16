# 中国科学技术大学学位论文 LaTeX 模板

[![GitHub release](https://img.shields.io/github/release/ustctug/ustcthesis/all.svg)](https://github.com/ustctug/ustcthesis/releases/latest)
[![GitHub commits](https://img.shields.io/github/commits-since/ustctug/ustcthesis/latest.svg)](https://github.com/ustctug/ustcthesis/commits/master)
[![Build](https://github.com/ustctug/ustcthesis/actions/workflows/main.yml/badge.svg)](https://github.com/ustctug/ustcthesis/actions/workflows/main.yml)

本项目是中国科学技术大学的学位论文 LaTeX 模板 ustcthesis，按照
《研究生学位论文撰写手册》（最近在修订中）
和
《[中国科学技术大学本科毕业论文（设计）格式](https://www.teach.ustc.edu.cn/?attachment_id=13867)》
的要求编写，兼容最新版的 TeX Live、MacTeX 、MiKTeX 发行版，支持跨平台使用。

注意：

1. 使用说明文档 `ustcthesis-doc.pdf` 在发布版中附带，用户也可自行编译；**使用模板前应仔细阅读**。

2. 本模板要求 TeX Live、MacTeX、MiKTeX 不低于 2017 年的发行版，
并且尽可能升级到最新。安装和升级方法见
[新手指南](https://github.com/ustctug/ustcthesis/wiki/新手指南)。

3. **不支持** [CTeX 套装](https://github.com/ustctug/ustcthesis/wiki/常见问题#3-模板支持用-ctex-套装编译吗)。


## 下载地址

- GitHub Releases：<https://github.com/ustctug/ustcthesis/releases>

- 校内镜像：<https://git.lug.ustc.edu.cn/ustctug/ustcthesis>

- TexPage 模板 <https://texpage.com/template/fe69d6fc-f811-4b8c-824f-7848a07c9551>

- Overleaf 模板 <https://www.overleaf.com/latex/templates/latex-template-for-ustc-thesis/qbfkwzbrfhbr>

- 研究生院网站（版本较旧，不推荐）：<https://gradschool.ustc.edu.cn/column/65>


## 编译文档

- 编译模板的使用说明文档 `ustcthesis-doc.pdf`：
   ```
   latexmk -xelatex ustcthesis-doc.tex
   # 论文（初始结构）

   本仓库为我的学位论文源码（初始结构），基于 `ustcthesis` 模板整理，包含章节草稿、模板文件与参考文献数据库。

   主要内容：
   - `main.tex`：主文件，使用 XeLaTeX 编译。
   - `chapters/`：章节源文件，`new/` 为当前工作稿，`history/` 为模板或历史稿。
   - `bib/ustc.bib`：BibTeX 数据库。
   - `figures/`：图像资源。

   快速编译（推荐顺序）：

   ```powershell
   xelatex -interaction=nonstopmode main.tex
   bibtex main
   xelatex -interaction=nonstopmode main.tex
   xelatex -interaction=nonstopmode main.tex
   ```

   或使用 `latexmk`（更简单）：
   ```bash
   latexmk -xelatex main.tex
   ```

   .gitignore 已添加以排除编译产生的临时文件（例如 `*.aux`、`*.log`、`*.pdf` 等）。

   远程仓库：已推送到你配置的远程（origin）。如需修改远程 URL，请提供新的仓库地址。

   贡献与备注：
   - 如果需要我继续整理章节结构或移除封面空白页，请告诉我需要的页面编号或直接上传编译后的 `main.pdf`。
   - 本仓库包含编译产物的临时文件历史，建议在本地编译后检查并删除不需要的中间文件，再提交。

   2026-01-16

