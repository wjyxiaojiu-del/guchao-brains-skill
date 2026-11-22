# 精读笔记：梨自交不亲和 S 位点的长读长组装与协同非己识别

## 文献

- 题名：Long-read genome sequencing reveals the sequence characteristics of pear self-incompatibility locus
- 作者：Chao Gu†, Ying Xu†, Lei Wu†, Xueping Wang, Kaijie Qi, Xin Qiao, Zewen Wang, Qionghou Li, Min He, Shaoling Zhang*（†共同第一作者；*通讯作者）
- 期刊/年份：Molecular Horticulture 5:13 (2025)
- DOI：https://doi.org/10.1186/s43897-024-00132-0
- 谷超老师角色：共同第一作者兼通讯作者（guchao@njau.edu.cn；与 Shaoling Zhang 并列通讯）

## 一句话结论

PacBio 长读长组装把梨 S17 位点展开为约 1.78 Mb、含 19 个 SFBB（S-locus F-box brother）基因的复杂区域；18 个 SFBB 花粉特异表达并与 S17-RNase 共分离，其中 8 个能与至少一种非己 S-RNase 互作而无一与自身 S17-RNase 互作，支持梨采用"多个 SFBB 分工协作覆盖非己 S-RNase、排除自我"的协同非己识别系统；S 位点富集 LTR 反转录转座子，可能与 SFBB 排列重塑相关。

## 研究问题

矮牵牛 S 位点含 16–20 个 F-box 基因并协同识别非己 S-RNase，但梨（Pyrus）中 S 位点 F-box 基因（SFBB）的完整数目、物理结构与哪些 SFBB 真正与非己 S-RNase 互作均不确定；短读长在高重复、串联 F-box 区域漏装严重。作者试图用长读长组装回答：梨 S17 位点多大、含多少 SFBB、其组织表达与遗传共分离如何、哪些 SFBB 参与非己识别？

## 实验设计

- 基因组组装：'Yali'（S17S21，P. bretschneideri）——63.57 Gb Illumina 短读长（17-mer 估计基因组 545.39 Mb、杂合度 1.35%）+ 34.44 Gb PacBio 长读长（平均 9,721 bp，20-kb 文库）；FALCON 组装 + Quiver/pilon 抛光；最终 534.45 Mb、582 个 contigs、contig N50 1.81 Mb、BUSCO 95.2%、45,092 个蛋白编码基因；566/582 contigs 可锚定到 'Cuiguan' 基因组；S17-RNase 位于 contig 33（17 号染色体末端）。
- SFBB 鉴定：以 Pyrus/Malus SFBB 保守 F-box motif 在 contig 33 中 BLAST（>150 aa 阈值）；并在已有长读长参考基因组中比较 P. communis S101、P. pyrifolia S5、P. betuleafolia S67、Malus S2/S3/S5/S9 及 'Dangshansuli' S7 位点（短读长 reads 比对）；Prunus S33/S9/S24 作对照。
- 序列分析：177 个 Pyrus/Malus SFBB 系统发育（22 组 I–XXII，MEGA5 NJ 法，1000 次 bootstrap）；组内/组间核酸与氨基酸一致性；5 kb 上下游侧翼序列一致性；MCScanX 预测复制事件（dispersed/proximal/tandem/transposed）；LTR 反转录转座子统计。
- 遗传共分离：'Yali'（S17S21）×'Xueqing'（S3S16）杂交后代 42 个个体（共 270 粒种子、113 株开花），S 基因型 1:1:1:1 检验（χ²=0.286<7.815）；19 对引物扩增 19 个 SFBB 全长并克隆测序，验证与 S17-RNase 共分离。
- 组织表达：'Dangshansuli' 已发表转录组 reads 比对到 'Yali' 基因组（花粉/花柱/根/茎/花瓣/叶/果实）。
- 蛋白互作：Y2H（9 种 S-RNase：S1、S2、S3、S5、S7、S12、S17、S18、S35——从 10 个品种花柱扩增，去信号肽，入 pGADT7；19 个 SFBB 入 pGBKT7；Y2HGold）；FLCI 复核 21 对阳性组合（8 SFBB × 8 S-RNase 中的 21 对，pCAMBIA1300-nLuc/cLuc，烟草共表达，3 DAI 检测）；HV 区缺失的 S5-/S7-RNase 与 PbrSFBB.VIII-S17 的 Y2H。
- 亚细胞定位：8 个互作 SFBB-GFP + PIP2A::mCherry 膜标记，烟草表皮细胞与原生质体共聚焦观察。

