# 🧠 Vision-to-Image Prompt Pipeline with LLMs & Diffusion

This project was developed as part of the **NVIDIA Rapid Application Development Using Large Language Models** course assessment. It showcases how to integrate **Vision-Language Models (VLMs)**, **Large Language Models (LLMs)**, and **diffusion models** into a unified AI-powered creative pipeline.

The system takes an **input image**, understands its content using AI, then generates **new AI-created images** using intelligently synthesized prompts.

---

## 🚀 Project Overview

This notebook demonstrates a complete multimodal AI workflow:

1. **Image Understanding** – A Vision-Language Model analyzes an image and generates a textual description  
2. **Prompt Synthesis** – A Large Language Model transforms that description into optimized prompts  
3. **Image Generation** – A diffusion model creates brand-new images from those prompts  

This reflects how modern AI systems combine perception and generation in real-world creative tools.

---

## 🏗️ Pipeline Architecture

**Input Image → VLM Description → LLM Prompt Engineering → Diffusion Image Generation**

| Stage | Model Type | Purpose |
|------|------------|---------|
| Image Analysis | Vision-Language Model | Converts visual content into descriptive text |
| Prompt Creation | LLM (via LangChain) | Enhances and optimizes prompts for image generation |
| Image Generation | Stable Diffusion (Hugging Face Diffusers) | Produces new AI-generated images |

---

## ✨ Features

✔ Image captioning using a Vision-Language Model  
✔ LLM-powered prompt enhancement  
✔ Automatic generation of multiple synthetic prompts  
✔ AI image generation with diffusion models  
✔ Fully automated end-to-end pipeline  

---

## 🧩 Key Functions Implemented

### 🖼️ `ask_about_image(image_path, question)`
Uses a Vision-Language Model to:
- Load and interpret an image  
- Answer a question about the image (default: **"Describe the image"**)  
- Return a detailed textual caption  

---

### 🎨 `generate_images(prompt, n)`
Uses Stable Diffusion to:
- Convert a text prompt into one or more images  
- Save generated images locally  
- Return the generated image outputs  

---

### ✍️ `llm_rewrite_to_image_prompts(description, n=4)`
Uses a Large Language Model to:
- Convert a long-form image description  
- Generate multiple short, high-quality prompts  
- Optimize prompts specifically for diffusion-based image models  

---

### 🔁 Final Automated Workflow

1. Load an input image  
2. Generate a visual description  
3. Produce multiple AI-optimized prompts  
4. Generate multiple AI-created images  

---

## 🛠️ Tech Stack

- **NVIDIA-hosted LLM API**  
- **LangChain** for prompt orchestration  
- **Hugging Face Diffusers** for Stable Diffusion  
- **PyTorch** for deep learning execution  
- **PIL & Matplotlib** for image handling and visualization  

---

## 📦 Installation

Install required Python libraries:

```bash
pip install torch diffusers transformers accelerate pillow matplotlib langchain
pip install langchain-nvidia-ai-endpoints
```

### Requirements

- Access to an NVIDIA LLM API endpoint  
- A system capable of running Stable Diffusion (GPU strongly recommended)

---

## ▶️ How to Run

1. Open the Jupyter Notebook  
2. Configure your NVIDIA API endpoint  
3. Provide the path to an input image  
4. Run all cells in order  

The notebook will:
- Analyze the image  
- Generate prompts automatically  
- Produce AI-generated images  
- Save results locally  

---

## 📁 Output

Generated images are stored in a folder similar to:

```
generated_images/
│── image_1.png
│── image_2.png
│── image_3.png
│── image_4.png
```

Each image corresponds to a different AI-generated prompt.

---

## 🎯 Learning Outcomes

This project demonstrates how to:

- Connect vision models with language models  
- Use LLMs for automated prompt engineering  
- Build multimodal AI pipelines  
- Combine perception and generative creativity  

---

## 📜 Credits

Developed as part of the **NVIDIA Deep Learning Institute** course:  
**Rapid Application Development Using Large Language Models**
