# Klasifikasi Gambar Kertas Batu Gunting ✋✊✌️

## Penulis

* **Nama:** Fariz Husain Albar
* **Email:** khudnul88@gmail.com
* **Dicoding ID:** farz-hha
* **Tahun:** 2023
---
*Dibuat untuk memenuhi submission Dicoding Indonesia.*

Proyek ini merupakan submission untuk kelas **"Belajar Machine Learning untuk Pemula"** di Dicoding Academy. Proyek ini membangun model Jaringan Saraf Tiruan (CNN) untuk mengklasifikasikan gambar tangan yang membentuk batu, gunting, atau kertas.

## Deskripsi Proyek

Model ini dilatih menggunakan dataset *Rock-Paper-Scissors* yang disediakan oleh Dicoding. Tujuannya adalah mengenali gestur tangan secara otomatis dengan tingkat akurasi yang tinggi (>97%).

### Fitur Utama:
* **Dataset Splitting:** Dataset dibagi menjadi **Train Set (60%)** dan **Validation Set (40%)**.
* **Image Augmentation:** Menggunakan `ImageDataGenerator` untuk memperkaya data latih (rotasi, *shear*, *horizontal flip*, dll).
* **Model Architecture:** Menggunakan Sequential CNN dengan layer Conv2D, MaxPooling2D, dan Dropout.
* **Optimizer:** Menggunakan `RMSprop`.
* **Custom Callback:** Pelatihan otomatis berhenti jika akurasi pelatihan dan validasii melampaui **97%** untuk mencegah *overfitting* dan menghemat waktu komputasi.

## Teknologi yang Digunakan

* **Bahasa:** Python
* **Framework:** TensorFlow & Keras
* **Library Pendukung:**
    * `pandas`, `numpy` (Pengolahan Data)
    * `matplotlib` (Visualisasi Grafik)
    * `sklearn` (Splitting Dataset)
    * `google.colab` (Handling file upload di Colab)

## Arsitektur Modell

Modell dibangun menggunakan pendekatan *Sequential* dengan rincian layer sebagai berikut:

1.  **Conv2D** (32 filters) + MaxPooling2D
2.  **Conv2D** (64 filters) + MaxPooling2D
3.  **Conv2D** (128 filters) + MaxPooling2D
4.  **Flatten**
5.  **Dropout** (0.5)
6.  **Dense** (512 units, Activation: ReLU)
7.  **Output Layer** (3 units, Activation: Softmax)

## Hasil Pelatihan

Model dilatih dengan konfigurasi berikut:
* **Epochs:** 20 (Berhenti di epoch ke- 18 karena callback)
* **Loss Function:** Categorical Crossentropy
* **Optimizer:** RMSprop

**Pencapaian Akhir:**
* Akurasi Training: **> 97%**
* Akurasi Validasi: **> 96%**

## Cara Menjalankan (Google Colab)

1.  Unduh file `.ipynb` dari repositori ini.
2.  Buka [Google Colab](https://colab.research.google.com/).
3.  Upload file notebook tersebut.
4.  Jalankan setiap sel kode secara berurutan (`Runtime` > `Run all`).
5.  Pada tahap akhir, Kamu dapat mengunggah gambar tangan Anda sendiri untuk diuji oleh model.
