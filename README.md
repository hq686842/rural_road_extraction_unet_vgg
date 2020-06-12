# rural_road_extraction_unet_vgg
农村道路提取（Unet和vgg-unet实现）
====
本项目主要通过unet和迁移学习(vgg16+unet)两种方式来实现语义分割，对遥感影像中的农村道路进行提取。通过迁移vgg-16卷积层的权值作为图像特征编码器到unet中来构建结合迁移学习改进的unet,其网络结构如下：
![Image text](https://github.com/hq-hub/rural_road_extraction_unet_vgg/blob/master/image/data.PNG)
