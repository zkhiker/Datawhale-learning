# 学习目标
• 掌握常见的评价函数和损失函数 Dice、IoU、BCE、Focal Loss、Lovász-Softmax； 
• 掌握评价/损失函数的实践；

# TP TN FP FN
• TP(真正例 true positive) 
• TN(真反例 true negative) 
• FP(假正例 false positive) 
• FN(假反例 false negative)
在分类问题中，我们经常看到上述的表述方式，以二分类为例，我们可以将所有的样本预测结果分成 TP、TN、FP、FN 四类，并且每一类含有的样本数量之和为总样本数量，即 TP+FP+FN+TN= 总样本数量。其混淆矩阵如
下:
<table>
    <tr>
        <th rowspan="2" >真实情况</th>
        <th colspan="2" >预测结果</th>
    </tr>
    <tr>
        <td>正例</td>
        <td>反例</td>
    </tr>
    <tr>
        <td>正例</td>
        <td>TP（真正例）</td>
        <td>FN（假反例）</td>
    </tr>
    <tr>
        <td>反例</td>
        <td>FP（假正例）</td>
        <td>TN（真反例）</td>
    </tr>
</table>

上述的概念都是通过以预测结果的视角定义的，可以依据下面方式理解：
• 预测结果中的正例 在实际中是正例 的所有样本被称为真正例（TP）< 预测正确 > 
• 预测结果中的正例 在实际中是反例 的所有样本被称为假正例（FP）< 预测错误 > 
• 预测结果中的反例 在实际中是正例 的所有样本被称为假反例（FN）< 预测错误 > 
• 预测结果中的反例 在实际中是反例 的所有样本被称为真反例（TN）< 预测正确 >

# 语义分割任务
将语义分割看作是对每一个图像像素的的分类问题。根据混淆矩
阵中的定义，我们亦可以将特定像素所属的集合或区域划分成 TP、TN、FP、FN 四类。

# Dice 评价指标

## Dice 系数
看不懂

## Dice Loss
看不懂

# IoU 评价指标
看不懂

# BCE 损失函数
看不懂

# Focal Loss
看不懂

# Lovász-Softmax
看不懂

# 待解决问问题
1. 补数学基础
