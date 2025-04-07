# 👁️ Diabetic Retinopathy Detection using Deep Learning

## 📝 Overview
Diabetic Retinopathy (DR), also known as diabetic eye disease, is a complication of diabetes that affects the eyes. It is a leading cause of vision impairment and blindness in adults. Early detection and treatment are critical, yet DR often lacks early warning signs, making automated screening tools vital.

This project focuses on building an automated deep learning system to classify the severity of DR from retina (fundus) images. Using transfer learning and image preprocessing techniques, the goal is to create a robust classifier that can work with limited and imbalanced data, which is often the case in real-world medical scenarios.

---

## 🎯 Problem Statement
You are provided with retina images labeled with DR severity from 0 to 4:

| Label | Description         |
|-------|---------------------|
| 0     | No DR               |
| 1     | Mild                |
| 2     | Moderate            |
| 3     | Severe              |
| 4     | Proliferative DR    |

Each image is either the left or right eye of a patient (e.g., `1_left.jpeg`, `1_right.jpeg`). Your task is to build a model that predicts the correct label based on the fundus image.

---

## 📂 Dataset
- ~1000 high-resolution retina images
- `labels.csv` mapping image filenames to severity labels
- Images vary in quality (focus, lighting, artifacts)
- ⚠️ **Highly imbalanced** dataset

> Note: This is a subset of a larger dataset originally containing ~35,000 images.

---

## ⚠️ Challenges
- ✅ Small dataset
- ✅ Class imbalance
- ✅ Image noise & variations
- ✅ Real-world diagnostic variation

---

## 🎯 Project Goals
- ✅ Use **transfer learning** with pre-trained CNNs (ResNet, EfficientNet)
- ✅ Apply **oversampling** to balance classes
- ✅ Use **progressive resizing** to boost performance on small data
- ✅ Incorporate **data augmentation**

---

## 🔧 Approach

### 🔍 Data Preprocessing
- Resize & normalize images
- Augment with rotation, brightness, zoom, etc.

### 🧠 Modeling
- Transfer learning with pre-trained CNN (e.g., ResNet50)
- Custom classification head for 5-class output
- Weighted cross-entropy loss

### 🏋️ Training
- Class oversampling
- Learning rate scheduler
- Evaluation using accuracy and Cohen’s Kappa

### 📊 Evaluation
- Confusion matrix
- Prediction visualization
- Metrics dashboard

---

## 🧰 Tech Stack

| Layer        | Tools/Frameworks                     |
|--------------|--------------------------------------|
| Language     | Python                               |
| DL Framework | PyTorch / TensorFlow / Keras         |
| Image        | OpenCV, PIL                          |
| Data         | Pandas, NumPy                        |
| Viz          | Matplotlib, Seaborn                  |

---
# 📁 Project Structure
```
├── Diabetic_Retinopathy_EYE_Detection.ipynb     # Main notebook for model training and inference
├── requirement.txt                                   # List of dependencies for the project
├── README.md                                    # Project documentation (this file)
```

## 🧪 Model Details
- **Architecture**: Transfer Learning (EfficientNetB0 / ResNet50)
- **Framework**: TensorFlow / Keras
- **Loss Function**: Categorical Crossentropy with Class Weights
- **Augmentation**: Rotation, Brightness, Contrast, Zoom, Flipping
- **Metrics**: Accuracy, Cohen's Kappa, Confusion Matrix

## 🚀 How to Run
### Prerequisites
- Python 3.8+
- Install dependencies:
```bash
pip install tensorflow opencv-python numpy pandas matplotlib seaborn
```

### Usage
1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Diabetic-Retinopathy-Detection.git
cd Diabetic-Retinopathy-Detection
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```

3. Open `Diabetic_Retinopathy_EYE_Detection.ipynb`
4. Run the notebook cells to preprocess images, train the model, and evaluate predictions

## 📊 Results
- Achieved ~80% accuracy on validation set (with augmentation and transfer learning)
- Robust against some degree of image artifacts (e.g., blur, exposure)

## 🎯 Future Work
- Expand to original 35k image dataset
- Add Grad-CAM visualization for explainability
- Develop frontend using Flask or Streamlit for deployment

## 📸 Sample Output
![image](https://github.com/user-attachments/assets/27e1f69f-d23b-4238-89b4-f35f9b408c72)
# Working Model
![image](https://github.com/user-attachments/assets/5c6903da-b334-4fdc-8dc3-e4811d1f60c1)


## 📜 License
This project is under the [MIT License](LICENSE).

## 🙌 Acknowledgments
- Kaggle Diabetic Retinopathy Detection Challenge
- Google Brain Research on Medical Imaging


## 👨‍💻 Author
**Tanusree Saha**  
GitHub: Tanusree Saha(https://github.com/imtanusreesaha)  
Email: imtanusreesahaa@gmail.com

