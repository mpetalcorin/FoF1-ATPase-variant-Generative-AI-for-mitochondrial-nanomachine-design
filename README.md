# FoF1-ATPase-variant-Generative-AI-for-mitochondrial-nanomachine-design
Proof of concept for using generative AI to design synthetic FoF1 ATPase subunit variants. Includes synthetic dataset, variational autoencoder model, visualizations, and reproducible notebook for mitochondrial bioengineering research.

# Deep Generative Models for FoF1 ATPase Variant Design

This repository provides a proof-of-concept demonstration for the paper:

***"Petalcorin M.I.R.(2025) Deep Generative Models for Designing Synthetic Variants of FoF1 ATPase Subunits in Bioengineering"***

It shows how **synthetic datasets** and **variational autoencoders (VAEs)** can be combined to generate novel FoF1 ATPase subunit variants with predicted improvements in torque stability and proton coupling efficiency.

## Project Overview

- **Synthetic dataset** simulates ATPase subunit "sequences" along with two functional metrics (torque stability, proton coupling).  
- **Variational Autoencoder (VAE)** learns a latent space representation and generates new candidate variants.  
- **Evaluation metrics** include reconstruction accuracy, predicted efficiency distributions, and comparison between real and generated variants.  
- **Visualizations** reproduce figures used in the paper:
  - Training loss curve  
  - Latent space embedding (PCA)  
  - Distribution of predicted efficiency  
  - Torque vs Proton coupling scatter  

## Dependencies

	•	torch
	•	numpy
	•	pandas
	•	matplotlib
	•	seaborn
	•	scikit-learn

## DataSheet

Name: **Synthetic FoF1 ATPase Variant Dataset**
Version: 1.0 (simulated, proof of concept)
Size: 5000 samples
Format: NumPy array and Pandas DataFrame

**Features**
	•	Sequence features: 50 positions per variant (numerical embeddings of amino acids).\
	•	Torque stability: Continuous variable (mean 0.7, std 0.1).\
	•	Proton coupling efficiency: Continuous variable (mean 0.65, std 0.1).\
	•	Efficiency score: Weighted average of torque and proton coupling.

**Motivation**
The dataset mimics structural and functional properties of FoF1 ATPase subunits. It is not biological data but is constructed to resemble realistic sequence-function relationships for training generative models.

**Intended Uses**
	•	Training and evaluating generative models (VAE, GANs).\
	•	Proof-of-concept demonstrations for AI-driven protein design.\
	•	Educational and illustrative purposes.

**Limitations**
	•	Not derived from experimental sequences.\
	•	Simplified statistical distributions.\
	•	Should not be used for direct biological inference.

## Model Card

Model Name: **Variational Autoencoder (VAE) for FoF1 Variant Generation**
Version: 1.0 (proof of concept)
Framework: PyTorch

**Model Description**
	•	Input: 52-dimensional vector (50 pseudo-sequence features, 2 performance metrics).
	•	Latent space: 16 dimensions.
	•	Encoder: 128-unit hidden layer, mean and logvar heads.
	•	Decoder: 128-unit hidden layer, output reconstructed vector.
	•	Loss: MSE reconstruction loss + KL divergence.

**Training Data**
	•	Synthetic dataset of 5000 subunit variants.
	•	Batch size: 64
	•	Epochs: 20
	•	Optimizer: Adam (lr=0.001)

**Evaluation**
	•	Reconstruction loss convergence.
	•	Latent space visualization using PCA.
	•	Efficiency distribution comparison between real and generated variants.
	•	Scatterplots of functional metrics (torque vs proton coupling).

**Intended Uses**
	•	Generate synthetic FoF1 ATPase subunit variants for research demonstrations.
 
 **Repository Structure**
 
<img width="341" height="256" alt="image" src="https://github.com/user-attachments/assets/ece98d8c-e41a-4422-9263-d726d7734bba" />

	•	Explore AI-driven design workflows in mitochondrial bioengineering.\
	•	Serve as an educational example for generative biology.\

**Limitations**
	•	Does not reflect real biological diversity.\
	•	Predictions are not validated experimentally.\
	•	Should be treated **strictly as a proof-of-concept**.

 **Citation**
Petalcorin, M. I. R. (2025).
Deep Generative Models for Designing Synthetic Variants of FoF1 ATPase Subunits in Bioengineering.
Manuscript in preparation.
