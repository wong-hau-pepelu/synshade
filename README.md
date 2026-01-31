# SynShade

A fine-tuned BERT model for detecting insider threat recruitment patterns in dark web communications.

## Overview

SynShade uses a fine-tuned Google BERT model (`small_bert/bert_en_uncased_L-4_H-256_A-4/2`) to analyze and classify Telegram chatter from dark web sources. The model performs binary classification to distinguish between general advertising content and active insider recruitment attempts.

## Model Architecture

- **Base Model**: Small BERT (4 layers, 256 hidden units, 4 attention heads)
- **Classification Head**: Sigmoid activation for binary classification
- **Framework**: TensorFlow
- **Task**: Binary classification (Advertising vs. Insider Recruiting)

## Use Case

The model analyzes dark web communications to identify potential insider threat recruitment activity, helping security teams:
- Monitor underground forums and channels
- Detect recruitment patterns early
- Differentiate noise from genuine threats

## Training Data

The model was trained on Telegram chatter collected from dark web sources, labeled for:
- **Class 0**: Advertising/general content
- **Class 1**: Insider recruitment attempts

Note: Due to the sensitive nature of the data, the training dataset is not publicly available.


## Training Details

- **Training samples**: 6,062
- **Validation samples**: 1,299
- **Test samples**: 1,300
- **Optimizer**: Adam (lr=3e-5)
- **Batch size**: 32
- **Max sequence length**: 128 tokens

## Disclaimer

This tool is intended for cybersecurity research and defensive purposes only.
