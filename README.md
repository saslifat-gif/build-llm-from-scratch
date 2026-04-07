# Build a Language Model from Scratch

I want to show you how to build a language model from scratch using PyTorch, step by step, no magic.

most tutorials give you the full model and explain it after. here we build it piece by piece, so you can see exactly what each part does and why it matters.

## What you will learn

- what is a language model and how it predicts the next character
- how to build a tokenizer (text → numbers)
- how to build a Bigram model using `nn.Embedding`
- how self-attention works and why it matters
- how to build a full transformer with multi-head attention, LayerNorm, and residual connections
- how RoPE (Rotary Position Embedding) works and why modern LLMs use it

## Series

| Part | Topic | Status |
|------|-------|--------|
| Part 1 | Bigram Language Model | ✅ done |
| Part 2 | Self Attention | ✅ done |
| Part 3 | Full Transformer + RoPE | ✅ done |

## Results

Trained on 三体 (The Three-Body Problem) Chinese text — 912K characters, 3648 unique chars.

| Config | Steps | Val Loss |
|--------|-------|----------|
| Baseline (absolute position embedding) | 5000 | 4.07 |
| RoPE | 10000 | 3.83 |

RoPE reaches lower loss and generalizes better — consistent with how modern LLMs like Qwen and LLaMA use it.

## How to run

```bash
git clone https://github.com/saslifat-gif/build-llm-from-scratch
cd build-llm-from-scratch
pip install torch
jupyter notebook
```

## About me

I am a CS student building toward a ML engineer role at HuggingFace.  
find me on [HuggingFace](https://huggingface.co/lifatsastain) | [GitHub](https://github.com/saslifat-gif)
