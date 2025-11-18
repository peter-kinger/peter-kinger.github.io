---
title: 'PyTorch入门笔记：从安装到第一个神经网络'
date: 2024-01-10
permalink: /posts/2024/01/pytorch-getting-started/
tags:
  - PyTorch
  - Deep Learning
  - Tutorial
  - 中文
categories:
  - tutorial
excerpt: '本文记录了 PyTorch 框架的入门学习过程，包括安装配置、基本概念和构建第一个神经网络的完整步骤。'
---

# PyTorch 入门指南

这是我在学习 PyTorch 过程中整理的笔记，适合初学者快速上手。

## 1. 安装 PyTorch

首先访问 [PyTorch 官网](https://pytorch.org/) 选择适合你的版本：

```bash
# CPU 版本
pip install torch torchvision

# GPU 版本 (CUDA 11.8)
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```

## 2. 基本概念

### 2.1 Tensor（张量）

Tensor 是 PyTorch 中的基本数据结构，类似于 NumPy 的 ndarray：

```python
import torch

# 创建张量
x = torch.tensor([[1, 2], [3, 4]])
print(x)
```

### 2.2 自动微分

PyTorch 的自动梯度计算功能：

```python
x = torch.tensor([2.0], requires_grad=True)
y = x ** 2
y.backward()
print(x.grad)  # 输出: tensor([4.])
```

## 3. 构建第一个神经网络

```python
import torch.nn as nn

class SimpleNet(nn.Module):
    def __init__(self):
        super(SimpleNet, self).__init__()
        self.fc1 = nn.Linear(10, 5)
        self.fc2 = nn.Linear(5, 1)
    
    def forward(self, x):
        x = torch.relu(self.fc1(x))
        x = self.fc2(x)
        return x

# 创建模型
model = SimpleNet()
print(model)
```

## 4. 训练流程

完整的训练流程包括：

1. **定义模型**
2. **准备数据**
3. **定义损失函数和优化器**
4. **训练循环**

```python
# 损失函数和优化器
criterion = nn.MSELoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.001)

# 训练循环
for epoch in range(100):
    # 前向传播
    outputs = model(inputs)
    loss = criterion(outputs, targets)
    
    # 反向传播
    optimizer.zero_grad()
    loss.backward()
    optimizer.step()
```

## 5. 资源推荐

* [PyTorch 官方教程](https://pytorch.org/tutorials/)
* [Deep Learning with PyTorch](https://pytorch.org/assets/deep-learning/Deep-Learning-with-PyTorch.pdf)
* [PyTorch 中文文档](https://pytorch-cn.readthedocs.io/)

## 小结

PyTorch 是一个强大且易用的深度学习框架，掌握基本概念后就可以开始实践各种模型了！

---

**下一篇预告：** 使用 PyTorch 实现卷积神经网络（CNN）

