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

hyperemeters:
vocab_size = 3648
block_size = 128
batch_size = 8
n_embd = 128
n_head = 8
n_layer = 4

model parameters: 1.729344M

| Config | Steps | Train Loss | Val Loss |
|--------|-------|------------|----------|
| Absolute | 4500 | 3.80 | 3.94 |
| Absolute | 9000 | 3.50 | 3.78 |
| RoPE | 4500 | 3.50 | 3.75 |
| RoPE | 9000 | 3.23 | 3.70 |
* RoPE best val loss: 3.69 at step 7500 (overfitting after)

RoPE reaches lower loss and generalizes better — consistent with how modern LLMs like Qwen and LLaMA use it.

## How to run

```bash
git clone https://github.com/saslifat-gif/build-llm-from-scratch
cd build-llm-from-scratch
pip install torch
jupyter notebook
```

## About me

I am a AI student building toward a ML engineer.  
find me on [HuggingFace](https://huggingface.co/lifatsastain) | [GitHub](https://github.com/saslifat-gif)
