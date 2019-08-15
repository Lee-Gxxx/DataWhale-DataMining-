# DataWhale-DataMining
## 数据挖掘实践任务
DataWhale DataMining Pratice 8   

### 任务 - 数据分析  
说明：这份数据集是金融数据（非原始数据，已经处理过了），我们要做的是预测贷款用户是否会逾期。  
表格中 "status" 是结果标签：0表示未逾期，1表示逾期。  
要求：数据切分方式 - 三七分，其中测试集30%，训练集70%，随机种子设置为2018  


#### 任务1：对数据进行探索和分析——时间：2天  
1.数据类型的分析  
2.无关特征删除  
3.数据类型转换  
4.缺失值处理  
5.……以及你能想到和借鉴的数据分析处理  


#### 任务2：特征衍生——时间：2天  
1.特征挑选：分别用IV值和随机森林等进行特征选择  
2.……以及你能想到特征工程处理  


#### 任务3：建立模型——时间: 2天
用逻辑回归、svm和决策树；随机森林和XGBoost进行模型构建，评分方式任意，如准确率等。（不需要考虑模型调参）


#### 任务4 - 模型评估—时间: 2天
记录5个模型（逻辑回归、SVM、决策树、随机森林、XGBoost）
关于accuracy、precision、recall和F1-score、auc值的评分表格，并画出ROC曲线。

.|正类|负类
-|-|-
**正类**|True Positives(**TP**   正类判定为正类）|false positives(**FP**   负类判定为正类）
**负类**|False Negatives(**FN**   正类判定为负类）|true negatives(**TN**   负类判定为负类）

**accuracy** = (TP + TN) / (P+N) = (TP + TN) / (TP + FN + FP + TN)     
**precision** = TP / (TP + FP)
**recall** = TP / (TP + FN)  
**F1-score** = (2 * P * R) / (P + R)  
**auc** =  处于ROC curve下方的那部分面积的大小,[0.5,1]之间。越大表示有越好的表现  
**ROC关注：**    
   True Positive Rate (**TPR**)  = TP / (TP + FN)     TPR代表能将正例分对的概率  
   False Positive Rate(**FPR**) = FP / (FP + TN)      FPR代表将负例错分为正例的概率  

#### 任务5 - 模型调优—时间: 2天  
任务5：使用网格搜索法对5个模型进行调优（调参时采用五折交叉验证的方式），并进行模型评估，记得展示代码的运行结果。 
