# 精读笔记：梨单倍型 T2T 基因组与泛基因组图：等位特异表达与果实品质

## 文献

- **题名**：Haplotype-resolved T2T genome assemblies and pangenome graph of pear reveal diverse patterns of allele-specific expression and the genomic basis of fruit quality traits
- **作者**（完整）：Qionghou Li†, Xin Qiao†, Lanqing Li†, **Chao Gu**, Hao Yin, Kaijie Qi, Zhihua Xie, Sheng Yang, Qifeng Zhao, Zewen Wang, Yuhang Yang, Jiahui Pan, Hongxiang Li, Jie Wang, Chao Wang, Loren H. Rieseberg, Shaoling Zhang, Shutian Tao*（†共同第一作者，*通讯作者：陶书田 taost@njau.edu.cn，南京农业大学）
- **期刊**：Plant Communications，2024，5:101000（2024 年 10 月 14 日）
- **DOI**：10.1016/j.xplc.2024.101000
- **谷超老师角色**：共同作者（作者列表第 4 位），未标注通讯；作者贡献声明为"wrote the manuscript with help from C.G. and H.Y."（协助撰写论文）→ **参与（未标注通讯），参与论文撰写**

## 一句话结论

用 trio-binning 策略组装出'玉露香'（KEL×XH）与'红香酥'（KEL×EL）两个同母异父杂交品种的 4 条 gap-free 单倍型 T2T 基因组，并建成梨首个泛基因组图：约 6000 个等位特异表达基因（ASEG）中，糖代谢基因的一致 ASE 与糖含量超亲（BPH）相关、LACS4 方向转换 ASE 与蜡质中亲相关，而酸度关键基因 PyrusMa1 在父本单倍型中整体缺失、在 139 份群体中呈剂量效应（0/0<1/0<1/1 的有机酸含量），果实与愈伤过表达 Ma1 均提高有机酸——"单倍型解析组装 → ASE/PAV 发现 → 群体关联 → 功能验证"的完整链条。

## 研究问题

梨约 73% 的新品种来自杂交育种，但杂种优势（糖超亲、酸低亲、蜡质中亲）的基因组机制不清；传统"镶嵌型"单倍体参考基因组丢失等位基因间差异，无法解析等位特异表达（ASE）与单亲表达（SPE）；梨此前没有泛基因组，结构变异（SV）与等位基因缺失（PAV）无法高分辨率检测。

## 实验设计

- **材料**：'玉露香'（YLX，母本库尔勒香梨 KEL × 父本雪花 XH）、'红香酥'（HXS，KEL × 早酥 EL）；果实 5 个发育阶段（30/60/90/120/150 DAFB）+ 叶、茎、卵巢、花瓣，RNA-seq 每样本 3 重复。
- **测序**：YLX：HiFi ~102×、Hi-C ~228×、Illumina ~100×；HXS：HiFi ~53×、Hi-C ~203×、Illumina ~100×；三亲本各 ~50× Illumina；补洞用 ~100× ONT 超长读长（YLX）与公开 PacBio CLR（HXS）。
- **组装与质控**：TrioCanu 分型 + 7 种组装器比较（HiFiasm-trio 胜出）；Hi-C 挂载（LACHESIS）；4 条单倍型 contig N50 25.35–29.51 Mb、BUSCO 99.5%+、LAI 20.56–22.43、phasing 错误率 0.07%–0.14%；着丝粒（quarTeT）与端粒（tidk + 手工补）全部解析，gap-free T2T；基因注释 46,848–49,238 个/单倍型（MAKER + 分型转录组）。
- **ASE 鉴定**：等位基因对 32,610（YLX）/33,490（HXS）；RNA-seq 读长分型比对（STAR 双比对 + AS 打分），DESeq2 判 ASE（|log2FC|>2 且 padj<0.05），一致/方向转换 ASE 按 Shao et al. 2019 标准；SPE 分 PAV-SPE 与非 PAV-SPE。
- **泛基因组**：Minigraph-Cactus，11 个基因组（4 新单倍型 + 7 已发表，覆盖 P. communis/pyrifolia/bretschneideri/sinkiangensis/betulifolia），YLXB 为骨架；vg giraffe 把 139 份重测序（113 旧 + 97 新，71 份重叠，合并后平均深度 ~22×）比对到图（中位比对率 ~98%）；vg call 检 SV；DeepVariant-GLnexus 检 SNP（19.6 M 双等位）；SV hotspot 用 10 kb 滑窗 SV index top 5%。
- **选择扫描**：FST top 5% + ROD>0.5 + XP-CLR top 5%（含正反互检）；亚洲/欧洲、新疆梨 vs 白梨 分别比较。
- **Ma1 验证**：亲本 XH/EL 用 ~50× Illumina 组装确认 Ma1 缺失；YLX/HXS 读长比对确认杂合；139 份群体 PAV 基因分型（0/0、1/0、1/1）+ UPLC 有机酸测定（Wilcoxon 检验）；YLX 果实 90/150 DAFB 瞬时过表达 + 'Clapp's Favorite' 果实愈伤稳定过表达（2 个 OE 株系，EV 对照）。

