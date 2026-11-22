# 精读笔记：PbrERF114 调控梨果实成熟中的乙烯合成

## 文献

- 题名：Transcription factor PbrERF114 is involved in the regulation of ethylene synthesis during pear fruit ripening
- 作者：Guoming Wang†, Zhihua Guo†, Tengjiao Wang, Xueping Wang, Kaijie Qi, Jiping Xuan, Chao Gu*, Shaoling Zhang*（†共同第一作者；*通讯作者）
- 期刊/年份：Molecular Horticulture 4:38 (2024)
- DOI：https://doi.org/10.1186/s43897-024-00114-2
- 谷超老师角色：通讯作者（guchao@njau.edu.cn；与 Shaoling Zhang 并列；Authors' contributions：C.G. and S.L.Z. designed the experiment）

## 一句话结论

PbrERF114（Pbr018333.1，核定位 ERF 转录因子）是梨果实成熟期乙烯合成的正调控因子：它直接结合并激活 **PbrACS3**（Pbr015575.1）启动子，同时直接激活 **PbrERF24**（Pbr012024.1）；PbrERF24 再直接结合并激活 **PbrACS3** 与 **PbrACO1**（Pbr031954.1），形成放大乙烯合成的转录级联；对 PbrACS1b/PbrACO1 启动子无直接激活，与 PbHB.G7.2/PbbHLH164（走 ACS1b）形成分支分工。

## 研究问题

乙烯信号通路研究很多，但梨果实中 ERF 介导的乙烯生物合成转录调控仍未阐明（此前梨中仅报道 PbrERF24 直接结合 PbrACO1 启动子，Hao et al. 2018）。作者要回答：哪些 ERF 参与梨成熟期乙烯合成？它们直接调控哪些 ACS/ACO 基因、是否存在级联？

## 实验设计

- 材料与处理：翠冠（Cuiguan，早熟 P. pyrifolia）果实，乙烯利（方法部分 1,000 μL/L；Fig. 1 图注写 300 ppm）或 1-MCP（1.5 μL/L）浸泡 10 min（约收获前 30 天，DBH），每处理约 40 果，黑袋密封 1 天后去除；对照为清水。乙烯利处理果（EF）成熟时采样，同天采对照（ECK）；1-MCP 处理对照（MCK）自然成熟时采样，同天采处理果（MF）。每次测量 ≥10 个样品。
- 转录组：4 个文库（ECK/EF/MCK/MF），clean reads 分别为 21.6/20.4/25.5/25.7 M；DEG 标准 P<0.05 且 |log2FC|≥1（DESeq，Benjamini-Hochberg 校正）；qRT-PCR 验证 12 个基因（3 生物学重复，内参 PbrTUB、Pbr028511）。
- 亚细胞定位：PbrERF114-GFP（pCAMBIA1300-35S）烟草叶片瞬时表达，DAPI 染核。
- 果肉瞬时转化：pSAK277-PbrERF114 过表达与 pTRV2-PbrERF114（约 400-bp 特异片段）VIGS 注射梨果肉（GV3101，重复 6 次；乙烯测定 6 生物学重复、qRT-PCR 3 重复；注射后 10 天 DAI 测定）。
- 蛋白-DNA：双荧光素酶（PbrACS1b/PbrACS3/PbrACO1/PbrERF24 各约 2-kb 启动子入 pGreenII0800-LUC；3 次独立实验 × 3 生物学重复）；Y1H（2-kb PbrACS3 启动子入 pAbAi）；EMSA（PbrERF114-His、PbrERF24-His 重组蛋白；biotin 探针与突变冷探针，10×/50×/200× 冷竞争）；生物层干涉动力学（ForteBio Octet 96 Red，KD 测定）。
- 蛋白-蛋白：Y2H（PbrERF114 × PbrERF24，AH109，SD/-Trp-Leu-His-Ade 筛选）。
- 跨品种验证：15 个品种（Pp：Nijisseiki、Kisui、Atago、Xueqing、Huanghua、Hangqing；Pb：Dangshang、Jinzhui、Yali、Huangguan；Ps：Kuerle；Ph：Xizilü、Xinya、Xinhang、Xuefeng）成熟果与膨大果（15 DBH 与 0 DBH）qRT-PCR。

## 关键证据链

