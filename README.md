#PENJELASAN STUDI KASUS 1
Struktur Kontrol Percabangan untuk Logika Diskon:

Struktur kontrol percabangan (atau seleksi) memungkinkan program untuk mengambil keputusan dan menjalankan blok kode yang berbeda berdasarkan kondisi tertentu. Dalam hal pemberian diskon, kita perlu memeriksa apakah total belanja pelanggan memenuhi syarat untuk mendapatkan diskon. Bayangkan anda sedang berbelanja online. Toko tersebut punya aturan diskon: "Jika belanjanya lebih dari 500 ribu, akan mendapatkan potongan 10%." Cara program tahu anda mendapat diskon atau tidak, dia pakai semacam "pintu keputusan". Pintu ini namanya struktur kontrol percabangan (atau kadang disebut seleksi ). Struktur kontrol if-else(atau variasi seperti if-elif-else) sangat cocok untuk logika ini.

Cara kerja logika diskon dengan percabangan:

1. Mendapatkan Total Belanja: Program pertama-tama akan mendapatkan total nilai belanja pelanggan.
2. Pemeriksaan Kondisi: Struktur kontrol ifakan digunakan untuk memeriksa apakah total belanja lebih besar dari Rp 500.000.
3. Aksi Jika Kondisi Terpenuhi ( ifblok): Jika kondisi pada langkah 2 benar (total belanja > Rp 500.000), maka blok kode di pernyataan dalam ifakan dieksekusi. Di dalam blok ini, diskon sebesar 10% akan dihitung dan diterapkan pada total belanja.
4. Aksi Jika Kondisi Tidak Terpenuhi ( elseblok - opsional): Jika kondisi pada langkah 2 salah (total belanja tidak lebih dari Rp 500.000), maka blok kode di dalam pernyataan else(jika ada) akan dieksekusi. Dalam kasus ini, biasanya tidak ada diskon yang diterapkan, dan total bayar adalah total belanja awal.

#PENJELASAN STUDI KASUS 2
Peran Tipe Data dan Operator:

Dalam menyelesaikan perhitungan nilai rata-rata dan menentukan status izin, tipe data dan operator memegang peranan yang sangat penting 
Misalnya anda sedang menghitung nilai rapot. Agar komputer bisa membantu komputer perlu jenis-jenis angka dan simbol yang anda berikan. Jadi itulah peran Tipe Data dan Operator :

1. Tipe Data:
   
Numerik (Integer dan Float):
1. Integer ( int): Integer atau angka bulat digunakan untuk menyimpan nilai ujian mata pelajaran. Nilai ujian biasanya berupa bilangan bulat (misalnya, 80, 95, 70).
2. Float ( float): Float atau angka koma digunakan untuk menyimpan hasil perhitungan rata-rata. Rata-rata seringkali menghasilkan bilangan desimal (misalnya, 76.5, 82.33). Penting menggunakan floatagar hasil rata-rata yang mungkin berupa pecahan tidak dibulatkan menjadi bilangan bulat.
3. Boolean ( bool): digunakan untuk menyimpan status kelulusan (True untuk lulus, False untuk tidak lulus). Hasil dari perbandingan (misalnya, rata-rata >= 75) akan menghasilkan nilai boolean.
4. String ( str): Digunakan untuk menyimpan nama mata pelajaran atau status pesan kelulusan yang akan ditampilkan kepada siswa.

2. Operatornya:

Operator Aritmatika:

1. Operator Penjumlahan ( +): Digunakan untuk menjumlahkan nilai dari mata pelajaran ketiga untuk mendapatkan nilai total.
2. Operator Pembagian ( /): Digunakan untuk membagi total nilai dengan jumlah mata pelajaran (3) untuk menghitung rata-rata.

Perbandingan Operator:

3. Operator Lebih Dari atau Sama Dengan ( >=): Digunakan untuk membandingkan nilai rata-rata dengan batas kelulusan (75). Hasil dari perbandingan ini akan menentukan status kelulusan (Benar atau Salah).
4. Operator Penugasan ( =): Digunakan untuk menyimpan nilai ke dalam variabel (misalnya, menyimpan nilai ujian ke variabel nilai1, nilai2, nilai3, menyimpan hasil rata-rata ke variabel rata_rata, dan menyimpan status izin ke variabel lulus).

Jadi kesimpulannya tipe data adalah seperti jenis jenis bahan yang anda punya (int, float, bool, str). Sedanfkan operator itu seperti alat alat yang anda gunakan untuk mengolah bahan tersebut ( alat untuk menambah, membagi, membandingkan, atau menyimpan). Agar komputer  bisa memahami dan menghitung nilai ujianmu komputer harus tau jenis datanya seperti apa dan operasi apa yang harus dilakukan.

