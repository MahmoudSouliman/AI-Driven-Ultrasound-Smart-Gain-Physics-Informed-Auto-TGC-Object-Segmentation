# AI-Driven-Ultrasound-Smart-Gain-Physics-Informed-Auto-TGC-Object-Segmentation
An AI-driven "Zero-Button" ultrasound image enhancement pipeline that combines sound wave physics with a PyTorch U-Net to automate Time Gain Compensation (TGC).
# AI-Driven Ultrasound Smart-Gain: Physics-Informed Auto-TGC & Object Segmentation

An advanced biomedical engineering and computer vision framework implemented in Python and PyTorch. This project revolutionizes image enhancement in ultrasound (echography) systems by combining the physics of acoustic attenuation with Real-Time Deep Learning semantic segmentation.

## 📌 Project Overview
Traditional ultrasound devices rely on manual Time Gain Compensation (TGC) hardware sliders to counteract depth-dependent acoustic attenuation. This manual adjustment is subjective and prone to artifacts. 

This project introduces a **Zero-Button "Smart-Gain" Pipeline** that:
1. Simulates raw acoustic wave attenuation using the exponential loss formula:  
   $$I = I_0 \cdot e^{-2\alpha f z}$$
2. Deploys a lightweight **U-Net architecture** (PyTorch) to automatically segment target anatomical structures/organs in real-time.
3. Computes a **Context-Aware Auto-TGC Curve** strictly based on the extracted organ pixels, ignoring background noise and surrounding tissue fluctuations to restore perfect image homogeneity.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Environment:** Google Colab / Jupyter Notebooks
* **Deep Learning Framework:** PyTorch
* **Image Processing & Math:** OpenCV, NumPy
* **Data Visualization:** Matplotlib

---

## 🚀 Repository Structure
* `AI_Driven_Ultrasound_Smart_Gain.ipynb`: The complete, fully documented Google Colab notebook containing code blocks, text cells, and evaluations.
* `README.md`: Project documentation and portfolio presentation.

<p align="center">
<img src="ultrasound_ai_pipeline.jpg" alt="AI-Driven Ultrasound Smart-Gain Pipeline Architecture" width="90%">
</p>

## 📖 Step-by-Step Pipeline Description

### Step 1: Environment Setup & Physics Simulation
Generates a synthetic ultrasound phantom containing a hypoechoic tissue target. Applies exponential acoustic attenuation coefficient ($\alpha = 0.0035$) across the vertical axis to simulate a raw, uncompensated ultrasound scan.

### Step 2: Mathematical Auto-TGC Calculation
Implements a baseline automated TGC using standard moving average and row-by-row image intensity distribution. 

### Step 3: Lightweight U-Net Architecture
Constructs and trains a deep convolutional encoder-decoder network utilizing binary cross-entropy loss to predict the target structure's spatial mask from the corrupted, attenuated input frame.

### Step 4: AI-Guided Smart-Gain (The Solution)
Combines the predicted mask with physics parameters to calculate the gain adjustment vector exclusively from within the target tissue region, optimizing contrast dynamically.

### Step 5: Final Evaluation Dashboard
Generates side-by-side comparative visualizations and pixel histogram metrics to validate the superior performance of the AI-guided method over standard mathematical approaches.

---

## 📊 Results Summary
* **Image Homogeneity:** The AI-driven approach successfully compensates for fading in deep tissue rows without over-amplifying shallow structural noise.
* **Histogram Alignment:** Quantitative pixel distribution plots show that the AI-guided output perfectly maps back to the ideal non-attenuated ground-truth signature.

---

## 👨‍💻 Author
**Mahmoud Souliman** *Machine Learning Engineer & Biomedical Equipment Specialist* [LinkedIn Profile](https://www.linkedin.com/in/mahmoud-souliman-b676bb238/) | [GitHub Portfolio](https://github.com/MahmoudSouliman)
