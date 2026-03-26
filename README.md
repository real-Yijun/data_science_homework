# data_science_homework
这个仓库用于存储 **Data Science for Finance** 课程的作业。

每一次作业都会作为一个相对独立的小项目进行整理，并放在单独的文件夹中。  

每个项目通常包含项目说明、数据处理过程、分析代码、结果输出，以及必要的图表和表格。

This repository is used to store coursework for the **Data Science for Finance** course.

Each homework assignment is organized as an independent project in its own folder.  
A typical project includes documentation, data processing, analysis notebooks, output results, and supporting figures or tables.

---

## 仓库结构 / Repository Structure

每个作业会放在一个单独的文件夹中，例如：  
Each assignment is stored in a separate folder, for example:

```text
topic01_beta/
├── README.md                    # 数据说明、运行环境、主要结论摘要 / project overview, environment, and key findings
├── 01_data_download.ipynb       # 数据下载与预处理 / data download and preprocessing
├── 02_beta_estimation.ipynb     # Beta 估计（全样本、分年度、滚动） / beta estimation (full sample, yearly, rolling)
├── 03_portfolio_analysis.ipynb  # 相关性分析与投资组合构建 / correlation analysis and portfolio construction
├── data_raw/                    # 原始下载数据 / raw downloaded data
├── data_clean/                  # 清洗后数据 / cleaned data
└── output/                      # 输出图形和表格 / output figures and tables
````

---

## 主要用途 / Purpose

这个仓库主要用于：
This repository is mainly used to:

* 存储课程作业
  Store coursework assignments

* 将每个主题整理为独立项目
  Organize each topic as a self-contained project

* 记录从数据获取、清洗到分析和结果展示的完整流程
  Document the full workflow from data collection and cleaning to analysis and results

* 规范整理 notebook、数据文件、图表和表格
  Keep notebooks, datasets, figures, and tables well organized

---

## 项目组织说明 / Project Organization

每个作业文件夹通常包含：
Each homework folder may contain:

* 项目级 `README.md`，用于说明研究问题、数据来源、方法和结论
  A project-level `README.md` describing the research question, data source, methods, and findings

* 一个或多个 Jupyter notebooks
  One or more Jupyter notebooks

* 原始数据与清洗后数据
  Raw and cleaned datasets

* 分析结果输出，例如图表、回归结果和汇总表
  Output results such as figures, regression results, and summary tables

---

## 备注 / Notes

* 本仓库中的内容主要用于课程学习与实践。
  The contents of this repository are mainly for course learning and practice.

* 文件夹命名通常采用主题编号形式，例如 `topic01_beta`。
  Folder names usually follow a topic-based naming convention, such as `topic01_beta`.

* 随着课程推进，后续作业会持续更新到这个仓库中。
  More projects will be added to this repository as the course progresses.
