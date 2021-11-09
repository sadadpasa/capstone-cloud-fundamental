# Capstone MariBelajar
[MariBelajar](http://maribelajarsite.southeastasia.cloudapp.azure.com/) merupakan aplikasi berbasis web yang bergerak di bidang pendidikan. Aplikasi ini berisi course-course mengenai sertifikasi Azure. Aplikasi ini berbasis Moodle. Moodle adalah paket perangkat lunak yang diproduksi untuk kegiatan belajar berbasis internet dan situs web. Di dalam Aplikasi MariBelajar, para peserta course dapat mengakses materi, soal, dan sumber belajar lain yang telah disiapkan oleh course-creator. 

[MariBelajar](http://maribelajarsite.southeastasia.cloudapp.azure.com/) dibuat menggunakan platform Azure dan menggunakan moodle yang ada di Azure Marketplace. Dengan menggunakan Moodle yang sudah tersedia di Azure Marketplace, akan lebih mudah dalam mendeploy dan mengonfigurasi aplikasi. 
- Pertama-tama masuk ke [Portal Azure](https://portal.azure.com/) kemudian login ke dalam akun yang sudah memiliki azure credit. Kemudian pada bagian Layanan Azure klik **Buat Sumber Daya**.

![ss](/images/1.png)

- Pada kolom pencarian, ketik **moodle** kemudian enter. Nantinya akan muncul beberapa layanan terkait mooodle.

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

![ss](/images/16-.png)

- Untuk mendapatkan user dan password dari administrator Moodle, buka kembali Virtual Machine Moodle. Pada menu bagian kiri cari **Diagnostik boot** kemudian klik. User dan password terdapat di tab **seri log**. Scroll down log sampai menemukan user dan password. User dan password inilah yang nantinya akan digunakan sebagai Administrator.

![ss](/images/17.png)

- Masukkan user dan password ke halaman login Moodle. Setelah berhasil masuk, Moodle sudah bisa dikonfigurasikan karena admin memiliki akses penuh terhadap aplikasi Moodle. Tampilan awal setelah berhasil masuk sebagai admin akan seperti di bawah:

![ss](/images/18.png)

- Untuk membuat course baru, dapat masuk ke menu **Site Administration**. Kemudian pilih tab **Course** dan klik **add course**.

![ss](/images/19--.png)

- Pada gambar dibawah, dibuat sebuah course dengan nama **Power Platform Fundamental** dengan codename **PL-900** yang akan dimulai dari taggal 10 November 2021 sampai 10 November 2022 dengan jumlah pertemuan sebanyak 8 kali dan maksimum file size 20Mb. Setelah selesai kemudian klik **Save**.

![ss](/images/20-.png)

- Course yang baru dibuat dapat dilihat pada menu **Site Home** Kemudian klik Course yang baru saja dibuat.

![ss](/images/21.png)

- Terlihat bahwa course Power Platform Fundamental memiliki 8 pertemuan, sesuai dengan apa yang dibuat diawal. Terlihat pula bahwa course ini masih kosong, belum ada activity atau resources seperti materi, tugas, kuis, dan lainnya. Untuk menambahkan activity dan resources klik tombol **Turn Editing On**.

![ss](/images/22.png)

- Setelah tombol **Turn Editing On** diklik, akan muncul tombol **Add an activity or resource** di tiap-tiap topik. Tiap-tiap topik nantinya dapat memiliki lebih dari 1 activity atau resource sekaligus. Misal apabila ingin menambahkan activity atau resource di Topic 1, klik tombol **Add an activity or resource** yang ada di Topic 1.

![ss](/images/23.png)

- Nantinya akan ada banyak jenis Activity dan Resource yang dapat ditambahkan ke dalam Topic 1, seperti assignment, file, book, quiz, dan masih banyak lagi.

![ss](/images/24.png)

- Setelah selesai membuat course, selanjutnya akan dibuat user untuk aplikasi MariBelajar ini. Untuk membuat user, dapat masuk ke menu **Site Administration**, kemudian masuk ke tab **User**. Lalu klik tombol **add user**.

![ss](/images/25.png)

- Setelah klik **add user**, akan muncul form yang harus diisi untuk user baru yang ingin dibuat, seperti nama, email, username, dan password. Username dan password inilah yang nantinya akan digunakan user untuk login sebagai akun MariBelajar. Setelah form selesai diisi, klik **create user**. 

![ss](/images/26.png)

- Secara default, user yang baru saja dibuat akan memiliki role sebagai student. Role student disini artinya user hanya dapat mengikuti course, tidak dapat menambahkan activity dan resource ke dalam course. Untuk dapat melakukan hal tersebut, user harus diganti role nya menjadi teacher atau course creator. Untuk merubah role user, masuk ke menu **Site Administration** lalu buka tab **Users**. Pada bagian **Permissions** klik tombol **Assign system roles**.

![ss](/images/27.png)

- Masuk ke **Course creator**.

![ss](/images/28.png)

