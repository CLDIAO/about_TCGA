# 1.	少量数据的下载：

![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319001.png)
 
在repository页面检索右下方框框内的数据可以加入购物车。添加完成后，选择右上角购物车图标

![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319002.png)
 
下载文件的方法有两种：manifest,需要使用GDC Data Transfer Tool以下载大量数据（>50M）；Cart,小量文件通过浏览器直接下载。

# 2.	使用GDC Data Transfer Tool批量下载

![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319003.png)

 下载合适版本客户端，如win。下载后放在合适的存储位子，解压后得到应用程序，无需安装。右键我的电脑-属性-高级系统设置-环境变量
 
 ![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319004.png)
 
新建：变量名-path，变量值-下载的客户端所在位置，点击确定（三个）。

![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319005.png)
 
Win +R – cmd ，输入

`gdc-client –h`

![](https://github.com/CLDIAO/about_TCGA/blob/master/photos/0319006.png)

设置完成。
在页面下载manifest，得到.txt文件。
进入下载目录，
运行

`gdc-client download –m D:/GDC/gdc_manifest_20180319_113132.txt`

# 3.	R包下载-

## RTCGAToolbox

#try http:// if https:// URLs are not supported
 
`source("https://bioconductor.org/biocLite.R")`

`biocLite("RTCGAToolbox")`

安装R包RTCGAToolbox。

`library("RTCGAToolbox")`

`getFirehoseDatasets()`
#查看肿瘤类型

` [1] "ACC"      "BLCA"     "BRCA"     "CESC"     "CHOL"     "COADREAD" "COAD"     "DLBC"     "ESCA"     "FPPP"     "GBMLGG"   "GBM"      "HNSC"     "KICH"    
[15] "KIPAN"    "KIRC"     "KIRP"     "LAML"     "LGG"      "LIHC"     "LUAD"     "LUSC"     "MESO"     "OV"       "PAAD"     "PCPG"     "PRAD"     "READ"    
[29] "SARC"     "SKCM"     "STAD"     "STES"     "TGCT"     "THCA"     "THYM"     "UCEC"     "UCS"      "UVM"  `   

`getFirehoseRunningDates()`
#查看数据库更新

`getFirehoseRunningDates(last = 2)`
#查看最近的两个

`getFirehoseData(dataset = "COAD", runDate = "20160128", RNASeqGene = TRUE, clinical = TRUE, mRNAArray = TRUE)`
#可查看使用帮助

## R包cgdsr



