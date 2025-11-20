# Deep Generative Models (DGM)


This repository contains the homework reports and implementations for the Deep Generative Models course.

## 📚 Course Syllabus
A comprehensive study of modern generative AI, covering:
* **Probabilistic Foundations:** Bayesian/Markov Networks & Variational Inference.
* **Explicit Density Models:** VAEs and Normalizing Flows.
* **Implicit Density Models:** GANs and their variants.
* **Score-Based Models:** Diffusion Models and SDEs.
* **Advanced Topics:** Audio/Video Generation, Mamba (SSMs), and Flow Matching.

---

## 📝 Homework 1: PGMs & Variational AutoEncoders

This assignment explores the math behind Probabilistic Graphical Models (PGMs) and analyzes disentanglement in VAEs.

### 1. Theoretical Report
* **Bayesian Networks:** modeled causal relationships for a medical diagnosis scenario and verified independence using d-separation.
* **Markov Networks:** Analyzed Markov Blankets, perfect maps, and factorization using maximal cliques.
* **Variational Inference:** Mathematically derived the Evidence Lower Bound (ELBO) and proved optimal parameter estimation for a specific distribution.

### 2. Implementation (VAE on dSprites)
Implemented a VAE from scratch to analyze **latent space disentanglement** using the dSprites dataset.

* **Core Architecture:** Standard VAE with Reparameterization Trick and BCE + KL Loss.
* **$\beta$-VAE Experiments:** Trained three models ($\beta=1, 4, 8$) to test the trade-off between reconstruction quality and disentanglement.
    * **$\beta=1$:** Best reconstruction (sharp images), entangled latent space.
    * **$\beta=8$:** Best disentanglement (MIG score: 0.1988), but blurry reconstructions.
* **Evaluation:**
    * **MIG Metric:** Quantified disentanglement success.
    * **PCA Visualization:** Visualized the latent space, showing clear structural separation for high-$\beta$ models.

### 3. Literature Review
Analyzed advanced VAE variants including **VQ-VAE** (Discrete Latent Space), **VampPrior** (Mixture of Posteriors), and **SC-VAE** (Sparse Coding via ISTA).
