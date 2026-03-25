# Spatial Control in 2D Diffusion Models using ControlNet

This repository contains the implementation and evaluation of **spatial control in image diffusion models** using **ControlNet**. The project was developed as part of a research workshop on computer vision and graphics, mentored by experts from Cornell, Stanford, Purdue, and Meta.

## 🔹 Overview

Diffusion models generate images from text prompts but often **struggle with spatial alignment**, especially for complex poses or structured content. This project focuses on:

- **Spatial Conditioning:** Using ControlNet to guide image generation based on input edge maps (Canny edges), ensuring the output respects the structure of the input.
- **Evaluation Metrics:** Edge IoU, Mask/Area IoU, and Edge F1 score are computed to quantitatively assess spatial alignment.
- **Visualization:** Original images, conditioning maps, generated images, and overlayed evaluation metrics are provided for intuitive analysis.

## 🛠 Key Features

- Integration with **FluxControlNetPipeline** for controlled image generation.
- End-to-end pipeline: Input → Edge Detection → ControlNet-guided Generation → Evaluation.
- Metrics visualization for **spatial consistency** between conditioning maps and generated outputs.
- Supports GPU acceleration with PyTorch.

## 💡 Highlights

- Achieves spatially aligned image generation even in **resource-limited environments**.
- Demonstrates clear improvements in structural alignment compared to standard diffusion outputs.
- Includes professional-level visualizations for both **qualitative and quantitative evaluation**.

## 📚 References

- Ho et al., *Denoising Diffusion Probabilistic Models*, 2020.  
- Zhang et al., *ControlNet: Adding Conditional Control to Text-to-Image Diffusion Models*, 2023.  
- Brohan et al., *InstructPix2Pix: Learning to Follow Image Editing Instructions*, 2023.  

## ⚡ Quick Start

```bash
pip install -q diffusers transformers accelerate safetensors torch torchvision torchaudio \
xformers opencv-python-headless pillow numpy scipy matplotlib
```
