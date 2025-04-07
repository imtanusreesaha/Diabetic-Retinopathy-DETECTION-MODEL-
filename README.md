# Diabetic Retinopathy Detection Web App

## 🔍 Overview
Diabetic Retinopathy (DR) is a diabetes complication that damages the retina, potentially leading to blindness. This project uses deep learning techniques to detect and classify the severity of DR using fundus images. It focuses on scalable solutions even when dealing with resource and storage limitations.

The model classifies images into five DR stages:
- **0**: No DR  
- **1**: Mild  
- **2**: Moderate  
- **3**: Severe  
- **4**: Proliferative DR  

## 🎯 Features
- 🔎 **Automated DR Detection**: Classifies retina images with CNN-based architecture.
- 🧠 **Transfer Learning**: Utilizes pre-trained models like EfficientNetB0 for enhanced performance.
- ⚖️ **Class Imbalance Handling**: Includes weighted losses and selective data extraction.
- 📈 **Evaluation Metrics**: Confusion matrix, classification report, and Kappa Score.

## 🧠 Model Architecture
- **Base**: EfficientNetB0 from Keras Applications.
- **Input**: Retina images in JPEG format.
- **Layers**:
  - GlobalAveragePooling
  - Dense (fully connected) layers
- **Loss Function**: Categorical Crossentropy (with class weights)
- **Optimization**: Adam Optimizer

## 🗃️ Dataset
- **Source**: Kaggle Diabetic Retinopathy Detection dataset
- **Format**: JPEG images + `trainLabels.csv`
- **Subset Used**: ~100 retina images (due to storage constraints on Kaggle/Colab)
- **Handling**:
  - Partial `.zip.001` extraction using `7zip`
  - Class labels mapped from CSV

## 🧪 Performance Metrics
- Accuracy
- Cohen's Kappa Score
- Confusion Matrix (via Seaborn heatmaps)
- Classification Report (Precision, Recall, F1)

## 🧰 Tech Stack
**Backend & Modeling**:
- Python (3.8+)
- TensorFlow / Keras
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn
- Skimage (for image reading)

**Utilities**:
- Shell commands for data extraction
- Google Colab/Kaggle notebooks for training environment

## 📁 Folder Structure
```
├── data/
│   └── train_11/             # Extracted image samples
├── trainLabels.csv           # Labels file
├── Diabetic_Retinopathy_EYE_Detection.ipynb  # Main notebook
├── requirements.txt          # (optional) dependencies
└── README.md
=
```

## 🚀 Getting Started

### Prerequisites
- Python >= 3.8
- pip, Jupyter
- Install required libraries:
```bash
pip install tensorflow pandas numpy matplotlib seaborn scikit-learn scikit-image
```

### Running the Notebook
1. Open the notebook in Jupyter or Google Colab.
2. Extract the image data:
   - Use `7zip` or unzip using the shell commands provided in the notebook.
3. Run cells sequentially to preprocess, train, and evaluate the model.

## 📸 Sample Output
![image](https://github.com/user-attachments/assets/27e1f69f-d23b-4238-89b4-f35f9b408c72)
# Working Model
![image](https://github.com/user-attachments/assets/5c6903da-b334-4fdc-8dc3-e4811d1f60c1)

## 🔮 Future Improvements
- Integrate Grad-CAM to visualize model attention.
- Expand dataset usage beyond the subset.
- Deploy as a Streamlit or Flask app.
- Optimize model for mobile or edge deployment.

## 📜 License
This project is under the [MIT License](LICENSE).

## 🙌 Acknowledgments
- Kaggle Diabetic Retinopathy Detection Challenge
- Google Brain Research on Medical Imaging
- TensorFlow, Keras, and the open-source ML community

## 👨‍💻 Author
**Tanusree Saha**  
GitHub: Tanusree Saha(https://github.com/imtanusreesaha)  
Email: imtanusreesahaa@gmail.com

