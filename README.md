# 🌽 Corn Leaf Diseases Detection


## 👤 Identitas Pembuat

* Nama: **Theopan Gerard Nainggolan**
* ID Cohort: **CACC284D6Y0944**

---
## 📌 Deskripsi Project

Project ini bertujuan untuk membangun model **Deep Learning berbasis Computer Vision** yang mampu mendeteksi penyakit pada daun jagung (*Corn Leaf Diseases*) menggunakan citra gambar.

Masalah utama yang ingin diselesaikan adalah:

* Identifikasi penyakit tanaman jagung secara **cepat dan otomatis**
* Mengurangi ketergantungan pada inspeksi manual oleh ahli pertanian
* Membantu petani dalam pengambilan keputusan yang lebih tepat untuk penanganan penyakit

Model ini mengklasifikasikan gambar daun jagung ke dalam beberapa kategori penyakit menggunakan arsitektur CNN.

---

## 🧠 Fitur Model

* Input gambar: **224 x 224 x 3 (RGB)**
* Arsitektur: Convolutional Neural Network (CNN)
* Framework: TensorFlow / Keras
* Output: Klasifikasi multi-class penyakit daun jagung
* Format deployment:

  * `SavedModel`
  * `TensorFlow Lite (.tflite)`
  * `TensorFlow.js`

---

## 📂 Dataset
Dataset yang digunakan bersumber dari Kaggle:

👉 Corn Leaf Diseases Dataset

### 🔗 Link Dataset

https://www.kaggle.com/datasets/yusufmurtaza01/corn-leaf-diseases/data

Dataset yang digunakan berisi gambar daun jagung yang terbagi dalam beberapa kelas:

* Corn__CommonRust
* Corn__GrayLeafSpot
* Corn__Healthy
* Corn__NorthernLeafBlight

### 📊 Karakteristik Dataset

* Tipe data: Gambar RGB
* Format: JPG / PNG
* Resolusi: Di-resize menjadi **224x224**
* Struktur folder:

```
dataset/
├── Corn__CommonRust/
├── Corn__GrayLeafSpot/
├── Corn__Healthy/
└── Corn__NorthernLeafBlight/
```

Dataset digunakan untuk:

* Training
* Validation
* Testing

---

## ⚙️ Metodologi

1. **Data Preprocessing**

   * Resize gambar ke 224x224
   * Normalisasi pixel (0–1)
   * Data augmentation

2. **Model Training**

   * CNN dengan layer:

     * Conv2D
     * MaxPooling
     * BatchNormalization
     * Dense & Dropout
   * Optimizer: Adam
   * Callback:

     * EarlyStopping
     * ReduceLROnPlateau
     * ModelCheckpoint

3. **Evaluasi**

   * Accuracy
   * Confusion Matrix
   * Classification Report

4. **Deployment**

   * Convert model ke:

     * TensorFlow Lite (mobile)
     * TensorFlow.js (web)