## 关键证据链

1. **四条 gap-free 单倍型 T2T 基因组质量过硬**——实验：contig N50 25–30 Mb、BUSCO>99.5%、LAI>20.6、Merqury/yak 评估 phasing 错误率 0.07–0.14%、亲本特异 k-mer 只出现在对应单倍型（Fig. 1C）、17 条染色体端粒齐全；证据强度：**强**（多项独立质控指标 + 亲本 k-mer 验证分型正确）。
2. **约 5807/5918 个 ASEG 的鉴定可靠**——实验：分型 RNA-seq 的 MDS 显示母/父单倍型表达谱清晰分离（Fig. 2A,C），DESeq2 双阈值筛选；证据强度：**强**（分型正确性是前提，已由 k-mer 验证；但 |log2FC|>2 阈值较严，会漏掉弱 ASE）。
3. **ASEG 特征：序列分化大、启动子 TE 富集**——实验：ASEG 比非 ASEG 的 Ka/Ks 高、编码区与 3000 bp 启动子一致性低；方向转换 ASEG 启动子 TE 更多（Fig. 2E–G）；证据强度：**中**（全基因组统计比较，关联而非因果）。
4. **糖含量 BPH 与 4 对一致 ASEG 对应**——实验：INV/SDH/ST/PGM 四个基因家族在两品种中均为一致 ASE（Fig. 3B,C），与超亲糖含量（Fig. S9A）共现；证据强度：**弱—中**（表达-表型共现，无分离群体或功能实验）。
5. **Ma1 父本缺失（PAV-SPE）且与酸度呈剂量效应**——实验：组装与读长比对证实 Ma1 在 XH/EL 完全缺失、在 YLX/HXS 杂合、KEL 纯合（Fig. 5D）；139 份群体中 12 份 0/0（11 份栽培）、17 份 1/0、103 份 1/1；有机酸含量 1/1 显著高于 1/0 与 0/0（Fig. 7B，Wilcoxon p<0.05）；证据强度：**强**（结构变异确认 + 群体表型关联 + FST 提示外显子选择信号）。
6. **Ma1 过表达提高有机酸**——实验：YLX 果实 90 与 150 DAFB 瞬时 OE 两时期有机酸均显著高于 EV；愈伤稳定 OE 两株系酸含量显著升高（Fig. 7D–J）；证据强度：**中—强**（同源瞬时 + 稳定两种体系、有 EV 对照；但无沉默/敲除反证，愈伤与果实生理背景不同）。
7. **泛基因组图提升变异检测**——实验：11 基因组图总长 1.01 Gb、核心仅 135 Mb（13%）；129,864 个 SV（含 84,962 插入）；139 份中位比对率 ~98%（vs 单参考 ~65%）；选择区亚洲 13.08 Mb、欧洲 10.78 Mb，比 2018 年多 1.41×/2.01×；证据强度：**强**（比对率与 SV 检出量客观提升；"核心仅 13%"同时提示参考偏差仍大）。

## 机制图（文字版）

```text
[数据] HiFi/Hi-C/ONT + trio-binning → 4 条 gap-free T2T 单倍型（YLXA/B, HXSA/B）
   ↓
[分析] 分型 RNA-seq（DESeq2）→ ASEG；Minigraph-Cactus → 泛基因组图；139 份重测序比对 → SV/SNP
   ↓
[结论链]
糖（BPH）：INV/SDH/ST/PGM 一致 ASE → 表达互补 → 可溶性糖超亲
蜡质（中亲/母本偏向）：LACS4 方向转换 ASE（S2 偏父、S4 偏母）+ KCS/LACS/LTPG 一致 ASE
酸（WPH）：PyrusMa1 父本单倍型缺失（PAV-SPE）→ 等位剂量减半 → 有机酸低于双亲
   └─ 群体层面：Ma1 0/0 < 1/0 < 1/1 有机酸含量（剂量效应，FST 提示驯化选择）
   └─ 功能：果实/愈伤过表达 Ma1 → 有机酸 ↑
```

## 优点

