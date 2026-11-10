# gpt-from-scratch

A character-level GPT built from scratch in PyTorch and trained on Tiny Shakespeare, following Andrej Karpathy's lecture [Let's build GPT: from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY).

## Progress

- [x] Data pipeline: character tokenizer, train/val split, batching
- [x] Bigram baseline (notebook)
- [ ] `bigram.py` script with train/val loss evaluation
- [ ] Self-attention math trick
- [ ] Single attention head
- [ ] Multi-head attention
- [ ] Feed-forward layer
- [ ] Residual connections and LayerNorm
- [ ] Dropout and scale-up

## Results

| Model | Loss |
|---|---|
| Uniform guess (`ln(65)`) | 4.17 |
| Bigram | ~2.4 (train batch) |

## Layout

```
notebooks/explore.ipynb   exploration: tokenizer, batching, bigram, attention
input.txt                 Tiny Shakespeare (~1.1M characters)
```

## Setup

Requires [uv](https://docs.astral.sh/uv/).

```
uv sync
```

Open `notebooks/explore.ipynb` in VS Code or Cursor and select the `.venv` kernel, or run `uv run --with jupyter jupyter lab`.

## Credits

Based on Andrej Karpathy's lecture and his [ng-video-lecture](https://github.com/karpathy/ng-video-lecture) code (MIT license).
