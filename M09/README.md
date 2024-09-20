# STRUKTUR KONTROL
## Percabangan (Conditional Statements)
### 1. Statement `if`
Pernyataan if adalah salah satu struktur kontrol paling dasar dalam pemrograman Python. Ia digunakan untuk membuat keputusan berdasarkan suatu kondisi. Jika kondisi tersebut bernilai `True`, maka kode di dalam blok if akan dijalankan. Jika kondisi bernilai `False`, maka kode tersebut akan dilewati. Gambar 1 adalah Diagram Alir Statement `if`.

![Gambar 1](img/Screenshot01.png)<br>Gambar 1. Diagram Alir Statement `if`

Sintaks Dasar:
```python
if kondisi:
    # Kode yang akan dijalankan jika kondisi benar
```
Misal :
```python
umur = 18
if umur >= 17:
    print("Anda sudah cukup umur untuk memiliki SIM.")
```
Cara Kerja:
1. **Evaluasi Kondisi**: Python akan mengevaluasi ekspresi di dalam kurung setelah kata kunci `if`. Ekspresi ini harus menghasilkan nilai boolean (`True` atau `False`).
2. **Eksekusi Blok Kode**: Jika hasil evaluasi adalah `True`, Python akan menjalankan semua pernyataan yang ada di dalam blok kode yang mengikuti `if`. Blok kode ini ditandai dengan indentasi (biasanya 4 spasi).
3. **Lewati Blok Kode**: Jika hasil evaluasi adalah `False`, Python akan langsung melewati blok kode di dalam `if` dan melanjutkan ke baris kode berikutnya.

Indentasi adalah penambahan spasi di awal baris kode. Dalam Python, indentasi digunakan untuk menunjukkan hirarki atau tingkatan dalam kode. Blok kode yang memiliki tingkat indentasi yang sama dianggap sebagai bagian dari blok kode yang sama. Aturan Indentasi di Python
- Konsisten: Gunakan jumlah spasi yang sama untuk setiap tingkat indentasi. Umumnya, 4 spasi adalah standar yang paling umum digunakan.
- Tab vs Spasi: Sebaiknya hindari mencampurkan tab dan spasi dalam satu file. Pilih salah satu dan gunakan secara konsisten.
- Editor Teks: Sebagian besar editor teks modern memiliki fitur otomatis untuk indentasi. Manfaatkan fitur ini untuk menjaga konsistensi indentasi.

Kesalahan Umum Terkait Indentasi
- Indentasi Tidak Konsisten: Menggunakan jumlah spasi yang berbeda untuk tingkat indentasi yang sama dapat menyebabkan IndentationError.
- Lupa Menutup Blok: Jika lupa menutup sebuah blok dengan mengurangi indentasi, Python akan menganggap baris berikutnya masih bagian dari blok sebelumnya.

ContohM0801.py adalah contoh penggunaan statement `if` untuk mengecek Bilangan Genap.
##### ContohM0801.py
```python
angka = int(input("Masukkan sebuah angka: "))
if angka % 2 == 0:
    print(angka, "adalah bilangan genap.")
```
ContohM0802.py adalah contoh penggunaan statement `if` untuk memeriksa Nilai Ujian.
##### ContohM0802.py
```python
nilai = int(input("Masukkan nilai ujian: "))
if nilai >= 80:
    print("Selamat, Anda mendapatkan nilai A!")
```
ContohM0803.py adalah contoh penggunaan statement `if` untuk mengecek Karakter Vokal.
##### ContohM0803.py
```python
karakter = input("Masukkan sebuah karakter: ")
if karakter in 'aiueoAIUEO':
    print(karakter, "adalah huruf vokal.")
```
ContohM0804.py adalah contoh penggunaan statement `if` untuk memeriksa kesesuaian Username dan Password.
##### ContohM0804.py
```python
username_benar = "admin"
password_benar = "rahasia123"
username = input("Masukkan username: ")
password = input("Masukkan password: ")
if username == username_benar and password == password_benar:
    print("Login berhasil!")
```
ContohM0805.py adalah contoh penggunaan statement `if` untuk memeriksa Jenis Segitiga Sama Sisi.
##### ContohM0805.py
```python
sisi_a = 5
sisi_b = 5
sisi_c = 5
if sisi_a == sisi_b and sisi_b == sisi_c:
    print("Segitiga sama sisi.")
```
ContohM0806.py adalah contoh penggunaan statement `if` untuk memeriksa Jenis Segitiga.
##### ContohM0806.py
```python
sisi_a = 5
sisi_b = 5
sisi_c = 5
if sisi_a == sisi_b and sisi_b == sisi_c:
    print("Segitiga sama sisi.")
if sisi_a == sisi_b or sisi_b == sisi_c or sisi_a == sisi_c:
    print("Segitiga sama kaki.")
if sisi_a != sisi_b and sisi_b != sisi_c and sisi_a != sisi_c:
    print("Segitiga sembarang.")
```
ContohM0807.py adalah contoh penggunaan statement `if` untuk memeriksa Kelulusan dengan Bobot Nilai, Kehadiran, dan Tugas Tambahan.
##### ContohM0807.py
```python
nilai_tugas = 85
nilai_uts = 70
nilai_uas = 90
persentase_kehadiran = 95
tugas_tambahan = True
if nilai_tugas >= 75 and nilai_uts >= 70 and nilai_uas >= 80 and persentase_kehadiran >= 80 and tugas_tambahan:
    print("Selamat, Anda lulus!")
```

