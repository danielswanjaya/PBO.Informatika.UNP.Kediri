# FUNCTION
## Function & Return Value
### 1. Konsep Function
Bayangkan fungsi sebagai sebuah resep masakan. Ketika kita ingin membuat sebuah hidangan, kita mengikuti resep yang telah ditentukan. Resep ini berisi bahan-bahan yang dibutuhkan (parameter) dan langkah-langkah pembuatannya (kode dalam fungsi). Setelah mengikuti semua langkah, kita akan mendapatkan hasil akhir berupa hidangan yang lezat.

Dalam pemrograman, fungsi memiliki peran yang serupa. Fungsi adalah sekumpulan instruksi yang dikelompokkan dan diberi nama. Kita dapat memanggil fungsi ini berkali-kali dengan memberikan input yang berbeda-beda, dan fungsi tersebut akan menghasilkan output yang sesuai. Misalnya, kita bisa membuat fungsi untuk menghitung luas persegi. Fungsi ini akan menerima panjang sisi sebagai input, kemudian menghitung dan mengembalikan luasnya.

Dalam pemrograman Python, fungsi adalah blok kode yang dirancang untuk menjalankan tugas tertentu. Bayangkan fungsi seperti sebuah mesin yang memiliki tugas spesifik. Anda memberikan input tertentu ke mesin itu, dan mesin akan memproses input tersebut lalu menghasilkan output.

Mengapa fungsi sangat berguna? **Pertama**, fungsi membuat kode program menjadi lebih terstruktur dan mudah dipahami. Bayangkan jika kita menulis semua kode dalam satu baris yang panjang, tentu akan sangat sulit untuk menemukan kesalahan atau memodifikasinya. Dengan menggunakan fungsi, kita dapat memecah kode menjadi bagian-bagian yang lebih kecil dan lebih mudah dikelola. **Kedua**, fungsi memungkinkan kita untuk menggunakan kembali kode yang sama. Misalnya, jika kita perlu menghitung luas persegi di beberapa bagian program, kita tidak perlu menulis ulang kode perhitungannya, cukup panggil fungsi yang sudah kita buat.

Fungsi juga memiliki beberapa konsep penting lainnya yang akan kita pelajari :
* Parameter: Variabel yang terdefinisi di dalam tanda kurung saat kita membuat sebuah fungsi. Parameter ini seperti tempat kosong yang akan diisi dengan nilai ketika fungsi tersebut dipanggil.
* Argumen: Nilai aktual yang kita berikan kepada parameter saat memanggil fungsi. Argumen ini digunakan untuk mengisi tempat kosong yang ada pada parameter.
* Variabel Lokal: Variabel yang dideklarasikan di dalam suatu fungsi. Artinya, variabel ini hanya "hidup" dan dapat diakses di dalam fungsi tersebut. Lingkup Variabel lokal hanya berlaku di dalam blok kode tempat ia didefinisikan. Setelah fungsi selesai dijalankan, variabel lokal akan "hilang". Tujuannya membatasi penggunaan variabel agar tidak mengganggu variabel dengan nama yang sama di bagian lain dari program. Ini membantu menghindari konflik nama dan membuat kode lebih terorganisir.
* Variabel Global: Variabel yang dideklarasikan di luar semua fungsi. Artinya, variabel ini dapat diakses dari mana saja dalam program. Lingkup Variabel global berlaku di seluruh program. Tujuannya menyimpan data yang perlu diakses oleh berbagai bagian dari program.
* Return Value: Nilai yang dikembalikan oleh sebuah fungsi setelah selesai dijalankan. Nilai ini bisa berupa angka, teks, list, atau tipe data lainnya. Kata kunci `return` digunakan untuk mengembalikan nilai dari sebuah fungsi.
* Fungsi Rekursif: Fungsi yang memanggil dirinya sendiri. Fungsi ini sangat berguna untuk menyelesaikan masalah yang dapat dipecah menjadi sub-masalah yang lebih kecil dan memiliki solusi yang serupa.
* Fungsi Lambda: Fungsi anonim yang ditulis dalam satu baris. Fungsi lambda sering digunakan untuk tugas-tugas sederhana dan biasanya dikombinasikan dengan fungsi lain seperti map, filter, atau reduce.

Struktur Dasar :
```python
def nama_fungsi(parameter1, parameter2, ...):
    # Blok kode yang akan dijalankan
    # ...
    return nilai_kembali  # Opsional, jika ingin mengembalikan nilai
```
dimana :
- `def`: Kata kunci yang menandakan awal dari definisi sebuah fungsi.
- `nama_fungsi`: Nama yang diberikan pada fungsi. Nama ini harus unik dan mengikuti aturan penamaan variabel di Python (misalnya, tidak boleh diawali dengan angka dan tidak boleh mengandung spasi).
- `parameter1, parameter2, ...`: Daftar parameter yang akan diterima oleh fungsi. Parameter ini bersifat opsional, artinya sebuah fungsi bisa saja tidak memiliki parameter. Parameter digunakan untuk memberikan input kepada fungsi.
- `blok kode`: Bagian di dalam fungsi yang berisi instruksi-instruksi yang akan dijalankan ketika fungsi dipanggil. Blok kode ini harus diawali dengan tanda titik dua (:) dan ditandai dengan indentasi (biasanya empat spasi).
- `return nilai_kembali`: Perintah untuk mengembalikan nilai dari fungsi. Bagian ini bersifat opsional. Jika tidak ada perintah return, maka fungsi tidak akan mengembalikan nilai apa pun (berfungsi sebagai prosedur).

Aturan Tambahan:
- Indentation: Indentasi sangat penting dalam Python untuk membedakan blok kode. Biasanya, indentasi menggunakan 4 spasi.
- Docstring: Sebaiknya tambahkan docstring di awal fungsi untuk menjelaskan fungsi tersebut. Docstring diapit oleh tiga tanda kutip (`"""`).
- Scope: Variabel yang didefinisikan di dalam fungsi hanya berlaku di dalam fungsi tersebut (variabel lokal). Variabel yang didefinisikan di luar fungsi berlaku di seluruh program (variabel global).

Kategori Fungsi
1. **Standard Library Function**: Fungsi-fungsi yang telah disediakan oleh Interpreter Python dalam file-file atau librarynya. Misalnya: raw_input(), input(), print(), open(), len(), max(), min(), abs() dll.
2. **Programme-Defined Function**: Function yang dibuat oleh programmer sendiri. Function ini memiliki nama tertentu yang unik dalam program, letaknya terpisah dari program utama, dan bisa dijadikan satu ke dalam suatu library buatan programmer itu sendiri.

### 2. Function tanpa return value (Procedure / Prosedur)
Prosedur atau Fungsi tanpa nilai kembalian (`return` value) adalah fungsi yang tidak mengembalikan hasil perhitungan atau nilai tertentu. Fungsi ini lebih berfokus pada melakukan suatu tindakan atau mengubah keadaan program tanpa menghasilkan output yang langsung dapat digunakan dalam ekspresi. Ciri khusus prosedur :
- Tidak menggunakan kata kunci `return`: Karena tidak mengembalikan nilai, maka tidak ada perintah `return` di dalam tubuh fungsi.
- Berfokus pada tindakan: Prosedur biasanya digunakan untuk menampilkan output ke layar, mengubah nilai variabel global, atau melakukan operasi input/output.
- Mungkin memiliki efek samping: Prosedur dapat mengubah nilai variabel di luar lingkup fungsi atau berinteraksi dengan perangkat keras.

ContohM1101.py adalah contoh pembuatan fungsi untuk mencetak teks tertentu
#### ContohM1101.py
```python
def nama_mata_kuliah():
    """
    Fungsi untuk mencetak teks 'Pemrograman Berorientasi Objek'
    """
    print('Pemrograman Berorientasi Objek')

def info_prodi():
    """
    Fungsi untuk mencetak nama Prodi, Fakultas dan Institusi
    """
    print('Prodi : Teknik Informatika')
    print('Fakultas : Teknik dan Ilmu Komputer')
    print('Institusi : Universitas Nusantara PGRI Kediri')
    
print('Panggil fungsi nama_mata_kuliah()')
nama_mata_kuliah()
print('\nPanggil fungsi info_prodi()')
info_prodi()
```
Bagian program yang diapit oleh tanda `"""` adalah Docstring.

ContohM1102.py adalah contoh pembuatan fungsi untuk mencetak kalimat perkenalan
#### ContohM1102.py
```python
def kalimatPerkenalan(nama):
    """
    Fungsi untuk mencetak teks perkenalan
    Args:
        nama (string): nama yang akan diperkenalkan
    """
    print('Assalamualaikum Wr. Wb.')
    print('Selamat pagi semua…')
    print(f'Perkenalkan Nama saya {nama}')
    print('Terima kasih 🙏')
    print('Wassalamualaikum Wr. Wb.')
    
namaAnda = input('Nama Anda:')
print('panggil fungsi kalimatPerkenalan()')
kalimatPerkenalan(namaAnda)
```
Untuk mengirim Argumen, bisa juga dengan menyebut nama parameter penerimanya, misal `kalimatPerkenalan(nama=namaAnda)`, hal ini disebut sebagai Penugasan Parameter secara Keyword. penugasan parameter secara keyword adalah cara kita memberikan nilai kepada parameter suatu fungsi dengan menyebutkan nama parameter secara eksplisit. Hal ini berbeda dengan penugasan posisi, di mana urutan parameter harus sesuai dengan definisi fungsi.

Mengapa Menggunakan Penugasan Keyword? **Pertama**, Kita bisa memberikan nilai hanya pada parameter yang ingin kita ubah, tanpa harus mengisi semua parameter sebelumnya. **Kedua**, Kode menjadi lebih mudah dibaca karena kita tahu persis parameter mana yang sedang kita isi nilainya. **Ketiga** Kita bisa menetapkan nilai default untuk parameter, sehingga jika parameter tersebut tidak diberikan nilai saat pemanggilan fungsi, maka nilai default akan digunakan.

ContohM1103.py adalah contoh pembuatan fungsi untuk mencetak Luas Persegi dan penggunaan Penugasan Parameter secara Keyword
#### ContohM1103.py
```python
def luasPersegi1(nama, sisi):
    """
    Fungsi untuk menghitung dan mencetak Luas Persegi tanpa satuan
    Args:
        nama (String): Nama Persegi yang akan diukur luasnya
        sisi (int): Panjang sisi Persegi
    """
    luas = sisi ** 2
    print(f'Luas Persegi {nama} adalah {luas} satuan\u00b2')
    
def luasPersegi2(nama, sisi, satuan):
    """
    Fungsi untuk menghitung dan mencetak Luas Persegi dengan satuan tertentu
    Args:
        nama (String): Nama Persegi yang akan diukur luasnya
        sisi (int): Panjang sisi Persegi
        satuan (String): Satuan pengukuran, misal : M, Cm, Inch
    """
    luas = sisi ** 2
    print(f'Luas Persegi {nama} adalah {luas} {satuan}\u00b2')

print('HITUNG LUAS PERSEGI')
namaBidang1 = input('Nama Persegi:')
panjangSisi1 = int(input('Panjang Sisi:'))
luasPersegi1(nama=namaBidang1, sisi=panjangSisi1)

namaBidang2 = input('Nama Persegi:')
panjangSisi2 = int(input('Panjang Sisi:'))
satuan = input('Satuan Pengukuran (M, Cm, Inch):')
luasPersegi2(satuan=satuan, nama=namaBidang2, sisi=panjangSisi2)
```
Keuntungan Penugasan Parameter secara Keyword adalah tidak perlu memperhatikan urutan pendefinisian. Seperti fungsi `luasPersegi2`, urutan parameternya adalah `nama`, `sisi` lalu `satuan`, tetapi pada saat pemanggilan `luasPersegi2` urutannya menjadi `satuan`, `nama` lalu `sisi`. 

