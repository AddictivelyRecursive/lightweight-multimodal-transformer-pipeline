# Lightweight Multimodal Transformer Pipeline

This repository provides a comprehensive pipeline for building a high-performance, resource-efficient image understanding system. By fine-tuning state-of-the-art **lightweight Vision Transformers (ViTs)**—specifically **MobileViT** and **DeiT-Tiny**—this project bridges the gap between accuracy and computational efficiency.

The resulting system goes beyond simple classification, offering a multi-faceted approach to image understanding including attribute prediction and cross-modal retrieval.

## Key Capabilities

The fine-tuned models in this repository are capable of three distinct downstream tasks:

1.  **Object Classification:** Accurate categorization of test images into 10 specific everyday object classes.
2.  **Visual Attribute Prediction:** extracting semantic details and relevant visual attributes from images (e.g., color, texture, shape).
3.  **Text-to-Image Retrieval:** Retrieving the most relevant images based on short textual queries.

## Datasets

The models were rigorously trained and evaluated on two distinct datasets to ensuring robustness:

* **Primary Dataset (Open Source):** A curated collection of ~600 self-collected images representing everyday objects.
    * **Access:** [Everyday Object Catalog on Kaggle](https://www.kaggle.com/datasets/arpitatomar04/everyday-object-catalog)
    * *Note: Detailed class lists and attribute taxonomies are available at the link above.*
* **Pooled Large-Scale Dataset:** A massive aggregation of over **11,000+ images** used to pre-train and stabilize the model weights (proprietary/unreleased).

## 📂 Repository Structure

| Directory | Description |
| :--- | :--- |
| **`./checkpoints`** | **Pre-trained Weights:** Download and use the trained model checkpoints directly for inference without re-training. |
| **`./notebooks`** | **Training Pipeline:** Complete Jupyter notebooks for fine-tuning MobileViT and DeiT-Tiny. Includes data loading, augmentation strategies, training loops, and hyperparameter configurations. |
| **`./interface.ipynb`** | **Inference Demo:** A user-friendly, interactive interface for testing the classification model on new images. |

## Performance & Evaluation

The `./notebooks` directory contains detailed training logs, including:
* **Accuracy Charts:** Visualization of training and validation accuracy over epochs.
* **Loss Curves:** Tracking convergence stability.
* **Evaluation Metrics:** Precision, Recall, and F1-score breakdowns for the fine-tuned models.

## Getting Started

To start using the classification interface:

1.  Clone the repository.
2.  Install dependencies (ensure `torch`, `torchvision`, and `transformers` are installed).
3.  Open `interface.ipynb`:
    ```bash
    jupyter notebook interface.ipynb
    ```
4.  Load a checkpoint from `./checkpoints` and start classifying!

---

*This project demonstrates the power of lightweight transformers for edge-ready computer vision applications.*