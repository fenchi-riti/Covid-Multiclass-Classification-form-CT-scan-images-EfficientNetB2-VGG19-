![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/b58517f3-6e34-4126-aa15-852f01833897)

**Background**: 
- Covid-19 merupakan salah satu jenis penyakit menular yang disebabkan oleh virus SARS-CoV-2 yang pertama kali muncul di Wuhan-Cina pada tahun 2019. Berdasarkan data dari WHO, hingga saat ini masih terdapat kasus Covid dan kasus orang meninggal karena Covid.
- Untuk diagnosis Covid-19 terdapat beberapa cara yang dilakukan salah satunya yaitu pemeriksaan radiologis menggunakan CT Scan paru-paru, karena gejala yang terjadi saat terinfeksi Covid-19 yaitu gangguan pernapasan akut. Penggunaan CT scans dilakukan karena CT adalah teknik yang lebih tepat untuk citra dada dan sensitivitasnya lebih tinggi jika dibandingkan dengan X-rays.

**Problem**:
- Dalam diagnosis oleh radiolog penyakit Covid-19 sulit dibedakan dengan pneumonia, sehingga kemungkinan kesalahan dalam mendiagnosis bisa terjadi, juga disebabkan karena pengalaman radiolog yang berbeda-beda, sehingga interprestasi citra CT scan bisa menyebabkan kesalahan diagnosis.

**Objective**:
- Mengembangkan model deep learning menggunakan  EfficientNetB2 dan VGG19 yang dapat mengklasifikasikan Covid-19,Normal, dan penyakit paru-paru  lainnya berdasarkan gambar CT scan  dengan  tingkat akurasi yang tinggi.
- Proyek ini akan berfokus pada klasifikasi citra CT scan paru-paru menjadi kelas ‘ 'Covid-19’, ‘Healthy',  'others’

Data Collection & Preparation
Dataset dari: https://www.kaggle.com/datasets/plameneduardo/a-covid-multiclass-dataset-of-ct-scans
Komposisi Dataset
Dataset ini terdiri tiga kelas, yaitu Covid-19 terdiri dari 2168, Healthy terdiri dari 758 data, dan penyakit pneumonia lainnya(Others) 1247 
![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/7bc01a99-c0d8-42bc-b9dd-93681cbf8423)

**Preprocessing**:
Hyperparameter Initiation
input_tensor  = Input(shape=(224,224,3))
learning_rate = 0.0001
epochs        = 60
image_size    = (224, 224)
batch_size    = 16
**Classification Report**:
VGG19 Akurasi: 74,64% ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/b4d47bdc-5502-40b1-9f25-9d5669938479)
EfficientNetB2 Akurasi: 94,05% ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/0d62417c-78c1-430d-91f1-a2c6e16fc597)
**Confussion Matrix**:
VGG19 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/4216a511-3392-482a-b687-abd38575dc37)
EfficientNetB2 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/94a897d1-778c-4d18-bcf1-35371bfd3ed9)
**Graphic Accuracy**:
VGG19 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/21f7e295-7a86-498b-82fd-ffb3b0997301)
EfficientNetB2 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/c87bd5e9-3e65-4306-9aa1-be21e7f6cf87)
**Graphic Loss**:
VGG19 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/200f5b50-cd47-4e13-b85c-aefd6143e06c)
EfficientNetB2 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/709624a8-9518-4c5b-a960-bc3ef276107c)
**Actual vs Prediction**:
EfficientNetB2 ![image](https://github.com/fenchi-riti/Covid-Multiclass-Classification-form-CT-scan-images-EfficientNetB2-VGG19-/assets/72839436/75b3c01c-27ab-4360-b1a3-40749805b103)
**Future Improvement**:
- Hyperparameter tuning digunakan untuk  menghasilkan model yang lebih baik lagi.
- Membuat variasi dataset untuk hasil yang lebih baik
- Mencoba pelatihan dataset kepada model-model lainnya seperti ResNet, Vision Transformer (ViT), dan InceptionResNet.
**conclusion**:
- Model EfficientNetB2  lebih baik dalam mengklasifikasikan citra CT scan dibandingkan model VGG19 karena akurasi klasifikasi lebih tinggi yaitu 94%
- Model EfficientNetB2 lebih baik dalam meminimalkan kesalahan klasifikasi karena presisinya lebih tinggi dibandingkan model VGG19
- Model EfficientNetB2 juga dapat memperoleh nilai metric f1-score dan recall yang lebih tinggi dibandingkan dengan model VGG19. walaupun demikian untuk recall perlu 
  ditingkatkan sehingga kelas dengan prediksi false positif dapat dikurangi (Pasien yang sakit diteksi tidak sakit)





