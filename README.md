# Capstone MariBelajar
[MariBelajar](http://maribelajarsite.southeastasia.cloudapp.azure.com/) merupakan aplikasi berbasis web yang bergerak di bidang pendidikan. Aplikasi ini berisi course-course mengenai sertifikasi Azure. Aplikasi ini berbasis Moodle. Moodle adalah paket perangkat lunak yang diproduksi untuk kegiatan belajar berbasis internet dan situs web. Di dalam Aplikasi MariBelajar, para peserta course dapat mengakses materi, soal, dan sumber belajar lain yang telah disiapkan oleh course-creator. 

MariBelajar dibuat menggunakan platform Azure dan menggunakan moodle yang ada di Azure Marketplace. Dengan menggunakan Moodle yang sudah tersedia di Azure Marketplace, akan lebih mudah dalam mendeploy dan mengonfigurasi aplikasi. 
- Pertama-tama masuk ke [Portal Azure](https://portal.azure.com/) kemudian login ke dalam akun yang sudah memiliki azure credit. Kemudian pada bagian Layanan Azure klik "Buat Sumber Daya".

![ss](/images/1.png)

- Pada kolom pencarian, ketik "moodle" kemudian enter. Nantinya akan muncul beberapa layanan terkait mooodle.

![ss](/images/2.png)

- Pilih Moodle Virtual Machine by Bitnami, lalu klik.

![ss](/images/3.png)

- Create layanan Moodle Virtual Machine. Nantinya setelah ini akan dilakukan pembuatan Virtual Machine seperti biasa karena layanan ini pada dasarnya berbasis Virtual Machine.

![ss](/images/4.png)

- Konfiguasikan Virtual Machine sesuai kebutuhan.

![ss](/images/5.png)

![ss](/images/6.png)

![ss](/images/7.png)

![ss](/images/8.png)

![ss](/images/9-.png)

![ss](/images/10-.png)

- Setelah lulus validasi, kemudian buat Virtual Machine tersebut.

![ss](/images/11-.png)

- Setelah Virtual Machine berhasil dibuat, kembali ke Home lalu buka Virtual Machine yang baru saja dibuat.

![ss](/images/12.png)

- Pada bagian DNS, terlihat bahwa DNS masih belum dikonfigurasikan. Sebenarnya kita bisa mengakses Virtual Machine dengan menggunakan public IP-nya akan tetapi tentu akan merepotkan apabila harus menghafal nomor-nomor public IP. Sehingga perlu dilakukan konfigurasi DNS.

![ss](/images/13.png)

- Selanjutnya buat nama DNS untuk Virtual Machine. DNS ini harus bersifat unik sehingga tidak boleh sama satu dengan yang lainnya.

![ss](/images/14.png)

- Apabila DNS berhasil dikonfigurasikan, nama DNS akan ditampilkan di bagian DNS. Sekarang Virtual Machine dapat diakses menggunakan DNS tersebut. 

![ss](/images/15.png)

- Salin nama DNS yang baru saja dibuat, kemudian buka di browser. Akan muncul aplikasi Moodle dan akan diminta login sebagai administrator.

![ss](/images/16.png)

- Untuk mendapatkan user dan password dari administrator Moodle, buka kembali Virtual Machine Moodle. Pada menu bagian kiri cari "Diagnostik boot" kemudian klik. User dan password terdapat di tab "seri log". Scroll down log sampai menemukan user dan password. User dan password inilah yang nantinya akan digunakan sebagai Administrator.

![ss](/images/17.png)
