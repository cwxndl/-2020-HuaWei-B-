# -2020年华为杯研究生数学建模比赛B题解答-
问题一到问题四的求解（Python）
## 问题一根据题目要求正常做就OK
## 问题二特征筛选选择相关系数法与Lasso问题结合，最终筛选了30个变量（加上因变量）
## 问题三采用SVR支持向量回归算法对产品辛烷值进行预测，采用XGBoost算法对产品硫含量进行预测
## 问题四采用遗传算法进行优化，目标函数与约束条件是参考了优秀论文（本项目中的PDF）
# 缺点与不足：
- 在问题二进行特征筛选时没有考虑产品硫含量作为因变量的情况，导致筛选出来的特征变量对产品辛烷值这个变量贡献较大，对产品硫含量这个变量影响较小，在使用XGBoost算法对产品硫含量进行预测时
效果并不是特别好
- 在使用SVR模型进行预测时没有加上**PSO粒子群算法**进行参数寻优，必须手动调参，本项目中所选择的参数值未必是最优的
- 在问题四中使用遗传算法进行优化时：只是运用了传统的遗传算法进行求解，并没有对该算法进行改进，后续有时间可以继续改进
