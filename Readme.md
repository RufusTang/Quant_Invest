# 1. Dividend_Information.ipynb

功能：
- 在joinquant平台提取股票分红信息
- 将近几年的信息提取后输出到dividend.csv文件

# 2.Pairs_Trading.ipynb

功能：
- 设置了plt中的rcParams参数，可以进行绘图默认设置
- 研究了spread情况，增加beta和不增加beta的确有差别，时间段适当选择长一点的时间段
- 验证了是否cointegration，是否stationary
- 统计所有可选的股票，逐个进行验证


# 3. ETF_Spread.ipynb

功能：
-  针对不同ETF进行验证，小盘、大盘的ETF之间是否会存在利差
-  进行线性回归，针对线性回归确定beta和alpha，针对残差进行分析
-  残差是否符合正态分布，是否需要采用log处理
-  验证了是否cointegration，是否stationary