Aturan Umum Penugasan Parameter Secara Keyword :
1. Saat menggunakan penugasan keyword, Anda tidak perlu mengikuti urutan parameter yang didefinisikan dalam fungsi. Ini memberikan fleksibilitas dalam memanggil fungsi.
2. Anda dapat memberikan nilai default untuk parameter saat mendefinisikan fungsi. Parameter dengan nilai default bersifat opsional, artinya Anda tidak perlu memberikan nilai saat memanggil fungsi.
3. Anda dapat menggabungkan kedua jenis penugasan ini dalam satu pemanggilan fungsi. Parameter yang nilainya diberikan secara posisi harus berada sebelum parameter yang nilainya diberikan secara keyword.

Contoh penugasan parameter saat pemanggilan yang benar, jika menggunakan penugasan posisi dan penugasan keyword bersamaan :
```python
luasPersegi2(namaBidang2, panjangSisi2, satuan)
# atau
luasPersegi2(namaBidang2, satuan=satuan, sisi=panjangSisi2)
# atau
luasPersegi2(namaBidang2, panjangSisi2, satuan=satuan)
```
Tetapi cara berikut tidak diperbolehkan
```python
luasPersegi2(nama=namaBidang2, panjangSisi2, satuan=satuan)
# atau
luasPersegi2(satuan=satuan, nama=namaBidang2, panjangSisi2)
```
Karena bagian yang diperbolehkan tidak disebutkan nama parameternya adalah urut dari awal.

ContohM1104.py adalah contoh pembuatan fungsi untuk menghitung volume balok, dimana salah parameternya memiliki nilai default
#### ContohM1104.py
```python
def hitung_volume_balok(nama, panjang, lebar, tinggi, satuan='Cm'):
    """
    Fungsi ini menghitung volume balok.
    Args:
        nama (String): Nama Persegi yang akan diukur luasnya
        panjang (int): Panjang balok (dalam satuan yang ditentukan).
        lebar (int): Lebar balok (dalam satuan yang ditentukan).
        tinggi (int): Tinggi balok (dalam satuan yang ditentukan).
        satuan (String): Satuan panjang (default: 'Cm').
    """
    volume = panjang * lebar * tinggi
    print(f'Volume balok {nama} adalah {volume} {satuan}\u00b3')

print('HITUNG VOLUME BALOK')
namaBalok1 = input('Nama Balok:')
panjangBalok1 = int(input('Panjang Balok:'))
lebarBalok1 = int(input('Lebar Balok:'))
tinggiBalok1 = int(input('Tinggi Balok:'))
hitung_volume_balok(nama=namaBalok1, panjang=panjangBalok1, lebar=lebarBalok1, tinggi=tinggiBalok1)

namaBalok2 = input('Nama Balok:')
panjangBalok2 = int(input('Panjang Balok:'))
lebarBalok2 = int(input('Lebar Balok:'))
tinggiBalok2 = int(input('Tinggi Balok:'))
satuanBalok2 = input('Satuan Pengukuran:')
hitung_volume_balok(nama=namaBalok2, panjang=panjangBalok2, lebar=lebarBalok2, tinggi=tinggiBalok2, satuan=satuanBalok2)
```

ContohM1105.py adalah contoh pembuatan fungsi untuk menghitung Luas Permukaan Balok, dimana semua parameter memiliki nilai default.
#### ContohM1105.py
```python
def hitung_luas_permukaan_balok(nama='TANPA NAMA', panjang=1, lebar=1, tinggi=1, satuan='cm'):
  """
  Fungsi ini menghitung luas permukaan balok.
  Args:
    nama (String): Nama balok (default: 'tanpa nama').
    panjang (int): Panjang balok (default: 1 cm).
    lebar (int): Lebar balok (default: 1 cm).
    tinggi (int): Tinggi balok (default: 1 cm).
    satuan (String): Satuan panjang (default: 'cm').
  """
  luas_permukaan = 2 * ((panjang * lebar) + (panjang * tinggi) + (lebar * tinggi))
  print(f"Luas permukaan balok {nama} adalah: {luas_permukaan} {satuan}\u00b2")

print('Perhitungan ke-1')
hitung_luas_permukaan_balok()
print('Perhitungan ke-2')
hitung_luas_permukaan_balok('Bak Mandi')
print('Perhitungan ke-3')
hitung_luas_permukaan_balok('Kotak Mainan', 5, 3, 2, 'm')
print('Perhitungan ke-4')
hitung_luas_permukaan_balok(nama='kubus kecil', tinggi=3)
print('Perhitungan ke-5')
hitung_luas_permukaan_balok(satuan='Inch', tinggi=3, nama='Kotak Hadiah', panjang=9, lebar=5)
print('Perhitungan ke-6')
hitung_luas_permukaan_balok(nama='Kamar Tidur', panjang=5, lebar=3, tinggi=2, satuan='m')
print('Perhitungan ke-7')
hitung_luas_permukaan_balok(panjang=5, lebar=3, tinggi=2)
print('Perhitungan ke-8')
hitung_luas_permukaan_balok('Kolam Renang', 1000, 5000, 200)
```

ContohM1106.py adalah contoh pembuatan fungsi untuk mendata dan mencetak daftar belanjaan.
#### ContohM1106.py
```python
daftar_belanja = {}
total_belanja = 0

def tambah_item(item, harga):
    """
    Menambahkan item ke daftar belanja dan menghitung total belanja.
    Args:
        item (String): Nama item yang akan ditambahkan.
        harga (int): Harga item.
    """
    global total_belanja
    daftar_belanja[item] = harga
    total_belanja += harga
    print(f"Item '{item}' dengan harga Rp{harga} telah ditambahkan.")
  
def tampilkan_daftar_belanja():
    """Menampilkan semua item dalam daftar belanja beserta harganya."""
    if daftar_belanja:
        print("Daftar Belanja:")
        for item, harga in daftar_belanja.items():
            print(f"- {item}: Rp{harga}")
    else:
        print("Daftar belanja masih kosong.")

print('DAFTAR BELANJAANKU')
tambah_item("Telur", 15000)
tambah_item("Susu", 10000)
tambah_item("Roti", 8000)
tambah_item("Selai", 11000)
tambah_item("Tepung", 6000)

tampilkan_daftar_belanja()

print(f"Total belanja akhir: Rp{total_belanja}")
```

Pada contoh tersebut variabel `daftar_belanja` dan `total_belanja` disebut sebagai Variabel Global. Variabel global adalah variabel yang dideklarasikan di luar semua fungsi atau blok kode dalam sebuah program. Ini berarti variabel tersebut dapat diakses dari mana saja dalam program tersebut, tanpa perlu dideklarasikan ulang di setiap fungsi atau blok kode. Variabel global dapat diakses dari seluruh bagian program, deklarasinya biasanya dilakukan di awal program (sebelum definisi fungsi-fungsi), dan nilai variabel global dapat diubah dari mana saja dalam program.

Tetapi saat menggunaan Variabel Global kita juga harus berhati-hati, karena :
- Jika banyak bagian program yang mengakses dan memodifikasi variabel global, akan sulit melacak perubahan nilai dan potensi kesalahan.
- Program menjadi kurang modular karena ketergantungan antar bagian program yang tinggi.
- Jika beberapa bagian program secara tidak sengaja mengubah nilai variabel global yang sama, dapat menyebabkan perilaku program yang tidak terduga.

```
Modular adalah konsep dalam pemrograman yang mengacu pada pembagian suatu program menjadi bagian-bagian yang lebih kecil, mandiri, dan dapat dikelola secara terpisah. Masing-masing bagian ini disebut modul. Modularisasi membantu kita membangun program yang lebih baik, lebih mudah dipelihara, dan lebih mudah dikembangkan. Dengan membagi program menjadi modul-modul yang lebih kecil, kita dapat meningkatkan kualitas perangkat lunak secara keseluruhan.
```

Variabel Global sebaiknya digunakan ketika :
- Konstanta: Nilai yang tidak akan pernah berubah, seperti nilai pi atau konversi satuan.
- Variabel konfigurasi: Menyimpan pengaturan program yang berlaku secara global.
- Variabel yang sering digunakan: Jika suatu variabel sangat sering digunakan di berbagai bagian program, mungkin lebih efisien untuk membuatnya global.

Saat kita ingin mengubah nilai variabel global dari dalam sebuah fungsi, kita perlu memahami konsep ruang lingkup (scope) variabel. Variabel global memiliki ruang lingkup yang luas, artinya dapat diakses dari mana saja dalam program. Namun, fungsi memiliki ruang lingkupnya sendiri, yang secara default tidak mencakup variabel global. Ada beberapa cara untuk memberikan nilai ke variabel global dari dalam fungsi, namun perlu diperhatikan bahwa penggunaan variabel global secara berlebihan seringkali dianggap sebagai praktik pemrograman yang buruk karena dapat membuat kode menjadi kurang terbaca dan sulit dipelihara. Salah satu caranya adalah menggunakan Keyword `global` seperti pada ContohM1106.py baris ke-11. Jika tidak menggunakan keyword `global` maka variabel `total_belanja` di dalam fungsi `tambah_item` akan dianggap sebagai Variabel Lokal.

Variabel lokal adalah variabel yang dideklarasikan dan hanya dapat diakses di dalam blok kode tertentu, seperti di dalam sebuah fungsi. Variabel ini memiliki ruang lingkup (scope) yang terbatas pada blok kode tempat ia didefinisikan. Setelah blok kode tersebut selesai dijalankan, variabel lokal akan hilang dari memori. Variabel Lokal sering digunakan untuk :
- Mengatur Ruang Lingkup: Membatasi penggunaan variabel hanya pada bagian kode yang relevan, sehingga menghindari konflik nama variabel.
- Meningkatkan Keterbacaan Kode: Membuat kode lebih mudah dipahami karena setiap fungsi memiliki variabelnya sendiri.
- Membuat Kode Lebih Modular: Memungkinkan kita membuat fungsi-fungsi yang independen dan dapat digunakan kembali.

##### Tabel 1. Perbedaan Variabel Lokal & Global
|Fitur|Variabel Lokal|Variabel Global|
|-|-|-|
|Ruang Lingkup|Terbatas pada blok kode tempat didefinisikan|Dapat diakses dari mana saja dalam program|
|Umur|Hilang setelah blok kode selesai dijalankan|Berada selama program berjalan|
|Konflik Nama|Tidak menimbulkan konflik jika ada variabel dengan nama yang sama di luar blok kode|Dapat menimbulkan konflik jika ada variabel dengan nama yang sama di blok kode lain|

ContohM1107.py adalah modifikasi ContohM1020.py, dimana untuk setiap operator dibuatkan fungsi sendiri dan operasi perhitungannya dicatat.
#### ContohM1107.py
```python
data = []
jumlah, opsi = None, 1

def tambah(angka):
    """Fungsi untuk menambahkan nilai variabel angka ke variabel jumlah dan mendata operasi perhitungannya"""
    global jumlah
    jumlah += angka
    data.append(f'+ {angka}')

def kurang(angka):
    """Fungsi untuk mengurangi nilai variabel jumlah dengan variabel angka dan mendata operasi perhitungannya"""
    global jumlah
    jumlah -= angka
    data.append(f'- {angka}')

def kali(angka):
    """Fungsi untuk mengalikan nilai variabel angka ke variabel jumlah dan mendata operasi perhitungannya"""
    global jumlah
    jumlah *= angka
    data.append(f'x {angka}')

def bagi(angka):
    """Fungsi untuk membagi nilai variabel jumlah dengan variabel angka dan mendata operasi perhitungannya"""
    global jumlah
    jumlah /= angka
    data.append(f'/ {angka}')
def cetak():
    """Fungsi untuk mencetak operasi perhitungannya"""
    hasil = ''
    for idx in range(len(data)) :
        if idx == 0 :
            hasil = data[idx]
        elif idx == 1 :
            hasil = hasil + ' ' + data[idx]
        else :
            hasil = f'({hasil}) {data[idx]}'
    print(hasil)

print("Kalkulator berjalan")
while opsi != '0' :
    if jumlah == None :
        jumlah = int(input("Masukan nilai awal:"))
        data.append(str(jumlah))
    else :
        print('Jumlah sementara:',jumlah)
        opsi = input("Masukan operator (+, -, x, /, 0 untuk selesai):")
        match opsi :
            case '+':
                angka = int(input("Masukan angka :"))
                tambah(angka)
            case '-':
                angka = int(input("Masukan angka :"))
                kurang(angka)
            case 'x':
                angka = int(input("Masukan angka :"))
                kali(angka)
            case '/':
                angka = int(input("Masukan angka :"))
                bagi(angka)
            case '0':
                print("Selesai.")
            case _ :
                print("Operator tidak dikenal.")
cetak()
print('Jumlah akhir:',jumlah)
```