## 关键证据链

1. **'Yali' 基因组组装质量可靠，S17 位点展开为约 1.78 Mb（S17-RNase 上下游 0.94/0.83 Mb 内 19 个 SFBB）** — PacBio 组装统计（Table S1）、contig 33 分析（Fig. 2a）— 证据强度：强（BUSCO 95.2%、测序深度 101.1×）；SFBB 数目（19）多于此前短读长时代的报道（15 个，Huang et al. 2023）。
2. **Pyrus/Malus S 位点一般含 17–21 个 SFBB、跨度 1.35–2.64 Mb，可分成 22 个系统发育组** — 8 个 S 位点比较 + 177 个 SFBB 系统发育（Fig. 2a,b）；组内氨基酸一致性 88.9%–97.9% — 证据强度：强（多物种多单倍型，非单一品种现象）。
3. **19 个 SFBB 与 S17-RNase 共分离，18 个花粉特异表达** — 42 个杂交后代 PCR/测序（Fig. 4a，χ² 符合 1:1:1:1）；转录组比对（Fig. 4b）；SFBB.XXII-S17 例外（花柱/根/茎/花瓣/叶/果实表达、花粉不表达）— 证据强度：强（遗传 + 表达两个独立证据）。
4. **8 个 SFBB 与至少一种非己 S-RNase 互作，无一与 S17-RNase 互作** — Y2H 9 种 S-RNase 矩阵（Fig. 5a、Table 2）+ FLCI 复核 21 对（Fig. 5b）— 证据强度：强（Y2H+FLCI 双方法；但 FLCI 未覆盖全部 8×9 组合）。
5. **S-RNase 的 HV 高变区对识别特异至关重要** — 去掉 HV 区后 S5-/S7-RNase 与 PbrSFBB.VIII-S17 互作丢失（Fig. 5c）— 证据强度：中强（仅测 2 个 S-RNase × 1 个 SFBB）。
6. **PbrSFBB.VIII-S17 识别面最广（S1/S2/S5/S7/S12/S18/S35），但不识别与 S5 高度相似（94.2% 氨基酸一致）的 S3-RNase** — Y2H 矩阵（Fig. 5a、Table 2）— 证据强度：中强（提示少数高变残基决定特异性，也预示约 5% 交叉不亲和可能）。
7. **8 个互作 SFBB 均定位于细胞质（非膜/非壁）** — GFP + PIP2A::mCherry 对照，表皮细胞与原生质体（Fig. 6）— 证据强度：强（与 SCF 复合体胞质功能一致）。
8. **S 位点富集 LTR 反转录转座子（占测试区约 13.49%；SFBB.XVI–VIII 区间密度为其他区域 3.89 倍），并与 SFBB 复制/缺失/倒位/易位相关** — LTR 统计（Table S12）与复制事件/共线性分析（Fig. 3c、S4–S11）— 证据强度：中强（相关性+机制推断）。

## 机制图（文字版）

```text
S17 单倍型（约 1.78 Mb，19 个 SFBB，富集 LTR）
   ├─ 18 个 SFBB 花粉特异表达 + 与 S17-RNase 共分离 → 花粉 S 决定因子候选
   ├─ 8 个 SFBB（Ia/Ib/II/VIII/X/XI/XII/XVIII）识别 ≥1 种非己 S-RNase（Y2H+FLCI）
   │    └─ 识别依赖 S-RNase HV 区；SFBB.VIII 识别面最广（S1/S2/S5/S7/S12/S18/S35）
   ├─ 无一识别自身 S17-RNase（排除自我）
   └─ 10 个 SFBB 未检出互作（可能因测试 S-RNase 覆盖面有限）
      ↓
  非己 S-RNase 被多个 SFBB 分工覆盖 → 被 SCF 复合体泛素化降解 → 相容
  自交 S-RNase 无 SFBB 识别 → 进入花粉管 → 毒性 → 花粉管停止生长
```

