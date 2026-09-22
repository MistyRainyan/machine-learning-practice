# Machine Learning Practice

本项目记录机器学习课程的算法实践过程，通过 Python 完成机器学习基础流程以及经典机器学习算法的实现与实验。

项目将按照课程章节持续更新，包括机器学习概述、KNN、朴素贝叶斯、线性回归、感知机、逻辑回归、决策树、支持向量机以及集成学习等内容。

## 实验环境

- Python 3.x
- Jupyter Notebook / JupyterLab
- NumPy
- Pandas
- Matplotlib
- scikit-learn

## 实验目录

| 周次 | 实验内容 | 状态 |
| --- | --- | --- |
| Week 01 | 从数据到预测：完整机器学习流程实践 | ✅ 已完成 |
| Week 02 | KNN | 待完成 |
| Week 03 | 朴素贝叶斯 | 待完成 |
| Week 04 | 线性回归 | 待完成 |
| Week 05 | 感知机 | 待完成 |
| Week 06 | 逻辑回归 | 待完成 |
| Week 07 | 决策树 | 待完成 |
| Week 08 | 支持向量机 | 待完成 |
| Week 09 | 集成学习 | 待完成 |

---

# Week 01：从数据到预测——完整机器学习流程实践

## 1. 实验目的

本实验以经典 Iris 鸢尾花分类任务为例，完成一个机器学习分类任务从数据加载到模型评价的完整流程。

通过实验理解以下机器学习基本概念：

- 特征（Features）
- 标签（Label）
- 训练集（Training Set）
- 测试集（Test Set）
- 模型训练（Fit）
- 模型预测（Predict）
- 模型评价（Evaluation）

## 2. 数据集

实验使用 scikit-learn 内置的 Iris 数据集。

数据集包含 150 个鸢尾花样本，共分为三个类别：

- Setosa
- Versicolor
- Virginica

每个样本包含四个特征：

1. Sepal Length
2. Sepal Width
3. Petal Length
4. Petal Width

实验任务是根据这四个特征预测鸢尾花所属的类别。

## 3. 实验流程

本实验按照以下流程完成：

1. 加载 Iris 数据集
2. 使用 Pandas 查看和分析数据
3. 对数据进行可视化
4. 将数据划分为训练集和测试集
5. 使用 Logistic Regression 训练分类模型
6. 使用测试集进行预测
7. 使用 Accuracy、混淆矩阵和分类报告评价模型
8. 分析模型的分类结果

## 4. 数据集划分

Iris 数据集共有 150 个样本。

按照 80% : 20% 的比例划分：

- 训练集：120 个样本
- 测试集：30 个样本

同时采用分层抽样，使三个类别在训练集和测试集中保持合理的类别比例。

## 5. 实验结果

模型在测试集上的分类准确率为：

**Accuracy = 96.67%**

30 个测试样本中：

- 正确分类：29 个
- 错误分类：1 个

混淆矩阵为：

| 真实类别 / 预测类别 | Setosa | Versicolor | Virginica |
| --- | ---: | ---: | ---: |
| Setosa | 10 | 0 | 0 |
| Versicolor | 0 | 9 | 1 |
| Virginica | 0 | 0 | 10 |

可以看到：

- Setosa 的 10 个样本全部分类正确；
- Versicolor 中 9 个分类正确，1 个被预测为 Virginica；
- Virginica 的 10 个样本全部分类正确。

唯一的分类错误发生在 Versicolor 和 Virginica 之间。

## 6. 分类评价

分类报告的主要结果如下：

| 类别 | Precision | Recall | F1-score |
| --- | ---: | ---: | ---: |
| Setosa | 1.00 | 1.00 | 1.00 |
| Versicolor | 1.00 | 0.90 | 0.95 |
| Virginica | 0.91 | 1.00 | 0.95 |

模型整体 Accuracy 约为 0.97。

实验结果表明，Iris 数据集中的四个特征能够较好地区分三种鸢尾花，其中 Setosa 的特征差异较为明显，而 Versicolor 和 Virginica 之间存在一定程度的特征重叠。

## 7. 实验总结

通过本次实验，完成了从数据加载、数据探索、数据可视化，到训练集与测试集划分、模型训练、预测和评价的完整机器学习流程。

本实验重点是建立对机器学习工作流程的整体认识，因此暂时将 Logistic Regression 作为分类模型使用，而不深入讨论其数学原理。后续实验将进一步学习和实现具体的机器学习算法。

## 8. 运行方式

进入项目根目录后，进入第一周实验目录：

```bash
cd 01_ml_introduction
```

启动 JupyterLab：

```bash
jupyter lab
```

在 JupyterLab 中打开：

```text
experiment.ipynb
```

依次运行 Notebook 中的代码单元即可复现实验结果。