#STUDI KASUS NOMOR 3
Manfaat Penggunaan Fungsi:

Menggunakan fungsi dalam pemrograman memiliki banyak manfaat, terutama dalam konteks tugas menghitung faktorial. Bayangkan anda mempunyai banyak tugas yang hampir sama. Daripada kamu tulis ulang caranya setiap kali lebih baik anda membuat satu alat yang bisa kamu pakai terus, nah fungsi itu seperti alat di program:

1. Modularitas: Fungsi memungkinkan kita memecah program yang kompleks menjadi bagian-bagian yang lebih kecil dan terkelola. Setiap fungsi bertanggung jawab atas tugas tertentu (dalam hal ini, menghitung faktorial). Ini membuat kode lebih mudah dibaca, dipahami, dan di-debug.

2. Reusabilitas (Penggunaan Kembali): Setelah fungsi dibuat, kita dapat memperdaya berkali-kali dari bagian program lain tanpa perlu menulis ulang logika perhitungan faktorial. Misalnya, jika kita perlu menghitung faktorial dari beberapa bilangan yang berbeda, kita cukup memanggil fungsi faktorial dengan bilangan yang berbeda sebagai argumen.

3. Organisasi Kode: Fungsi membantu mengorganisasi kode secara logistik. Kode yang terkait dengan faktorial perhitungan dikomunikasikan dalam fungsi faktorial, sehingga kode program utama menjadi lebih bersih dan fokus pada alur logika yang lebih tinggi.

4. Abstraksi: Fungsinya menyembunyikan detail implementasi perhitungan faktorial. Bagian program lain yang memanggil fungsi faktorialtidak perlu tahu bagaimana faktorial itu dihitung (apakah menggunakan loop atau rekursi). Mereka hanya perlu tahu cara memanggil fungsi dan menerima hasilnya.

Bagaimana Rekursi Bekerja dalam Menghitung Faktorial:

Rekursi adalah teknik pemrograman di mana sebuah fungsi memanggil dirinya sendiri di dalam definisinya. Dalam konteks faktorial, rekursi bekerja berdasarkan definisi matematis dari faktorial:

n! = n * (n-1)! (untuk n > 0)
0! = 1 (kasus dasar atau kasus dasar)
Berikut adalah bagaimana fungsi rekursif menghitung faktorial:

Kasus Dasar (Base Case): Fungsi rekursif harus memiliki satu atau lebih kondisi yang menghentikan rekursi. Dalam faktorial, kasus dasarnya adalah ketika bilangan yang dihitung faktorialnya adalah 0. Jika input adalah 0, fungsi langsung mengembalikan 1 (sesuai definisi 0! = 1).

Langkah Rekursif: Jika bilangan yang dihitung faktorialnya bukan 0 (n > 0), fungsi akan melakukan dua hal:

Mengalikan bilangan ndengan hasil dari pemanggilan fungsi faktorialitu sendiri dengan argumen n-1.
Ini berarti fungsi "menunda" perhitungan akhir dan memanggil dirinya sendiri untuk menghitung faktorial dari bilangan yang lebih kecil ( n-1).
Proses Pemanggilan Berulang: Langkah rekursif ini akan terus berulang hingga mencapai kasus dasar (n = 0). Setiap fungsi pemanggilan akan menyimpan "keadaan" perhitungan saat ini (nilai n) di dalam call stack .

Pengembalian Nilai: Setelah mencapai kasus dasar, fungsi-fungsi yang tertunda di call stack akan mulai mengembalikan nilai secara berurutan. Hasil dari faktorial(0)adalah 1. Kemudian, faktorial(1)akan mengembalikan 1 * faktorial(0)= 1 * 1 = 1. Selanjutnya, faktorial(2)akan mengembalikan 2 * faktorial(1)= 2 * 1 = 2, dan seterusnya, hingga memanggilan fungsi awal faktorial(n)mengembalikan hasil faktorial yang sebenarnya.

Kesimpulannya 
1. Fungsi semacam alat serba guna agar program tidak ribet dan bisa di pakai lagi 
2. ⁠Rekursi cara unik fungsi belerja dengan bertanya ke dirinya sendiri untuk memecahkan masalah yang lebih keccil sampai ketemu jawaban dasarnya

#STUDI KASUS NOMOR 4
Penggunaan Peruangan dan Array (List):