1. **乙烯利促进成熟、1-MCP 延迟成熟（硬度/可溶性固形物相反变化）** — Fig. 1（≥10 样品/测量，Student's t-test）— 证据强度：强（表型层面，为后续材料定义成熟/未成熟状态）。
2. **721 个成熟相关 DEGs 中 PbrACS3 与 PbrERF114 协同上调** — 4 组转录组比较（ECK vs EF：4,381 DEGs，其中 1,427 上调；MCK vs MF：2,040 DEGs，其中 1,251 上调；成熟相关 = 263 上调 + 458 下调 = 721）；qRT-PCR 验证 12 基因与转录组一致（Fig. 2）— 证据强度：中强（每处理组单文库，无生物学重复的转录组，靠 qRT-PCR 补强）。
3. **PbrERF114 定位于细胞核** — PbrERF114-GFP + DAPI（Fig. 3A）— 证据强度：强。
4. **PbrERF114 正调控乙烯与 PbrACS3 表达（PbrACS1b/PbrACO1 无显著变化）** — 果肉瞬时 OE 10 DAI：乙烯与 PbrACS3 升；VIGS：两者降（Fig. 3B,C）— 证据强度：强（双向扰动；瞬时体系，品种未在文中指明）。
5. **PbrERF114 直接结合并激活 PbrACS3 启动子** — 双LUC（PbrACS1b/PbrACO1 启动子几乎不受影响，Fig. 4B）、Y1H（Fig. 4C）、EMSA（冷竞争与突变探针，Fig. 4D）— 证据强度：强（三重方法）。
6. **PbrERF114 直接结合并激活 PbrERF24 启动子（GCC-box）** — 双LUC、Y1H、EMSA、动力学（结合饱和于 8,382 nM，KD<1 μM）（Fig. 5）— 证据强度：强。
7. **PbrERF24 直接结合并激活 PbrACS3 与 PbrACO1 启动子** — PbrACS3：双LUC、Y1H、EMSA、动力学（KD<0.1 μM，Fig. 6）；PbrACO1 为团队前期已报道（Hao et al. 2018）— 证据强度：强（本论文补上 PbrERF24→PbrACS3 新边）。
8. **PbrERF114 成熟期高表达、膨大期低表达（跨 15 品种）** — qRT-PCR：15 个品种中 14 个成熟果高、膨大果极低（Fig. 7）— 证据强度：强（跨品种；1 个品种例外未解释）。
9. **PbrERF24 不调控 PbrERF114（双LUC，Fig. S1），二者也无蛋白互作（Y2H，Fig. S2）** — 级联为单向（PbrERF114→PbrERF24），非反馈环 — 证据强度：中强（阴性证据）。

## 机制图（文字版）

```text
成熟/乙烯信号
      ↓
 PbrERF114（核内）
   ↙             ↘
直接激活       直接激活
PbrACS3       PbrERF24
                  ↓
          直接激活 PbrACS3、PbrACO1
                  ↓
          ACC 合成/氧化增强 → 乙烯增加 → 成熟推进

（PbrERF24 不反馈调控 PbrERF114；两蛋白无直接互作；
  PbrERF114 对 PbrACS1b/PbrACO1 启动子无直接激活）
```

## 优点

1. 用乙烯利/1-MCP 双向处理定义"成熟相关"转录组（721 DEGs），并注意 EIL1/2/3 等信号核心因子无一致差异这一细节（Fig. 2C），避免把处理效应全部归为直接靶基因。
2. "直接结合"证据完整且分层：启动子报告 + Y1H + EMSA（含突变探针）+ 动力学 KD 定量（PbrERF114–PbrERF24 KD<1 μM；PbrERF24–PbrACS3 KD<0.1 μM）。
3. 用阴性结果界定网络结构：PbrERF114 不激活 PbrACS1b/PbrACO1 启动子、PbrERF24 不调控 PbrERF114、两蛋白无互作（Fig. S1、S2），使级联模型清晰可证伪。
4. 跨 15 品种（4 个种/杂交类群）的表达验证把相关性提升到物种水平（Fig. 7）。

## 证据边界

1. "直接结合"证据主要来自烟草叶片、酵母和体外体系，成熟果实染色质中的实际占位（ChIP/CUT&Tag）未测量。
2. 因果方向有过表达与 VIGS 的相反表型支持，但为短期、局部操作；缺稳定遗传材料、等基因背景互补与成熟表型系统量化；瞬时转化所用品种文中未指明。
3. 转录组每处理组仅 1 个文库，721 个 DEGs 不应全部解释为 PbrERF114 直接靶基因；乙烯利/1-MCP 同时改变成熟状态与信号背景。
4. PbrERF114→PbrERF24→PbrACO1 的"间接"链条合理，但论文未证明 PbrERF24 是 PbrERF114 影响 PbrACO1 的唯一中介，也未解析二者是否在 PbrACS3 启动子上协同占位。
5. 15 品种中 14 个符合"成熟高/膨大低"，1 个品种（图注未点名）不符合，作者未解释。

## 与谷超老师既有论文的连接

- 与 2024 年 PbbHLH164/PbRAD23C-D.1 论文共同指向"转录因子—ACS/ACO—乙烯"模块，但 PbrERF114 研究强调 ERF 转录级联，PbbHLH164 研究强调蛋白稳定性调控；两者靶基因不同（ACS3 vs ACS1b）。
- 与 2024 年 PbHB.G7.2 论文（PbHB.G7.2→PbACS1b）互补：梨成熟乙烯网络不是单一主开关，而是多个 TF 在不同 ACS/ACO 启动子上的分工与级联（ACS1b：HB/bHLH 分支；ACS3/ACO1：ERF 分支）。
- 与 2023 年 PbrEBF3 研究可组成"乙烯信号（EBF/EIN3）—ERF—ACS/ACO"的上下游网络；先后关系需时间序列与遗传互作确认。

## 下一步实验

1. 成熟果实 ChIP-qPCR/CUT&Tag，验证 PbrERF114 与 PbrERF24 对 PbrACS3/PbrACO1 的真实占位与时间顺序。
2. 对 GCC-box 做启动子精确突变，再在稳定材料中测乙烯、硬度、可溶性固形物和成熟时间。
3. PbrERF114×PbrERF24 双扰动或互补实验，判断 PbrERF114 对 PbrACO1 的影响是否完全依赖 PbrERF24。
4. 对 PbrERF114 的乙烯响应位置做时间序列分析，区分其是乙烯信号下游响应因子还是存在自激活/反馈回路。

## 精读依据

全文（本地 PDF 15 页，图 1–8、补充图 S1–S2、方法部分均已核对）。开放版本：https://pmc.ncbi.nlm.nih.gov/articles/PMC11566906/；DOI: 10.1186/s43897-024-00114-2。
