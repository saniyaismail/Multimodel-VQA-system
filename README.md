# VR_final_project

## Project Overview

This project is part of the VR course and focuses on building a multimodal Visual Question Answering (VQA) system using the Amazon Berkeley Objects (ABO) dataset. The goal is to create a multiple-choice VQA dataset by leveraging product images and metadata, evaluate baseline models, fine-tune selected models using Low-Rank Adaptation (LoRA), and assess performance using standard metrics.

---

## Project Structure
```
├── accuracy.ipynb # Notebook to analyse the accuracy
├── baseline_models/ # Folder containing baseline model notebooks, results, and evaluation files
│ ├── BLIP/
│ ├── BLIP2/
│ └── VILT/
├── data_curation/ # Data curation notebook and curated dataset CSV
├── finetuned_model/ # Finetuned BLIP model using LORA
└── README.md # Project README
```
---

## Features

- Data curation pipeline to generate a single-word answer VQA dataset from ABO dataset images using multimodal APIs and on-device models.
- Evaluation of multiple off-the-shelf baseline VQA models including BLIP, BLIP2, and VILT.
- Fine-tuning of selected models with LoRA for parameter-efficient adaptation.
- Performance evaluation using Accuracy, F1 Score, and additional advanced metrics like BERTScore and BARTScore.
- Experimentation with model compression and optimization techniques for faster inference.

---

## Installation Instructions

1. Clone this repository:

   ```bash
   git clone https://github.com/Shriya8704/VR_final_project.git
   cd VR_final_project
   ```
2. Download the small variant of the Amazon Berkeley Objects (ABO) dataset (3GB):
- Dataset link: [ Amazon Berkeley Objects (ABO) dataset](https://amazon-berkeley-objects.s3.amazonaws.com/index.html)
- Use the metadata CSV and 256x256 product images.

3. Set up API keys or local environment for multimodal models if using Gemini 2.0 API

## Usage Guide
1. Data Curation
- Navigate to the data_curation/ folder.
- Run data_curation.ipynb to process the ABO dataset, generate VQA question-answer pairs, and save the curated dataset as data_curation_output.csv.

2. Baseline Evaluation
- Baseline models are implemented in baseline_models/BLIP/, baseline_models/BLIP2/, and baseline_models/VILT/.
- Run the respective Jupyter notebooks (*_baselinemodel.ipynb) to evaluate pre-trained models on the curated dataset.
- Results and evaluation metrics are saved within each baseline model folder.

3. Fine-Tuning
- Fine tuned the blip model using LORA. Run the jupyter notebook in finetuned_model/ to train.

4. Evaluation
- Evaluate model performance using accuracy.ipynb
- F1 score, and other metrics are implemented in the notebooks.
- Visualize and analyze results using plots and CSV summaries included in baseline model folders.
