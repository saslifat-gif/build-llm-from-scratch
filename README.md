# Build a Language Model from Scratch

I want to show you how to build a language model from scratch using PyTorch, step by step, no magic.

most tutorials give you the full model and explain it after. here we build it piece by piece, so you can see exactly what each part does and why it matters.

## What you will learn

- what is a language model and how it predicts the next character
- how to build a tokenizer (text → numbers)
- how to build a Bigram model using `nn.Embedding`
- how to train it and generate text

## Series

| Part | Topic | Status |
|------|-------|--------|
| Part 1 | Bigram Language Model | done |
| Part 2 | Self Attention | coming soon |
| Part 3 | Full Transformer |  coming soon |

## How to run

```bash
git clone https://github.com/saslifat-gif/build-llm-from-scratch
cd build-llm-from-scratch
pip install torch
jupyter notebook
```

then open `how_to_build_a_basic_LanguageModel.ipynb` and run all cells.

## About me

I am a CS student building toward a ML engineer role at HuggingFace.  
find me on [HuggingFace](https://huggingface.co/lifatsastain) | [GitHub](https://github.com/saslifat-gif)
