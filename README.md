# My GPT

A PyTorch implementation of a GPT-style transformer model for text generation.

## Overview

This project implements a GPT (Generative Pre-trained Transformer) model from scratch using PyTorch. The model is trained on the TinyShakespeare dataset to generate text in the style of Shakespeare. It demonstrates the fundamental concepts of transformer-based language models including self-attention, multi-head attention, and positional encodings.

## Features

- Character-level tokenization
- Self-attention mechanism
- Multi-head attention
- Positional encodings
- Layer normalization and residual connections
- Text generation capabilities

## Implementation Details

The implementation follows the architecture described in the "Attention Is All You Need" paper, but scaled down for educational purposes. Key components include:

- **Tokenization**: Simple character-level tokenization
- **Embedding**: Token and positional embeddings
- **Self-Attention**: Implementation of scaled dot-product attention
- **Feed-Forward Networks**: Multi-layer perceptrons between attention blocks
- **Decoder Block**: Combination of self-attention and feed-forward layers with residual connections
- **Layer Normalization**: Applied before each sub-layer in the decoder
- **Text Generation**: Autoregressive sampling to generate new text

## Training

The model is trained on the TinyShakespeare dataset with the following parameters:
- Context length (block size): 256 characters
- Batch size: 64
- Embedding dimension: 384
- Number of attention heads: 6
- Number of transformer layers: 6
- Dropout rate: 0.2
- Learning rate: 3e-4

## Future Improvements

- Implement more sophisticated tokenization (e.g., BPE or WordPiece)
- Scale up model size (more layers, larger embedding dimensions)
- Train on larger and more diverse datasets
- Implement more efficient attention mechanisms (e.g., flash attention)
- Add model checkpointing and resumable training

## References

- "Attention Is All You Need" paper: https://arxiv.org/pdf/1706.03762.pdf
- GPT-3 paper: https://arxiv.org/pdf/2005.14165.pdf
- Based on educational materials by Andrej Karpathy: https://karpathy.ai/zero-to-hero.html
- nanoGPT implementation: https://github.com/karpathy/nanoGPT