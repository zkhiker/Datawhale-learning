# 数据与背景
比赛地址：https://tianchi.aliyun.com/competition/entrance/531872/introduction

开源内容：https://github.com/datawhalechina/team-learning-cv/tree/master/AerialImageSegmentation

# 目标
*  理解赛题背景和赛题数据
*  完成赛题报名和数据下载，理解赛题的解题思路
*  比赛baseline构建

# 数据

## train.zip
是模型训练数据，一张张原始图片。

## train_mask.csv
包含了train.zip中的图片，第一列为图片名，后面的数据不清楚是什么含义，来自哪里。
看了代码示例，应该是RLE编码结果。但为什么是第一列的值？还是理解错误？print(rle_encode(mask) == train_mask['mask'].iloc[0]) 为True。
打印出来了结果，文件名在第一列，后面所有的列都是train_mask内容。看python源码也会有帮助。

## test_a.zip
测试数据集，模型训练出来后用这个来验证模型。 TODO

## test_a_samplesubmit.csv
测试结果。TODO

# 思路
1. 对文件进行RLE编码；就是打标签；（读教学文档再次感悟：具体的标签为图像像素类别，分为有无两种情况）
2. 一部分作为训练模型数据，一部分为校验数据；

# baseline
未完成：
1. 无python基础；-- 边写边学，对我来说不难。
2. 不熟悉库；-- 看文档和源码
3. 只了解监督型训练模型的流程，对此主题不了解；
4. 需要补充基础知识；

# 解决的问题
## 数据集添加
Jupyter 新建文件不能添加比赛的数据集，通过下面的链接创建项目直接有数据集，打开jupyter文件即可直接下载使用。 
https://tianchi.aliyun.com/competition/entrance/531872/notebook

## 完善资料失败，报不了名
登录后，点击参赛链接，跳转到完善资料页面。在验证手机号的时候，不能把手机号码赋值到最后的提交表单，导致提交资料的时候一直报“手机号不能为空”。
解决方法：重新登录，先完善资料再报名参赛。

## 本地用阿里云的源
不管在Idea还是JupyterLab中都方便很多。DSW总是保存不了。

# 待解决问题
1. 图片的像素也是语义？
2. DSW出错，保存不了代码。 -- 改用Idea或Anaconda的JupyterLab。
3. print(rle_encode(mask) == train_mask['mask'].iloc[0]) 为True不理解。 -- 输出数据内容，发现是train_mask是cvs中除第一列的其他所有的列。
4. 训练模型的代码好短，没发现数据传入的地方。 TODO
5. FCN模型是什么？和语义分析有什么关系？
6. 优化、损失函数不懂，不知道该用在哪里。
7. 深度学习还是机器学习，也要打标签？
