# FOSTER-
机器学习课程期末大作业 方向一持续学习 FOSTER论文复现代码

## 环境要求
**pytorch1.8 python3.8 与pytroch版本和GPU型号相对应的CUDA和cudnn**

可以参照下面的超链接:

- [torch](https://github.com/pytorch/pytorch)
- [torchvision](https://github.com/pytorch/vision)
- [tqdm](https://github.com/tqdm/tqdm)
- [numpy](https://github.com/numpy/numpy)

## 训练指令

**在训练前，需要终端cd到FOSTER目录下，然后执行下面的指令，进行对应的训练**

- 训练 CIFAR-100

b0inc10代表初始0类、增量10类，b50inc10代表初始50类、增量10类，以此类推
  ```
  python main.py --config=./configs/cifar/b0inc10.json
  ```
- 训练 ImageNet-100

  ```
  python main.py --config=./configs/foster-imagenet100.json
  ```
- 训练 FOSTER-RMM

  ```
  python main.py --config=./configs/foster-rmm.json
  ```
  
  **注意，每个json文件，例如foster-imagenet100.json，都可以自行修改训练配置参数，实现自定义的训练。**

**对于CIFAR100的训练，只需执行对应的指令即可自动下载CIFAR100数据集，并进行训练；或者将已经下载好的数据集放入data文件夹，再执行指令进行训练**

**若要使用ImageNet100训练，代码不提供自动下载数据集功能，需要自行下载，并将utils/data.py中ImageNet类的地址变量改为数据集的存放位置，再执行指令进行训练**
