---
title: 'ICIG 2023 Conference Notes: Hyperspectral Image Processing'
date: 2024-03-15
permalink: /posts/2024/03/icig2023-conference-notes/
tags:
  - Conference
  - Hyperspectral Imaging
  - Computer Vision
  - ICIG
categories:
  - research
excerpt: 'My notes and reflections from attending ICIG 2023, focusing on hyperspectral image processing and super-resolution techniques.'
---

# ICIG 2023 参会笔记

参加 International Conference on Image and Graphics (ICIG 2023) 的一些记录和思考。

## 会议概况

* **时间：** 2023年11月
* **地点：** 中国
* **主题：** Image and Graphics Processing
* **我的论文：** Hyperspectral Image Super-Resolution using CoDenNet

## 印象深刻的研究

### 1. Vision Transformers in Remote Sensing

Keynote speaker 介绍了 Transformer 架构在遥感图像中的应用，相比传统 CNN：
- 更好的长距离依赖建模
- 适合大尺度遥感图像处理
- 但计算成本较高

**启发：** 可以尝试将 Transformer 引入高光谱图像重建任务。

### 2. Self-Supervised Learning for Image Restoration

有多个 paper 探讨了自监督学习在图像恢复中的应用：
- 不需要配对的训练数据
- 适合真实场景应用
- 性能接近监督方法

**相关工作：**
- Noise2Noise
- Blind2Unblind
- Self2Self

### 3. Efficient Network Design

轻量级网络设计是热门方向：
- MobileNet variants
- EfficientNet
- 知识蒸馏技术

## 关于我的报告

### 主要内容

介绍了 **CoDenNet** (Coupled Dense Convolutional Network)：
1. 无监督高光谱超分辨率重建
2. 密集卷积网络 + 自编码器架构
3. 在基准数据集上的性能提升

### 收到的反馈

**积极反馈：**
- ✅ 无监督方法很有实用价值
- ✅ 网络架构设计合理
- ✅ 实验结果令人信服

**建议改进：**
- 🤔 可以考虑加入注意力机制
- 🤔 在更多数据集上验证泛化能力
- 🤔 分析计算复杂度和推理速度

## 下一步研究方向

基于会议交流，我计划：

1. **短期目标：**
   - 实现轻量级版本的 CoDenNet
   - 添加注意力机制模块
   - 在更多高光谱数据集上测试

2. **长期目标：**
   - 探索 Transformer 在高光谱处理中的应用
   - 研究自监督学习方法
   - 开发端到端的高光谱图像处理系统

## 有用的资源

会议上获得的一些资源链接：
- [Awesome Hyperspectral Imaging](https://github.com/...)
- [Hyperspectral Datasets](https://...)
- [相关论文合集](https://...)

## 感想

这次会议收获很大，不仅展示了自己的工作，还学习到了很多前沿技术。与其他研究者的交流也让我对未来的研究方向有了更清晰的认识。

期待明年的 ICIG 2024！

