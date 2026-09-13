# Industry Corpus Manufacturing Guide (Open Edition)

> 制造业中英双语语料开源指南 —— BAAI IndustryCorpus2 制造业子集的使用手册。
> 源数据集 License：Apache-2.0（可商用可修改，保留声明）· 本指南为独立重组导读

## 这是什么

BAAI（北京智源人工智能研究院）发布的工业领域大规模预训练语料库，`other_manufacturing` 为制造业子集，**中英双语**收录。父集（IndustryCorpus2）本体量达万亿 token 级别（n>1T），是当前少有的中文工业领域大规模预训练语料之一。

**核心洞察**：制造业 + 中英双语 = AI 时代出海工具的地基数据。无论是智能客服、合同审阅还是工艺文档生成，都需要"懂工业语境"的模型——这个语料就是炼这种模型的原料。

## 核心价值

### 1. 大模型微调基底料
用制造业中英平行语料微调 LLMs，可产出懂"冲压工艺""SMT 贴片""注塑参数"等专业语境的大模型，直接服务智能客服/合同审阅/工艺文档生成。

### 2. 中英翻译模型训练
制造业术语标准化是跨境技术文档的痛点——"tolerance" 在机械语境是"公差"而非"容忍度"。此语料可训练领域专属翻译模型。

### 3. 智能选品 / 采购 AI
语料含大量产品规格描述，可训练产品属性提取模型，从供应商网站/产品目录自动结构化，替代人工录入。

## Schema 引用（父集）

```
@doi = 10.57967/hf/3488
@misc{shi2024industrycorpus2}
authors: Xiaofeng Shi, Lulu Zhao, Hua Zhou, Donglin Hao (BAAI)
year: 2024
license: Apache-2.0
```

## 典型工作流

此语料面向模型训练而非直接使用，典型流程：
**下载 → 清洗 → 混入基座 → LoRA 微调 → 评测**

💡 推荐与 `openai/gsm8k`（MIT，124 万下载）组合，训练"能说人话 + 懂工业术语"的混合垂类模型。

## License & 来源声明

- 源数据：https://huggingface.co/datasets/BAAI/IndustryCorpus2_other_manufacturing （Apache-2.0）
- 父集 DOI：10.57967/hf/3488
- 本指南：CC0 1.0 Universal，可自由使用/修改/商用，署名自愿（欢迎注明 Lunarwave @ lu7897859-tech）
- 加工声明：重组自源数据卡 + 独立增量解读（工作流/场景/组合建议），非原文搬运

## Keywords

manufacturing corpus, industry corpus, chinese english bilingual, LLM fine-tuning, LoRA, technical translation, BAAI IndustryCorpus, 制造业语料, 中英双语语料, 工业大模型, 微调基底, 智能采购, 工艺文档, domain-specific LLM, 工业领域预训练语料
