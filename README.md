<h1 align="center">🧬 AlphaFold2 模型架构学习笔记</h1>

<p align="center"><em>—— 2026.09.01</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/Model-AlphaFold2-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Field-Structure%20Prediction-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Reference-OpenFold-555?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat-square" />
</p>

---

## 内容索引

| 文档 | 说明 |
| :--- | :--- |
| [papers/](./papers/) | AF2 原始论文与补充材料 PDF |
| [AlphaFold2_Algorithm_Map.md](./AlphaFold2_Algorithm_Map.md) | Algorithm 1-32 ↔ SI 页码 ↔ OpenFold 源码 的对照索引 |
| [AlphaFold2_01_Overview.md](./AlphaFold2_01_Overview.md) | 宏观数据流；m / z / s 三个表示的形状与含义 |
| [AlphaFold2_02_Embeddings.md](./AlphaFold2_02_Embeddings.md) | 输入特征嵌入、相对位置编码 |
| [AlphaFold2_03_Evoformer.md](./AlphaFold2_03_Evoformer.md) | Evoformer 全部算子：MSA 注意力、外积均值、三角乘法与三角注意力 |
| [AlphaFold2_04_Template_ExtraMSA.md](./AlphaFold2_04_Template_ExtraMSA.md) | 模板通道与额外 MSA 通道 |
| [AlphaFold2_05_StructureModule.md](./AlphaFold2_05_StructureModule.md) | 刚体帧、IPA、骨架更新、全原子坐标重建 |
| [AlphaFold2_06_Loss.md](./AlphaFold2_06_Loss.md) | FAPE、扭转角损失、pLDDT 与各辅助输出头 |
| [AlphaFold2_07_Recycling.md](./AlphaFold2_07_Recycling.md) | 循环迭代机制与再嵌入 |
| [AlphaFold2_08_DataPipeline.md](./AlphaFold2_08_DataPipeline.md) | 数据管线：检索、过滤、聚类、裁剪、特征化、自蒸馏 |
| [AlphaFold2_09_Training.md](./AlphaFold2_09_Training.md) | 训练配方：阶段划分、优化器、初始化、dropout、显存优化 |

---

## 学习路线

| 阶段 | 做什么 | 材料 |
| :-: | :--- | :--- |
| 0 | 跑通一次短序列推理，为后面打断点看 shape 做准备 | OpenFold 源码 |
| 1 | 宏观：能自己画出数据流图 | 正文 Fig 1 / Fig 3、SI 1.4 |
| 2 | 建立伪代码与源码的对照关系 | Algorithm_Map、`model.py` |
| 3 | 逐算子精读：SI 伪代码 ↔ 源码 ↔ 实际张量形状 | 笔记 02-07 |
| 4 | 数据管线 | 笔记 08、`openfold/data/` |
| 5 | 训练：小数据集上跑通一次 overfit | 笔记 09、OpenFold 论文 |

> 每个算子按四段来记：**要解决什么 / 张量进出 / 关键步骤 / 实现细节与坑**。
> 其中「张量进出」写不出来就说明还没真懂，回去打断点。

---

##### [AlphaFold2 论文](https://www.nature.com/articles/s41586-021-03819-2) &nbsp;|&nbsp; [OpenFold 源码](https://github.com/aqlaboratory/openfold) &nbsp;|&nbsp; [The Illustrated AlphaFold](https://elanapearl.github.io/blog/2024/the-illustrated-alphafold/)
