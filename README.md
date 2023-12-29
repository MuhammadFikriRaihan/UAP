# :ringed_planet: UJIAN AKHIR PRAKTIKUM
UAP ini adalah untuk menyusun dan mengintegrasikan model machine learning
pada sisi klien menggunakan TensorFlow.js atau teknologi sejenis. Bagaimana menyajikan model
machine learning sebagai layanan web menggunakan Flask dan mengimplementasikan model machine learning dengan aplikasi web

## Dataset 
Dataset yang digunakan adalah dataset image yang dimana berisi gambar Rock, Pape dan scissors
spliting Dataset: Training = 70%, Validation = 20%, Testing = 10% 
Set Image Statistics :

Training set statistics:
{'paper': 588, 'rock': 588, 'scissors': 588}

Validation set statistics:
{'paper': 210, 'rock': 210, 'scissors': 210}

Test set statistics:
{'paper': 42, 'rock': 42, 'scissors': 42}

## MobileNet
MobileNet adalah sebuah arsitektur jaringan saraf tiruan (neural network) yang dirancang khusus untuk tugas-tugas penglihatan komputer pada perangkat mobile dan aplikasi dengan sumber daya terbatas. Model ini dikembangkan oleh Google dan dirancang untuk memiliki ukuran yang kecil dan efisien, sehingga cocok untuk perangkat dengan daya komputasi yang terbatas seperti ponsel pintar.

Keunggulan MobileNet terletak pada desainnya yang menggunakan separable depthwise convolution. Pendekatan ini membantu mengurangi jumlah parameter dan operasi komputasi, sehingga menghasilkan model yang lebih ringan tanpa mengorbankan performa secara signifikan. MobileNet juga dapat digunakan sebagai dasar untuk transfer learning dalam pelatihan model khusus pada dataset tertentu.

Model MobileNet tersedia dalam beberapa varian, seperti MobileNetV1, MobileNetV2, dan MobileNetV3, dengan setiap versi membawa peningkatan dalam hal efisiensi dan kinerja. MobileNet telah menjadi populer dalam berbagai aplikasi mobile vision, termasuk deteksi objek dan pengenalan gambar.

## Preprocessing dan Modelling 
* **Preprocessing training dan validation** :
   Rescaling image menjadi 1./255, Rotasi image ±30° secara random, Perbesar image kisaran 20%, dan Flip image secara   
   horizontal, fill_mode='nearest', Target size image(150), Menerapkan pengacakan pada image, Menerapkan batch size dan   
   Menerapkan mode kelas
* **Modelling MobileNetV2**
   Menggunakan Model MobileNetV2, melakukan imagegenerator dengan melakukan 10 epcoh
   baseModel.summarry:

![Screenshot 2023-12-30 033108](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/cf3d5a11-f0db-4bdb-8709-1f742f719668)
   Model: "sequential_1" :

![Screenshot 2023-12-30 033835](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/c672590e-af0e-43ce-9ddc-5c4fb0345636)

   Visualization Accuracy, Val Accuracy, Loss and Val Loss :
   
![image](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/2eeb5fdc-3e50-4502-a384-69ab232416b4)

   Classification Report :

![image](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/2d337698-d318-4821-b146-4ae36b02e82d)

## Predict Data
Dengan 10 gambar acak :

![image](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/1a9f1c2a-8fd7-43ff-b860-982eaa7d707e)

## Website Development

![image](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/96b8dbee-a454-4d2e-9ea5-623baa297a3d)

![image](https://github.com/MuhammadFikriRaihan/UAP/assets/71715268/99672742-ff53-4210-a6e8-3a5cd39a7f9e)



