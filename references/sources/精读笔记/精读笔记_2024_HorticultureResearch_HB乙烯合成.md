# 精读笔记：PbHB.G7.2 及其互作因子调控梨果实乙烯合成

## 文献

- 题名：Interaction among homeodomain transcription factors mediates ethylene biosynthesis during pear fruit ripening
- 作者：Su-Hao Cao†, Zhi-Hua Guo†, Hong Liu, Guo-Ming Wang, Kai-Jie Qi, Ze-Wen Wang, Rui-Ping Tian, Shou-Feng Sha*, Shao-Ling Zhang*, Chao Gu*（†共同第一作者；*通讯作者）
- 期刊/年份：Horticulture Research 11: uhae086 (2024)
- DOI：https://doi.org/10.1093/hr/uhae086
- 谷超老师角色：通讯作者之一（guchao@njau.edu.cn / guchao_lw@tom.com；另两位通讯为 Zhang Shaoling、Sha Shou-Feng）

## 一句话结论

HD-ZIP II 转录因子 PbHB.G7.2 直接结合 **PbACS1b** 启动子（定位到起始密码子上游 −300~−200 bp）并促进乙烯合成；PbHB.G1（Pbr035813.1）和 PbHB.G2.1（Pbr004979.1）也能结合该启动子（分别为 −1800~−1700 bp 与 −1060~−940 bp）并各自激活，但与 PbHB.G7.2 的蛋白互作（G1/G2.1 的 D 区 × G7.2 的 D+C 区）会削弱三者对 PbACS1b 的转录激活；成熟期 PbHB.G7.2 表达高于 G1/G2.1，使 G7.2 主导激活，构成依赖表达量与蛋白互作状态的乙烯合成调节器。三者表达均不响应乙烯信号。

## 研究问题

跃变型果实（梨）成熟中乙烯生物合成（SAM→ACC→乙烯）的转录调控在梨中远不如番茄/苹果清楚；此前梨中仅报道 PbERF24 调控 PbACO1。作者要回答：HB（同源异型盒）转录因子是否参与梨乙烯合成调控？PbACS1b 由哪些转录因子直接调控？转录因子间的蛋白互作如何调节该输出？

## 实验设计

- 材料：13 个品种（Housui、Cuiguan、Xueqing 各 5 个发育点 + 10 个品种成熟果验证：Huasu、Zhongli No.1、Xizilv、Zaomeisu、Liuyueshuang、Jinhua、Eli No.1、Ningmenghuang、Jinsui No.1、Xinhang），南京农业大学江浦果园；每期 3 个生物学重复 × ≥4 果。
- 转录组筛选：3 品种膨大/成熟期转录组中检测 4 ACS、4 ACO、78 HB（共 85 个基因），筛选成熟期上调基因。
- 外源处理：Cuiguan 树上果实约 80 DAFB 用乙烯利（图注 300 ppm；方法部分 300 μL/L）或 1-MCP（1.5 μL/L）浸泡 5 min，黑袋密封 24 h，≥40 果/处理、6 个生物学重复 × ≥6 果；测可溶性固形物与乙烯。
- 愈伤转化：PbHB.G7.2 过表达于 'Clapp's Favorite' 果肉愈伤（pSAK277 空载体对照），测乙烯与 qRT-PCR。
- 果肉瞬时转化：cv. Sucui No.1（成熟期黄皮）— 过表达（pSAK277，EHA105，40 果）与 VIGS 沉默（520-bp 片段入 pTRV2，GV3101，40 果 + 40 果对照）；乙烯测定 ≥5 果/3-L 罐 × 4 重复。
- 蛋白-DNA：双荧光素酶（2,000-bp PbACS1b 启动子及 P1–P8、P10–P17 分段报告子；≥6 次测量/实验）；Y1H（P、P9、P16、P17 片段入 pAbAi，50 ng/mL AbA）；EMSA（34-bp、33-bp、40-bp 生物素探针，冷探针 10×/100×）。
- 蛋白-蛋白：Y2H 文库筛选（Cuiguan 果实 cDNA 文库，PbHB.G7.2 为诱饵，10 个候选蛋白）；FLCI、Co-IP 验证；N/D/C 三片段拆分定位互作区（酵母无自激活验证）。
- 统计：Student's t-test / ANOVA（P<0.05）。

