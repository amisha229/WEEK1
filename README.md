# WEEK2
# 👗 AI Closet: Smart Wardrobe Sustainability Advisor 🌱

## 🌍 Overview
Fast fashion is one of the biggest sustainability problems of our generation. Millions of garments are produced and discarded each year, contributing to landfill overflow, water pollution, and carbon emissions.  
**AI Closet** uses Convolutional Neural Networks (CNNs) to analyze clothing images, identify their apparel category, and suggest eco-friendly actions such as *reuse, donation, or recycling.*  
The goal is to help Gen Z consumers make more responsible wardrobe decisions through AI-based insights.

---

## 🧩 Problem Statement
Fast fashion trends drive unsustainable consumption. Most consumers are unaware of the environmental impact of their clothes.  
This project develops a CNN-based image recognition model that classifies clothing types (e.g., T-shirt, coat, sneaker, bag) and provides sustainability recommendations depending on their ecological footprint.

---

## 🎯 Objectives
- Train a CNN to classify clothing images with high accuracy.  
- Map predicted categories to sustainability information.  
- Recommend eco-friendly actions such as **Reuse**, **Repair**, **Donate**, or **Recycle.**  
- Demonstrate how AI can promote conscious fashion consumption.

---

## 🌱 Sustainability Link
- **Environmental:** Reduces textile waste and microplastic pollution.  
- **Social:** Promotes circular fashion and sustainable lifestyle awareness.  
- **Technological:** Showcases how AI can drive eco-conscious innovation.

---

## ⚙️ Technologies Used
- **Python**, **TensorFlow/Keras**, **NumPy**, **Pandas**, **Matplotlib**, **OpenCV**, **Seaborn**  
- (Optional) **Streamlit / Flask** for future UI deployment  

---

## 🗂 Dataset
- **Fashion-MNIST** — lightweight dataset of 70 000 clothing images (10 classes).  
  - Source: [Zalando Research](https://github.com/zalandoresearch/fashion-mnist)  
  - Loaded automatically via:  
    ```python
    from tensorflow.keras.datasets import fashion_mnist
    (x_train, y_train), (x_test, y_test) = fashion_mnist.load_data()
    ```

*Future upgrade:* integrate the **DeepFashion dataset** for real-world apparel imagery.

---

## 🧠 Model Architecture
| Layer | Details |
|-------|----------|
| Conv2D + ReLU + BN | 32 filters, 3×3 kernel |
| MaxPooling | 2×2 |
| Conv2D + ReLU + BN | 64 filters, 3×3 kernel |
| MaxPooling | 2×2 |
| Conv2D + ReLU + BN | 128 filters, 3×3 kernel |
| Flatten + Dropout(0.4) | Prevents overfitting |
| Dense(128, ReLU) | Fully connected layer |
| Dense(10, Softmax) | Output classes |

**Optimizer:** Adam  **Loss:** Categorical Cross-Entropy  **Metrics:** Accuracy  

---

## 📊 Week 2 Training Results

| Metric | Value |
|--------|--------|
| **Training Accuracy (Final Epoch)** | 90.9 % |
| **Validation Accuracy (Best Epoch)** | 91.3 % |
| **Validation Loss (Best Epoch)** | 0.2397 |
| **Training Loss (Final Epoch)** | 0.2449 |
| **Test Accuracy** | **≈ 91 %** |
| **Epochs Run** | 20 (Early Stopping around 16) |

### Key Observations
- Smooth convergence with no overfitting due to **BatchNorm + Dropout + Early Stopping.**  
- Minor class overlap between *T-shirt/top* and *Shirt.*  
- Consistently high accuracy across visually distinct categories (*Sneaker*, *Bag*, *Dress*).  

---

## 🧾 Sustainability Mapping
Each predicted clothing type is linked to estimated material, impact, and eco-action:

| Clothing Type | Material | Impact | Recommended Action |
|---------------|-----------|---------|--------------------|
| T-shirt/top | Cotton | Low | Reuse / Donate |
| Trouser | Denim | Medium | Repair / Reuse |
| Pullover | Wool | Medium | Upcycle |
| Dress | Synthetic Blend | High | Recycle / Donate |
| Coat | Polyester | High | Recycle |
| Sandal | Rubber | High | Reuse / Repair |
| Shirt | Cotton | Low | Donate / Reuse |
| Sneaker | Synthetic | High | Repair / Recycle |
| Bag | PU Leather | High | Repurpose / Recycle |
| Ankle boot | Leather | High | Repair / Resell |

---

## 📈 Visual Outputs
- **Training Curves:** Loss & Accuracy over epochs.  
- **Confusion Matrix:** 10×10 heatmap of predictions.  
- **Sample Prediction:** `predict_and_suggest()` output showing sustainability advice.

*(See `/assets` folder for screenshots.)*

---

## 📅 Internship Progress

| Week | Focus | Deliverables |
|------|--------|--------------|
| **Week 1** | Project concept, repo structure | Problem statement + README |
| **Week 2** | CNN implementation + training | Notebook + model + notes |

---

## 🧠 Improvisations Done
- Added **data augmentation**, **batch normalization**, and **dropout** to stabilize and improve accuracy.  
- Integrated **early stopping** and **model checkpointing** for optimal weight selection.  
- Created a **sustainability-mapping layer** that turns AI predictions into meaningful eco-advice.  
- Achieved consistent ~91 % accuracy, demonstrating a strong, generalizable model.

---

## 📘 Future Scope
- Train on **DeepFashion** (real-world dataset) for better visual realism.  
- Use **transfer learning** (MobileNetV2 / EfficientNet).  
- Build a **Streamlit web app** for interactive wardrobe analysis.  
- Extend mapping with real carbon-footprint data per fabric type.

---

## 👩‍💻 Author
**Amisha Singh**  
AICTE × Shell Edunet Green Skills Internship 2025  
l Edunet Green Skills Internship 2025  