ContohM1108.py adalah contoh pembuatan fungsi untuk mendata anggota baru, transaksi menabung dan tarik tunai, cek saldo dan riwayat transaksi di Koperasi Siswa Harapan Cerdas.
#### ContohM1108.py
```python
data_anggota = {
    1: {
        "nama": "Andi",
        "saldo": 130000,
        "riwayat": [
            "Buka rekening dengan saldo awal 100000",
            "Menabung sebesar Rp 50000",
            "Tarik tunai sebesar Rp 20000"
        ]
    },
    2: {
        "nama": "Budi",
        "saldo": 90000,
        "riwayat": [
            "Buka rekening dengan saldo awal 50000",
            "Menabung sebesar Rp 30000",
            "Tarik tunai sebesar Rp 10000",
            "Menabung sebesar Rp 20000"
        ]
    },
    3: {
        "nama": "Cici",
        "saldo": 90000,
        "riwayat": [
            "Buka rekening dengan saldo awal 150000",
            "Tarik tunai sebesar Rp 50000",
            "Menabung sebesar Rp 10000",
            "Tarik tunai sebesar Rp 20000"
        ]
    },
    4: {
        "nama": "Dedi",
        "saldo": 100000,
        "riwayat": [
            "Buka rekening dengan saldo awal 80000",
            "Menabung sebesar Rp 40000",
            "Tarik tunai sebesar Rp 30000",
            "Menabung sebesar Rp 20000",
            "Tarik tunai sebesar Rp 10000"
        ]
    },
    5: {
        "nama": "Eni",
        "saldo": 140000,
        "riwayat": [
            "Buka rekening dengan saldo awal 120000",
            "Menabung sebesar Rp 30000",
            "Tarik tunai sebesar Rp 20000",
            "Menabung sebesar Rp 10000"
        ]
    }
}

def tampilkan_menu():
    """Menampilkan menu pilihan kepada pengguna."""
    print("Pilih menu:")
    print("1. Buka Tabungan Baru")
    print("2. Menabung")
    print("3. Tarik Tunai")
    print("4. Cek Saldo")
    print("5. Cetak Riwayat Transaksi")
    print("6. Keluar")

def buka_tabungan_baru():
    """Membuka tabungan baru untuk anggota koperasi."""
    nomor_anggota = len(data_anggota) + 1
    nama = input("Masukkan nama anggota: ")
    data_anggota[nomor_anggota] = {
        "nama": nama,
        "saldo": 0,
        "riwayat": [f"Buka rekening dengan saldo awal 0"]
    }
    print(f"Selamat! Anda berhasil membuka rekening dengan nomor {nomor_anggota}")

def menabung():
    """Menambahkan saldo pada rekening anggota."""
    nomor_anggota = int(input("Masukkan nomor anggota: "))
    jumlah = float(input("Masukkan jumlah yang akan ditabung: "))

    if nomor_anggota in data_anggota:
        data_anggota[nomor_anggota]["saldo"] += jumlah
        data_anggota[nomor_anggota]["riwayat"].append(f"Menabung sebesar Rp {jumlah}")
        print("Saldo Anda berhasil diperbarui.")
    else:
        print("Nomor anggota tidak ditemukan.")

def tarik_tunai():
    """Mengurangi saldo pada rekening anggota."""
    # ... (implementasi serupa dengan fungsi menabung)

def cek_saldo():
    """Menampilkan saldo dan riwayat transaksi anggota."""
    nomor_anggota = int(input("Masukkan nomor anggota: "))

    if nomor_anggota in data_anggota:
        print(f"Nama: {data_anggota[nomor_anggota]['nama']}")
        print(f"Saldo: Rp {data_anggota[nomor_anggota]['saldo']}")
        print("Riwayat Transaksi:")
        for transaksi in data_anggota[nomor_anggota]["riwayat"]:
            print(f"- {transaksi}")
    else:
        print("Nomor anggota tidak ditemukan.")

def cetak_riwayat_transaksi():
    """Mencetak riwayat transaksi anggota."""
    nomor_anggota = int(input("Masukkan nomor anggota: "))

    if nomor_anggota in data_anggota:
        print(f"Riwayat Transaksi Anggota {nomor_anggota} ({data_anggota[nomor_anggota]['nama']}):")
        for transaksi in data_anggota[nomor_anggota]["riwayat"]:
            print(transaksi)
    else:
        print("Nomor anggota tidak ditemukan.")

print("Selamat datang di Koperasi Siswa Harapan Cerdas!")
while True:
    tampilkan_menu()
    pilihan = input("Masukkan pilihan Anda: ")

    match pilihan:
        case '1':
            buka_tabungan_baru()
        case '2':
            menabung()
        case '3':
            tarik_tunai()
        case '4':
            cek_saldo()
        case '5':
            cetak_riwayat_transaksi()
        case '6':
            print("Terima kasih telah menggunakan layanan kami!")
            break
        case _:
            print("Pilihan tidak valid.")
```

### 3. Function dengan return value
Function dengan return value adalah jenis fungsi yang tidak hanya menjalankan kode, tetapi juga mengembalikan suatu nilai hasil eksekusi fungsi tersebut. Nilai yang dikembalikan ini bisa berupa tipe data apa saja, seperti angka, string, list, bahkan objek. Ciri khusus Function dengan return value :
- Mengembalikan Nilai: Ciri paling utama adalah fungsi ini akan menghasilkan suatu nilai sebagai output setelah proses di dalamnya selesai dijalankan. Nilai ini bisa berupa tipe data apa pun, mulai dari angka, teks, hingga struktur data yang lebih kompleks seperti list atau dictionary.
- Kata Kunci return: Penggunaan kata kunci return adalah wajib dalam fungsi yang ingin mengembalikan nilai. Setelah return, diikuti dengan nilai yang akan dikembalikan.
- Penghenti Eksekusi: Saat return dijalankan, eksekusi fungsi akan langsung berhenti dan nilai yang ditentukan akan dikembalikan ke bagian kode yang memanggil fungsi tersebut.
- Fleksibel dalam Penggunaan: Nilai yang dikembalikan dapat disimpan dalam variabel, digunakan dalam perhitungan selanjutnya, atau bahkan dijadikan argumen untuk fungsi lain.
- Opsional: Tidak semua fungsi harus memiliki return value. Jika tidak ada kata kunci return, fungsi akan secara otomatis mengembalikan nilai None.

ContohM1109.py adalah contoh pembuatan fungsi untuk menghitung basaran Energi Potensial.
#### ContohM1109.py
```python
def gravitasi_ms2():
    """Mengembalikan nilai gravitasi bumi dalam satuan meter/detik^2"""
    return 9.81

def gravitasi_inchs2():
    """Mengembalikan nilai gravitasi bumi dalam satuan inch/detik^2"""
    return gravitasi_ms2() * 39.3701

massa = int(input("Masukkan massa benda (kg): "))
print("Pilih satuan ketinggian:")
print("1. Meter")
print("2. Inch")
pilihan = int(input("Masukkan pilihan Anda (1 atau 2): "))

match pilihan :
    case 1 : 
        g = gravitasi_ms2()
        satuan = 'Meter'
    case 2 : 
        g = gravitasi_inchs2()
        satuan = 'Inch'
    case _:
        print("Pilihan tidak valid. Satuan Meter")
        g = gravitasi_ms2()
        satuan = 'Meter'

ketinggian = int(input(f"Masukkan ketinggian benda ({satuan}): "))
ep = massa * g * ketinggian
print(f"Energi potensial benda: {ep:.3f} Joule")
```

ContohM1110.py adalah contoh pembuatan fungsi untuk menghitung rata-rata dari beberapa data acak. 
#### ContohM1110.py
```python
import random
def hitung_rata_rata(angka):
    """
    Hitung rata-rata dari list angka.
    Args:
        angka (int): List of numbers.
    Returns:
        Rata-rata dari list angka.
    """
    return sum(angka) / len(angka)

print("HITUNG RATA-RATA DARI BEBERAPA DATA ACAK")
banyak = int(input("Masukan banyak data:"))
bawah = int(input("Batas bawah:"))
atas = int(input("Batas atas:"))

if atas < bawah :
    atas, bawah = bawah, atas

angka = [random.randint(bawah,atas+1) for _ in range(banyak)]
rata_rata = hitung_rata_rata(angka)

print("Data :\n",angka)
print("Rata-rata:", rata_rata)
```

