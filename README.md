# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Institut merupakan salah satu institusi pendidikan tinggi yang telah berdiri sejak tahun 2000 dan telah menghasilkan banyak lulusan dengan reputasi yang baik. Namun, masih terdapat permasalahan serius terkait tingginya jumlah mahasiswa yang tidak menyelesaikan pendidikannya (dropout).

Tingginya angka dropout menjadi tantangan besar bagi institusi karena dapat berdampak pada kualitas pendidikan, reputasi, serta efektivitas proses pembelajaran. Oleh karena itu, Jaya Jaya Institut ingin mendeteksi sejak dini mahasiswa yang berpotensi mengalami dropout agar dapat diberikan bimbingan khusus.

Dalam proyek ini, dilakukan analisis data mahasiswa serta pembangunan model machine learning untuk memprediksi status mahasiswa (Dropout, Enrolled, atau Graduate). Selain itu, dibuat dashboard interaktif untuk membantu pihak institusi dalam memahami pola data dan memonitor performa mahasiswa

### Permasalahan Bisnis

Permasalahan bisnis yang ingin diselesaikan dalam proyek ini adalah:

- Tingginya jumlah mahasiswa yang mengalami dropout.
- Kesulitan dalam mengidentifikasi mahasiswa yang berpotensi dropout secara dini.
- Kurangnya insight terkait faktor-faktor yang memengaruhi status mahasiswa.
- Belum adanya sistem monitoring berbasis data untuk mendukung pengambilan keputusan

### Cakupan Proyek

Cakupan proyek ini meliputi:

- Analisis dan eksplorasi data mahasiswa.
- Data preprocessing (data splitting, handling imbalanced data, encoding, dan scaling).
- Pembangunan model machine learning untuk klasifikasi status mahasiswa.
- Evaluasi performa model.
- Pengembangan prototype aplikasi prediksi menggunakan Streamlit.
- Pembuatan dashboard analisis menggunakan Tableau.

### Persiapan

Sumber data: https://github.com/dicodingacademy/dicoding_dataset/tree/main/students_performance

Setup environment:

```
conda create -name final_student python=3.9
conda activate final_student

pip install pandas numpy scikit-learn matplotlib seaborn streamlit joblib

```

## Business Dashboard

Dashboard dibuat menggunakan Tableau untuk membantu pihak Jaya Jaya Institut dalam memahami kondisi mahasiswa secara menyeluruh.

Dashboard menampilkan:

- Total mahasiswa
- Persentase Dropout, Graduate, dan Enrolled
- Analisis berdasarkan:
  - Gender
  - Age
  - Admission Grade
  - Course
  - Marital Status
  - Scholarship
  - Tuition Status
  - Inflation Rate

Dashboard ini memudahkan pihak institusi dalam mengidentifikasi pola dan faktor yang memengaruhi risiko dropout, sehingga dapat digunakan sebagai dasar pengambilan keputusan.

Link Dashboard Tableu Public :

https://public.tableau.com/views/JayaJayaInstitutAnalysisDashboardDropOut/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Menjalankan Sistem Machine Learning

Prototype sistem dikembangkan menggunakan Streamlit untuk memprediksi status mahasiswa secara interaktif.

Fitur yang digunakan dalam model:

- Gender
- Course
- Age at Enrollment
- Debtor
- Marital Status
- Scholarship Holder
- Tuition Fees Up to Date
- Admission Grade
- Inflation Rate

Cara menjalankan:

```
streamlit run app.py
```

Setelah aplikasi dijalankan, pengguna dapat memasukkan data mahasiswa dan sistem akan memberikan hasil prediksi berupa:

- Dropout
- Enrolled
- Graduate

Link Streamlit Cloud : https://proyek-student-dropout-mnchaod33w6hqgg4pyp8il.streamlit.app/

## Conclusion

Berdasarkan hasil analisis data (Exploratory Data Analysis) dan visualisasi pada dashboard, dapat disimpulkan bahwa faktor utama yang memengaruhi terjadinya dropout pada mahasiswa berkaitan dengan aspek akademik dan finansial. Mahasiswa dengan nilai admission grade yang lebih rendah cenderung memiliki risiko dropout yang lebih tinggi. Selain itu, status pembayaran biaya kuliah (tuition fees) juga menjadi faktor penting, di mana mahasiswa yang tidak membayar tepat waktu memiliki kemungkinan dropout yang lebih besar. Faktor kondisi keuangan, seperti status debtor, serta kepemilikan beasiswa juga turut memengaruhi keberlangsungan studi mahasiswa.

Selain itu, terdapat perbedaan risiko dropout berdasarkan karakteristik demografis seperti usia dan gender, serta variasi tingkat dropout pada masing-masing program studi. Hal ini menunjukkan bahwa risiko dropout tidak hanya dipengaruhi oleh satu faktor, melainkan kombinasi dari berbagai aspek akademik, finansial, dan karakteristik individu mahasiswa.

Dari sisi pemodelan, model machine learning yang dibangun menggunakan algoritma Random Forest telah disesuaikan menjadi klasifikasi biner (Dropout dan Graduate) sesuai dengan tujuan bisnis. Model menghasilkan performa yang cukup baik dengan nilai akurasi sebesar 74.5%, serta nilai F1-score sebesar 0.79 untuk kelas Graduate dan 0.68 untuk kelas Dropout. Nilai recall pada kelas Dropout sebesar 0.73 menunjukkan bahwa model cukup efektif dalam mendeteksi mahasiswa yang berpotensi dropout.

Dengan performa tersebut, model sudah dapat digunakan sebagai sistem peringatan dini (early warning system) untuk membantu institusi dalam mengidentifikasi mahasiswa yang berisiko dropout. Selain itu, fitur-fitur seperti admission grade, status pembayaran tuition, dan kondisi finansial menjadi faktor yang paling berpengaruh dalam menentukan prediksi model, sehingga dapat dijadikan fokus utama dalam pengambilan keputusan.

### Rekomendasi Action Items

Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

- Mengembangkan program bantuan finansial bagi mahasiswa dengan risiko ekonomi tinggi.
- Memberikan pendampingan akademik khusus bagi mahasiswa dengan nilai masuk (admission grade) rendah.
- Melakukan monitoring berkala terhadap mahasiswa dengan risiko dropout.
- Mengembangkan model dengan fitur tambahan atau algoritma lain untuk meningkatkan performa prediksi.
- Mengintegrasikan dashboard dan sistem prediksi ke dalam sistem internal institusi untuk monitoring real-time.
