Nama: Muhammad Rafi Zia Ulhaq<br>
NPM: 2206814551<br>
Kelas: Pemrograman Lanjut B<br>

# Module 5

## Reflection
### Perbedaan JMeter dengan IntelliJ Profiler
perbedaan antara JMeter dan IntelliJ Profiler dalam konteks optimisasi kinerja aplikasi yaitu:
* JMeter digunakan untuk menganalisis kinerja aplikasi dalam situasi beban yang tinggi atau skenario penggunaan yang realistis. Analisis ini dilakukan dengan mengirimkan permintaan HTTP atau protokol lainnya ke server aplikasi dan mengukur waktu respons, throughput, dan lainnya.
* IntelliJ Profiler digunakan untuk menganalisis perilaku dan kinerja aplikasi secara mendetail pada tingkat kode. Analisis ini meliputi pemantauan penggunaan CPU, alokasi memori, waktu eksekusi, dan lainnya.

### Proses *Profiling*
*Profiling* membantu mengidentifikasi dan memahami titik lemah aplikasi dengan memberikan informasi tentang perilaku aplikasi saat berjalan seperti identifikasi fungsi, metode, atau blok kode yang memakan waktu eksekusi yang signifikan, analisis penggunaan memori yang berlebihan, analisis pola penggunaan CPU, dan analisis panggilan fungsi dan *stack trace*.

### Efektifitas IntelliJ Profiler
Menurut saya, IntelliJ Profiler adalah alat yang sangat efektif untuk membantu mengidentifikasi dan menganalisis *bottlenecks* dalam kode aplikasi. Hal ini karena IntelliJ Profiler menawarkan serangkaian fitur komprehensif yang dirancang untuk memberikan informasi mendalam tentang berbagai aspek kinerja aplikasi seperti analisis secara real-time, visualisasi data penggunaan memori dan CPU, analisis penggunaan memori, dan profil penggunaan CPU. Dengan fitur-fitur tersebut saya dapat dengan mudah untuk mengidentifikasi dan menganalisis *bottlenecks* dalam kode saya.

### Tantangan saat melakukan *performance testing* dan *profiling*
Tantangan yang saya hadapi dalam melakukan *performance testing* dan *profiling* yaitu:
* Sulit untuk memahami data yang dihasilkan oleh alat *performance testing* dan *profiling*. Solusi: memahami bagaimana alat *performance testing* dan *profiling* bekerja dan cara terbaik untuk membaca hasilnya.
* Mengetahui masalahnya, namun sulit untuk menemukan dan menerapkan solusi peningkatan kinerja yang tepat. Solusi: Refactoring kode dengan melakukan perubahan kecil dan bertahap untuk melihat dampak dari perubahan tersebut terhadap kinerja secara keseluruhan.

### Manfaat Utama IntelliJ Profiler
IntelliJ Profiler memberikan manfaat berupa informasi mendalam mengenai kinerja aplikasi secara real-time, memungkinkan identifikasi atas *bottleneck*, kebocoran memori, dan masalah kinerja lainnya. Dengan visualisasi yang intuitif dan analisis detil dari penggunaan CPU, memori, dan thread, IntelliJ Profiler membantu saya mengerti perilaku aplikasi dalam kondisi berbeda, sehingga saya dapat dengan cepat membuat keputusan berdasarkan data dalam proses *refactoring* dan optimisasi kode. Selain itu dengan IntelliJ Profiler saya tidak perlu menggunakan *third party apps* untuk melakukan *profiling* karena sudah tersedia dalam IDE yang saya gunakan yaitu Intellij IDEA.

### Inkonsistensi IntelliJ Profiler dan JMeter
Untuk menangani situasi ini, saya akan mengevaluasi kembali kasus pengujian yang digunakan dengan memastikan kedua alat diatur untuk kondisi yang serupa, selain itu saya juga akan menyesuaikan konfigurasi aplikasi untuk mencapai konsistensi antara hasil *performance testing* dan *profiling*.

### Strategi Optimisasi Kode Aplikasi
Untuk mengoptimalkan kode aplikasi, saya menerapkan beberapa strategi seperti *refactoring* kode untuk menghilangkan *bottleneck*, mengoptimalkan *query database*, dan mengurangi kompleksitas algoritma. Untuk memastikan perubahan tidak mempengaruhi fungsionalitas aplikasi, saya melakukan beberapa pengujian untuk memverifikasi bahwa perubahan kode tidak memicu *bug* atau masalah dalam fitur yang ada. Dengan cara ini, perubahan yang dilakukan tidak hanya meningkatkan kinerja tetapi juga mempertahankan kualitas keseluruhan aplikasi.

## JMeter Report and Test Results
### Endpoint `/all-student`
Test Result<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/test-result-1.png?raw=true)
Before Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/before-all-student-request.png?raw=true)
After Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/after-all-student-request.png?raw=true)

### Endpoint `/all-student-name`
Test Result<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/test-result-2.png?raw=true)
Before Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/before-all-student-name.png?raw=true)
After Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/after-all-student-name.png?raw=true)

### Endpoint `/highest-gpa`
Test Result<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/test-result-3.png?raw=true)
Before Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/before-highest-gpa.png?raw=true)
After Optimization<br>
![alt text](https://github.com/rafizia/exercise-profiling/blob/optimize/image/after-highest-gpa.png?raw=true)

### Kesimpulan
Dari beberapa gambar di atas, terlihat bahwa terdapat peningkatan kinerja berdasarkan hasil *sample time* yang diperoleh. Waktu eksekusi setelah dilakukan *refactoring* dan optimisasi jauh lebih cepat dibandingkan saat belum dilakukan optimisasi. Kesimpulannya proses optimisasi kode dengan bantuan alat seperti JMeter dan Intellij Profiler dapat meningkatkan kinerja dari suatu kode aplikasi.