ContohM1111.py adalah contoh pembuatan fungsi untuk menghitung volume Tetrahedron (Gambar 1)
![Gambar 1](https://polyhedr.com/images/polyhedra/001/Tetrahedron350x350.jpg)<br>Gambar 1. Bangun Ruang Tetrahedron.
#### ContohM1111.py
```python
def volume_tetrahedron(rusuk=1):
    """
    Fungsi ini menghitung volume tetrahedron beraturan.

    Args:
        rusuk (int): Panjang rusuk tetrahedron. Nilai defaultnya 1.

    Returns:
        float: Volume tetrahedron.
    """

    volume = (rusuk**3 * 2**0.5) / 12
    return volume
print('HITUNG VOLUME TETRAHEDRON')
panjang_rusuk = int(input("Masukkan panjang rusuk tetrahedron (Meter): "))

hasil = volume_tetrahedron(panjang_rusuk)
print(f"Volume tetrahedron adalah: {hasil:.3f} M³")
print(f"Volume tetrahedron dengan panjang rusuk 1 Meter adalah: {volume_tetrahedron():.3f} M³")
```

ContohM1112.py adalah contoh pembuatan fungsi untuk menghitung nilai Permutasi dan Kombinasi
#### ContohM1112.py
```python
def faktorial(n):
    """
    Fungsi untuk menghitung nilai faktorial dari bilangan bulat non-negatif.
    Args:
        n (int): Bilangan bulat non-negatif.
    Returns:
        Nilai faktorial dari n.
    """

    if n < 0:
        return "Faktorial tidak terdefinisi untuk bilangan negatif"
    elif n == 0 or n == 1:
        return 1
    else:
        hasil = 1
        for i in range(2, n+1):
            hasil *= i
        return hasil

def permutasi(n, r):
    """
    Fungsi untuk menghitung nilai permutasi.
    Args:
        n (int): Jumlah total elemen.
        r (int): Jumlah elemen yang dipilih.
    Returns:
        Nilai permutasi.
    """

    hasil = faktorial(n) / faktorial(n-r)
    return hasil

def kombinasi(n, r):
    """
    Fungsi untuk menghitung nilai kombinasi.
    Args:
        n (int): Jumlah total elemen.
        r (int): Jumlah elemen yang dipilih.
    Returns:
        Nilai kombinasi.
    """
    hasil = faktorial(n)/(faktorial(r)*faktorial(n-r))
    return hasil

print('HITUNG NILAI PERMUTASI DAN KOMBINASI')
n = int(input('Total Elemen:'))
r = int(input('Banyak Elemen yang dipilih:'))

hasil_permutasi = permutasi(n, r)
hasil_kombinasi = kombinasi(n, r)

print("Permutasi P(", n, ",", r, ") = ", hasil_permutasi)
print("Kombinasi C(", n, ",", r, ") = ", hasil_kombinasi)
```

ContohM1113.py adalah contoh pembuatan fungsi untuk menghitung frekuensi kata dalam sebuah kalimat 
#### ContohM1113.py
```python
def hitung_frekuensi(kalimat):
    """
    Menghitung frekuensi kemunculan setiap kata dalam kalimat.
    Args:
        kalimat: Kalimat yang akan dihitung frekuensinya.
    Returns:
        Dictionary di mana key adalah kata dan value adalah frekuensinya.
    """

    kata_list = kalimat.split()
    frekuensi = {}
    for kata in kata_list:
        frekuensi[kata] = frekuensi.get(kata, 0) + 1
    return frekuensi

kalimat = "Hari demi hari, minggu demi minggu, bulan demi bulan, \
Dia ingin pergi, tapi dia takut; dia ingin tinggal, tapi dia bosan."
kalimat_tanpa_tanda_baca = ''.join(c for c in kalimat if c.isalnum() or c.isspace())
hasil = hitung_frekuensi(kalimat_tanpa_tanda_baca)
print(hasil)
```

ContohM1114.py adalah contoh pembuatan fungsi untuk menghitung nilai determinan matriks ordo 2 dan 3.
#### ContohM1114.py
```python
import random

def determinan_2x2(matriks):
    """
    Fungsi untuk menghitung determinan matriks ordo 2.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks 2x2.
    Returns:
        Nilai determinan dari matriks.
    """
    determinan = matriks[0][0] * matriks[1][1] - matriks[0][1] * matriks[1][0]
    return determinan

def determinan_3x3(matriks):
    """
    Fungsi untuk menghitung determinan matriks ordo 3 menggunakan metode ekspansi kofaktor.

    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks 3x3.

    Returns:
        Nilai determinan dari matriks.
    """
    n = len(matriks)
    determinan = 0
    for j in range(n):
        minor = [[matriks[i][k] for k in range(n) if k != j] 
                for i in range(1, n)]

        kofaktor = (-1)**(1+j+1) * determinan_2x2(minor)

        determinan += matriks[0][j] * kofaktor
    return determinan

def cetak_matriks(matriks):
    """
    Fungsi untuk mencetak matriks dengan rapi.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks.
    """
    for baris in matriks:
        for elemen in baris:
            print(f"{elemen:>4}", end=" ")
        print()

print('DETERMINAN MATRIKS')
matriks_ordo2 = [[random.randint(-10, 10) for _ in range(2)] for _ in range(2)]
matriks_ordo3 = [[random.randint(-10, 10) for _ in range(3)] for _ in range(3)]

print("Matriks Ordo 2:")
cetak_matriks(matriks_ordo2)
print("Determinan matriks:", determinan_2x2(matriks_ordo2))
print("\nMatriks Ordo 3:")
cetak_matriks(matriks_ordo3)
print("Determinan matriks:", determinan_3x3(matriks_ordo3))
```

ContohM1115.py adalah contoh pembuatan fungsi untuk membuat sebuah matriks ordo tertentu secara acak dan mencetak hasil transposenya.
#### ContohM1115.py
```python
import random
from ContohM1114 import cetak_matriks 

def buat_matriks(row=2, col=2):
    """
    Membuat sebuah matriks dengan ukuran baris (row) dan kolom (col) yang ditentukan.
    Args:
        row: Jumlah baris matriks (default: 2).
        col: Jumlah kolom matriks (default: 2).
    Returns:
        Sebuah list of lists yang merepresentasikan matriks.
    """
    matriks = [[random.randint(-20, 20) for _ in range(col)] for _ in range(row)]
    return matriks

def transpose_matriks(matriks):
    """
    Mentranspose sebuah matriks.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks.
    Returns:
        Sebuah list of lists yang merepresentasikan matriks transposenya.
    """
    baris = len(matriks)
    kolom = len(matriks[0])
    transpose = [[matriks[j][i] for j in range(baris)] for i in range(kolom)]
    return transpose

print('MATRIKS TRANSPOSE')
matriksA = buat_matriks()
transpose_matriksA = transpose_matriks(matriksA)
print('Matriks A (ordo 2 x 2):')
cetak_matriks(matriksA)
print('Hasil Transpose:')
cetak_matriks(transpose_matriksA)

print('\nMatriks B:')
baris = int(input("Masukkan jumlah baris: "))
kolom = int(input("Masukkan jumlah kolom: "))
matriksB = buat_matriks(baris, kolom)
transpose_matriksB = transpose_matriks(matriksB)
print(f'Matriks A (ordo {baris} x {kolom}):')
cetak_matriks(matriksB)
print(f'Hasil Transpose (ordo {kolom} x {baris}):')
cetak_matriks(transpose_matriksB)
```
Pada baris ke-2 terdapat perintah :
```python
from ContohM1114 import cetak_matriks
```
Perintah ini merupakan bagian dari sintaks impor dalam bahasa pemrograman Python. Secara sederhana, perintah ini berfungsi untuk "mengimpor" atau "membawa masuk" sebuah fungsi bernama `cetak_matriks` dari sebuah modul (file Python) yang bernama `ContohM1114`. Dengan mengimpor fungsi `cetak_matriks`, kita bisa menggunakannya secara langsung dalam program kita tanpa perlu menulis ulang (atau copy-paste) kodenya.

Tetapi saat file ContohM1115.py dieksekusi, kode utama dari file ContohM1114.py juga ikut tereksekusi. Untuk mengatasi hal ini modifikasi file ContohM1114.py dengan menambahkan kondisi :
```python
if __name__ == '__main__'
```
Sehingga file ContohM1114.py menjadi seperti berikut :
```python
import random

def determinan_2x2(matriks):
    # definisi tidak berubah

def determinan_3x3(matriks):
    # definisi tidak berubah

def cetak_matriks(matriks):
    # definisi tidak berubah

if __name__ == '__main__' :
    print('DETERMINAN MATRIKS')
    # selanjutnya tidak berubah, cukup tambahkan identasi.
```
Perintah tersebut digunakan untuk menentukan apakah sebuah modul Python sedang dijalankan secara langsung (sebagai script utama) atau sedang diimpor sebagai modul ke dalam script Python lainnya. Ketika kondisi `__name__ == '__main__'` benar (yaitu, ketika modul sedang dijalankan secara langsung), maka kode yang berada di dalam blok if akan dieksekusi. `__name__` adalah variabel khusus dalam Python yang berisi nama dari modul saat ini. `__main__` adalah nilai khusus yang diberikan kepada `__name__` ketika sebuah modul dijalankan secara langsung (sebagai script utama).

ContohM1116.py adalah contoh pembuatan fungsi untuk mencetak teks tertentu
#### ContohM1116.py
```python
from ContohM1114 import determinan_2x2
from ContohM1114 import determinan_3x3
from ContohM1114 import cetak_matriks
from ContohM1115 import buat_matriks

def invers_matriks_2x2(matriks):
    """
    Menghitung invers dari matriks 2x2.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks 2x2.
    Returns:
        Invers dari matriks jika ada, atau pesan error jika tidak ada invers.
    """
    determinan = determinan_2x2(matriks)

    if determinan == 0:
        return "Matriks tidak memiliki invers"

    invers = [[matriks[1][1]/determinan, -matriks[0][1]/determinan],
            [-matriks[1][0]/determinan, matriks[0][0]/determinan]]

    return invers

def invers_matriks_3x3(matriks):
    """
    Menghitung invers matriks 3x3 menggunakan metode adjoin.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks 3x3.
    Returns:
        Invers dari matriks jika ada, atau pesan error jika tidak ada invers.
    """
    det = determinan_3x3(matriks)
    if det == 0:
        return "Matriks tidak memiliki invers"

    kofaktor = [[0 for _ in range(3)] for _ in range(3)]
    for i in range(3):
        for j in range(3):
            minor = [[matriks[x][y] for y in range(3) if y != j] for x in range(3) if x != i]
            kofaktor[i][j] = (-1)**(i+j) * determinan_2x2(minor)

    adjoin = [[kofaktor[j][i] for j in range(3)] for i in range(3)]
    invers = [[x/det for x in baris] for baris in adjoin]
    return invers

def cetak_matriks_desimal(matriks):
    """
    Fungsi untuk mencetak matriks dengan rapi.
    Args:
        matriks: Sebuah list of lists yang merepresentasikan matriks.
    """
    for baris in matriks:
        for elemen in baris:
            print(f"{elemen:>7.3f}", end=" ")
        print()

print('INVERS MATRIKS')
print('Matriks ordo 2:')
matriksA = buat_matriks()
cetak_matriks(matriksA)
hasilA = invers_matriks_2x2(matriksA)
if(type(hasilA) == type(matriksA)):
    cetak_matriks_desimal(hasilA)
else:
    print(hasilA)

print('Matriks ordo 3:')
matriksB = buat_matriks(3, 3)
cetak_matriks(matriksB)
hasilB = invers_matriks_3x3(matriksB)
if(type(hasilB) == type(matriksB)):
    cetak_matriks_desimal(hasilB)
else:
    print(hasilB)
```
Pada file ContohM1116.py terdapat 4 baris perintah import, salah satunya dari file ContohM1115.py, maka pada file ContohM1115.py perlu ditambahkan perintah :
```python
if __name__ == '__main__' :
```
sebelum perintah :
```python
print('MATRIKS TRANSPOSE')
```
sekaligus identasi pada awal semua baris setelah perintah tersebut.

### 4. Parameter Fungsi
Pada materi di atas terdapat istilah parameter dan argumen serta contohnya. Parameter fungsi sendiri adalah nilai yang diberikan kepada fungsi saat dipanggil. Nilai-nilai ini digunakan di dalam fungsi untuk melakukan perhitungan atau operasi tertentu. Pemahaman yang baik tentang parameter fungsi sangat penting dalam menulis kode yang fleksibel dan dapat digunakan kembali. 

Argumen adalah nilai yang kita berikan kepada suatu fungsi saat kita memanggilnya. Argumen ini digunakan oleh fungsi untuk melakukan tugas tertentu. Bayangkan fungsi sebagai sebuah mesin yang membutuhkan bahan baku untuk diolah, dan argumen adalah bahan baku tersebut.

Dalam konteks pemrograman Python, argumen dan parameter seringkali digunakan secara bergantian, namun sebenarnya memiliki makna yang sedikit berbeda :
* **Parameter**: Ini adalah variabel yang terdefinisi dalam definisi suatu fungsi. Mereka bertindak sebagai placeholder untuk nilai yang akan diberikan saat fungsi dipanggil.
* **Argumen**: Ini adalah nilai aktual yang diberikan kepada parameter saat fungsi dipanggil.

Hubungan Antara Argumen dan Parameter:
* Saat fungsi dipanggil, argumen yang diberikan akan dicocokkan dengan parameter yang sesuai berdasarkan posisi atau nama.
* Argumen memberikan nilai aktual kepada parameter, sehingga parameter dapat digunakan di dalam tubuh fungsi.
* Argumen memberikan fleksibilitas dalam cara kita memanggil fungsi, memungkinkan kita untuk memberikan nilai yang berbeda-beda pada setiap pemanggilan.

Jenis-jenis Parameter :
1. **Parameter Posisional**. Parameter yang urutannya sangat penting. Saat memanggil fungsi, argumen harus diberikan dalam urutan yang sama dengan definisi parameter. Misal :
```python
def hitung_luas(panjang, lebar):
    luas = panjang * lebar
    return luas

hasil = hitung_luas(5, 3)
```
2. **Parameter Keyword**. Parameter yang dapat dipanggil dengan menggunakan nama parameternya. Urutannya tidak penting. Misal :
```python
def hitung_luas(panjang, lebar):
    luas = panjang * lebar
    return luas

hasil = hitung_luas(lebar=3, panjang=5)
```
3. **Parameter Default**. Parameter yang memiliki nilai default jika tidak diberikan nilai saat pemanggilan fungsi. Misal :
```python
def hitung_luas(panjang=1, lebar=1):
    luas = panjang * lebar
    return luas

hasil1 = hitung_luas()
hasil2 = hitung_luas(10)
hasil3 = hitung_luas(panjang=10)
hasil4 = hitung_luas(lebar=0.5)
```
4. **Parameter Variabel (Arbitrary Arguments)**. Parameter yang dapat menerima jumlah argumen yang tidak terbatas, sehingga kita dapat menulis kode yang lebih dinamis dan dapat beradaptasi dengan berbagai situasi. Python menyediakan dua cara untuk menangani parameter variabel:
    1. **`*args` (Arbitrary Positional Arguments)**. Digunakan untuk menerima sejumlah argumen posisional yang tidak diketahui jumlahnya. Argumen-argumen ini akan dikemas menjadi sebuah tuple. Misal :
        ```python
        def jumlahkan(*angka):
            total = 0
            for angka in angka:
                total += angka
            return total

        hasil = jumlahkan(1, 2, 3, 4, 5)
        print(hasil)  # Output: 15
        ```
        Sekilas penggunaan `*args` dan argumen bertipe List, Tuple, dan Set terlihat sama, karena sama-sama menampung banyak data. hanya saja jika kita menggunakan `*args`, kita langsung memberikan nilai saat memanggil fungsi, dan jika menggunakan argumen bertipe List, Tuple, dan Set, maka kita harus menyimpan datanya ke dalam variabel terlebih dahulu, lalu mengirimkannya melalu fungsi. Dalam prakteknya, pengunaan `*args` hanya ditujukan untuk akses nilai yang terkandung di dalam argumennya. Akan tetapi jika kita hendak mengubah nilai argumen yang dikirimkan di dalam fungsi, maka lebih baik menggunakan List.
    2. **`**kwargs` (Arbitrary Keyword Arguments)**. Digunakan untuk menerima sejumlah argumen keyword yang tidak diketahui jumlahnya. Argumen-argumen ini akan dikemas menjadi sebuah dictionary. Misal :
        ```python
        def buat_profil(**info):
            for kunci, nilai in info.items():
                print(kunci, ":", nilai)

        buat_profil(nama="Andi Laksono", umur=25, kota="Nganjuk", gender='Pria')
        ```
        Penggunaan `**kwargs` tidak berbeda dengan argumen bertipe Dictionary, karena sama-sama menampung data berpasangan (key dan value) sejumlah yang dibutuhkan. Tetapi tipe data dari key yang dikirimkan jika menggunakan `**kwargs` harus String, tidak seperti jika menggunakan variabel bertipe Dictionary.

    Aturan Umum penggunaan Parameter Variabel :
    1. Jika menggunakan 2 cara saat mendefinisikan fungsi, `*args` harus ditempatkan sebelum `**kwargs`. Ini karena Python akan mengumpulkan argumen posisional yang tersisa ke dalam *args sebelum mengolah argumen keyword.
    2. Argumen yang diterima oleh *args dan **kwargs akan dikemas dalam bentuk tuple dan dictionary, masing-masing. Jika Anda ingin mengakses elemen-elemennya, Anda perlu mengiterasi atau mengaksesnya sesuai dengan tipe data tersebut.
    3. Gunakan parameter variabel dengan bijak. Terlalu banyak parameter variabel dapat membuat kode menjadi kurang jelas dan sulit dipelihara.

ContohM1117.py adalah contoh penggunaan `*args` untuk menjumlahkan beberapa data
#### ContohM1117.py
```python
def jumlahkan_semua(*angka):
    """
    Menghitung jumlah dari semua angka yang diberikan.
    Args:
        *angka: Jumlah angka yang tidak terbatas.
    Returns:
        Jumlah dari semua angka.
    """
    total = 0
    for num in angka:
        total += num
    return total

berat = [80, 100, 95, 88]
nilai = (65, 77, 89, 75, 90, 60)
tinggi = {165, 169, 170, 168, 166, 160}
hasil1 = jumlahkan_semua(1, 2, 3, 4, 5)
hasil2 = jumlahkan_semua(1, 4, 9, 16, 25, 36, 49, 64, 81, 100)
hasil3 = jumlahkan_semua(*berat)
hasil4 = jumlahkan_semua(*nilai)
hasil5 = jumlahkan_semua(*tinggi)
print('Perhitungan ke-1:', hasil1)
print('Perhitungan ke-2:', hasil2)
print('Perhitungan ke-3 (berat):', hasil3)
print('Perhitungan ke-4 (nilai):', hasil4)
print('Perhitungan ke-5 (tinggi):', hasil5)
```
Operator `*` di depan berat, nilai dan tinggi disebut sebagai operator unpacking. Operator ini digunakan untuk "membuka" semua elemen dalam sebuah iterable (seperti tuple, list, atau string) dan menyebarkannya ke dalam beberapa variabel atau argumen fungsi.

ContohM1118.py adalah contoh penggunaan `*args` menghitung frekuensi angka 1 - 10 dari sekumpulan data, dan menunjukan pebedaan penggunaan `*args` (fungsi `hitung_frekuensi`) dengan argumen bertipe List (fungsi `hitung_frekuensi_list`).
#### ContohM1118.py
```python
import random
def hitung_frekuensi(*items):
    """
    Menghitung frekuensi kemunculan setiap elemen dalam sebuah iterable.
    Args:
        *items: angka-angka yang akan dicari frekuensinya.
    Returns:
        Dictionary yang berisi frekuensi setiap elemen.
    """
    frekuensi = {}
    cetak_data(items)
    for item in items:
        frekuensi[item] = frekuensi.get(item, 0) + 1
    return frekuensi

def hitung_frekuensi_list(items):
    """
    Menghitung frekuensi kemunculan setiap elemen dalam sebuah List.
    Args:
        items: List yang berisi kumpulan angka yang akan dicari frekuensinya.
    Returns:
        Dictionary yang berisi frekuensi setiap elemen.
    """
    frekuensi = {}
    items.extend([11,12,13,14,15,16,17,18,19,20])
    cetak_data(items)
    for item in items:
        frekuensi[item] = frekuensi.get(item, 0) + 1
    return frekuensi

def cetak_data(data):
    """Fungsi untuk mencetak isi dari data"""
    print('Data :')
    for idx in range(len(data)):
        if (idx+1) % 10 == 0:
            print(f'{data[idx]:>4}')
        else:
            print(f'{data[idx]:>4}', end='')
    print()

print('FREKUENSI ANGKA')
data = [random.randrange(11,21) for _ in range(30)]

hasil1 = hitung_frekuensi(3, 8, 9, 8, 10, 5, 5, 5, 2, 3, 3, 10, 1, 1, 1, 6, 7, 1, 5, 9)
hasil2 = hitung_frekuensi_list(data)

print('Frekuensi :')
for angka in range(1,11):
    print(angka,':',hasil1.get(angka,0))

print('\nFrekuensi :')
for angka in range(11,21):
    print(angka,':',hasil2.get(angka,0))
```

ContohM1119.py adalah contoh penggunaan `**kwargs` untuk menjumlahkan beberapa Membuat Profil Pengguna
#### ContohM1119.py
```python
def buat_profil(**info_pengguna):
    """
    Membuat profil pengguna berdasarkan informasi yang diberikan.
    Args:
        **info_pengguna: Informasi pengguna dalam bentuk pasangan kunci-nilai.
    Returns:
        Dictionary berisi profil pengguna.
    """
    profil = {}
    for kunci, nilai in info_pengguna.items():
        profil[kunci] = nilai
    return profil

dataku = {'nama':'Ali Santoso', 'usia':28, 'kota':'Surabaya', 'pekerjaan':'System Analysis'}
profil_ku = buat_profil(**dataku) ## tanda ** adalah operator unpacking
profil_saya = buat_profil(nama="Beni Nugroho", usia=30, kota="Jakarta", pekerjaan="Programmer")
print('Profil ke-1\n',profil_ku)
print('Profil ke-2\n',profil_saya)
```

ContohM1120.py adalah contoh penggunaan `**kwargs` untuk
#### ContohM1120.py
```python
def tampilkan_isi_kwargs(**kwargs):
    """
    Menampilkan isi dari semua pasangan kunci-nilai yang diberikan.
    Args:
        **kwargs: Kumpulan pasangan kunci-nilai yang akan ditampilkan.
    """
    print('Konten :')
    for kunci, nilai in kwargs.items():
        print(f"Kunci: {kunci}, Nilai: {nilai}")

def tampilkan_isi_dict(kwargs):
    """
    Menampilkan isi dari Dictionary yang diberikan.
    Args:
        kwargs: Dictionary yang berisi kumpulan pasangan kunci-nilai yang akan ditampilkan.
    """
    print('Konten :')
    for kunci, nilai in kwargs.items():
        print(f"Kunci: {kunci}, Nilai: {nilai}")

my_dict1 = {1: 'A', 2: 'B', 3: 'C', 4: 'D', 5: 'E'}
my_dict2 = {'1': 'a', '2': 'b', '3': 'c', '4': 'd', '5': 'e'}

print('my_dict1:')
tampilkan_isi_dict(my_dict1)
#tampilkan_isi_dict(**my_dict1)
print('my_dict2:')
tampilkan_isi_kwargs(**my_dict2)
print('my_dict3:')
#tampilkan_isi_kwargs(1='Aa', 2='Bb', 3='Cc', 4='Dd', 5='Ee')
tampilkan_isi_kwargs(k1='Aa', k2='Bb', k3='Cc', k4='Dd', k5='Ee')
```
Jika baris 26 (```tampilkan_isi_dict(**my_dict1)```) diaktifkan, maka akan memunculkan error 'keywords must be strings', karena jika menggunakan `**kwargs` maka key-nya harus berupa string, tidak bisa berupa numerik. Hal ini sama seperti jika baris ke-30 diaktifkan, maka akan memunculkan error 'Expected parameter namePylance' karena nama parameter harus diawali dengan huruf (mengikuti aturan penamaan variabel).

ContohM1121.py adalah contoh penggunaan `*args` dan `**kwargs` untuk mencetak transaksi belanja
#### ContohM1121.py
```python
harga = {'apel':5000, 'melon':15000, 'pisang':2000, 'durian':50000, 'jeruk':8000}

def format_rupiah(nominal):
    """
    Memformat angka menjadi format mata uang Rupiah Indonesia.
    Args:
        nominal (int): Jumlah uang dalam bentuk angka.
    Returns:
        str: String yang mewakili jumlah uang dalam format Rupiah Indonesia,
             dengan pemisah ribuan menggunakan titik (.) dan simbol rupiah (Rp.).
    Contoh: format_rupiah(1234567) = 'Rp. 1.234.567'
    """
    return f'Rp. {nominal:,}'.replace(',', '.')

def cetak_daftar_belanja(*barang, **banyak):
    """
    Mencetak traksaksi belanja dengan barang dan jumlah yang diberikan.
    Args:
        *barang: Nama-nama barang yang akan dibeli.
        **banyak: Jumlah masing-masing barang.
    """
    total = 0
    print('Daftar Belanja:')
    for idx in range(len(barang)):
        jumlah = banyak[barang[idx]] * harga[barang[idx]]
        total += jumlah
        print(f'{barang[idx]} : {banyak[barang[idx]]} pcs = Rp. {format_rupiah(jumlah)}')
    print(f'Total belanja {format_rupiah(total)}')

print('PAK RONI:')
cetak_daftar_belanja("apel", "pisang", "jeruk", pisang=3, apel=2, jeruk=1)
print('\PAK YOYOK:')
cetak_daftar_belanja("melon", "durian", durian=8, melon=10)
```

ContohM1122.py adalah contoh program yang menggabungkan parameter posisi, parameter default, *args, dan **kwargs untuk
#### ContohM1122.py
```python
def cetak_resep(nama_masakan, bahan_utama, *bahan_tambahan, waktu_masak=30, suhu=180, **instruksi):
    """
    Mencetak resep masakan dengan detail lengkap.
    Args:
        nama_masakan (String): Nama masakan.
        bahan_utama (String): Bahan utama masakan.
        *bahan_tambahan: Bahan-bahan tambahan lainnya.
        waktu_masak (int): Waktu memasak dalam menit (default: 30).
        suhu (int): Suhu oven dalam derajat Celcius (default: 180).
        **instruksi: Langkah-langkah memasak.
    """
    resep = f"## Resep {nama_masakan}\n\n**Bahan:**\n* {bahan_utama}"
    for bahan in bahan_tambahan:
        resep += f"\n* {bahan}"

    resep += f"\n\n**Cara Membuat:**\n"
    for langkah, detail in instruksi.items():
        resep += f"{langkah}. {detail}\n"

    resep += f"\n**Waktu Memasak:** {waktu_masak} menit\n"
    resep += f"**Suhu Oven:** {suhu} derajat Celcius"
    
    print(resep)

print('RESEP KE-1:')
cetak_resep("Kue Bolu", "Telur", "Gula", "Tepung Terigu", "Baking Powder",
            waktu_masak=45, suhu=170,
            langkah1="Kocok telur dan gula hingga mengembang",
            langkah2="Ayak tepung dan baking powder, lalu masukkan ke adonan",
            langkah3="Tuang adonan ke loyang dan panggang")
print('\nRESEP KE-2:')
cetak_resep("Sup Sayur", "Air", "Wortel", "Kentang", "Brokoli",
            waktu_masak=20,
            langkah1="Rebus air hingga mendidih",
            langkah2="Masukkan wortel dan kentang, masak hingga empuk",
            langkah3="Tambahkan brokoli, masak sebentar",
            nutrisi={'Kalori': '100 kkal', 'Protein': '5g', 'Karbohidrat': '15g'})
```

### 5. Return Value
Pada materi di atas beberapa kali disebut tentang return value. Return Value adalah nilai yang dihasilkan oleh sebuah fungsi dan dapat digunakan di bagian lain dari program. Ketika sebuah fungsi mencapai pernyataan return, eksekusi fungsi akan berhenti dan nilai yang mengikuti kata kunci return akan dikembalikan ke tempat pemanggilan fungsi. Berikut Cara kerja return value, misal :
```python
def hitung_luas(panjang, lebar):
    luas = panjang * lebar
    return luas

hasil = hitung_luas(5, 3)
print("Luas persegi panjang:", hasil)
```
1. `hitung_luas(panjang, lebar)`: Ini adalah definisi fungsi. Fungsi ini menerima dua parameter: `panjang` dan `lebar`.
2. `luas = panjang * lebar`: Di dalam fungsi, kita menghitung luas dan menyimpan hasilnya dalam variabel `luas`.
3. `return luas`: Kata kunci `return` digunakan untuk mengembalikan nilai `luas` ke tempat pemanggilan fungsi.
4.  `hasil = hitung_luas(5, 3)`: Di sini, kita memanggil fungsi dengan memberikan nilai `5` untuk `panjang` dan `3` untuk `lebar`. Hasil perhitungan (yaitu, `15`) akan disimpan dalam variabel `hasil`.

Keyword `return` juga bisa digunakan pada fungsi tanpa return value, seperti ContohM1123.py. Hal ini digunakan untuk mengakhiri eksekusi fungsi, ketika return dijalankan, eksekusi fungsi akan segera berhenti, dan nilai yang ditentukan akan dikembalikan ke tempat di mana fungsi tersebut dipanggil.
#### ContohM1123.py
```python
from random import randrange
def cari(batas, angkas):
    """
    Mencari apakah terdapat angka dalam list 'angkas' yang kurang dari 'batas'.
    Args:
        batas (int): Batas nilai yang akan dibandingkan.
        angkas (list): List of numbers to search.
    """
    for angka in angkas:
        if angka < batas:
            print('Terdapat angka yang kurang dari',batas)
            return
    print('Semua angka nilainya lebih besar atau sama dengan',batas)

data = [randrange(1,1000,10) for _ in range(20)]
batas1 = 10
batas2 = 100

print('PERIKSA DATA')
print('Data :\n',data)
print('batas1:')
cari(batas1,data)
print('batas2:')
cari(batas2,data)
```
Pada perintah `if`, Jika nilai `angka` kurang dari `batas`, maka:
* Mencetak pesan bahwa terdapat angka yang kurang dari batas.
* Mengembalikan fungsi (return). Perintah return akan langsung menghentikan eksekusi fungsi, sehingga perulangan akan berhenti dan tidak perlu memeriksa elemen-elemen selanjutnya.

Ketika `return` ditempatkan di dalam blok `if`, `if-else` atau `elif`, maka fungsi akan langsung berhenti dan mengembalikan nilai yang ditentukan jika kondisi dalam if terpenuhi. Hal ini biasa digunakan karena :
* Jika kondisi terpenuhi, tidak perlu mengecek kondisi lainnya. return langsung menghentikan fungsi. Sehingga dapat mengoptimalkan kinerja.
* Dengan return, kita dapat menghindari penggunaan variabel tambahan untuk menyimpan hasil sementara. Sehingga dapat membuat kode lebih ringkas
* Penggunaan return dalam kondisi membuat kode lebih mudah dipahami, karena setiap cabang kondisi memiliki hasil yang jelas.

Catatan penting saat menggunakan `return` di dalam blok kondisi :
* **Satu Fungsi, Satu `return` (Opsional)**: Meskipun Anda bisa memiliki beberapa `return` dalam satu fungsi, umumnya disarankan untuk memiliki satu `return` utama di akhir fungsi untuk meningkatkan keterbacaan. Hal ini opsional karena Python tidak mengharuskan Anda hanya memiliki satu return dalam sebuah fungsi. Anda bisa memiliki beberapa return di berbagai cabang if, elif, atau bahkan di luar blok kondisi.
* **`return` Tanpa Nilai**: Jika Anda ingin menghentikan fungsi tanpa mengembalikan nilai tertentu, Anda bisa menggunakan `return` tanpa diikuti oleh ekspresi apa pun. 

### 6. Return Multiple Values
Dalam pemrograman Python, fungsi secara default hanya dapat mengembalikan satu nilai. Namun, terkadang kita ingin sebuah fungsi mengembalikan beberapa hasil sekaligus. Python menyediakan cara yang elegan untuk melakukan hal ini. Terdapat 2 cara untuk mengembalikan beberapa hasil :
1. Mengembalikan Tuple
    Seperti yang telah kita ketahui bahwa Tuple adalah struktur data yang tidak dapat diubah (immutable) dan terdiri dari sekumpulan item yang diurutkan. Ketika kita ingin mengembalikan beberapa nilai dari sebuah fungsi, tuple menjadi pilihan yang sangat baik karena:
    * Membuat tuple sangat sederhana, cukup dengan memisahkan nilai-nilai dengan koma dan melampirkannya dalam kurung.
    * Tuple biasanya lebih efisien dibandingkan list karena sifatnya yang tidak dapat diubah.
    * Elemen-elemen dalam tuple dapat diakses menggunakan indeks.
2. Mengembalikan Dictionary
    Jika ingin mengembalikan hasil dalam bentuk yang lebih terstruktur, kita dapat menggunakan dictionary. Dictionary menjadi pilihan yang sangat baik karena:
    * Dictionary memungkinkan kita untuk menyimpan data dalam pasangan kunci-nilai (key-value pair), memberikan fleksibilitas dalam mengatur dan mengakses data.
    * Dengan menggunakan kunci yang deskriptif, kode menjadi lebih mudah dibaca dan dipahami.
    * Dalam satu dictionary, kita bisa mengembalikan berbagai jenis data, seperti bilangan, string, bahkan list atau dictionary lainnya.

ContohM1124.py adalah contoh fungsi yang mengembalikan Tuple, untuk menghitung Luas dan Keliling Persegi Panjang.
#### ContohM1124.py
```python
def hitung_luas_keliling_persegi_panjang(panjang, lebar):
    """
    Menghitung luas dan keliling persegi panjang.
    Args:
        panjang (int): Panjang persegi panjang.
        lebar (int): Lebar persegi panjang.
    Returns:
        tuple: Tuple berisi luas dan keliling persegi panjang.
    """
    luas = panjang * lebar
    keliling = 2 * (panjang + lebar)
    return luas, keliling

print('LUAS DAN KELILING PERSEGI PANJANG')
panjang_pp = int(input('Panjang :'))
lebar_pp = int(input('Lebar :'))
luas, keliling = hitung_luas_keliling_persegi_panjang(panjang_pp, lebar_pp)
print(f"Luas: {luas}\nKeliling: {keliling}")
```
![Gambar 2](https://www.triangle-calculator.com/images/triangle_ABC_angles.gif)<br>Gambar 2. Segitiga ABC.
ContohM1125.py adalah contoh fungsi yang mengembalikan Tuple, untuk menghitung besar sudut segitiga ABC (Gambar 2).
#### ContohM1125.py
```python
import math
def cek_sisi_segitiga(sisi_a, sisi_b, sisi_c):
    """
    Memeriksa apakah tiga sisi dapat membentuk sebuah segitiga.
    Args:
        sisi_a: Panjang sisi a.
        sisi_b: Panjang sisi b.
        sisi_c: Panjang sisi c.
    Returns:
        bool: Mengembalikan `True` jika ketiga sisi tidak dapat membentuk segitiga (salah satu sisi lebih panjang dari jumlah dua sisi lainnya), dan `False` jika ketiga sisi dapat membentuk segitiga.
    """
    return sisi_a + sisi_b <= sisi_c or \
        sisi_a + sisi_c <= sisi_b or \
        sisi_b + sisi_c <= sisi_a

def hitung_sudut_segitiga(sisi_a, sisi_b, sisi_c):
    """
    Hitung besar sudut-sudut segitiga menggunakan hukum cosinus.
    Args:
        sisi_a: Panjang sisi a.
        sisi_b: Panjang sisi b.
        sisi_c: Panjang sisi c.
    Returns:
        tuple: Tuple berisi besar sudut A, B, dan C dalam derajat.
    """
    cos_A = (sisi_b**2 + sisi_c**2 - sisi_a**2) / (2 * sisi_b * sisi_c)
    sudut_A = math.degrees(math.acos(cos_A))

    cos_B = (sisi_a**2 + sisi_c**2 - sisi_b**2) / (2 * sisi_a * sisi_c)
    sudut_B = math.degrees(math.acos(cos_B))

    sudut_C = 180 - sudut_A - sudut_B

    return sudut_A, sudut_B, sudut_C
    
if __name__ == '__main__' :
    print('HITUNG BESAR SUDUT SEGITIGA')
    sisi_a = float(input('Panjang sisi a:'))
    sisi_b = float(input('Panjang sisi b:'))
    sisi_c = float(input('Panjang sisi c:'))
    if cek_sisi_segitiga(sisi_a, sisi_b, sisi_c):
        print("Bukan Segitiga, karena ketiga sisi tidak dapat membentuk segitiga")
    else:
        sudut_A, sudut_B, sudut_C = hitung_sudut_segitiga(sisi_a, sisi_b, sisi_c)
        print(f"Sudut A: {sudut_A:.2f}°, Sudut B: {sudut_B:.2f}°, Sudut C: {sudut_C:.2f}°") 
```

ContohM1126.py adalah contoh fungsi yang mengembalikan Tuple, untuk menghitung Mean, Median, Modus, Kuartil 1, Kuartil 2 dan Kuartil 3 dari suatu data acak.
#### ContohM1126.py
```python
import random

def hitung_statistika(data):
    """
    Hitung mean, median, modus, kuartil 1 (Q1), kuartil 2 (Q2), dan kuartil 3 (Q3) dari sekumpulan data.
    Args:
        data: List of numbers.
    Returns:
        tuple: Tuple berisi mean, median, modus, Q1, Q2, dan Q3.
    """
    data.sort()
    print('Data setelah diurutkan:')
    cetak_data(data)
    n = len(data)

    mean = sum(data) / n

    if n % 2 == 0:
        median = (data[n//2] + data[n//2 - 1]) / 2
    else:
        median = data[n//2]

    modus = max_count = 0
    for num in data:
        count = data.count(num)
        if count > max_count:
            max_count = count
            modus = num

    Q1 = data[n//4]
    Q2 = median
    Q3 = data[3*n//4]

    return mean, median, modus, Q1, Q2, Q3

def cetak_data(data):
    """Fungsi untuk mencetak isi dari data"""
    for idx in range(len(data)):
        if (idx+1) % 10 == 0:
            print(f'{data[idx]:>3}')
        else:
            print(f'{data[idx]:>3}', end='')
    print()

if __name__ == '__main__' :
    print('HITUNG MEAN, MEDIAN, MODUS, Q1, Q2 & Q3')
    banyak = int(input("Masukkan banyak data: "))
    data = [random.randint(1, 11) for _ in range(banyak)]
    print("Data:")
    cetak_data(data)

    hasil = hitung_statistika(data)
    print(f"Mean: {hasil[0]:.2f}")
    print(f"Median: {hasil[1]:.2f}")
    print(f"Modus: {hasil[2]}")
    print(f"Q1: {hasil[3]}")
    print(f"Q2: {hasil[4]}")
    print(f"Q3: {hasil[5]}")
```

ContohM1127.py adalah contoh fungsi yang mengembalikan Tuple, untuk konversi suhu.
#### ContohM1127.py
```python
satuan_suhu = ('°C','°F','°R','K')
def celcius_ke_semua(celsius):
    """
    Mengkonversi suhu dari Celcius ke Reamur, Fahrenheit, dan Kelvin.
    Args:
        celsius: Suhu dalam Celcius.
    Returns:
        tuple: Tuple berisi suhu dalam Reamur, Fahrenheit, dan Kelvin secara berurutan.
    """
    reamur = celsius * 4/5
    fahrenheit = (celsius * 9/5) + 32
    kelvin = celsius + 273.15
    return 0, reamur, 2, fahrenheit, 1, kelvin, 3

def reamur_ke_semua(reamur):
    """
    Mengkonversi suhu dari Reamur ke Celcius, Fahrenheit, dan Kelvin.
    Args:
        reamur: Suhu dalam Reamur.
    Returns:
        tuple: Tuple berisi suhu dalam Celcius, Fahrenheit, dan Kelvin secara berurutan.
    """
    celcius = reamur * 5/4
    fahrenheit = (reamur * 9/4) + 32
    kelvin = (reamur * 5/4) + 273.15
    return 2, celcius, 0, fahrenheit, 1, kelvin, 3

def fahrenheit_ke_semua(fahrenheit):
    """
    Mengkonversi suhu dari Fahrenheit ke Celcius, Reamur, dan Kelvin.
    Args:
        fahrenheit: Suhu dalam Fahrenheit.
    Returns:
        tuple: Tuple berisi suhu dalam Celcius, Reamur, dan Kelvin secara berurutan.
    """
    celcius = (fahrenheit - 32) * 5/9
    reamur = (fahrenheit - 32) * 4/9
    kelvin = (fahrenheit + 459.67) * 5/9
    return 1, celcius, 0, reamur, 2, kelvin, 3

def kelvin_ke_semua(kelvin):
    """
    Mengkonversi suhu dari Kelvin ke Celcius, Reamur, dan Fahrenheit.
    Args:
        kelvin: Suhu dalam Kelvin.
    Returns:
        tuple: Tuple berisi suhu dalam Celcius, Reamur, dan Fahrenheit secara berurutan.
    """
    celcius = kelvin - 273.15
    reamur = (kelvin - 273.15) * 4/5
    fahrenheit = (kelvin * 9/5) - 459.67
    return 3, celcius, 0, reamur, 2, fahrenheit, 1

def validasi_satuan_suhu(satuan):
    """
    Memvalidasi apakah satuan suhu yang diberikan valid.
    Args:
        satuan: Satuan suhu yang akan divalidasi (C, F, R, atau K).
    Returns:
        bool: True jika satuan valid, False jika tidak valid.
    """    
    return satuan.upper() in ['C', 'F', 'R', 'K']

def konversi_suhu(nilai_suhu, satuan_awal):
    """
    Mengkonversi suhu dari satu satuan ke semua satuan lainnya.
    Args:
        nilai_suhu: Nilai suhu yang akan dikonversi.
        satuan_awal: Satuan suhu awal (C, F, R, atau K).
    Returns:
        tuple: Tuple berisi suhu dalam semua satuan jika berhasil, atau pesan kesalahan jika tidak valid.
    """
    match satuan_awal:
        case 'C': 
            return celcius_ke_semua(nilai_suhu)
        case 'R':
            return reamur_ke_semua(nilai_suhu)
        case 'F':
            return fahrenheit_ke_semua(nilai_suhu)
        case _:
            return kelvin_ke_semua(nilai_suhu)

if __name__ == '__main__' :
    print('KONVERSI SUHU')
    suhu = float(input("Masukkan nilai suhu: "))
    satuan = input("Masukkan satuan suhu awal (C, F, R, K): ").upper()
    while not validasi_satuan_suhu(satuan):
        print('Satuan tidak dikenal, silakan ulangi lagi')
        satuan = input("Masukkan satuan suhu awal (C, F, R, K): ").upper()
        
    hasil = konversi_suhu(suhu, satuan)

    print(f"{suhu} {satuan_suhu[hasil[0]]} setara dengan:")
    print(f"- {hasil[1]:.2f} {satuan_suhu[hasil[2]]}")
    print(f"- {hasil[3]:.2f} {satuan_suhu[hasil[4]]}")
    print(f"- {hasil[5]:.2f} {satuan_suhu[hasil[6]]}")
```

ContohM1128.py adalah contoh fungsi yang mengembalikan Dictionary, untuk membuat distribusi frekuensi dari data acak.
#### ContohM1128.py
```python
from random import randint
from math import log10

def buat_distribusi_frekuensi(data, jumlah_data):
    """
    Membuat distribusi frekuensi dari data yang diberikan.
    Args:
        data: data yang akan diproses.
        jumlah_data: Jumlah data.
    Returns:
        dict: Kamus dengan batas bawah kelas sebagai key dan frekuensi sebagai value.
    """
    rentang = max(data) - min(data)
    jumlah_kelas = round(1 + 3.322 * log10(jumlah_data))
    lebar_kelas = rentang // jumlah_kelas
    frekuensi = {}
    batas_bawah = min(data)

    for i in range(jumlah_kelas):
        batas_atas = batas_bawah + lebar_kelas
        frekuensi[f"{batas_bawah:>2} - {batas_atas:>2}"] = len([x for x in data if batas_bawah <= x < batas_atas])
        batas_bawah = batas_atas

    return frekuensi

banyak = int(input("Masukkan banyak data: "))
data = [randint(1, 101) for _ in range(banyak)]

distribusi = buat_distribusi_frekuensi(data, banyak)
print("Distribusi Frekuensi:")
for kelas, frekuensi in distribusi.items():
    print(f"{kelas}: {frekuensi}")
```

ContohM1129.py adalah contoh fungsi yang mengembalikan Dictionary, modifikasi dari ContohM1125.py.
#### ContohM1129.py
```python
from math import degrees, acos
from ContohM1125 import cek_sisi_segitiga

def hitung_sudut_segitiga(sisi_a, sisi_b, sisi_c):
    """
    Hitung besar sudut-sudut segitiga menggunakan hukum cosinus.
    Args:
        sisi_a: Panjang sisi a.
        sisi_b: Panjang sisi b.
        sisi_c: Panjang sisi c.
    Returns:
        Dictionary: Dictionary berisi besar sudut A, B, dan C dalam derajat.
    """
    cos_A = (sisi_b**2 + sisi_c**2 - sisi_a**2) / (2 * sisi_b * sisi_c)
    sudut_A = degrees(acos(cos_A))

    cos_B = (sisi_a**2 + sisi_c**2 - sisi_b**2) / (2 * sisi_a * sisi_c)
    sudut_B = degrees(acos(cos_B))

    sudut_C = 180 - sudut_A - sudut_B

    return {'sudut_A': sudut_A, 'sudut_B': sudut_B, 'sudut_C': sudut_C}

print('HITUNG BESAR SUDUT SEGITIGA')
sisi_a = float(input('Panjang sisi a:'))
sisi_b = float(input('Panjang sisi b:'))
sisi_c = float(input('Panjang sisi c:'))
if cek_sisi_segitiga(sisi_a, sisi_b, sisi_c):
    print("Bukan Segitiga, karena ketiga sisi tidak dapat membentuk segitiga")
else:
    hasil = hitung_sudut_segitiga(sisi_a, sisi_b, sisi_c)
    print(f"Sudut A: {hasil['sudut_A']:.2f}°, Sudut B: {hasil['sudut_B']:.2f}°, Sudut C: {hasil['sudut_C']:.2f}°")
```

ContohM1130.py adalah contoh fungsi yang mengembalikan Dictionary, modifikasi dari ContohM1126.py.
#### ContohM1130.py
```python
from random import randint
from ContohM1126 import cetak_data
def hitung_statistika(data):
    """
    Hitung mean, median, modus, kuartil 1 (Q1), kuartil 2 (Q2), dan kuartil 3 (Q3) dari sekumpulan data.
    Args:
        data: List of numbers.
    Returns:
        Dictionary: Dictionary berisi mean, median, modus, Q1, Q2, dan Q3.
    """
    data.sort()
    print('Data setelah diurutkan:')
    cetak_data(data)
    n = len(data)

    mean = sum(data) / n

    if n % 2 == 0:
        median = (data[n//2] + data[n//2 - 1]) / 2
    else:
        median = data[n//2]

    modus = max_count = 0
    for num in data:
        count = data.count(num)
        if count > max_count:
            max_count = count
            modus = num

    Q1 = data[n//4]
    Q2 = median
    Q3 = data[3*n//4]

    return {'mean':mean, 'median':median, 'modus':modus, 'q1':Q1, 'q2':Q2, 'q3':Q3}

print('HITUNG MEAN, MEDIAN, MODUS, Q1, Q2 & Q3')
banyak = int(input("Masukkan banyak data: "))
data = [randint(1, 11) for _ in range(banyak)]
print("Data:")
cetak_data(data)

hasil = hitung_statistika(data)
print(f"Mean: {hasil['mean']:.2f}")
print(f"Median: {hasil['median']:.2f}")
print(f"Modus: {hasil['modus']}")
print(f"Q1: {hasil['q1']}")
print(f"Q2: {hasil['q2']}")
print(f"Q3: {hasil['q3']}")
```

ContohM1131.py adalah contoh fungsi yang mengembalikan Dictionary, modifikasi dari ContohM1127.py
#### ContohM1131.py
```python
from ContohM1127 import validasi_satuan_suhu
satuan_suhu = {"Celcius":'°C',"Fahrenheit":'°F',"Reamur":'°R',"Kelvin":'K'}
def celcius_ke_semua(celcius):
    """
    Mengkonversi suhu dari Celcius ke Fahrenheit, Kelvin, dan Reamur.
    Args:
        celcius: Suhu dalam Celcius.
    Returns:
        dict: Kamus berisi suhu dalam Fahrenheit, Kelvin, dan Reamur.
    """
    fahrenheit = (celcius * 9/5) + 32
    kelvin = celcius + 273.15
    reamur = celcius * 4/5
    return {"Fahrenheit": fahrenheit, "Kelvin": kelvin, "Reamur": reamur}

def fahrenheit_ke_semua(fahrenheit):
    """
    Mengkonversi suhu dari Fahrenheit ke Celcius, Kelvin, dan Reamur.
    Args:
        fahrenheit: Suhu dalam Fahrenheit.
    Returns:
        dict: Kamus berisi suhu dalam Celcius, Kelvin, dan Reamur.
    """
    celcius = (fahrenheit - 32) * 5/9
    kelvin = (fahrenheit + 459.67) * 5/9
    reamur = (fahrenheit - 32) * 4/9
    return {"Celcius": celcius, "Kelvin": kelvin, "Reamur": reamur}

def reamur_ke_semua(reamur):
    """
    Mengkonversi suhu dari Reamur ke Celcius, Fahrenheit, dan Kelvin.
    Args:
        reamur: Suhu dalam Reamur.
    Returns:
        dict: Kamus berisi suhu dalam Celcius, Fahrenheit, dan Kelvin.
    """
    celcius = reamur * 5/4
    fahrenheit = (reamur * 9/4) + 32
    kelvin = (reamur * 5/4) + 273.15
    return {"Celcius": celcius, "Fahrenheit": fahrenheit, "Kelvin": kelvin}

def kelvin_ke_semua(kelvin):
    """
    Mengkonversi suhu dari Kelvin ke Celcius, Fahrenheit, dan Reamur.
    Args:
        kelvin: Suhu dalam Kelvin.
    Returns:
        dict: Kamus berisi suhu dalam Celcius, Fahrenheit, dan Reamur.
    """
    celcius = kelvin - 273.15
    fahrenheit = (kelvin * 9/5) - 459.67
    reamur = (kelvin - 273.15) * 4/5
    return {"Celcius": celcius, "Fahrenheit": fahrenheit, "Reamur": reamur}

def konversi_suhu(nilai_suhu, satuan_awal):
    """
    Mengkonversi suhu dari satu satuan ke semua satuan lainnya.
    Args:
        nilai_suhu: Nilai suhu yang akan dikonversi.
        satuan_awal: Satuan suhu awal (C, F, R, atau K).
    Returns:
        dict: Dictionary berisi suhu dalam semua satuan jika berhasil, atau pesan kesalahan jika tidak valid.
    """
    match satuan_awal:
        case 'C': 
            return celcius_ke_semua(nilai_suhu)
        case 'R':
            return reamur_ke_semua(nilai_suhu)
        case 'F':
            return fahrenheit_ke_semua(nilai_suhu)
        case _:
            return kelvin_ke_semua(nilai_suhu)

print('KONVERSI SUHU')
suhu = float(input("Masukkan nilai suhu: "))
satuan = input("Masukkan satuan suhu awal (C/F/R/K): ").upper()
hasil_konversi = konversi_suhu(suhu, satuan)

print("Hasil konversi:")
for satuan, nilai in hasil_konversi.items():
    print(f"{satuan.capitalize()}: {nilai:.2f} {satuan_suhu[satuan]}")
```

ContohM1132.py adalah contoh fungsi yang mengembalikan Dictionary, untuk menghitung nilai performa klasifikasi data. ([Sumber materi](https://socs.binus.ac.id/2020/11/01/confusion-matrix/))
#### ContohM1132.py
```python
from random import randint
def hitung_metrik(y_true, y_pred):
    """
    Fungsi untuk menghitung metrik evaluasi klasifikasi.
    Args:
        y_true: Array berisi label sebenarnya.
        y_pred: Array berisi prediksi model.
    Returns:
        dict: Kamus berisi nilai TP, FP, FN, TN, akurasi, presisi, sensitivity, dan specificity.
    """
    n = len(y_true)
    tp = sum([1 for i in range(n) if y_true[i] == 1 and y_pred[i] == 1])
    fp = sum([1 for i in range(n) if y_true[i] == 0 and y_pred[i] == 1])
    fn = sum([1 for i in range(n) if y_true[i] == 1 and y_pred[i] == 0])
    tn = sum([1 for i in range(n) if y_true[i] == 0 and y_pred[i] == 0])

    accuracy = (tp + tn) / (tp + fp + fn + tn)
    precision = tp / (tp + fp)
    sensitivity = tp / (tp + fn)
    specificity = tn / (tn + fp)

    return {
        'TP': tp, 'FP': fp, 'FN': fn, 'TN': tn,
        'Accuracy': accuracy, 'Precision': precision,
        'Sensitivity': sensitivity, 'Specificity': specificity
    }

print('PERFORMA KLASIFIKASI BINER')
y_true = [randint(0, 1) for _ in range(20)]
y_pred = [randint(0, 1) for _ in range(20)]

print('y_true:', y_true)
print('y_pred:', y_pred)
hasil = hitung_metrik(y_true, y_pred)
for label, nilai in hasil.items():
    print(f"{label}: {nilai}")
```

### 7. Pass by Reference dan Pass by Value
Ketika kita mengirimkan argumen ke sebuah fungsi dalam Python, ada dua cara utama bagaimana Python menangani argumen tersebut:
* **Pass by value**: mekanisme di mana **nilai** dari sebuah variabel dikopi dan dikirimkan ke fungsi. Perubahan pada argumen di dalam fungsi tidak akan mempengaruhi nilai variabel asli di luar fungsi. Tipe data dari argumennya adalah Tipe data primitif (immutable): Seperti int, float, string, tuple. Ketika kita mengirimkan variabel bertipe data primitif ke sebuah fungsi, yang sebenarnya dikirimkan adalah nilai kopian dari variabel tersebut. Jadi, perubahan di dalam fungsi tidak akan mempengaruhi variabel asli.
* **Pass by reference**: mekanisme di mana **referensi** ke sebuah objek (bukan nilai kopiannya) dikirimkan ke fungsi. Perubahan pada argumen di dalam fungsi akan juga mengubah objek asli di luar fungsi. Tipe data dari argumennya adalah Tipe data non-primitif (mutable): Seperti List, Dictionary dan Set. Ketika kita mengirimkan variabel bertipe data non-primitif ke sebuah fungsi, yang sebenarnya dikirimkan adalah referensi ke objek tersebut. Jadi, perubahan pada objek di dalam fungsi akan juga mengubah objek asli di luar fungsi.

ContohM1133.py adalah contoh program untuk membedakan Pass by Reference dan Pass by Value
#### ContohM1133.py
```python
def tambah_angka(angka):
    """
    Fungsi ini menambahkan 5 ke angka yang diberikan.
    Args:
        angka: Angka yang akan ditambah.
    """
    angka += 5
    print("Nilai angka di dalam fungsi:", angka)

def tambah_elemen(daftar):
    """
    Fungsi ini menambahkan elemen 'apel' ke dalam daftar yang diberikan.
    Args:
        daftar: Daftar yang akan ditambahkan elemennya.
    """
    daftar.append('apel')
    print("Daftar di dalam fungsi:", daftar)

# Memanggil fungsi
bilangan = 10
print("Nilai bilangan sebelum fungsi dipanggil:", bilangan)
tambah_angka(bilangan)
print("Nilai bilangan setelah fungsi dipanggil:", bilangan)

# Memanggil fungsi
buah = ['pisang', 'mangga', 'jambu', 'melon', 'jeruk']
print("\nDaftar buah sebelum fungsi dipanggil:", buah)
tambah_elemen(buah)
print("Daftar buah setelah fungsi dipanggil:", buah)
```

Supaya argumen yang dikirim dengan cara Pass by Reference nilainya tidak berubah setelah keluar dari fungsi, maka kita dapat menggunakan teknik Shallow Copy atau Deep Copy.
1. Shallow Copy: membuat salinan baru dari sebuah objek, tetapi elemen-elemen di dalam objek tersebut masih merujuk ke objek asli (Gambar 3). Artinya, jika kita mengubah elemen di dalam salinan, perubahan tersebut juga akan berdampak pada objek asli. Shallow Copy baik digunakan ketika kita ingin membuat salinan cepat dan tidak perlu khawatir tentang perubahan pada elemen-elemen di dalam objek. Atau ketika objek yang kita salin relatif kecil dan tidak memiliki struktur yang terlalu kompleks. Dalam python, ini diimplementasikan menggunakan fungsi `copy()`. 
2. Deep Copy: membuat salinan baru dari sebuah objek, termasuk semua elemen di dalamnya secara rekursif (Gambar 4). Dengan kata lain, setiap elemen dari objek asli akan diduplikasi, sehingga salinan yang dihasilkan benar-benar independen. Deep Copy baik dgunakan ketika kita ingin membuat salinan yang benar-benar independen dari objek asli. Atau ketika objek yang kita salin memiliki struktur yang kompleks dan kita ingin menghindari perubahan yang tidak diinginkan pada objek asli. Dalam python, ini diimplementasikan menggunakan fungsi `deepcopy()`. 

|![Gambar 3](https://media.geeksforgeeks.org/wp-content/uploads/shallow-copy.jpg)<br>Gambar 3. Ilustrasi Shallow Copy|![Gambar 4](https://media.geeksforgeeks.org/wp-content/uploads/deep-copy.jpg)<br>Gambar 4. Ilustrasi Deep Copy|
|-|-|

ContohM1134.py adalah contoh program untuk membedakan Shallow Copy dan Deep Copy.
#### ContohM1134.py
```python
import copy

def shallow_copy_example(original_list):
    """
    Fungsi ini menunjukkan contoh Shallow Copy pada list.
    Args:
        original_list: List yang akan dijadikan objek untuk shallow copy.
    """
    copied_list = copy.copy(original_list)
    print("Original list:", original_list)
    print("Copied list (shallow):", copied_list)

    # Modifikasi elemen dalam list bersarang
    copied_list[2][0] = 99
    print("Setelah modifikasi:")
    print("Original list:", original_list)
    print("Copied list (shallow):", copied_list)

def deep_copy_example(original_list):
    """
    Fungsi ini menunjukkan contoh Deep Copy pada list.
    Args:
        original_list: List yang akan dijadikan objek untuk deep copy.
    """
    copied_list = copy.deepcopy(original_list)
    print("Original list:", original_list)
    print("Copied list (deep):", copied_list)

    # Modifikasi elemen dalam list bersarang
    copied_list[2][0] = 99
    print("Setelah modifikasi:")
    print("Original list:", original_list)
    print("Copied list (deep):", copied_list)

dataku1 = [1, 2, [3, 4]]
dataku2 = [1, 2, [3, 4]]
print("Shallow Copy:")
shallow_copy_example(dataku1)

print("\nDeep Copy:")
deep_copy_example(dataku2)
```

ContohM1135.py adalah contoh program untuk menggunakan Shallow Copy, untuk menyalin konfigurasi aplikasi.
#### ContohM1135.py
```python
import copy

def buat_konfigurasi(nama_aplikasi, database, server):
    """
    Membuat konfigurasi aplikasi dalam bentuk dictionary.
    Args:
        nama_aplikasi: Nama aplikasi.
        database: Informasi database.
        server: Informasi server.
    Returns:
        Dictionary yang berisi konfigurasi aplikasi.
    """
    return {'nama': nama_aplikasi, 'database': database, 'server': server}

def salin_konfigurasi(konfigurasi):
    """
    Menyalin konfigurasi aplikasi untuk lingkungan pengembangan.
    Args:
        konfigurasi: Konfigurasi aplikasi asli.
    """
    # Shallow copy cukup untuk sebagian besar konfigurasi
    konfigurasi_dev = konfigurasi.copy()
    konfigurasi_dev['database']['host'] = 'localhost'  # Ubah host database untuk pengembangan

    print("Konfigurasi asli:")
    print(konfigurasi)

    print("Konfigurasi pengembangan:")
    print(konfigurasi_dev)

# Contoh penggunaan
config = buat_konfigurasi("MyApp", {'host': 'prod.db.com', 'port': 3306}, 'prod.server.com')
print('konfigurasi awal:')
print(config)
salin_konfigurasi(config)
```

ContohM1136.py adalah contoh program untuk menggunakan Deep Copy, untuk Menyalin Data Mahasiswa.
#### ContohM1136.py
```python
import copy

def buat_mahasiswa(nama, nim, nilai):
    """
    Membuat data mahasiswa dalam bentuk dictionary.
    Args:
        nama: Nama mahasiswa.
        nim: Nomor induk mahasiswa.
        nilai: Daftar nilai mahasiswa.
    Returns:
        Dictionary yang berisi data mahasiswa.
    """
    return {'nama': nama, 'nim': nim, 'nilai': nilai}

def salin_data_mahasiswa(mahasiswa):
    """
    Menyalin data mahasiswa untuk analisis lebih lanjut.
    Args:
        mahasiswa: Data mahasiswa asli.
    """
    # Deep copy untuk menghindari perubahan pada data asli
    mahasiswa_salinan = copy.deepcopy(mahasiswa)

    # Simulasi analisis: mengubah nilai rata-rata
    total_nilai = sum(mahasiswa_salinan['nilai'])
    rata_rata = total_nilai / len(mahasiswa_salinan['nilai'])
    mahasiswa_salinan['nilai'].append(rata_rata)

    print("Data mahasiswa asli:")
    print(mahasiswa)

    print("Data mahasiswa salinan (dengan nilai rata-rata):")
    print(mahasiswa_salinan)

# Contoh penggunaan
andi = buat_mahasiswa("Andi", '12345', [80, 90, 76])
print("Data mahasiswa awal:")
print(andi)
salin_data_mahasiswa(andi)
```

|[# Awal](../README.md)<br>[# Materi Sebelumnya](../M10/README.md)<br>[# Materi Berikutnya](../M12/README.md)|
|-|