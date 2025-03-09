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



# 4. Kalman Example
功能：
-  依据ETF的价格，使用Kalman 方程来进行模拟
-  Kalman方程最核心的是transition matrix、observation matrix
-  如果observation matrix会发生变化，则只能使用update函数循环进行kalman匹配
-  对比rollingOls，最后按照return rate计算出来的beta、alpha结果相差不大


# 5.  HMM Example
功能：
-  使用收益率、成交量、波动率构建观察变量
-  通过观察到的变量推测市场处于的状态
-  通过状态转移矩阵与当前状态推测下一阶段的状态
-  不同的状态有不同的均值，在不同的状态下可以设置不同的组合暴露


# 6.  LightBGM
功能：
- 使用因子、历史收益率、波动率进行建模
- 确定未来10天是否大于1%的涨幅作为判断label
- 使用LightBGM进行二分类
- 判断未来10天涨幅是否大于1%

# 7.  Moving Average
功能：
- 通过检测不同时期的利差，通过利差的均值回归属性来投资
- 长期、中期、短期综合评估
- 综合考虑起始周期对后续的影响
- 观察时需要观测不同周期的情况

# 8.  RSI
功能：
- 计算RSI
- RSI实际是价格的显示，比价格的波动要剧烈，周期是一致的
- 对比价格均线差、成交量均线差
- 市场价格是按照均线差行动

