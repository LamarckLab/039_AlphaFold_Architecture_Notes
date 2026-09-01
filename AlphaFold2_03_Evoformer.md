<p align="left">
  <a href="./README.md">首页</a>
</p>

## Lamarck &nbsp; &nbsp; &nbsp; 2026-09-01
#### 该文档记录 Evoformer 的全部算子，对应 SI 1.6（p14-20，全文最核心的 7 页）
---

## Alg 06 &nbsp; EvoformerStack &nbsp; Evoformer 主堆栈
> **SI p14** &nbsp;|&nbsp; OpenFold `evoformer.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 07 &nbsp; MSARowAttentionWithPairBias &nbsp; MSA 行注意力（带 pair 偏置）
> **SI p15** &nbsp;|&nbsp; OpenFold `msa.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 08 &nbsp; MSAColumnAttention &nbsp; MSA 列注意力
> **SI p16** &nbsp;|&nbsp; OpenFold `msa.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 09 &nbsp; MSATransition &nbsp; MSA 前馈层
> **SI p17** &nbsp;|&nbsp; OpenFold `msa.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 10 &nbsp; OuterProductMean &nbsp; MSA 到 pair 的信息注入
> **SI p17** &nbsp;|&nbsp; OpenFold `outer_product_mean.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 11 &nbsp; TriangleMultiplicationOutgoing &nbsp; 三角乘法更新（出边）
> **SI p18** &nbsp;|&nbsp; OpenFold `triangular_multiplicative_update.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 12 &nbsp; TriangleMultiplicationIncoming &nbsp; 三角乘法更新（入边）
> **SI p18** &nbsp;|&nbsp; OpenFold `triangular_multiplicative_update.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 13 &nbsp; TriangleAttentionStartingNode &nbsp; 三角注意力（起始节点）
> **SI p19** &nbsp;|&nbsp; OpenFold `triangular_attention.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 14 &nbsp; TriangleAttentionEndingNode &nbsp; 三角注意力（终止节点）
> **SI p20** &nbsp;|&nbsp; OpenFold `triangular_attention.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 15 &nbsp; PairTransition &nbsp; pair 前馈层
> **SI p20** &nbsp;|&nbsp; OpenFold `pair_transition.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

