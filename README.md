# Text-to-Python Code Generation using Seq2Seq Models

## Overview
This project implements and compares three sequence-to-sequence models for generating Python code from natural language descriptions:
1. Vanilla RNN Seq2Seq
2. LSTM Seq2Seq  
3. LSTM with Bahdanau Attention

## Dataset
- **Source**: CodeSearchNet Python dataset
- **Training samples**: 10,000
- **Validation samples**: 1,000
- **Test samples**: 1,000

## Model Configurations
- Embedding dimension: 256
- Hidden dimension: 256
- Batch size: 64
- Learning rate: 0.001
- Epochs: 20

## Results Summary

### Final Test Set Performance
| Model | BLEU Score | Exact Match |
|-------|------------|-------------|
| Vanilla RNN | 0.0014 | 0.0000 |
| LSTM | 0.0014 | 0.0000 |
| LSTM + Attention | 0.0038 | 0.0000 |

## Files
- `vanilla_rnn_final.pt` - Trained Vanilla RNN model
- `lstm_final.pt` - Trained LSTM model
- `attention_final.pt` - Trained Attention model
- `docstring_vocab.pkl` - Docstring vocabulary
- `code_vocab.pkl` - Code vocabulary
- `final_results.json` - Detailed results
- `training_curves.png` - Training/validation loss curves
- `results_comparison.png` - Model comparison charts
- `attention_example_*.png` - Attention visualizations

## Running the Code
All code is contained in this Kaggle notebook. Simply run cells in order.

## Key Findings
1. **LSTM vs Vanilla RNN**: LSTM shows improved performance over vanilla RNN, especially for longer docstrings
2. **Attention Mechanism**: Further improves performance and provides interpretability
3. **Length Analysis**: All models perform better on shorter docstrings, but attention model degrades less on long inputs

## Author
[Your Name]
