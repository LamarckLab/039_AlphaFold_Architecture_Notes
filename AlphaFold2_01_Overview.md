<p align="left">
  <a href="./README.md">首页</a>
</p>

## Lamarck &nbsp; &nbsp; &nbsp; 2026-09-01
#### 该文档记录 AF2 的宏观架构与整体数据流，对应 SI 1.4
---

## 00 &nbsp; 全流程数据流
> 从氨基酸序列到全原子坐标，一张图能画出来才算过关



## 01 &nbsp; 两条张量主线
> 全篇只有两个表示在流动，抓住它们就抓住了 AF2

| 表示 | 符号 | 形状 | 含义 |
| :-- | :-- | :-- | :-- |
| MSA 表示 | m | `[N_seq, N_res, c_m=256]` |  |
| pair 表示 | z | `[N_res, N_res, c_z=128]` |  |
| single 表示 | s | `[N_res, c_s=384]` |  |



## Alg 02 &nbsp; Inference &nbsp; AlphaFold 主推理流程
> **SI p12** &nbsp;|&nbsp; OpenFold `model.py`

**要解决什么**



**张量进出**



**关键步骤**



**实现细节与坑**



---

