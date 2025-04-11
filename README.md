# BART Text Summarization Project

This repository contains a complete pipeline for fine-tuning, testing, and using the BART model for text summarization.

## Project Structure

- `bart_fine_tuning.ipynb`: Notebook used for fine-tuning the BART model on a summarization dataset.
- `bart_testing.ipynb`: Notebook used for testing the performance of the fine-tuned BART model.
- `data_proc.ipynb`: Notebook that handles data preprocessing tasks required before model training.

## Installation

To set up the environment and install all dependencies, simply install the packages listed in the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

## Usage

1. Preprocess your dataset using `data_proc.ipynb`.
2. Fine-tune the BART model using `bart_fine_tuning.ipynb`.
3. Test the fine-tuned model using `bart_testing.ipynb`.

## 📈 Evaluation Metrics

Both ROUGE and BLEU metrics were used to evaluate the quality of generated summaries compared to reference summaries.

---

## 📊 ROUGE Evaluation Results

| Metric        | Pre-trained BART | Fine-tuned BART |
|---------------|------------------|-----------------|
| ROUGE-1       | 0.3202 (±0%)     | 0.4465 (**+39%**) |
| ROUGE-2       | 0.1250 (±0%)     | 0.2370 (**+90%**) |
| ROUGE-L       | 0.2130 (±0%)     | 0.3610 (**+69%**) |
| ROUGE-Lsum    | 0.2138 (±0%)     | 0.3613 (**+69%**) |

### ⏱️ Evaluation Time

| Model           | Time (s)     |
|------------------|--------------|
| Pre-trained BART | 21.51        |
| Fine-tuned BART  | 7.99         |
| **Speed-up**     | **~2.7x faster** |

---

## 📊 BLEU Evaluation Results

| Metric   | Pre-trained BART | Fine-tuned BART |
|----------|------------------|-----------------|
| BLEU     | 0.0411 (±0%)     | 0.1067 (**+160%**) |

### ⏱️ Evaluation Time

| Model           | Time (s)     |
|------------------|--------------|
| Pre-trained BART | 17.91        |
| Fine-tuned BART  | 6.78         |
| **Speed-up**     | **~2.64x faster** |

---

## License

This project is open-source and available under the MIT License.
