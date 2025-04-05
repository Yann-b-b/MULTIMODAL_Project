# Bridging Spaces Between Modalities

This project investigates multimodal learning techniques for aligning and integrating multiple data types—image, audio, and text—into a shared latent representation space. We propose a novel, scalable framework that enables indirect cross-modal translation by using translator functions structured as edges in a graph architecture.

## 📄 Full Report

You can find the full paper [here](https://github.com/Yann-b-b/MULTIMODAL_Project/blob/main/MULTIMODAL_COURSE_PROJECT%20(1).pdf).

## 🔍 Overview

Current models like CLIP and ImageBind are limited by their dependence on image-paired datasets and modality gaps. Our framework enables:

- **Flexible addition of new modalities**  
- **Indirect traversal between unpaired modalities**  
- **Preservation of modality-specific features**  
- **Improved cross-modal alignment through contrastive fine-tuning and post-hoc techniques**

## 🧠 Key Concepts

- **Graph-based modality bridging**: Modalities = nodes, translators = edges  
- **MLP-based translators**: Enable cross-modal embedding conversion  
- **Reconstruction Loss**: Measures information preservation after cross-modal traversal  
- **Contrastive fine-tuning**: Improves cross-modal cohesion  
- **Post-hoc alignment**: Refines latent spaces after training  

## 📊 Modalities Used

- **Image/Video** embeddings via pretrained visual encoders (e.g., ImageBind)  
- **Audio** embeddings via pretrained audio encoders  
- **Text** embeddings via transformers  

Each data sample includes precomputed (image, audio, text) embeddings.

## 🏗️ Architecture

- Each translator is a small MLP mapping one modality to another.
- Traversals like `image → text → audio → image` are used to measure how well information is preserved.
- Cosine similarity is used as a reconstruction loss.

### Reconstruction Loss Formula:

L_recon = 1 - cosine_similarity(x_original, x_reconstructed)



## 🔁 Adding New Modalities

1. Create an encoder for the new modality.
2. Link it to at least one existing modality using contrastive learning.
3. Train a translator MLP.
4. Embed it into the existing graph.

## 📈 Evaluation Metrics

- **Inter-modality distance** (cosine/Euclidean)  
- **Cluster separability**  
- **Retrieval accuracy**

## 🧪 Experiments

- Compared results of CLIP, ImageBind, and DMVAE  
- Visualized modality gaps  
- Evaluated reconstruction performance using synthetic multi-hop translations  

## 📚 References

- [CLIP](https://arxiv.org/abs/2103.00020)  
- [ImageBind](https://arxiv.org/abs/2305.05665)  
- [DMVAE](https://openaccess.thecvf.com/content/CVPR2021W/CVPM/html/Lee_Private-Shared_Disentangled_Multimodal_VAE_for_Learning_of_Latent_Representations_CVPRW_2021_paper.html)  
- [Mind the Gap](https://arxiv.org/abs/2203.02053)  
- [Escaping Plato's Cave](https://arxiv.org/abs/2503.05283)
