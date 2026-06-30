# DBRX: A New Standard for Efficient Open Source LLMs

**Source:** Databricks Blog (March 27, 2024)
**URL:** https://www.databricks.com/blog/announcing-dbrx-new-standard-efficient-open-source-customizable-llms

> **Note:** DBRX was released as a technical blog post, not an academic paper. There is no arXiv preprint or conference publication for DBRX. Below is a summary of the technical details from the official blog post.

---

## Architecture

DBRX is a **transformer-based decoder-only Mixture-of-Experts (MoE)** model built on the **MegaBlocks** research and open-source project (arXiv:2211.15841, https://github.com/databricks/megablocks).

## Expert Configuration

- **Total parameters:** 132B
- **Active parameters:** 36B (per token)
- **16 experts, Top-4 routing** (fine-grained MoE — 65x more possible expert combinations than Mixtral's 8×7B Top-2)
- Other architectural choices: RoPE, GLU, Grouped Query Attention (GQA), GPT-4 (tiktoken) BPE tokenizer

## Training

- **Training data:** 12T tokens of text and code
- **Context length:** 32K tokens
- **Training cost:** ~$10M, ~2 months
- Built entirely on Databricks platform (Unity Catalog, Apache Spark, Lilac AI for data processing)
- Full pipeline: data curation → pre-training → post-training (DPO) → evaluation → serving

## Performance

- Outperforms all leading open-source models (LLaMA2-70B, Mixtral, Grok-1) on language understanding, programming, math, and logic
- Beats GPT-3.5 on most benchmarks (MMLU, HumanEval, GSM8K)
- ~2x faster inference than comparable dense models due to MoE sparsity
- Evaluated on internal "Gauntlet" benchmark with 30+ SOTA benchmarks

## Key Innovations

1. **Fine-grained MoE** — 16 small experts with Top-4 routing for more expert combinations
2. **MegaBlocks integration** — Sparse matrix operations for efficient parallel expert computation
3. **Heterogeneous expert sizing** — Different experts can have different parameter counts
4. **Fully open-source** — Weights, code, and training recipes released under Apache 2.0

## Resources

- Blog: https://www.databricks.com/blog/announcing-dbrx-new-standard-efficient-open-source-customizable-llms
- GitHub: https://github.com/databricks/dbrx
- HuggingFace: https://huggingface.co/databricks/dbrx-instruct
- MegaBlocks paper: https://arxiv.org/abs/2211.15841