### 2. Statement `else`
`else` adalah sebuah kata kunci dalam Python yang digunakan bersama dengan `if` untuk menentukan blok kode yang akan dijalankan jika kondisi dalam `if` bernilai `False`. Sederhananya, else menyediakan opsi alternatif ketika kondisi utama tidak terpenuhi. Gambar 2 adalah Diagram Alir Statement `if` dan `else`.

![Gambar 2](img/Screenshot02.png)<br>Gambar 2. Diagram Alir Statement `if` dan `else`
Sintaks Dasar:
```python
if kondisi:
    # Blok kode yang dijalankan jika kondisi True
else:
    # Blok kode yang dijalankan jika kondisi False
```
Misal :
```python
umur = 17
if umur >= 18:
    print("Anda sudah dewasa.")
else:
    print("Anda belum dewasa.")
```

Cara Kerja:
1. Evaluasi Kondisi: Python akan mengevaluasi kondisi yang diberikan setelah kata kunci if.
2. Eksekusi Blok Kode:
    1. Jika kondisi bernilai True, maka blok kode di dalam if akan dijalankan, dan blok kode di dalam else akan dilewati.
    2. Jika kondisi bernilai False, maka blok kode di dalam if akan dilewati, dan blok kode di dalam else akan dijalankan.

ContohM0808.py adalah contoh penggunaan statement `if ... else` untuk memeriksa Bilangan Genap atau Ganjil.
##### ContohM0808.py
```python
bilangan = int(input("Masukkan bilangan: "))

if bilangan % 2 == 0:
    print("Bilangan genap")
else:
    print("Bilangan ganjil")
```
ContohM0809.py adalah contoh penggunaan statement `if ... else` untuk memeriksa apakah suatu huruf adalah vokal atau konsonan.
##### ContohM0809.py
```python
huruf = input("Masukkan sebuah huruf: ")
vokal = 'aiueo'

if huruf.lower() in vokal:
    print(huruf, "adalah huruf vokal.")
else:
    print(huruf, "adalah huruf konsonan.")
```
ContohM0810.py adalah contoh penggunaan statement `if ... else` untuk memeriksa apakah suatu hari adalah hari kerja.
##### ContohM0810.py
```python
hari = input("Masukkan hari (Senin, Selasa, ...): ")
hari_kerja = ["Senin", "Selasa", "Rabu", "Kamis", "Jumat"]

if hari.title() in hari_kerja:
    print(hari, "adalah hari kerja.")
else:
    print(hari, "adalah hari libur.")
```
ContohM0811.py adalah contoh penggunaan statement `if ... else` untuk memeriksa Tahun Kabisat atau bukan.
##### ContohM0811.py
```python
tahun = int(input("Masukkan tahun: "))

if (tahun % 4 == 0 and tahun % 100 != 0) or tahun % 400 == 0:
    print(tahun, "adalah tahun kabisat")
else:
    print(tahun, "bukan tahun kabisat")
```
ContohM0812.py adalah contoh penggunaan statement `if ... else` untuk memeriksa Jenis Segitiga, Panjang Sisi, dan Sudut.
##### ContohM0812.py
```python
sisi_a = 5
sisi_b = 5
sisi_c = 5
sudut_terbesar = 90

if sisi_a == sisi_b and sisi_b == sisi_c and sisi_a > 5 and sudut_terbesar == 90:
    print("Segitiga sama sisi siku-siku dengan sisi lebih dari 5.")
else:
    print("Bukan segitiga yang memenuhi kriteria tersebut.")
```
ContohM0813.py adalah contoh penggunaan statement `if ... else` untuk emeriksa apakah bilangan adalah faktor dari angka1 dan angka2
##### ContohM0813.py
```python
bilangan = int(input("Masukkan bilangan: "))
angka1 = int(input("Masukkan angka pertama: "))
angka2 = int(input("Masukkan angka kedua: "))

if bilangan > 0 and angka1 % bilangan == 0 and angka2 % bilangan == 0:
    print(f"{bilangan} adalah faktor dari {angka1} dan {angka2}.")
else:
    print(f"{bilangan} bukan faktor dari {angka1} dan {angka2}.")
```
ContohM0814.py adalah contoh penggunaan statement `if ... else` untuk mengetahui apakah seseorang lulus seleksi atau gagal
##### ContohM0814.py
```python
nama = input('Ketikan Nama Peserta : ')
tulis = int(input('> Nilai Tulis : '))
wawancara = int(input('> Nilai Wawancara : '))
rata = (tulis + wawancara)/2.0

if (tulis >= 60 and wawancara >= 60) or rata >= 60 :
    print(nama,': Lulus Seleksi')
else :
    print(nama,': Gagal Seleksi')
```
### 3. Statement `elif`