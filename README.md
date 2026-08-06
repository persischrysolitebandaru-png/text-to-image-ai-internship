# 🌸 Text-to-Image Generation using Conditional GAN, Self-Attention, and Stable Diffusion

## 📌 Project Overview

This project demonstrates the development of an end-to-end **Text-to-Image Generation** pipeline using modern deep learning techniques. The system generates flower images from natural language descriptions by integrating multiple AI models into a single workflow.

The project was developed using the **Oxford-102 Flowers Dataset** and combines text preprocessing, generative adversarial networks, self-attention mechanisms, and a pre-trained Stable Diffusion model.

---

## 🚀 Features

- 📂 Oxford-102 Flowers Dataset Analysis
- 📝 Text Preprocessing using Hugging Face Transformers
- 🎨 Conditional Generative Adversarial Network (CGAN)
- 🧠 Self-Attention Enhanced Generator
- 🌼 Stable Diffusion Integration
- 🔄 End-to-End Text-to-Image Generation Pipeline
- 📊 Dataset Visualization and Analysis
- 💾 Model Saving and Reusability

---

## 🛠️ Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Diffusers
- Stable Diffusion
- TorchVision
- Matplotlib
- NumPy
- PIL (Pillow)
- Google Colab

---

## 📂 Dataset

**Dataset:** Oxford-102 Flowers Dataset

- 102 flower categories
- 7,169 training images
- 1,020 testing images

The dataset was used for:
- Dataset exploration
- Image preprocessing
- Conditional image generation
- Stable Diffusion workflow

---

## 🧩 Project Workflow

```
User Text Prompt
        │
        ▼
Hugging Face Text Processing
        │
        ▼
Text Embeddings
        │
        ▼
Conditional GAN + Self-Attention
        │
        ▼
Stable Diffusion
        │
        ▼
Generated Flower Image
```

---

## 📁 Project Structure

```
Text_to_Image_Generation/
│
├── Text_to_Image_Generation_Final.ipynb
├── README.md
├── requirements.txt
├── generated_images/
├── saved_models/
└── dataset/
```

---

## 📚 Project Sections

- Project Setup
- Dataset Loading and Analysis
- Text Preprocessing
- Conditional GAN (CGAN)
- Self-Attention Enhanced CGAN
- Stable Diffusion Integration
- Complete Text-to-Image Pipeline
- Results
- Conclusion

---

## 📈 Results

The project successfully demonstrates:

- Loading and analyzing a custom dataset.
- Preprocessing textual inputs using Hugging Face Transformers.
- Building a Conditional GAN for image generation.
- Enhancing the Generator using a Self-Attention mechanism.
- Integrating a pre-trained Stable Diffusion model.
- Generating flower images from natural language prompts.

---

## 🔮 Future Improvements

- Fine-tune Stable Diffusion on larger custom datasets.
- Replace class labels with descriptive captions.
- Integrate Cross-Attention mechanisms.
- Improve image quality through longer training.
- Deploy the application using Streamlit or Gradio.

---

## 👩‍💻 Author

**Persis Chrysolite**

B.Tech – Artificial Intelligence & Machine Learning

Passionate about Artificial Intelligence, Machine Learning, Deep Learning, and Generative AI.

---

## ⭐ Acknowledgements

- Hugging Face
- PyTorch
- Diffusers Library
- Oxford-102 Flowers Dataset
- Google Colab

---

## 📜 License

This project is intended for educational and learning purposes.
