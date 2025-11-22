MNIST Curation Lab – Enhanced MNIST with an IDK Category

This repository contains my work for Dataset Curation Lab 1 – MNIST, completed as part of the Applied Hands-On Computer Vision course.

🔎 Project Summary

In this assignment, I carried out a complete data-curation pipeline on the MNIST dataset. The main steps include:

Loading MNIST using FiftyOne together with PyTorch datasets

Generating image embeddings with a modern LeNet-5 style CNN

Exploring the embedding distribution using PCA and UMAP inside FiftyOne

Computing a difficulty score for each digit and identifying the top 2% most challenging samples

Reassigning these difficult examples to a new IDK (“I Don’t Know”) class

Marking these ambiguous samples in FiftyOne for manual review

Training a classifier with 11 classes (digits 0–9 plus the new IDK class)

Comparing model behavior on standard digits vs. the curated IDK samples

📘 Notebook

The complete implementation is available in:

Lab_Assignment_1_MNIST_Curation.ipynb

You can run this notebook directly in Google Colab or view it on GitHub.

📦 Curated Dataset on HuggingFace

The final MNIST dataset (with the extra IDK label) is published on HuggingFace:

👉 https://huggingface.co/datasets/MJ3099/mnist-curated-idk

The dataset follows the ImageClassificationDirectoryTree layout, with one directory per class:

0, 1, 2, ..., 9, 10 (IDK)

🧰 Requirements

High-level dependencies include:

Python 3.10 or newer

PyTorch

torchvision

FiftyOne

UMAP-learn

scikit-learn

huggingface_hub

All required installations are handled automatically in the first cell of the notebook.

🧪 How to Reproduce the Workflow

Open the notebook in Google Colab

Run the installation cell

Execute the notebook from top to bottom to:

Create embeddings

Visualize PCA and UMAP plots

Select and relabel hard samples

Train and evaluate the 11-class classifier

(Optional) Export the curated dataset and upload it to your own HuggingFace account
