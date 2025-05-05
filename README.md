# EbookManager 📚
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

本项目为基于 Python 构建的电子书管理目录网站项目。通过该项目，用户可以轻松地从 Excel 文件中读取电子书信息，并将其展示在一个美观且功能丰富的网页上。项目提供了书籍搜索、分类浏览、标签筛选等功能。

## 主要功能

- **数据读取**：从 Excel 文件中读取电子书的详细信息，包括书名、作者、出版社、出版日期、分类和标签等。
- **网页展示**：基于 Jinja2 及 Bootstrap5 创建网页，将电子书基本信息以卡片式布局展示在网页上。
- **书籍搜索**：提供搜索框，允许用户按书名、作者、出版社或标签检索电子书。
- **分类展示**：通过侧边栏展示书籍的所属类型，用户可以通过分类列表查看不同类型的书籍。
- **打开电子书**：通过书籍分类及名称匹配文件路径，单击网页中书籍卡片中的按钮即可打开电子书文件。

## 使用教程

1. 准备包含电子书信息的 Excel 文件 (`ebooks.xlsx`)，确保其包含以下列：书名、作者、出版社、出版年份、类别和标签，并将其与 `generate_ebook_website.py` 和 `ebook_template.html` 放置在同一目录下。

2. 根据书籍类别及名称，将书籍 PDF 文件保存至正确的文件夹。例如【地理】分类的《地理信息系统》一书应以【地理信息系统.pdf】的名称保存至与代码文件同一目录下的【地理】文件夹中。

3. 确保已安装 Python 3.6 或更高版本。

4. 安装项目所需的 Python 依赖库：`pandas` 和 `Jinja2`。可以使用以下命令安装：
   ```bash
   pip install pandas Jinja2
   ```

5. 运行 Python 脚本：
   ```bash
   python generate_ebook_website.py
   ```

6. 打开生成的 `ebooks.html` 文件，即可在浏览器中查看电子书管理网页。

## 技术栈

- **核心框架**：Python 3.8+
- **数据处理**：pandas + re
- **网页生成**：Jinja2 + Bootstrap5

## 项目结构

- **generate_ebook_website.py**: Python 脚本，用于读取 Excel 文件并生成电子书 HTML 网页。
- **ebook_template.html**: HTML 模板文件，定义了电子书管理网页的结构和样式。
- **ebooks.xlsx**：Excel 文件，存储电子书信息（需自行创建或准备）。
- **ebooks.html**：生成的输出文件，包含电子书管理网页内容。
- **书籍存储目录**：按照自定义书籍分类创建不同文件夹目录对书籍进行存储，以便于在生成的网页文件中直接找到并打开所需的电子书文件。
