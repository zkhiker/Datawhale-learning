# 示例代码
https://tianchi.aliyun.com/notebook-ai/detail?spm=5176.12586969.1002.3.67127c94J7yxsB&postId=170488

# 目标
• 理解基础的数据扩增方法
• 学习 OpenCV 和 albumentations 完成数据扩增
• Pytorch 完成赛题读取

# 数据扩增

## 意义
数据扩增是一种有效的正则化方法，可以防止模型过拟合，在深度学习模型的训练过程中应用广泛。数据扩增的目的是增加数据集中样本的数据量，同时也可以有效增加样本的语义空间。

## 注意
1. 不同的数据，拥有不同的数据扩增方法；
2. 数据扩增方法需要考虑合理性，不要随意使用；
3. 数据扩增方法需要与具体任何相结合，同时要考虑到标签的变化；

## 图像扩增分类
1. 标签不变的数据扩增方法：数据变换之后图像类别不变；
2. 标签变化的数据扩增方法：数据变换之后图像类别变化；

# OpenCV 数据扩增
OpenCV 是计算机视觉必备的库，可以很方便的完成数据读取、图像变化、边缘检测和模式识别等任务。

# albumentations 数据扩增

# Pytorch 数据读取
看代码只加载了train_mask.csv的数据，train目录的图片没用到。需要继续理解代码。TODO

# 解决的问题
1. 示例代码调通，主要是包安装，路径不对；
2. plt.imshow(cv2.flip(img, 0).squeeze()) 示例代码少了squeeze()的调用，出现异常；

# 待解决问题
1. OpenCV的随机裁剪调用失败，需要继续查资料看源码：TypeError: Invalid shape (0, 8, 256) for image data；
2. OpenCV的垂直和水平翻转结果无区别，需要检查API是否正确调用，或者参数错误；
3. albumentations的错误：ValueError: Requested crop size (256, 256) is larger than the image size (1, 256)；
3. 