## 优点

1. 长读长解决了短读长在高重复、串联 F-box 区域中的漏装问题，首次给出梨 S 位点的完整候选集合与物理顺序（19 个 vs 此前 15 个），是"序列结构—共分离—组织表达—蛋白互作矩阵"四位一体的工作，不止是发表一个参考基因组。
2. 跨梨（S17/S5/S67/S101/S7）与苹果（S2/S3/S5/S9）8 个 S 位点比较，把"17–21 个 SFBB"确立为 Maloideae 普遍特征而非单一品种现象；Prunus 对照（12–14 个 SLF/SFB、位点 2.82–3.07 Mb）凸显梨/苹果位点更紧凑。
3. 遗传共分离用了真实的 42 个杂交后代（χ² 检验 + 19 对引物全长克隆测序），组织表达与共分离相互独立、互相支撑。
4. HV 区缺失实验与 SFBB.VIII 不识别高相似 S3-RNase 的细节，把"识别特异性由少数高变残基决定"落到实验证据，并为群体中约 5% 交叉不亲和提供了机制解释。

## 证据边界

1. 论文测试 9 种 S-RNase（S1/S2/S3/S5/S7/S12/S17/S18/S35），而自然群体 S 等位基因远多于此；其余 10 个 SFBB 未检出互作可能只是测试面不足，不能判定为无功能。
2. Y2H/FLCI 证明物理互作或接近，不等于 SFBB 已把目标 S-RNase 招募进 SCF 复合体并完成泛素化、降解与相容授粉——体内降解证据（花粉管内 S-RNase 命运）缺失。
3. 18 个基因共同位于低重组 S 位点并共分离，无法逐个证明遗传功能；真正关键验证是单基因/组合敲除后出现特定交配型缺口（目前梨无法做到，仍是公认难点）。
4. 'Yali' 组装仍是 contig 级（582 contigs、N50 1.81 Mb）而非完全单倍型分辨的 T2T；跨单倍型结构变异与等位特异表达仍有空间。
5. LTR 与 SFBB 重排的关联是统计与推断性的，缺少功能/因果实验。

## 与谷超老师既有论文的连接

- 代表自交不亲和主线从"自 S-RNase 进入花粉管后抑制哪些生长模块"（2023 COBRA、2025 PbrWHY2）向上游推进到"花粉如何先识别并清除非己 S-RNase"：前者解释拒绝反应的细胞效应，后者解释 S 位点的遗传识别逻辑，二者共同构成从 S 位点到花粉管停止生长的多尺度框架。
- 与 2022 年 84 份中国梨 S 基因型鉴定、2018 年梨驯化基因组等资源型工作衔接：S 位点单倍型结构为栽培品种 S 基因型鉴定与授粉品种配置提供基因组基础。
- 与 2024 年 Plant Communications 单倍型 T2T 泛基因组论文互补：本文聚焦 S 位点内部结构，泛基因组论文关注全基因组单倍型差异。

## 下一步实验

1. 用单倍型分辨的 T2T 组装（Hi-C + 新长读长平台）确认 S17 位点的完整单倍型结构与等位差异。
2. 在可转化的梨材料（愈伤/胚性细胞）中用 CRISPR 逐个或组合敲除花粉特异 SFBB，寻找特定交配型缺口（S 位点低重组下的功能验证策略）。
3. 在花粉管体内直接追踪非己 S-RNase 的泛素化与降解命运（荧光标记 S-RNase + SCF 组分扰动），把互作矩阵升级为体内机制。
4. 扩大 S-RNase 测试面板（覆盖更多自然等位基因），重新评估 10 个"无互作"SFBB 的功能状态，并解析 SFBB.VIII 与 S3-RNase 特异性的关键残基（定点突变）。

## 精读依据

全文（本地 PDF 19 页，图 1–7、补充材料索引与方法部分均已核对）。PubMed：https://pubmed.ncbi.nlm.nih.gov/40022260/；DOI: 10.1186/s43897-024-00132-0（Molecular Horticulture, BMC 开放获取）。
