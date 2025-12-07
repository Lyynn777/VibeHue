# 🌈 VibeHue
![Python](https://img.shields.io/badge/Python-3.9-3776AB?style=for-the-badge&logo=python&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Models-FFCC00?style=for-the-badge&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-NLP-orange?style=for-the-badge&logo=huggingface)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Pillow](https://img.shields.io/badge/Pillow-Image%20Processing-6A0DAD?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-003B57?style=for-the-badge&logo=python&logoColor=white)

This project takes a text input (a sentence describing a mood) and predicts an emotion using two open-source NLP models.  
Based on the predicted emotion, it generates a simple 5-color palette.  
Everything runs locally in Google Colab without any external API keys.

---

## What This Project Actually Does
- Uses **two publicly available HuggingFace models** to classify the emotion in a short text input.
- Combines their predictions using a basic weighted average (an ensemble).
- Maps the final predicted emotion to a predefined RGB color.
- Creates four small color variations around that base color.
- Outputs these five colors as a single image.

---

## What This Project **Does Not** Do
- It does **not** understand emotions deeply like a human.
- It does **not** analyze tone, sarcasm, or complex multi-layer emotions.
- It does **not** generate “psychologically accurate” colors — it just uses a fixed mapping.
- It does **not** produce any real-world emotional insights.
- It does **not** work perfectly for short or vague inputs.
- It does **not** function as a mood or therapy tool.

---

## How the Emotion Detection Works 
- Model A predicts one of 7 basic emotions.
- Model B predicts one of 6 basic emotions.
- These outputs are placed into the same set of categories.
- A simple weighting picks a final emotion.
- This is **not a scientifically validated method** — it’s just a practical merging of model outputs.

This means the emotion prediction is approximate and sometimes wrong.

---

## How the Color Generation Works
- Each emotion is linked to one fixed RGB color.
- No deep research behind it — just general associations (e.g., sadness → blue).
- A few brightness/shift values are added to create a palette.
- Output is saved as `mood_palette.png`.

This produces visually consistent but **not emotionally “accurate”** colors.

---

## Why This Project Exists
- To demonstrate how to combine two NLP models in a simple ensemble.
- To show how model outputs can drive a small creative visualization task.
- To practice integrating transformers + Python image generation.
- It is a small, experimental project — not a polished application.

---

## Requirements
transformers
torch
pillow
matplotlib

yaml
Copy code
Google Colab installs these automatically.

---

## Limitations
- Emotion predictions are not always reliable.
- The palette generation is extremely simple.
- Works only with English text.
- Longer or more nuanced sentences may confuse the models.
- This is more of an **educational experiment** than a practical tool.

---
