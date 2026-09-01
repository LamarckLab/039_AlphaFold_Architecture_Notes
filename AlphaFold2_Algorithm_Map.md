<p align="left">
  <a href="./README.md">首页</a>
</p>

## Lamarck &nbsp; &nbsp; &nbsp; 2026-09-01
#### 该文档是 AF2 补充材料伪代码与 OpenFold 源码的对照索引，读 SI 时按图索骥
---

## 01  说明

补充材料（`papers/AlphaFold2_SI.pdf`，共 62 页）给出 Algorithm 1-32 的完整伪代码，OpenFold 基本是把这份伪代码逐条翻译成 PyTorch，源码注释里直接标着 Algorithm 编号。

- **页码**指 SI 内部页码
- **OpenFold** 路径相对于 `openfold/` 包，`model/` 下的文件名已核对官方仓库目录，`utils/` 下的三项待 clone 后确认
- **笔记**指本仓库中对应的文档

## 02  对照表

| Alg | 名称 | SI 页 | OpenFold | 笔记 |
| :-: | :--- | :-: | :--- | :--- |
| 1 | MSABlockDeletion | 6 | `data/` | 08 |
| 2 | Inference | 12 | `model.py` | 01 |
| 3 | InputEmbedder | 13 | `model/embedders.py` | 02 |
| 4 | relpos | 13 | `model/embedders.py` | 02 |
| 5 | one_hot | 13 | `utils/tensor_utils.py` | 02 |
| 6 | EvoformerStack | 14 | `model/evoformer.py` | 03 |
| 7 | MSARowAttentionWithPairBias | 15 | `model/msa.py` | 03 |
| 8 | MSAColumnAttention | 16 | `model/msa.py` | 03 |
| 9 | MSATransition | 17 | `model/msa.py` | 03 |
| 10 | OuterProductMean | 17 | `model/outer_product_mean.py` | 03 |
| 11 | TriangleMultiplicationOutgoing | 18 | `model/triangular_multiplicative_update.py` | 03 |
| 12 | TriangleMultiplicationIncoming | 18 | `model/triangular_multiplicative_update.py` | 03 |
| 13 | TriangleAttentionStartingNode | 19 | `model/triangular_attention.py` | 03 |
| 14 | TriangleAttentionEndingNode | 20 | `model/triangular_attention.py` | 03 |
| 15 | PairTransition | 20 | `model/pair_transition.py` | 03 |
| 16 | TemplatePairStack | 21 | `model/template.py` | 04 |
| 17 | TemplatePointwiseAttention | 21 | `model/template.py` | 04 |
| 18 | ExtraMsaStack | 22 | `model/evoformer.py` | 04 |
| 19 | MSAColumnGlobalAttention | 22 | `model/msa.py` | 04 |
| 20 | StructureModule | 25 | `model/structure_module.py` | 05 |
| 21 | rigidFrom3Points | 26 | `utils/rigid_utils.py` | 05 |
| 22 | InvariantPointAttention | 28 | `model/structure_module.py` | 05 |
| 23 | BackboneUpdate | 29 | `model/structure_module.py` | 05 |
| 24 | computeAllAtomCoordinates | 30 | `utils/feats.py` | 05 |
| 25 | makeRotX | 30 | `utils/rigid_utils.py` | 05 |
| 26 | renameSymmetricGroundTruthAtoms | 31 | `utils/loss.py` | 06 |
| 27 | torsionAngleLoss | 33 | `utils/loss.py` | 06 |
| 28 | computeFAPE | 34 | `utils/loss.py` | 06 |
| 29 | predictPerResidueLDDT | 37 | `model/heads.py` | 06 |
| 30 | RecyclingInference | 41 | `model/model.py` | 07 |
| 31 | RecyclingTraining | 41 | `model/model.py` | 07 |
| 32 | RecyclingEmbedder | 42 | `model/embedders.py` | 07 |

## 03  SI 章节导航

| SI 章节 | 页 | 内容 | 笔记 |
| :--- | :-: | :--- | :--- |
| 1.1 | 4 | Notation | — |
| 1.2 | 5 | Data pipeline | 08 |
| 1.3 | 9 | Self-distillation dataset | 08 |
| 1.4 | 10 | AlphaFold Inference | 01 |
| 1.5 | 13 | Input embeddings | 02 |
| 1.6 | 14 | Evoformer blocks | 03 |
| 1.7 | 20 | Additional inputs | 04 |
| 1.8 | 23 | Structure module | 05 |
| 1.9 | 32 | Loss functions and auxiliary heads | 06 |
| 1.10 | 41 | Recycling iterations | 07 |
| 1.11 | 43 | Training and inference details | 09 |
| 1.12 | 46 | CASP14 assessment | — |
| 1.13 | 47 | Ablation studies | — |
| 1.14 | 51 | Network probing details | — |
| 1.15 | 52 | Novel fold performance | — |
| 1.16 | 54 | Visualization of attention | — |
| 1.17 | 56 | Additional results | — |
