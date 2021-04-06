# classification_Pytorch_Proj-master
#### Classification Project based on Pytorch
####这是一份基于Pytorch的分类代码，用于deep-learning、Pytorch的学习。
#### 相关信息
    开始日期：2019.6.9
#### 环境要求
    Pytorch1.0+
    tensorboardX
    yaml
    easydict
    Some other libraries (find what you miss when running the code. hhhhh~)
#### 实现模型
    LeNet
    AlexNet
    ResNet
#### 数据准备
    1.cifar10:
    直接运行训练代码即可，可以自行下载解压；
    介绍：
    CIFAR-10数据集：
	CIFAR-10数据集包含10个类别的60000个32X32彩色图像，其中每个类别有
	6000千张图像，有50000万张训练图像和10000张测试图像
    数据集是分为5个训练批次和一个测试批次，每个批次具有10000张图像。测试批次包含
    每个类别中恰好1000个随机选择的图像。训练批次按随机顺序包含其余图像。但是某些
    训练批次可能包含比另一类更多的图像。在他们之间训练批次包含全部的5000张图像的
    对于这个数据集主要是对应的这10个类别
    飞机，汽车，鸟，猫，鹿，狗，青蛙，马，船，卡车这些类之间完全是互斥的
    。汽车和卡车之间是没有重叠。“汽车”包括轿车，越野车和类似的东西
    卡车是仅包括大型卡车，是不包含皮卡车的。
    
#### 预训练模型
    需要的预训练模型会自动下载在.cache/torch下；
#### 使用方法
    实验名在exp_configs文件夹下以文件夹名体现；
    模型输出在exp_output，在classification_pytorch_Proj-master路径下新建一个exp_output，
    内新建对应的实验名文件夹;
    运行方法是先在exp_configs里做好实验配置，再运行指定好的train.py文件。
####  解释
       首先是这个代码是从train.py来开始运行这段代码，文件所有的配置信息的都是在exp_configs/cifar10_lenet下
       的文件夹中，当然我们这里命名其实应该是cifar10_resnet152而不是使用lenet网络来进行训练我们使用的resnet152
       网络来进行训练的。，其中trainer.py是主要的运行的代码的。起着一个中央控制的作用，其中我们在运行代码的时候是首先
       输出resnet_152参数架构的。然后才开始输出相应的训练和验证的过程的。并且我们在进行输出相应的信息的时候，在会console
       输出相应的信息的，并且会在exp_output输出相应的日志文件log.txt,exp_output本来是你需要自己创建的，但是这里我帮你
       创建了。
####  重要
       本文所出现的注释都是都是自己所书写的注释，## 出现两个这个符号的是自己所书写的注释，# 出现一个的是原文中所带的注释
       现在我也是在开始学习的过程中也是在一点一点学习，所以我的注释是不一定准确的。所以请浏览者注意