Dalam kasus ini, kita perlu mengelola nilai dari 5 siswa. Penggunaan perulangan dan array (list di Python) sangat efisien dan terstruktur untuk tugas ini:

1. Array (Daftar):
Penyimpanan Koleksi Data: Array atau list memungkinkan kita menyimpan kumpulan nilai (dalam kasus ini, nilai ujian siswa) dalam satu variabel. Daripada membuat 5 variabel terpisah untuk setiap nilai siswa ( nilai_siswa1, nilai_siswa2, dst.), kita bisa menggunakan satu daftar seperti daftar_nilai.
Akses Mudah: Setiap elemen dalam daftar memiliki indeks (posisi), dimulai dari 0. Ini memungkinkan kita mengakses nilai setiap siswa dengan mudah menggunakan indeksnya (misalnya, daftar_nilai[0]untuk nilai siswa pertama, daftar_nilai[1]untuk nilai siswa kedua, dan seterusnya).

2. Perulangan ( forloop):
Input Berulang: Karena kita perlu menerima input nilai dari 5 siswa, menggunakan perulangan forjauh lebih ringkas daripada menulis 5 baris kode input()secara terpisah. Kita bisa mengatur perulangan berjalan sebanyak 5 kali, dan di setiap iterasi, kita meminta input nilai untuk siswa berikutnya. 
Pemrosesan Koleksi Data: Setelah semua nilai disimpan dalam list, kita bisa menggunakan perulangan forlagi untuk memproses setiap nilai dalam list, misalnya untuk mencari nilai tertinggi.

Bagaimana Perulangan dan List Bekerja Bersama dalam Kasus Ini:

1. Inisialisasi Daftar Lowongan: Kita akan membuat daftar kosong (misalnya, daftar_nilai = []) untuk menampung nilai-nilai siswa.
2. Perulangan untuk Input: Kita akan menggunakan perulangan foryang berjalan sebanyak 5 kali (sesuai jumlah siswa). Di dalam perulangan:
Kita akan meminta pengguna memasukkan nilai untuk siswa ke-i (dengan iindeks perulangan + 1 agar lebih mudah dipahami pengguna).
Nilai yang diinput akan ditambahkan ke dalam daftar daftar_nilaimenggunakan metode .append().
3. Pencarian Nilai Tertinggi: Setelah semua nilai masuk ke dalam daftar, kita dapat menggunakan salah satu cara berikut untuk mencari nilai tertinggi:
4. Menggunakan fungsi max(): Python memiliki fungsi bawaan max()yang dapat langsung menemukan nilai terbesar dalam sebuah list.
5. Menggunakan Peruulangan dan Perbandingan: Kita bisa menggunakan perulangan foruntukIterasi melalui list, menyimpan nilai tertinggi yang ditemukan sejauh ini dalam sebuah variabel, dan memperbarui variabel tersebut jika kita menemukan nilai yang lebih tinggi. Kita juga bisa menyimpan indeks (posisi) nilai tertinggi untuk mengetahui siswa ke berapa.

Kesimpulan
Daftar (List) tempat menyimpan banyak data seperti lemari
Perulangan (for loop) seperti robot yang bisa melakukan tugas yang sama berkali kali. Mereka bekerja sama untuk mengurus data dengan lebih mudah dan teratur


#STUDI KASUS NOMOR 5
Langkah-Langkah Algoritma:

Algoritma adalah serangkaian langkah-langkah yang terstruktur dan logis untuk menyelesaikan suatu masalah. 

Berikut adalah langkah-langkah algoritma untuk menghitung total harga pembelian 3 barang:

1. Mulai: Tandai awal dari proses perhitungan.
2. Baca Harga Barang 1: Minta kasir untuk memasukkan harga barang pertama. Simpan harga ini dalam sebuah variabel (misalnya, harga_barang1).
3. Baca Harga Barang 2: Minta kasir untuk memasukkan harga barang kedua. Simpan harga ini dalam variabel lain (misalnya, harga_barang2).
4. Baca Harga Barang 3: Minta kasir untuk memasukkan harga barang ketiga. Simpan harga ini dalam variabel (misalnya, harga_barang3).
4. Hitung Total Harga: Jumlahkan harga ketiga barang tersebut. Simpan hasil penjumlahan dalam variabel baru (misalnya, total_harga). Operasi yang dilakukan adalah: total_harga = harga_barang1 + harga_barang2 + harga_barang3.
5. Tampilkan Total Harga: Tampilkan nilai dari variabel total_hargakepada kasir atau pelanggan. Ini adalah total pembayaran yang harus dilakukan.
6. Selesai: Tandai akhir dari proses perhitungan.

