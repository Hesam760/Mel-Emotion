# 🎵 Audio Sentiment Classification with CNN

This repository contains an experiment in classifying **audio sentiment** (happy, sad, etc.) using extracted audio features and a custom **1D Convolutional Neural Network (CNN)**.

---

# 📊 Dataset

The model is trained using the [Persian-Speech-Dataset](https://huggingface.co/datasets/SeyedAli/Persian-Speech-Dataset) available on Hugging Face. This dataset contains Persian audio clips with corresponding transcriptions and emotion labels.  

**Dataset details:**

- `audio` 🎧: Path to the audio file  
- `transcription` 📝: Text transcription of the audio  
- `emotion` 😄😢😡😐: Emotion label (e.g., happy, sad, angry, neutral)  

*Note: The dataset is licensed under the MIT License.*

---

# 🛠️ Project Overview

- **Feature Extraction** 🔍:  
  Extracted features from audio files, including:  
  - **MFCC (Mel-Frequency Cepstral Coefficients)**  
  - **Chroma**  
  - **Zero Crossing Rate**  
  - **Spectral Rolloff**  
  - **Tonnetz (harmonic features)**  
  - Additional audio features  

- **Data Augmentation** ✨:  
  Applied several augmentations to improve model generalization:  
  - Noise injection 🔊  
  - Time shifting ⏩  
  - Time stretching ⏱️  
  - Pitch shifting 🎵  

- **Data Preparation** 📂:  
  - Features are stored in a Pandas DataFrame  
  - Split into training and testing sets  

- **Model** 🧠:  
  - Custom **1D CNN architecture** trained on the feature vectors  
  - **Validation Accuracy** ✅: ~85%  
  - **Test Accuracy** 🧪: ~61%  

> ⚠️ Note: The gap between validation and test accuracy suggests potential overfitting and room for improvement.

---

# ⚙️ How It Works

1. Load the Persian-Speech-Dataset 📥  
2. Extract features (MFCC, Chroma, Zero Crossing Rate, Spectral Rolloff, Tonnetz, etc.) 🎶  
3. Apply data augmentation for more training samples ✨  
4. Store features in a structured Pandas DataFrame 🗂️  
5. Split data into train/test sets 🔀  
6. Train a custom 1D CNN on the extracted features 🧠  
7. Evaluate model performance on validation and test sets 📊  

---

# 📚 Libraries Used

- **librosa** 🎧 – audio processing and feature extraction  
- **matplotlib** 📈 – plotting and visualization  
- **tensorflow** 🤖 – building and training CNN models  
- **keras** 🛠️ – high-level API for CNN architecture  
- **numpy** 🔢 – numerical operations  
- **pandas** 🗃️ – data manipulation and storage  
- **io** 💾 – input/output operations (built-in Python library)  

---

# 📓 Notebook

All steps are included in the Jupyter Notebook (`.ipynb`) provided in this repository.  
Open the notebook to explore:  
- Feature extraction 🔍  
- Data augmentation ✨  
- CNN training 🧠  
- Model evaluation 📊  

---

# 💻 Installation

Install dependencies using pip:

```bash
pip install librosa matplotlib tensorflow keras numpy pandas
```

