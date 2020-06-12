# rural_road_extraction_unet_vgg
农村道路提取（Unet和vgg-unet实现）
====
本项目主要通过unet和迁移学习(vgg16+unet)两种方式来实现语义分割，对遥感影像中的农村道路进行提取。通过迁移vgg-16卷积层的权值作为图像特征编码器到unet中来构建结合迁移学习改进的unet,其网络结构如下：
![Image text](https://github.com/hq-hub/rural_road_extraction_unet_vgg/blob/master/image/data.PNG)
## 项目文件介绍
data.ipynb：读取图片将图片转化为numpy数组存放在npy_data文件夹中；  
unet.ipynb：训练unet;
VGG_Unet.ipynb:训练结合vgg-16进行迁移学习的unet;
predict.ipynb:使用训练好的unet对道路图片进行提取测试,将测试结果保存在results文件夹中；
predict_vggunet.ipynb：使用训练好的迁移学习改进的unet对道路图片进行提取测试，将测试的结果保存在results_vgguent文件夹中；
pre_data.ipynb:主要是对原始遥感影像进行一些随机裁剪和数据增强等操作；
pos_process.ipynb:后处理，对预测的结果进行数学形态学优化，绘制loss_acc变化图,进行精度评价等；

mytensotboard文件夹：用于存放unet训练过程中tensorboard记录的一些数据，方便对模型的loss值和acc值的变化进行观察；
mytensorboard_vggunet文件夹：用于存放结合迁移学习改进的unet训练过程中tensorboard记录的一些数据，方便对模型的loss值和acc值的变化进行观察；
npy_data文件夹：存放data.ipynb运行后产生的numpy数组文件；
orig_data文件夹：存放原始的数据，测试集，训练集等；
results文件夹：保存unet预测的结果；
results_vggunet文件夹：保存结合迁移学习改进的unet的预测结果；
## 使用说明
1、运行data.inpynb:生成numyp数组创建训练数据；2、运行分别unet.ipynb,VGG_unet.inpynb分别对unet和结合迁移学习改进的unet进行训练；3、分别运行predict.ipynb、predict_vggunet.ipynb分别使用训练后的模型进行预测
## 注意
1、本项目使用的为python3，keras使用tensorflow做为backend；
2、本项目使用的数据集为自行制作，需要自取：* [data](https://pan.baidu.com/s/1qrW9DS9gcaUf_6zEadvrVQ )，提取码：elno
数据集中部份数据如下：
![Image text](https://github.com/hq-hub/rural_road_extraction_unet_vgg/blob/master/image/data.PNG)
3、unet的搭建主要参考了：* [U-net：运行你的第一个U-net进行图像分割](https://blog.csdn.net/awyyauqpmy/article/details/79290710)







