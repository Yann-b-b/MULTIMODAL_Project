# Bridging Spaces Between Modalities

This project explores multimodal learning techniques to align and integrate multiple data types into a shared representation space. We investigate models such as CLIP, ImageBind, and DMVAE, analyzing their strengths and limitations in learning cross-modal relationships.

## 🔍 Key Topics
- **CLIP**: Contrastive language-image pretraining for shared latent space.
- **ImageBind**: Multimodal learning across six data types.
- **An Eye for an Ear**: Cross-modal alignment for zero-shot audio captioning.
- **DMVAE**: Disentangled representation learning with shared and private latent spaces.
- **TextBind (Proposed Approach)**: Reformulating ImageBind around text for enhanced cross-modal alignment.

## 📂 Project Structure
- `project.ipynb` – Code and analysis for multimodal learning experiments.
- `media/` – Figures and diagrams used in the paper.
- `references.bib` – Bibliography of related research papers.

## 🚀 Getting Started

### Install Dependencies
```bash
pip install transformers torch torchvision torchaudio
