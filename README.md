# ResNet50-CUB 鸟类分类项目

## 项目概述
本项目使用ResNet50模型对CUB（Caltech-UCSD Birds-200-2011）数据集中的鸟类进行分类。项目中涉及多个脚本，包括模型训练、测试、数据处理等内容，并使用了多种评估指标如F1分数、Precision（精确率）、Recall（召回率）以及混淆矩阵来分析模型表现。

## 文件结构
 ```bash
|-- hm1/                        # 主项目文件夹
    |-- utils/                  # 实用工具或辅助脚本文件夹
        |-- __pycache__/        # Python 缓存目录
        |-- __init__.py         # 初始化文件，使 utils 成为一个 Python 包
        |-- data_sort.py        # 数据排序脚本
        |-- load.py             # 数据加载相关功能脚本
        |-- net_cub.py          # 用于定义神经网络结构的脚本
        |-- set_seed.py         # 设置随机种子的脚本，确保实验结果可复现
        |-- train.py            # 训练神经网络的辅助函数脚本
        |-- transform.py        # 数据转换处理相关脚本
        |-- weight_init.py      # 模型权重初始化的脚本
    |-- main.py                 # 项目主脚本
    |-- net_train.py            # 用于训练神经网络模型的脚本
    |-- plot.py                 # 用于绘制结果或可视化的脚本
    |-- test.py                 # 用于测试模型或功能的脚本
```

## 文件说明

- **utils/**: 包含多个实用工具脚本，用于数据处理、网络初始化和训练辅助。
  - **__init__.py**: 使 `utils/` 成为Python包的初始化文件。
  - **data_sort.py**: 负责数据排序功能。
  - **load.py**: 数据加载脚本，负责读取训练和测试数据。
  - **net_cub.py**: 定义神经网络模型的脚本。
  - **set_seed.py**: 设置随机种子以确保实验的可复现性。
  - **train.py**: 包含神经网络训练过程中的辅助函数。
  - **transform.py**: 处理数据转换的脚本，用于数据增强或预处理。
  - **weight_init.py**: 模型权重初始化脚本，确保网络权重设置合理。

- **main.py**: 项目的主运行脚本，整合所有功能模块，启动模型训练、测试和评估流程。

- **net_train.py**: 主要用于训练ResNet50模型，对数据进行预处理，设置训练参数，并执行模型训练。

- **plot_curves.py**: 负责绘制可视化结果，包括模型的性能指标图，如Precision、Recall、F1分数图等。

- **test.py**: 负责测试模型的性能，执行分类任务，并生成评估指标。

## 模型评估
项目中使用了多种评估指标来分析模型的分类表现，包括：

1. **F1分数图**：展示了模型对每个类别的F1分数，反映了分类精度与召回率的平衡。
2. **Precision（精确率）图**：展示了每个类别的精确率，反映了模型对各类预测的准确性。
3. **Recall（召回率）图**：展示了每个类别的召回率，反映了模型对各类样本的敏感性。
4. **混淆矩阵图**：可视化了模型的分类正确率及错误分类的类别，帮助发现模型的分类误差来源。

## 运行方法
1. 克隆该仓库：
```bash
   git clone https://github.com/Cyancity27/ResNet50-CUB-.git
 ```
2. 安装所需依赖
```bash
   pip install -r requirements.txt
 ```
3. 运行主程序
```bash
   python main.py
 ```
## 评估模型性能
1. 查看微调模型在测试集上的性能指标：
```bash
   python test.py
 ```
2. 查看微调模型在训练过程中和在测试集上的各类图表结果
```bash
   python plot_curves.py
 ```
## 数据集
- 使用CUB-200-2011鸟类数据集，该数据集包含200种不同的鸟类，适用于图像分类任务。
- 数据集可以从以下链接下载：https://data.caltech.edu/records/65de6-vp158
  
    
