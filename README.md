# 🧩 MoE混合专家模型 · 从入门到精通

> 📘 28章 实战体系 · 交互式 HTML 课程

> **English TL;DR:** An all-Chinese 28-chapter course on **Mixture-of-Experts (MoE)** — from the 1991 theoretical origin (Adaptive Mixture of Local Experts) and the 2017 sparsely-gated breakthrough, through routing mechanisms (token-choice vs expert-choice), load balancing (aux loss / capacity factor / expert collapse), and engineering foundations (GShard, expert parallelism, all-to-all communication), to the modern open lineage: Switch → GShard → Mixtral → DeepSeekMoE → DeepSeek-V2/V3 (MLA + auxiliary-loss-free balancing + MTP + FP8). Covers multi-task MMoE, heterogeneous/OLMoE, expert interpretability, routing geometry & temporal memory, inference optimization (prefill/decode, expert fetch, speculative), consumer-hardware deployment, a PyTorch MoE build-from-scratch, and 2025–26 frontiers (mHC, MoE Lens).

## 📖 课程简介

本课程系统拆解 **MoE（Mixture of Experts）混合专家模型**：从 1991 年的理论鼻祖与 2017 年的 Sparse 开山之作讲起，厘清条件计算、稀疏激活、Top-K 路由与负载均衡的底层原理；随后沿开源工业主线——Switch / GShard / Mixtral / DeepSeekMoE / DeepSeek-V2 / V3——看 MoE 如何从学术实验走向万亿参数级工业落地。后半程深入路由理论（辅助损失-free 均衡、几何耦合、时域记忆、可解释性）、推理优化与消费级部署，最后以 PyTorch 从零搭建 MoE 的综合实战收束。

## 🚀 快速开始

```bash
open index.html   # macOS，纯静态即开即看
```

## 📂 项目结构

```text
MOE-tutorial/
├── index.html / 01.html ~ 28.html / courses.json / theme.css
```

## 📖 章节目录（阶段映射）

| 阶段 | 章节 | 核心 |
|------|------|------|
| **理念与起源** | 01–05 | MoE 演进史、1991 理论鼻祖、条件计算、2017 开山之作 |
| **路由与均衡** | 06–08 | Token/Expert-Choice、负载均衡、Switch 极简路由 |
| **工程基座** | 09–10 | GShard、专家并行、All-to-All 通信 |
| **开源明星** | 11–15 | Mixtral、DeepSeekMoE、V2(Long+MLA)、V3(ALF-free) |
| **路由深论** | 16–20 | ALF-LB、MMoE 多任务、异构/开放、知识聚合、几何 |
| **前沿+推理** | 21–25 | 时域记忆、可解释性、推理优化、消费部署、自适应路由 |
| **实战** | 26–28 | 从零搭 MoE、2025-26 前沿、领域专家系统项目 |

## ✨ 技术亮点

- 以 DeepSeek 系为工业主线（MoE + MLA + 无辅助损失 + MTP + FP8）
- 从理论 → 分布式工程 → 前沿理论的完整覆盖面
- 含 PyTorch 从零实现 MoE 的训练实战章节（ch.26）

## 🎯 前置知识

- 适合：大模型研究与工程 / 对稀疏模型好奇的学习者
- 建议具备：Transformer + FFN/注意力基础；无需 GPU

## ✨ 特色

- 唯一把「理论鼻祖 → 分布式 → 前沿」串成一条线的 MoE 课程
- 即开即用纯静态 HTML

---
*本课程由 `MOE-tutorial/` 项目维护。*