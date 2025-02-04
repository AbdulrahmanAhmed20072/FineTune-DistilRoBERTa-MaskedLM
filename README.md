# Fine-Tuning DistilRoBERTa for Masked Language Modeling (MLM)

This repository fine-tunes DistilRoBERTa for Masked Language Modeling (MLM) using Parameter-Efficient Fine-Tuning (PEFT) with LoRA and BitsAndBytes quantization.

## Features

- **DistilRoBERTa Fine-Tuning**: Adapts DistilRoBERTa for masked language modeling.
- **LoRA & BitsAndBytes**: Efficient training with low-rank adaptation and 4-bit quantization.
- **Dataset Preparation**: Uses the ELI5 dataset for training.
- **Training Pipeline**: Utilizes Hugging Face `Trainer` for efficient model training.
- **Evaluation**: Computes perplexity and accuracy for masked token prediction.

## Files

1. **`MaskedLM_LoRA_BnB.ipynb`**: Python script implementing the training pipeline.
2. **Dataset**: ELI5 dataset for masked language modeling.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AbdulrahmanAhmed20072/FineTune-MaskedLM-DistilRoBERTa.git
   ```
2. Install the required dependencies:
   ```bash
   pip install datasets bitsandbytes accelerate evaluate transformers torch peft numpy
   ```

## Usage

1. Load and preprocess the dataset.
2. Fine-tune DistilRoBERTa with LoRA and quantization.
3. Evaluate model performance.
4. Perform masked token prediction.

Run the script:
```bash
python MaskedLM_LoRA_BnB.ipynb
```

## Outputs

- Fine-tuned DistilRoBERTa model for masked language modeling.
- Perplexity and accuracy evaluation on test data.
- Predicted masked token replacements.

## Example

Input Text:
```
I'm going to school every <mask>
```

Predicted Tokens:
```
morning, day, afternoon, night, week
```