## 关键证据链

1. **PbACS1b、PbACO1、PbHB.G7.2 在 3 品种成熟果中表达升高；PbHB.E10.2 无稳定差异** — 转录组 + qRT-PCR（Fig. 1a,b；Housui 157 vs 104/82 DAFB，Cuiguan/Xueqing 136 vs 96/76 DAFB）— 证据强度：中强（多品种一致）。
2. **PbHB.G7.2 正调控乙烯合成，主要输出为 PbACS1b（PbACO1 不变）** — 愈伤过表达：乙烯与 PbACS1b 上升、PbACO1 基本不变（Fig. 2a,b）；Sucui No.1 果肉瞬时 OE 果皮变黄/乙烯升、VIGS 果皮偏绿/乙烯降（Fig. 4）— 证据强度：强（双向扰动；瞬时体系）。
3. **PbHB.G7.2 直接结合 PbACS1b 启动子 −300~−200 bp 区域** — 双LUC 片段定位（P1–P8，Fig. 2d,e）、Y1H（P、P9，Fig. 2f）、EMSA（34-bp 探针，Fig. 2g）— 证据强度：强（三重方法）。
4. **乙烯利/1-MCP 改变成熟进程与 PbACS1b/PbACO1 表达，但不改变 PbHB.G7.2 表达** — 树上处理实验（Fig. 3）— 证据强度：中（表达层面，"independent of ethylene signaling"的支撑）。
5. **PbHB.G7.2 与 PbHB.G1、PbHB.G2.1 物理互作** — Y2H 文库筛选 + 回验（Fig. 5a）、FLCI（Fig. 5b）、Co-IP（Fig. 5c）；互作区为 G1/G2.1 的 D 区（含 HOMEOBOX 域）× G7.2 的 D+C 区（Fig. 5e–h）— 证据强度：强（多方法 + 区段拆分）。
6. **三者单独均激活 PbACS1b 启动子；共表达 G7.2+G1 或 G7.2+G2.1 后 LUC 活性下降** — 双LUC（Fig. 6b）— 证据强度：中强（仅报告基因读数，机制未探明）。
7. **G1/G2.1 结合区与 G7.2 不同（−1800~−1700 bp / −1060~−940 bp），且与互作区分离** — 双LUC 分段（Fig. 6c,d）、Y1H（P16/P17）、EMSA（Fig. 6e,f）— 证据强度：强。
8. **成熟期 PbHB.G7.2 表达高于 G1/G2.1（3 品种 + 10 品种验证）** — qRT-PCR（Fig. 7a,c）— 证据强度：强（跨品种）；据此提出"低表达的 G1/G2.1 减弱对 G7.2 的抑制 → G7.2 主导激活"的模型（Discussion/Conclusion）。

## 机制图（文字版）

```text
成熟阶段：PbHB.G7.2 高表达，PbHB.G1/G2.1 相对低表达
                  ↓
      PbHB.G7.2 ──直接结合(−300~−200 bp)──> PbACS1b ──> ACC ──> 乙烯
          ↙              ↘
   与 G1/G2.1 互作     （G1 结合 −1800~−1700 bp；G2.1 结合 −1060~−940 bp，
     （G1/G2.1 的 D 区      三者各自均可激活 PbACS1b 启动子）
      × G7.2 的 D+C 区）
          ↓
   三者转录激活能力均减弱 → 成熟期 G1/G2.1 低表达 → 抑制解除 → 乙烯爆发
   （三者表达均不受乙烯信号诱导）
```

## 优点

