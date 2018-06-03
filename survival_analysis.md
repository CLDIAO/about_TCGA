这里将记录我对于生存分析的学习。

# 分析资料：

## 估计：Kaplan-Meier法

乘积极限法，一种非参数法，适用于小样本和大样本。

## 比较：log-rank检验进行组建生存率的比较

非参数检验，用于比较两组或多组生存曲线或生存时间是否相同。
单因素分析。
要求各组生存曲线不能交叉，如果交叉提示存在混杂因素，应采用分层分析方法或多因素方法来矫正。
检验统计量为卡方。
p=<0.05,则生存曲线不同；p>0.05，生存曲线差别无统计学意义。


## 影响因素分析：Cox比例风险回归模型

优点：多因素分析方法、不考虑生存时间分布、利用截尾数据。


## 预测：Cox回归模型预测生存率


一般谈论的生存分析，说的是KM方法估计生存函数，并且画出生存曲线，然后可以根据分组检验
生存曲线是否有显著性差异。


# 方法一：生信人小工具(https://www.shengxin.ren/article/209)

## 1 选择下载数据集

在TCGA简易下载工具中选择需要下载的数据集，双击进行检索

## 2 选择下载的资源

检索完成后，选择需要的资源

## 3 下载

点击下载HTseq-FPKM并选择存储位置

## 4 数据合并

下载完成后，点击合并文件

## 5 数据归一化

使用数据归一化工具，将FPKM数据转换为TPM 

[STATQUEST-TPM/FPKM/RPKM](https://statquest.org/2015/07/09/rpkm-fpkm-and-tpm-clearly-explained/)

[菜鸟团-TPM/FPKM/RPKM](http://mp.weixin.qq.com/s?__biz=MzUzMTEwODk0Ng==&mid=2247485311&idx=1&sn=5bf43f27567b3ab679affe55a4e8e424&chksm=fa46c242cd314b541e02aa49dee1172cf4c59817720338db60718475a55be497358aad00a033&mpshare=1&scene=1&srcid=0603UgHm35LJc7rzG9NBq7rq#rd)

## 6 ID转换

使用便捷ID转换器，转换得到编码基因表达矩阵：选择需转换文件即4中得到的matrix；文件包含表头；多对一处理选择；转换方式；
转换导出。可以查找目的基因对应样本的表达量

## 7 下载clinical数据

下载资源选择clinical，下载完成后，选择合并文件。此数据集包含156种随访信息，我们需要其中的"bcr_patient_barcode", "days_to_death", "days_to_last_followup"，"vital_status".

## 8 



![](http://www.bio-info-trainee.com/1313.html)
