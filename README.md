# CCS2


# Music Emotion Recognition (MER) - Comparative Analysis of Unimodal and Multimodal Models

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

This project examines Music Emotion Recognition (MER) through a comparative study of **unimodal** (audio or lyrics features) and **multimodal** (combined audio and lyrics) approaches. Using machine learning techniques, we evaluated the effectiveness of each model in predicting emotions in music. The **Music4All** and **Music4All-Onion** datasets provide a foundation for our research, supporting analysis and model training.

## Project Structure

- **Data Processing**: 
  - Data cleaning: Removed duplicates and standardized.
  - Dimensionality Reduction: Reduced features using PCA (audio to 350 components, lyrics to 220 components).

- **Model Training**:
  - Implemented three Random Forest classifiers on audio, lyrics, and multimodal feature sets.
  - Hyperparameter tuning applied via Bayesian optimization for enhanced accuracy.

- **Testing and Evaluation**:
  - Cross-validation ensured model stability.
  - Statistical testing (t-tests) assessed significant differences among models.

## Datasets

- **Music4All**: Provides metadata, 30-second audio clips, lyrics, and valence ratings, supporting Music Information Retrieval (MIR) tasks.
- **Music4All-Onion**: Expands upon Music4All with additional multimodal features and metadata for a deeper MER analysis.

## Installation

Clone the repository and install required dependencies.

```bash
git clone https://github.com/AkiraWinds/CCS2.git
cd CCS2
pip install -r requirements.txt
```

## Usage

1. **Data Preparation**: Download the Music4All and Music4All-Onion datasets and place them in the `data/` directory.
2. **Run Preprocessing**: Execute `preprocess.py` to clean, standardize, and apply dimensionality reduction.
3. **Model Training and Evaluation**: Run `train_model.py` to train models and evaluate performance.

```bash
python preprocess.py
python train_model.py
```

## Results

- **Baseline Accuracy**:
  - Audio model: **64.21%**
  - Lyrics model: **60.11%**
  - Multimodal model: **64.55%**

- **Optimized Accuracy**:
  - Audio model: **65.65%**
  - Lyrics model: **62.87%**
  - Multimodal model: **67.14%**

The multimodal model achieved the highest accuracy, underscoring the potential of combining audio and lyrics features for MER tasks.

## Conclusions

Our study supports the hypothesis that multimodal methods improve MER accuracy compared to unimodal approaches. However, limitations, such as dataset quality and feature alignment, suggest room for improvement. Future research could focus on larger datasets and temporal alignment for better feature integration.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


