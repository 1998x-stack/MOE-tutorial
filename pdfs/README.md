# MoE (Mixture of Experts) 经典论文合集

按发展脉络排列：理论奠基 → Transformer稀疏MoE → 分布式工程 → 开源轻量化 → 国产创新 → 拓展方向

## 论文列表

| # | 论文 | 年份 | 出处 | 文件 |
|---|------|------|------|------|
| 1 | Adaptive Mixture of Local Experts (Jacobs, Jordan, Hinton) | 1991 | Neural Computation | `01_Adaptive_Mixture_of_Local_Experts_1991_Jacobs.pdf` |
| 2 | Sparsely-Gated Mixture-of-Experts Layer (Shazeer et al.) | 2017 | ICLR / arXiv:1701.06538 | `02_Sparsely-Gated_MoE_2017_Shazeer.pdf` |
| 3 | GShard: Scaling Giant Models with Conditional Computation (Lepikhin et al.) | 2020 | ICLR / arXiv:2006.16668 | `03_GShard_2020_Lepikhin.pdf` |
| 4 | Switch Transformers: Scaling to Trillion Parameter Models (Fedus et al.) | 2021 | JMLR / arXiv:2101.03961 | `04_Switch_Transformer_2021_Fedus.pdf` |
| 5 | Mixtral of Experts (Jiang et al.) | 2024 | Mistral AI / arXiv:2401.04088 | `05_Mixtral_of_Experts_2024_Jiang.pdf` |
| 6 | DeepSeekMoE: Towards Ultimate Expert Specialization (Dai et al.) | 2024 | ACL / arXiv:2401.06066 | `06_DeepSeekMoE_2024_Dai.pdf` |
| 7 | DeepSeek-V2: A Strong, Economical, and Efficient MoE LM (Liu et al.) | 2024 | arXiv:2405.04434 | `07_DeepSeek-V2_2024_Liu.pdf` |
| 8 | DeepSeek-V3 Technical Report (Liu et al.) | 2024 | arXiv:2412.19437 | `08_DeepSeek-V3_2024_Liu.pdf` |
| 9 | MMoE: Multi-gate Mixture-of-Experts (Ma et al.) | 2018 | KDD 2018 | `09_MMoE_2018_Ma.pdf` |
| 10 | DBRX: A New Standard for Efficient Open Source LLMs | 2024 | Databricks Blog (无学术论文) | `10_DBRX_Databricks_2024_Reference.md` |
| 11 | A Review of Sparse Expert Models in Deep Learning (Fedus et al.) | 2022 | arXiv:2209.01667 | `11_Review_Sparse_Expert_Models_2022_Fedus.pdf` |
| 12 | OLMoE: Open Mixture-of-Experts Language Models (Muennighoff et al.) | 2024 | AI2 / arXiv:2409.02060 | `12_OLMoE_2024_Muennighoff.pdf` |

## 阅读路线推荐

1. **零基础入门MoE理论:** 1 → 2 → 4
2. **千亿分布式MoE训练:** 3 → 8
3. **开源轻量化落地:** 5 → 6 → 7
4. **国产中文MoE研究:** 6 → 7 → 8
5. **综述快速掌握全领域:** 11

## 核心4篇必读

1. **1991 Local Experts** — MoE概念起源
2. **2017 Sparsely-Gated MoE** — 现代稀疏MoE标准架构
3. **Mixtral** — 开源轻量化MoE普及标杆
4. **DeepSeekMoE** — 国产专业化MoE创新底层

## 注意事项

- DBRX (#10) 为 Databricks 博客发布，无学术论文版本。参考文件为技术摘要 markdown，含官方博客链接和关键架构参数。
- 1991年论文 (#1) 从 Geoffrey Hinton 个人主页下载（非 arXiv），为 MoE 领域奠基文献。
- MMoE (#9) 为 KDD 2018 会议论文，面向多任务学习场景，是推荐系统/多任务微调经典。
