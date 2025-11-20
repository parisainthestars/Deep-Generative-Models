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
* [cite_start]**Bayesian Networks:** modeled causal relationships for a medical diagnosis scenario and verified independence using d-separation [cite: 33-86].
* [cite_start]**Markov Networks:** Analyzed Markov Blankets, perfect maps, and factorization using maximal cliques [cite: 102-137].
* [cite_start]**Variational Inference:** Mathematically derived the Evidence Lower Bound (ELBO) and proved optimal parameter estimation for a specific distribution [cite: 212-260].

### 2. Implementation (VAE on dSprites)
Implemented a VAE from scratch to analyze **latent space disentanglement** using the dSprites dataset.

* [cite_start]**Core Architecture:** Standard VAE with Reparameterization Trick and BCE + KL Loss [cite: 275-328].
* [cite_start]**$\beta$-VAE Experiments:** Trained three models ($\beta=1, 4, 8$) to test the trade-off between reconstruction quality and disentanglement[cite: 396].
    * **$\beta=1$:** Best reconstruction (sharp images), entangled latent space.
    * [cite_start]**$\beta=8$:** Best disentanglement (MIG score: 0.1988), but blurry reconstructions [cite: 465-467].
* **Evaluation:**
    * **MIG Metric:** Quantified disentanglement success.
    * [cite_start]**PCA Visualization:** Visualized the latent space, showing clear structural separation for high-$\beta$ models [cite: 489-495].

### 3. Literature Review
[cite_start]Analyzed advanced VAE variants including **VQ-VAE** (Discrete Latent Space), **VampPrior** (Mixture of Posteriors), and **SC-VAE** (Sparse Coding via ISTA) [cite: 505-548].
