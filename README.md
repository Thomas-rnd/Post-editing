# BART Fine-Tuning For Post-Editing

### Abstract:

This project aims to improve Automatic Speech Recognition (ASR) output using a Bidirectional Auto-Regressive Transformer (BART) for error correction. Inspired by Samrat Dutta's work on "Error Correction in ASR using Sequence-to-Sequence Models" [1], the approach involves fine-tuning BART with a custom dataset created by simulating errors in ASR predictions.

![design]()

### Acknowledgment:

This work builds upon the Hugging Face documentation [here](https://huggingface.co/docs/transformers/model_doc/bart) and the fine-tuning example by Patrick von Platen [here](https://huggingface.co/blog/fine-tune-wav2vec2-english)

### Objective:

This notebook provides a comprehensive overview of the fine-tuning process for BART, transforming it into a powerful post-editing tool for ASR errors. The custom dataset creation involves simulating errors in ASR predictions, leveraging a pre-existing ASR dataset.

### Dataset Creation Using Wav2Vec2

1. Load Timit dataset using datasets library.
2. Preprocess the dataset, preparing input values and labels.
3. Use Wav2Vec2 to predict and simulate errors.
4. Compute metrics and export results to a CSV file for BART fine-tuning.

### BART Fine-Tuning

1. Tokenize the dataset using BART tokenizer.
2. Create PyTorch dataset and dataloaders.
3. Initialize BART model and set hyperparameters.
4. Hyperparameters selection
5. Test the model and calculate Word Error Rate (WER).

### Results

![results]()

## References:

[1] Samrat Dutta, Shreyansh Jain, Ayush Maheshwari, Souvik Pal, Ganesh Ramakrishnan, and Preethi Jyothi. Error correction in ASR using sequence-to-sequence models. 2022.
