# Week 2 – Model Implementation & Results

## Summary
During Week 2 of the “AI Closet: Smart Wardrobe Sustainability Advisor” internship project, I implemented and trained a Convolutional Neural Network (CNN) in Google Colab using the Fashion-MNIST dataset.  
The model’s objective was to recognize different types of clothing items and connect them to sustainability information (material, environmental impact, and suggested eco-action).

---

## Key Steps Completed
- Loaded and preprocessed the **Fashion-MNIST** dataset (60,000 training + 10,000 test images).  
- Resized all images from 28×28 to 32×32×1 and normalized pixel values.  
- Applied data augmentation to improve generalization (rotation, zoom, shift).  
- Built a **three-block CNN** architecture with Batch Normalization and Dropout (0.4).  
- Trained the model using **Adam optimizer** and **early stopping** for up to 20 epochs.  
- Evaluated results using accuracy, loss, and confusion matrix visualizations.  
- Integrated the **Sustainability Mapping Layer** to associate predictions with eco-actions such as *Reuse, Donate, Repair,* and *Recycle.*

---

## Results

| Metric | Value |
|--------|--------|
| **Training Accuracy (Final Epoch)** | 90.9 % |
| **Validation Accuracy (Best Epoch)** | 91.3 % |
| **Validation Loss (Best Epoch)** | 0.2397 |
| **Training Loss (Final Epoch)** | 0.2449 |
| **Test Accuracy** | 91.0 % |
| **Epochs Run** | 20 (with Early Stopping at Epoch 16) |

### **Observations**
- The CNN model converged smoothly and avoided overfitting due to early stopping and dropout.  
- Accuracy stabilized around **91%**, indicating strong generalization for 10 apparel categories.  
- Minor misclassifications occurred between *T-shirt/top* and *Shirt* (expected due to visual similarity).  
- Confusion matrix confirms solid separation for visually distinct classes such as *Sneaker* and *Bag.*  

---

## Screenshots to Include
- **Training & Validation Curves:** Loss and Accuracy plots showing convergence.  
- **Confusion Matrix:** Heatmap of predicted vs true labels.  
- **Sample Output:** Screenshot of `predict_and_suggest()` showing predicted class and sustainability recommendation.  

---

## Improvisations Done
- Enhanced model robustness by integrating **data augmentation**, **batch normalization**, and **dropout**, which improved test accuracy by ~5% compared to a baseline CNN.  
- Added **early stopping** and model checkpointing to prevent overfitting and automatically save the best model weights.  
- Created a **sustainability mapping layer** that translates CNN predictions into material estimates and eco-friendly recommendations (e.g., “Cotton → Low impact → Reuse/Donate”).  
- Documented the entire training workflow with reproducible results and prepared the notebook for public release via GitHub.  

---

## Next Steps (Week 3 Plan)
- Switch from Fashion-MNIST to a **real-world dataset** (DeepFashion).  
- Implement **transfer learning** using pre-trained models like MobileNetV2 or EfficientNet.  
- Develop a **simple Streamlit interface** to upload images and receive sustainability insights in real time.  
- Create visuals and performance graphs for the Week 3 PPT presentation.