1. 结合区定位做到几十 bp 尺度：PbACS1b 启动子分 P1–P8、P10–P17 两轮片段，最终把 G7.2 定位到 −300~−200 bp、G1 到 −1800~−1700 bp、G2.1 到 −1060~−940 bp，并分别用 Y1H 与 EMSA 确认（Fig. 2、6）。
2. 蛋白互作三重验证（Y2H + FLCI + Co-IP）且做了 N/D/C 区段拆分，证明互作域与 DNA 结合域分离，支撑"互作不是简单阻断 DNA 结合"的解读（Fig. 5、6）。
3. 用表达量权衡解决"三个激活因子谁主导"的问题：3 品种 + 10 品种成熟果中 G7.2 均高于 G1/G2.1（Fig. 7），使模型具有跨品种基础。
4. 与桃 PpHB.G7 同源比较：梨 G7.2 只结合 ACS 启动子而桃结合 ACS+ACO，同组 HB 在近缘物种中的功能分化点明确（Discussion）。

## 证据边界

1. 直接结合证据（双LUC/Y1H/EMSA）来自烟草叶片、酵母与体外体系，成熟梨果实染色质中的实际占位（ChIP）未测量。
2. 过表达/沉默表型来自愈伤组织与果肉瞬时转化，无稳定遗传材料与等基因背景互补。
3. "互作削弱激活"仅由共表达后 LUC 下降支持；互作是否改变核内定位、DNA 占位、蛋白稳定性或共激活子招募均未检测。
4. "independent of ethylene signaling"是表达水平结论（外源乙烯利/1-MCP 不改变其表达），不等于 PbHB.G7.2 在生理上与乙烯信号完全无关。
5. Conclusion 部分对"膨大期 G7.2 低表达使其只与 G1/G2.1 互作、成熟期高表达解除抑制"的表述较简略，且膨大期三者互作的真实蛋白比例无直接测量；模型细节宜按 Discussion 版本（G1/G2.1 成熟期低表达减弱互作）理解。

## 与谷超老师既有论文的连接

- 补充了 PbrERF114 研究中的另一条 ACS1b 分支，表明梨成熟乙烯网络不是单个"主开关"，而是多个转录因子分别作用于 ACS1b、ACS3 和 ACO1，并通过蛋白互作调节输出强度：

```text
PbHB.G7.2 ──> PbACS1b
PbbHLH164 ──> PbACS1b（受 PbRAD23C/D.1 蛋白降解调控）
PbrERF114 ──> PbrACS3
PbrERF114 ──> PbrERF24 ──> PbrACS3 / PbrACO1
```

- 与 PbbHLH164 论文对比：两者都直接激活 PbACS1b，但一个受同家族转录因子互作抑制，一个受蛋白稳定性闸门调控；与 2023 PbrEBF3 研究（乙烯信号 EBF/EIN3）可组成"乙烯信号—TF—ACS/ACO"上下游网络，先后关系需时间序列与遗传互作确认。

## 下一步实验

1. 成熟果实 ChIP-qPCR/CUT&Tag，验证 PbHB.G7.2/G1/G2.1 在 PbACS1b 启动子上的真实占位，并检测互作是否改变占位。
2. 三者是否竞争同一共激活子，或通过 HD-ZIP II 亮氨酸拉链形成不同复合体（生化拆分）。
3. 在稳定遗传材料中分别突变 PbHB.G7.2 的 DNA 结合域与互作域，把"结合"与"被互作抑制"两个功能拆开验证。
4. PbACS1b（HB/bHLH 分支）与 PbrACS3（ERF 分支）在不同品种、成熟阶段和乙烯处理下的分工与时间顺序。

## 精读依据

全文（本地 PDF 12 页，图 1–7、补充图 S1–S6、方法部分均已核对）。开放版本：https://academic.oup.com/hr/article/11/5/uhae086/7637755；DOI: 10.1093/hr/uhae086。
