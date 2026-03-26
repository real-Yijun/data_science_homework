# A 股个股 Beta 系数估计与投资组合分析（topic01_beta）

## 1. 项目说明
本项目基于 CAPM 框架，完成 5 只 A 股股票的系统性风险（Beta）估计与等权组合分析，覆盖：
- 数据下载与清洗
- 收益率统计特征与正态性检验
- 全样本、分年度、滚动 Beta 估计
- 相关性结构与组合绩效评估
- （选做）均值-方差与有效前沿

## 2. 股票信息
按作业要求覆盖不同行业（银行、消费、科技、医药、能源等）。本项目使用以下 5 只股票。

| 序号 | 股票代码(symbol) | 股票名称(name) | 行业(industry) |
|---|---|---|---|
| 1 | 600036 | 招商银行 | 银行 |
| 2 | 600519 | 贵州茅台 | 消费 |
| 3 | 002475 | 立讯精密 | 科技 |
| 4 | 600276 | 恒瑞医药 | 医药 |
| 5 | 601088 | 中国神华 | 能源 |

`STOCKS` 填写示例格式：

```python
STOCKS = [
  {"symbol": "600036", "name": "招商银行", "industry": "银行"},
  {"symbol": "600519", "name": "贵州茅台", "industry": "消费"},
  {"symbol": "002475", "name": "立讯精密", "industry": "科技"},
  {"symbol": "600276", "name": "恒瑞医药", "industry": "医药"},
  {"symbol": "601088", "name": "中国神华", "industry": "能源"}
]
```

## 3. 数据范围
- 起始日期：2019-01-01
- 截止日期：运行当日
- 市场基准：沪深300指数（`000300`）
- 无风险利率：年化 2.5%，日频换算 $r_f=0.025/252$

## 4. 项目结构

```text
topic01_beta/
├── README.md
├── 01_data_download.ipynb
├── 02_beta_estimation.ipynb
├── 03_portfolio_analysis.ipynb
├── data_raw/
├── data_clean/
└── output/
```

## 5. 运行环境
- Python 3.10+（推荐 3.11）
- 主要依赖：
  - akshare
  - pandas
  - numpy
  - scipy
  - statsmodels
  - matplotlib
  - seaborn
  - jupyter

建议安装命令：

```bash
pip install akshare pandas numpy scipy statsmodels matplotlib seaborn jupyter
```

## 6. 运行顺序
请按以下顺序执行全部单元：
1. `01_data_download.ipynb`
2. `02_beta_estimation.ipynb`
3. `03_portfolio_analysis.ipynb`

## 7. 输出结果说明
运行后，主要结果会保存到 `output/`：
- `descriptive_stats.csv`
- `returns_timeseries.png`
- `full_sample_capm.csv`
- `residual_diagnostic_tests.csv`
- `annual_beta_2019_2024.csv`
- `annual_beta_line.png`
- `rolling_beta_60d.csv`
- `rolling_beta_60d_events.png`
- `rolling_beta_stability.csv`
- `stock_correlation_matrix.csv`
- `stock_correlation_heatmap.png`
- `rolling_pair_corr_60d.csv`
- `rolling_pair_corr_60d.png`
- `portfolio_daily_returns.csv`
- `portfolio_performance_metrics.csv`
- `portfolio_beta_comparison.csv`
- `portfolio_nav_vs_hs300.png`
- （可选）`optional_efficient_frontier.png`

## 8. 主要发现（基于本次运行结果）
1. 全样本 Beta 显示科技股立讯精密（002475）最高（$\beta=1.337$），能源股中国神华（601088）最低（$\beta=0.294$），行业风险暴露差异明显。
2. 分年度上，2021 年多数股票 Beta 抬升（如贵州茅台从 2020 年 $0.837$ 升至 2021 年 $1.292$），2024 年招商银行降至 $0.581$，体现 Beta 的时变性。
3. 滚动 Beta 稳定性排序中，002475 波动最大（rolling beta 标准差 $0.356$），601088 最稳定（$0.203$）。
4. 相关性方面，样本期内最高相关组合为招商银行-贵州茅台（$0.478$），最低为立讯精密-中国神华（$0.024$），跨行业配置仍有分散化价值。
5. 等权组合年化收益率 $14.43\%$、年化波动率 $19.18\%$、最大回撤 $-35.08\%$、夏普比率 $0.622$；组合 Beta 为 $0.838194$，与个股 Beta 均值几乎完全一致（差值约 $1.11\times10^{-16}$），验证了等权条件下 Beta 可加性。

## 9. 提交前检查
- 已填写 5 只股票代码、名称、行业，并成功下载数据。
- 三个 Notebook 均可从头完整运行，图表标题/坐标轴/图例完整。
- 每部分结果后有简短文字解释（已在 Notebook 中预留“分析建议”单元）。
- 打包提交 `topic01_beta` 文件夹为 `.zip`。