1. **组装技术标杆**：梨首个 gap-free 单倍型 T2T 基因组（4 条单倍型），从 7 种组装器中选择 HiFiasm-trio，用亲本特异 k-mer 验证分型正确性，质量指标（N50/BUSCO/LAI/switch error）报告完整，流程开源（GitHub）。
2. **同母异父的实验设计**：YLX 与 HXS 共享母本 KEL，天然对照可分离"母本效应 vs 父本效应"，使 ASE 方向性比较（YLX 母本偏多、HXS 父本偏多）具有解释力。
3. **梨首个泛基因组图**：11 基因组、1.01 Gb 图，vg giraffe 将 139 份重测序的中位比对率从 ~65% 提升到 ~98%，SV/SNP 检出大幅改善，是梨群体遗传的标准基础设施。
4. **Ma1 从发现到功能的完整链条**：T2T 单倍型直接暴露父本等位缺失 → 亲本独立组装确认 → 139 份群体 PAV 基因分型 + HPLC 表型（剂量效应）→ 果实瞬时 + 愈伤稳定过表达双重验证，是 PAV 驱动果实品质的教科书式案例。
5. **数据完全开放**：原始数据 PRJCA022120（CRA013997），组装/注释/泛基因组图在 PearMODB，流程在 GitHub，可复现性极好。

## 证据边界

1. **ASE 的生物学样本有限**：仅 2 个品种、各 1 个个体（克隆系），ASE 是品种特异还是普遍规律未知；RNA-seq 分型比对在重复区/高相似等位基因上可能错分（虽有 MDS 佐证）。
2. **杂种优势-ASE 关联是相关性**：糖 BPH 与一致 ASEG、蜡质中亲与 LACS4 方向转换 ASE 均无遗传分离群体验证（无 F2/回交/亲本杂交组合重复），也未做等位基因互换实验；作者表述为"suggest/contribute"，应读作假说。
3. **Ma1 功能验证不完整**：缺沉默/敲除反证；瞬时过表达只有 5 天培养窗口，愈伤与果实代谢背景差异大；群体 PAV-表型关联中 0/0 仅 12 份（11 份栽培），统计功效有限，且酸度是多个基因共同决定的复杂性状。
4. **泛基因组代表性仍不足**：核心基因组仅 13%，说明 11 个基因组远未饱和；139 份群体栽培/野生比例不均衡；SV 用 50 bp 阈值、MAF<0.05 过滤，小 SV 与低频 SV 被漏检。
5. **选择扫描仍是统计信号**：13.08/10.78 Mb 选择区与 ASEG 富集（149/945，p=3.40×10⁻⁴）是相关证据，未做群体遗传模拟检验。

## 与谷超老师既有论文的连接

(1) 这是谷超老师研究网络里"基因组支撑方向"的集大成：**2018 年 Genome Biology 的 113 份重测序数据**在本篇被复用并加深（~22×），选择区检出量扩大 1.4–2.0 倍，两文形成"群体重测序 → 单倍型 T2T → 泛基因组"的递进；(2) 与谷超一作的 **2025 S 位点长读长组装论文（Molecular Horticulture）** 互补——那篇是单基因座（S17，1.78 Mb）的 T2T 级解析，本篇是全基因组 T2T，两者共享长读长组装方法论；(3) **2021 GWAS 的位点**可在此泛基因组中做等位基因/PAV 分型（Ma1 即示范）；(4) 与谷超一作的 **2024 DNA 甲基化多组学（Genome Biology）** 共享果实发育阶段设计，甲基化对 ASE 的贡献（水稻 CHG 甲基化-ASE 关联）是两文未来交叉点；(5) ASEG 富集防御反应、选择区富集抗病基因，为其 **自交不亲和/抗病** 方向提供了基因组资源。

## 下一步实验

1. 构建（YLX/HXS × 亲本）分离群体或更多同母异父组合，检验 ASE 与 BPH/WPH 的遗传传递，把相关性变成遗传证据；
2. 对 Ma1 做梨稳定转基因敲除/RNAi 或等位基因特异性编辑，完成因果闭合；同时测定 Ma1 蛋白的转运/通道活性（ALMT 家族）解释剂量-酸度关系；
3. 对糖通路一致 ASEG（INV/SDH/ST/PGM）与 LACS4 做等位基因互换表达实验（父本等位转入母本背景），直接测试等位差异的表达后果；
4. 整合 **DNA 甲基化与 small RNA 多组学**（延续其 2024 Genome Biology 工作），检验 TE 富集启动子上的甲基化差异是否驱动方向转换 ASE；
5. 把泛基因组扩展到 500+ 份并做 SV-GWAS（含酸度、糖、石细胞、锈斑），检验 Ma1 之外的新 PAV 位点。

## 精读依据

全文精读（21 页正文 + 方法，含 Results、Discussion、Methods、作者贡献与数据可用性）。
DOI：10.1016/j.xplc.2024.101000
