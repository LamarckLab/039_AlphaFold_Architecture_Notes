<p align="left">
  <a href="./README.md">首页</a>
</p>

## Lamarck &nbsp; &nbsp; &nbsp; 2026-09-01
#### 该文档记录损失函数与各辅助输出头，对应 SI 1.9
---

## Alg 26 &nbsp; renameSymmetricGroundTruthAtoms &nbsp; 对称原子重命名
> **SI p31** &nbsp;|&nbsp; OpenFold `utils/loss.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 27 &nbsp; torsionAngleLoss &nbsp; 骨架与侧链扭转角损失
> **SI p33** &nbsp;|&nbsp; OpenFold `utils/loss.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 28 &nbsp; computeFAPE &nbsp; 帧对齐点误差（FAPE）
> **SI p34** &nbsp;|&nbsp; OpenFold `utils/loss.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## Alg 29 &nbsp; predictPerResidueLDDT &nbsp; 置信度预测 pLDDT
> **SI p37** &nbsp;|&nbsp; OpenFold `heads.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

## 其余辅助头
> SI 1.9.7-1.9.11，无独立伪代码

| 输出头 | SI 小节 | OpenFold |
| :-- | :-- | :-- |
| TM-score 预测（PAE） | 1.9.7 &nbsp; p37 | `heads.py` |
| Distogram 预测 | 1.9.8 &nbsp; p39 | `heads.py` |
| Masked MSA 预测 | 1.9.9 &nbsp; p39 | `heads.py` |
| Experimentally resolved | 1.9.10 &nbsp; p39 | `heads.py` |
| 结构违约惩罚 | 1.9.11 &nbsp; p40 | `utils/loss.py` |



