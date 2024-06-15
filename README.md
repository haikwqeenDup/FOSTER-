# FOSTER-
机器学习课程期末大作业 方向一持续学习 FOSTER论文复现代码

## 环境要求
pytorch1.8 python3.8
The following packages are required to run the scripts:

- [torch](https://github.com/pytorch/pytorch)
- [torchvision](https://github.com/pytorch/vision)
- [tqdm](https://github.com/tqdm/tqdm)
- [numpy](https://github.com/numpy/numpy)

## 训练指令

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
