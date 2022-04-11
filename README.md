# COFER: Content Category & Fake User Identifier

***

## Problem
Jumlah influencer di Instagram sudah cukup banyak, yakni lebih dari 37 juta untuk yang memiliki followers sebanyak 1000 followers.
![image](https://user-images.githubusercontent.com/97724828/162657204-c7fad5a8-a0f7-42e0-8648-10b607f89460.png)
* Semakin banyak pengguna instagram, terutama influencer, sehingga konten instagram perlu diklasifikasikan menurut kategori untuk meningkatkan ketertarikan banyak orang.
* Seiring dengan banyaknya pengguna instagram telah memicu menyebarnya berbagai informasi palsu di kalangan masyarakat. Akun palsu dapat menyebarkan berita palsu. Akibat dari berita palsu yang disebarluaskan dapat menyesatkan masyarakat yang mengandalkan sosial media untuk memperoleh informasi, dan berita palsu juga dapat memberikan dampak misinformasi di kalangan pengguna.
* Berkembangnya aplikasi Sosial Media juga dapat membuka peluang yang luas bagi orang-orang tertentu untuk melakukan penipuan dengan menggunakan akun palsu. Salah satu kecurangan dari adanya akun palsu adalah penyalahgunaan identitas seseorang atau instansi yang nantinya akan digunakan untuk melakukan kejahatan seperti jual beli barang atau berbisnis. Penipuan ini dapat menimbulkan kesalahpahaman antara pengguna dalam jual beli barang dan berbisnis sehingga banyak orang atau pengguna harus berhati-hati dalam melakukan transaksi online.
* Akun palsu juga sering ditemukan memberikan komentar spam di sosial media dengan komentar yang dianggap tidak relevan secara kontekstual. Sebagai contoh komentar spam pada halaman Instagram public figure, komentar spam tersebut dapat berupa postingan yang tidak ada kaitannya dengan postingan dan status pada halaman yang bersangkutan, seperti mengirimkan informasi yang tidak diinginkan oleh pengguna. Aktivitas spam memang mengganggu karena dapat menimbulkan informasi yang menyesatkan dan mengganggu alur diskusi dalam status hingga kesulitan mencari informasi. Apalagi komentator spam di sosial media dilakukan oleh akun palsu yang identitasnya tidak diketahui.
* Cyberbullying juga merupakan salah satu yang patut mendapat perhatian dari dampak akun palsu sebagai tindakan pelecehan menggunakan teknologi. Aktivitas tersebut biasanya dilakukan dalam bentuk komentar jahat, posting gambar, atau video yang dimaksudkan untuk menyakiti atau mempermalukan orang lain. Hal ini berdampak besar baik bagi masyarakat maupun pengguna OSN karena dapat menimbulkan kepanikan yang berujung pada kematian. Selain itu, cyberbullying juga dapat menyebabkan penurunan mental bagi pengguna yang menjadi korbannya.
* Oleh karena itu, untuk mengatasi masalah di atas, kami mengusulkan model untuk mengidentifikasi akun Instagram terkait kategori konten dan termasuk akun palsu atau bukan.

## COFER 
COFER bertujuan untuk mengidentifikasi akun Instagram berdasarkan Content Category dan akun tersebut termasuk Fake User atau bukan.

Keunggulan dari COFER ini
* Aksesibilitas : Semua orang dengan perangkat dapat menggunakan aplikasi COFER
* Kemudahan : Hanya dengan mengikuti rekomendasi dan melihat insight yang diberikan
* Hemat Biaya : Semua bebas untuk menggunakan aplikasi COFER

Sasaran COFER
* Instagram user : Semua pengguna instagram dapat menggunakan aplikasi COFER
* Individu/ Public Figure/ Company : Semua orang yang membutuhkan informasi akun instagram tertentu

## Tahapan Pembuatan Model
1. Preparing dan preprocessing dataset
2. Modeling dan training
3. Evaluasi Model
4. Inference dan deployment

## Dataset Content Instagram
Terdapat 5 target class

**The image below is an example of the different images in the dataset.**
![image](https://user-images.githubusercontent.com/97724828/162658336-21ac2a26-828b-4026-bbd6-7e0e959e0c77.png)

## Dataset Fake User
Feature untuk memprediksi fake user:
1. Rasio angka terhadap jumlah karakter di username
2. Jumlah karakter di full names
3. Rasio angka terhadap jumlah karakter di full names
4. Username dan full name sama atau tidak
5. Jumlah karakter di bio
6. Mempunyai URL atau tidak
7. Private atau tidak
8. Ada foto profil atua tidak
9. Jumlah postingan
10. Jumlah followers
11. Jumlah following

# Code and Resources used
***
* **Tool:** Google Colaboratory
* **Packages:** Pandas, Numpy, Keras, Matplotlib

# Findings
## Model Content Instagram
Model yang digunakan **Convolutional Neural Network : Efficient Net**

Hasil pengujian model:
| Evaluation 	|    Nilai    |
--------- |-------------------| 
|Accuracy	      |  89%      |
|Precision	      |  89%          |
|Recall	      |  89%         |
|F1-score	      |  89%            |

Hasil Pengujian Confusion Matrix:
|   Kategori	|    Berhasil Diprediksi    |    Salah prediksi    |
--------- |-------------------|-------------------|  
|Beauty	      |  55      |  5      |
|Family	      |  52          |  8      |
|Fashion	      |  45      |  15      |
|Fitness	      |  54          |  6      |
|Food	      |  60          |  0      |
|Total	      |  266         |  34      |

**Train dan Validation Loss**

![image](https://user-images.githubusercontent.com/97724828/162658891-9e7396e8-9e36-4bd6-b65b-68626033f11c.png)


## Model Fake User
Model yang digunakan **Artificial Neural Network (ANN)**

Hasil pengujian model:
| Evaluation 	|    Nilai    |
--------- |-------------------| 
|Accuracy	      |  96%      |
|Precision	      |  96%          |
|Recall	      |  96%         |
|F1-score	      |  96%            |

Hasil Pengujian Confusion Matrix:
|   Kategori	|    Berhasil Diprediksi    |    Salah prediksi    |
--------- |-------------------|-------------------|  
|Real User	      |  105      |  6      |
|Fake User	      |  91          |  6      |
|Total	      |  196         |  12      |

**Train dan Validation Loss**

![image](https://user-images.githubusercontent.com/97724828/162659044-d4dc3a99-90d4-445d-aa97-b84c314cad8c.png)
