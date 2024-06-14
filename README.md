# Super-Model

## Overview
This repository contains the code and data for our project on generating images from textual descriptions using a combination of a transformer model for data preparation and a pretrained Stable Diffusion model for image generation and evaluation. Our study explores the performance of Stable Diffusion in generating realistic images from captions of varying lengths and assesses the quality and relevance of these images using Inception Score (IS) and CLIP Score.

## Project Structure
The project is divided into two main parts:

1. **Data Preparation with Transformer:**
   - We use a transformer model to generate captions for our datasets.
   - This part involves downloading the datasets, generating textual descriptions using the BLIP model based on Vision Transformers (ViT) from Hugging Face, and splitting the data into training and validation subsets.
   - The code for this part is available in the `data_preparation` directory.

2. **Image Generation and Evaluation with Stable Diffusion:**
   - We use the `model.py` script to employ the pretrained Stable Diffusion model to generate images from the captions.
   - This script also calculates the CLIP Scores and performs comparisons between different caption lengths.
   - Our findings indicate that for different animals, both the IS and CLIP Scores increase as the caption length grows.
   - The code for this part is available in the `model` directory.

## Repository Contents
- `data_preparation/`: Contains scripts for data preparation and caption generation.
- `model/`: Contains the `model.py` script for image generation and evaluation.
- `images/`: Contains example images for comparison.

## Getting Started
### Prerequisites
- Python 3.7+
- PyTorch
- Transformers (Hugging Face)
- Diffusers (Hugging Face)
- torchvision
- pandas
- PIL
- torch-fidelity

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/super-model.git
   cd super-model
