# 🎧 Prediksi Churn Pengguna Layanan Streaming Musik Menggunakan Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Project-Churn%20Prediction-blue">
  <img src="https://img.shields.io/badge/ML-Supervised%20Learning-green">
  <img src="https://img.shields.io/badge/Model-XGBoost-orange">
  <img src="https://img.shields.io/badge/Data-Spotify%20Behavior%202025-purple">
</p>

---

## 🚀 Ringkasan Proyek
Proyek ini membangun **model machine learning** untuk memprediksi apakah pengguna layanan streaming musik (mirip Spotify) berpotensi melakukan **churn**, yaitu berhenti menggunakan layanan.

Fokus utama model adalah **meminimalkan false negative** sehingga pengguna yang berisiko tinggi tidak terlewat, dan strategi retensi dapat disusun secara proaktif.

Dataset digunakan: **Spotify User Behavior Analysis 2025**

---

## ❓ Problem Statement
> “Bisakah kita mengetahui siapa saja pengguna yang kemungkinan besar akan berhenti sebelum mereka benar-benar pergi?”

Menjawab pertanyaan ini sangat krusial bagi tim marketing & produk untuk:
- Mengurangi tingkat churn  
- Mengoptimalkan biaya retensi  
- Meningkatkan lifetime value pengguna

---

## 🎯 Tujuan Project
- Memprediksi probabilitas churn setiap pengguna  
- Mengutamakan **recall** agar pengguna berisiko tidak terlewat  
- Membangun pipeline end-to-end siap produksi  
- Memberikan **insight fitur** yang paling memengaruhi churn  

---

## 🧩 Latar Belakang
Industri streaming musik menghadapi tantangan besar pada churn:  
**biaya akuisisi pelanggan baru jauh lebih mahal** daripada menjaga pelanggan lama.

Dengan machine learning, perusahaan dapat:
- Mengidentifikasi pengguna yang mulai menunjukkan tanda “ingin pergi”  
- Mengerti pola perilaku pengguna aktif vs churn  
- Menjalankan strategi retensi yang lebih tepat sasaran  

---

## 📂 Dataset
Sumber: Kaggle — *Spotify User Behavior 2025*

🔗 **Dataset (Google Drive)**  
https://drive.google.com/file/d/1Iozfy3u1vEsrdHpDfFjBeUhpCW8hgVtS/view?usp=sharing

### 📝 Deskripsi Fitur
| Fitur | Deskripsi |
|-------|-----------|
| `user_id` | ID unik pengguna |
| `gender` | Jenis kelamin |
| `age` | Usia pengguna |
| `country` | Negara |
| `subscription_type` | Tipe langganan |
| `listening_time` | Total waktu mendengarkan musik |
| `songs_played_per_day` | Lagu yang diputar per hari |
| `skip_rate` | Persentase lagu yang di-skip |
| `device_type` | Jenis perangkat yang digunakan |
| `ads_listened_per_week` | Jumlah iklan dalam seminggu |
| `offline_listening` | 1 = Ya, 0 = Tidak |
| `is_churned` | Target (1 = Churn) |

---

## 🛠️ Metodologi Machine Learning
**Pendekatan:** Supervised Classification

**Model yang diuji:**
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- **XGBoost (performansi terbaik)**  

**Tahapan Proyek:**
1. EDA interaktif  
2. Feature engineering  
3. Handling outlier & missing values  
4. SMOTE untuk imbalanced data  
5. Hyperparameter tuning (GridSearchCV)  
6. Pembuatan pipeline otomatis  
7. Export model `.pkl`  

---

## 🧰 Tech Stack

**Python Tools:**
- pandas, numpy  
- seaborn, matplotlib  
- scikit-learn, xgboost  
- imbalanced-learn  
- feature_engine  

**Evaluasi Model:**
- Accuracy  
- Precision  
- **Recall (utama)**  
- F1-score  
- Confusion Matrix  

---

## 📁 Struktur Repository
📦 churn-prediction-spotify  
├── dataset.csv  
├── notebook.ipynb  
├── README.md  

---

## ⭐ Highlight Proses
- Visualisasi perilaku pengguna  
- Korelasi fitur dengan **phik**  
- Oversampling menggunakan SMOTE  
- Hyperparameter tuning → XGBoost dengan recall tertinggi  
- Pipeline otomatis: preprocessing → training → prediction  
- Simpan model: `model_xgboost_pipeline.pkl`  
- Deployment sederhana via Hugging Face  

---

## 📦 Model, Dataset & Deployment

📌 **Model (.pkl)**  
https://drive.google.com/file/d/1Q4Krl3Ayl0yYdoVT2rQDnnJjs3sWGXNe/view?usp=sharing  

📌 **Dataset**  
https://drive.google.com/file/d/1Iozfy3u1vEsrdHpDfFjBeUhpCW8hgVtS/view?usp=sharing  

📌 **Deployment Hugging Face Spaces**  
https://huggingface.co/spaces/Annisa123/Spotify_rmt047  

---

## 📊 Output Akhir
- Model churn berbasis **XGBoost dengan recall optimal**  
- Pipeline siap digunakan untuk batch prediction atau API  
- Notebook EDA
- Insight fitur penting untuk pengambilan keputusan:
  - Tingginya **skip rate**  
  - Rendahnya **listening time**  
  - Banyaknya **paparan iklan**  

---

