# Disease Prediction Using Fine-Tuned BERT

An educational deep learning project that uses a fine-tuned BERT model to classify symptom descriptions into 22 disease categories.

## Project Overview

This project uses the pretrained `bert-base-uncased` transformer and fine-tunes it for multi-class symptom-text classification. A Gradio interface allows users to submit a symptom description and view the model's top three candidate labels.

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-learn
- Gradio
- Google Colab

## Dataset

Dataset: [Symptom to Diagnosis — Gretel AI](https://huggingface.co/datasets/gretelai/symptom_to_diagnosis)

- Training examples before validation split: 853
- Validation examples: 128
- Training examples used for gradient updates: 725
- Held-out test examples: 212
- Disease classes: 22

## Model Training

- Base model: BERT-base-uncased
- Task: Multi-class text classification
- Experiment 1: 3 epochs, learning rate 2e-5
- Experiment 2: 5 epochs, learning rate 1e-5
- Evaluation metrics: Accuracy, macro precision, macro recall, macro-F1

## Experiment 2 — Test Results

| Metric | Score |
|---|---:|
| Test loss | 1.9493 |
| Accuracy | 75.00% |
| Macro precision | 78.82% |
| Macro recall | 74.53% |
| Macro-F1 | 72.07% |

These results are from the current held-out test evaluation. The same test set was used during iterative development, so the scores should not be interpreted as an independent clinical benchmark.

## Running the Project

1. Open the notebook in Google Colab.
2. Install the required Python libraries.
3. Run the notebook cells in order.
4. Fine-tune the model or load a compatible saved checkpoint.
5. Launch the Gradio interface to test symptom descriptions.

See `requirements.txt` for the main Python dependencies.

## Limitations and Disclaimer

This project is intended for educational and research demonstration purposes only. It has not been clinically validated and must not be used to diagnose or treat medical conditions.

Predicted labels and model scores are experimental outputs, not validated clinical probabilities.
