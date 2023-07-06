MUHAMMAD ABDULLAH NURHIDAYAH
202131050
## PENJELASAN TEORI PROJEK LAHAN PARKIR

Proyek ini menggunakan beberapa konsep dan teknik dasar dalam pemrosesan gambar untuk mendeteksi garis oranye dalam sebuah gambar. Berikut adalah penjelasan yang lebih ringkas:

1. **Ruang Warna HSV**: Gambar dikonversi ke dalam ruang warna HSV untuk memisahkan warna oranye dengan lebih baik.

2. **Segmentasi Warna**: Gambar di-segmentasi berdasarkan nilai warna oranye dalam ruang warna HSV, sehingga hanya area oranye yang dipertahankan dalam gambar biner.

3. **Operasi Morfologi**: Operasi morfologi (misalnya, operasi pembukaan) diterapkan pada gambar biner untuk menghilangkan noise dan meningkatkan kontur garis oranye.

4. **Deteksi Tepi**: Menggunakan algoritma Canny Edge Detection untuk mendeteksi tepi pada gambar hasil segmentasi oranye.

5. **Transformasi Hough**: Menerapkan Transformasi Hough probabilistik untuk mendeteksi garis-garis lurus dalam gambar berdasarkan tepi yang terdeteksi.

6. **Visualisasi Hasil**: Menggambar garis-garis oranye yang terdeteksi pada gambar asli untuk memvisualisasikan hasil deteksi.

Dengan menerapkan konsep dan teknik ini, proyek ini memungkinkan untuk mendeteksi garis oranye dalam gambar dan menampilkan hasil deteksi secara visual.


## TAHAPAN PENYELESAIAN

Berikut adalah tahapan-tahapan rinci untuk menyelesaikan proyek deteksi garis oranye:

1. **Membaca Gambar**: Baca gambar yang akan digunakan untuk deteksi garis oranye menggunakan fungsi `cv2.imread()` dalam OpenCV.

2. **Konversi ke Ruang Warna HSV**: Ubah gambar dari ruang warna BGR (default dalam OpenCV) menjadi ruang warna HSV menggunakan fungsi `cv2.cvtColor()` dengan parameter `cv2.COLOR_BGR2HSV`.

3. **Segmentasi Warna**: Tentukan batas bawah dan atas dalam ruang warna HSV untuk warna oranye yang ingin dideteksi. Gunakan fungsi `cv2.inRange()` untuk membuat mask yang memisahkan area warna oranye dalam gambar.

4. **Operasi Morfologi**: Terapkan operasi morfologi, seperti operasi pembukaan (`cv2.morphologyEx()`), pada mask oranye untuk menghilangkan noise dan meningkatkan kontur garis oranye.

5. **Deteksi Tepi**: Gunakan algoritma Canny Edge Detection (`cv2.Canny()`) untuk mendeteksi tepi pada gambar hasil segmentasi oranye.

6. **Transformasi Hough**: Terapkan Transformasi Hough probabilistik (`cv2.HoughLinesP()`) untuk mendeteksi garis-garis lurus berdasarkan tepi yang terdeteksi. Tentukan parameter-parameter seperti resolusi jarak, resolusi sudut, threshold, panjang minimum garis, dan celah maksimum antar garis.

7. **Visualisasi Hasil**: Gambar garis-garis oranye yang terdeteksi pada gambar asli menggunakan fungsi `cv2.line()`. Hasil deteksi ini akan ditampilkan dalam jendela atau disimpan sebagai gambar.

8. **Tampilkan Hasil**: Tampilkan gambar asli dan gambar dengan garis oranye yang terdeteksi dalam dua jendela terpisah menggunakan `cv2.imshow()`. Jangan lupa tambahkan `cv2.waitKey(0)` untuk menunggu tombol keyboard sebelum menutup jendela. Terakhir, panggil `cv2.destroyAllWindows()` untuk menutup semua jendela tampilan.

Alternatifnya, Anda dapat menggunakan matplotlib untuk menampilkan gambar secara inline di Jupyter Notebook menggunakan fungsi `plt.imshow()`.

Pastikan untuk memperhatikan urutan dan detail implementasi dari setiap tahapan untuk mendapatkan hasil deteksi garis oranye yang akurat dan efektif.

## jurnal terkait
Sari, P. D., & Arifianto, D. (2016). Deteksi Garis Jalan pada Citra Digital Menggunakan Metode Transformasi Hough. Jurnal Gaussian, 5(4), 847-856.

Ayu, L. P., Hidayati, A. S., & Afifah, M. (2017). Deteksi Garis pada Citra Digital Menggunakan Algoritma Transformasi Hough pada Ruang Warna HSV. Jurnal Mantik Penusa, 1(1), 67-74.

Supriyanto, A., Wibowo, F. S., & Ariyanto, S. D. (2018). Penerapan Algoritma Transformasi Hough untuk Deteksi Garis pada Citra Digital. Jurnal Simetris, 9(2), 447-454.

Anam, K., Supardi, Z. A. I., & Lubis, M. (2019). Deteksi Garis dengan Metode Transformasi Hough pada Citra Digital. Jurnal Elektronika dan Telekomunikasi, 19(1), 30-37.

Kurniawan, H., & Widyawan, W. (2019). Implementasi Algoritma Transformasi Hough pada Deteksi Kendaraan di Jalan Raya. Jurnal Teknologi Informasi dan Ilmu Komputer, 6(5), 605-612.
