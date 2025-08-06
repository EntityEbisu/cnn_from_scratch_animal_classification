# 🧠 CNN Animal Image Classification (from Scratch)

This project builds a Convolutional Neural Network (CNN) **from scratch**, without relying on pre-trained models (e.g., ResNet, VGG), to classify **6 different types of animals**.  
It was originally developed as part of a Data Scientist internship test and later optimized using Kaggle GPU resources for performance benchmarking.

---

## 📌 Project Highlights

- ✅ Pure CNN architecture (no transfer learning)
- ✅ Classification of 6 animal types using image data
- ✅ Dataset preprocessing with augmentation and normalization
- ✅ Dual environment support: Local + Kaggle GPU
- ✅ Clean modular code structure
- ✅ Documented reflections and training plots

---

## 🐾 Classes Used

The dataset was trimmed from a larger private dataset to include the following 6 animal categories:

- `cat`
- `cow`
- `chicken`
- `dog`
- `duck`
- `sheep`

> 🔒 **Note**: The full dataset was provided via private email as part of an internship challenge and is not publicly redistributed. A dummy version with sample images is included for structure reference.

---

## 📁 Directory Structure

```
cnn-animal-classification/
├── dummy_dataset/            # Demo folder structure for replication
│   ├── cat/
│   │   └── cat_sample1.jpg
│   ├── cow/
│   │   └── cow_sample1.jpg
│   └── ...
├── notebooks/
│   └── finpros_ds_intern_NguyenTrongMinh_CnnFromScratch.ipynb
├── docs/
│   └── CNN Image Classification - Documentation.pdf
├── README.md
└── requirements.txt
```

---

## ⚙️ GPU Acceleration and Dual Data Preparation

This project was tested on both **local hardware** and **Kaggle's free GPU environment** (Tesla T4 ×2).  
On Kaggle, the training performance improved by over **10×** compared to a typical local laptop.

### 🧩 Dual Dataset Functions

Two dataset preparation functions are included to support both platforms:

- `prepare_dataset(...)`:  
  For local development. Handles zipped datasets, extracts selected classes, and builds datasets.

- `prepare_dataset_kaggle(...)`:  
  For Kaggle Notebooks. Deals with Kaggle's nested dataset folders (`cat/cat/image.jpg`) by flattening the directory using symbolic links.

```python
# Local zipped folder logic
dataset/
├── cow.zip → cow/
│            └── cow001.jpg

# Kaggle nested folder format
/kaggle/input/.../
├── cow/
│   └── cow/
│       └── cow001.jpg
```

---

## 🧪 Model Training Performance (10 Epochs)

| Metric        | Value     |
|---------------|-----------|
| Best Val Accuracy | **~70.6%** |
| Final Train Accuracy | ~73.6% |
| Image Size | 64×64 |
| Batch Size | 32 |
| Epochs | 10 |
| GPU | Kaggle Tesla T4 |

Training and validation performance plots are included in the notebook.

---

## 📄 Documentation

A detailed reflection and explanation of the development process can be found in:

📄 `docs/CNN Image Classification - Documentation.pdf`

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/cnn-animal-classification.git
cd cnn-animal-classification
```

### 2. Install requirements
```bash
pip install -r requirements.txt
```

### 3. Replace dummy dataset with your own
Ensure your dataset follows this structure:
```
your_dataset/
├── cat/
│   └── image1.jpg
├── dog/
│   └── image1.jpg
...
```

### 4. Run the notebook
Choose either:
- Local execution with zipped folders → `prepare_dataset(...)`
- Kaggle with nested folders → `prepare_dataset_kaggle(...)`

---

## 📬 Contact

Made by **Nguyễn Trọng Minh** for the **Finpros Data Scientist Internship Test**.

For questions or collaborations:  
📧 tminh193.bil@gmail.com 

---

## 📝 License

This project is released for **educational and portfolio purposes only**. Do not redistribute the full dataset without permission.
