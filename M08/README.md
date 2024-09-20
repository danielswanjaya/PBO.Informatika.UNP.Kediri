# DASAR PYTHON
## Tipe Data String
### 1. Membuat String
String adalah sebuah urutan karakter yang diwakili oleh tanda kutip tunggal (`'`) atau ganda (`"`). String digunakan untuk merepresentasikan teks, seperti nama, kalimat, atau bahkan paragraf. Misal :
```python
# Menggunakan tanda kutip tunggal
prodi = 'Teknik Informatika'

# Menggunakan tanda kutip ganda
kampus = "Universitas Nusantara PGRI Kediri"
```
Kita juga bisa menggunakan Triple quotes (`"""`) atau (`'''`), untuk membuat string multi-baris dalam Python. Ini memungkinkan Anda untuk menulis string yang mencakup beberapa baris tanpa perlu menggunakan karakter escape seperti \n untuk baris baru. Misal :
```python
lagu_pelangi = """
Pelangi, pelangi, alangkah indahmu
Merah, kuning, hijau di langit yang biru
Pelukismu agung, siapa gerangan?
Pelangi, pelangi, ciptaan Tuhan
"""
lagu_cemara = '''
Naik, naik ke puncak gunung 
Tinggi, tinggi sekali 
Naik, naik ke puncak gunung 
Tinggi, tinggi sekali   
Kiri, kanan, kulihat saja 
Banyak pohon cemara
'''
```

Secara umum Triple quotes digunakan untuk :
- String Multi-baris: Ideal untuk menulis teks yang panjang atau mencakup beberapa baris, seperti paragraf, docstring, atau template.
- Docstrings: Digunakan untuk menulis dokumentasi dalam fungsi, kelas, dan modul. Docstrings memberikan informasi tentang penggunaan, parameter, dan nilai pengembalian suatu entitas.
- Template String: Dapat digunakan untuk membuat template string yang lebih mudah dibaca dan ditulis, terutama saat melibatkan variabel atau ekspresi.

ContohM0801.py adalah contoh pembuatan String dengan tanda kutip tunggal, ganda dan Triple quotes.
##### ContohM0801.py
```python
prodi = 'Teknik Informatika'
kampus = "Universitas Nusantara PGRI Kediri"
lagu_pelangi = """
Pelangi, pelangi, alangkah indahmu
Merah, kuning, hijau di langit yang biru
Pelukismu agung, siapa gerangan?
Pelangi, pelangi, ciptaan Tuhan
"""
lagu_cemara = '''
Naik, naik ke puncak gunung 
Tinggi, tinggi sekali 
Naik, naik ke puncak gunung 
Tinggi, tinggi sekali   
Kiri, kanan, kulihat saja 
Banyak pohon cemara
'''
print('prodi :',prodi)
print('\nkampus :',kampus)
print('\nLagu Pelangi :',lagu_pelangi)
print('Lagu Cemara :',lagu_cemara)
```

### 2. Indeks dalam String
Indeks dalam string Python adalah cara untuk mengakses karakter-karakter individu dalam sebuah string. Setiap karakter dalam string memiliki indeks yang unik, dimulai dari 0. Manfaat indeks pada String adalah :
1. **Akses Karakter**: Indeks memungkinkan Anda untuk mengakses karakter tertentu dalam string. Misalnya, jika Anda ingin mendapatkan karakter pertama dalam string `"Hello"`, Anda dapat menggunakan indeks 0.
2. **Slicing**: Indeks juga digunakan untuk melakukan slicing, yaitu mengambil bagian dari string. Misalnya, untuk mengambil substring `"world"` dari string `"Hello, world!"`, Anda dapat menggunakan indeks 7 hingga 12.
3. **Manipulasi String**: Banyak operasi pada string, seperti penggabungan, pemotongan, dan penggantian, menggunakan indeks untuk menentukan karakter-karakter yang akan dilibatkan.
4. **Iterasi**: Anda dapat menggunakan indeks untuk mengiterasi setiap karakter dalam string, misalnya untuk menghitung kemunculan suatu karakter atau melakukan operasi tertentu pada setiap karakter.

Sama seperti pada List dan Tuple, setiap karakter dalam sebuah string memiliki indeks yang menunjukkan posisinya. Indeks dimulai dari 0 untuk karakter pertama. Indeks negatif, di sisi lain, digunakan untuk mengakses karakter dari akhir string. Indeks -1 mengacu pada karakter terakhir, -2 mengacu pada karakter kedua dari belakang, dan seterusnya.

ContohM0802.py adalah contoh penggunaan indeks untuk akses karakter pada String
##### ContohM0802.py
```python
teks = "Universitas Nusantara PGRI Kediri"
karakter_pertama = teks[0]
karakter_kelima = teks[4]
karakter_terakhir = teks[-1]
substring1 = teks[:5]
substring2 = teks[10:]
substring3 = teks[5:10]
substring4 = teks[::2]
teks_balik = teks[::-1]

print('karakter pertama :',karakter_pertama)
print('karakter kelima  :',karakter_kelima)
print('karakter terakhir:',karakter_terakhir)
print('substring 1:',substring1)
print('substring 2:',substring2)
print('substring 3:',substring3)
print('substring 4:',substring4)
print('teks balik :',teks_balik)
```

### 3. Konversi String ke Tipe Data Kolektif
#### 1. Konversi string menjadi List
Fungsi `list()` secara langsung mengonversi string menjadi list, dengan setiap karakter menjadi elemen terpisah dalam list. ContohM0803.py adalah contoh konversi String menjadi List.
##### ContohM0803.py
```python
string = "Informatika"
list_string = list(string)
print(list_string)
```

#### 2. Konversi string menjadi Tuple
Cara paling sederhana untuk mengkonversi string ke tuple di Python adalah dengan menggunakan fungsi `tuple()`. Setiap karakter dalam string akan menjadi elemen dalam tuple yang baru. ContohM0804.py adalah contoh konversi String menjadi Tuple.
##### ContohM0804.py
```python
string = "Informatika"
tuple_string = tuple(string)
print(tuple_string)
```
#### 3. Konversi string menjadi Dictionary
Proses konversi string menjadi Dictionary bisa dilakukan menggunakan bantuan fungsi `enumerate()`, fungsi `enumerate()` sangat berguna ketika kita ingin membuat dictionary dari sebuah string, di mana setiap karakter (atau bagian string) menjadi kunci, dan nilai yang terkait bisa berupa indeks, nilai lain, atau hasil perhitungan tertentu. ContohM0804.py adalah contoh konversi String menjadi Dictionary menggunakan fungsi `enumerate()`.
##### ContohM0805.py
```python
string = "Informatika"
dict_string = dict(enumerate(string))
print(dict_string)
```
#### 4. Konversi string menjadi Set
Metode `set()` adalah fungsi yang paling umum dan langsung, cukup memberikan string sebagai argumen ke fungsi `set()`. Hasil konversinya adalah karakter-karakter unik dalam string.
ContohM0806.py adalah contoh konversi String menjadi Set.
##### ContohM0806.py
```python
kampus = "universitas nusantara pgri kediri"
set_kampus = set(kampus)
print('set kampus:',set_kampus)
```
### 4. Fungsi bawaan String : Mengubah Kasus Huruf
1. `upper()`: Mengubah semua huruf menjadi kapital. Contoh: "hello" menjadi "HELLO".
2. `lower()`: Mengubah semua huruf menjadi kecil. Contoh: "HELLO" menjadi "hello".
3. `title()`: Membuat huruf pertama setiap kata menjadi kapital. Contoh: "hello world" menjadi "Hello World".
4. `capitalize()`: Membuat huruf pertama string menjadi kapital. Contoh: "hello" menjadi "Hello".
5. `swapcase()` : Mengubah huruf besar menjadi huruf kecil dan sebaliknya pada sebuah string.

ContohM0807.py adalah contoh penggunaan fungsi `upper()`, `lower()`, `title()`, `capitalize()`, dan `swapcase()` pada string.
##### ContohM0807.py
```python
teks = "univerSITAS NUSAntara PGRI keDIri"
teks_uppercase = teks.upper()
teks_lowercase = teks.lower()
teks_title = teks.title()
teks_capitalize = teks.capitalize()
teks_swapcase = teks.swapcase()

print("Teks asli:", teks)
print("Semua huruf besar:", teks_uppercase)
print("Semua huruf kecil:", teks_lowercase)
print("Huruf pertama setiap kata kapital :", teks_title)
print("Huruf pertama besar, sisanya kecil:", teks_capitalize)
print("Huruf besar-kecil ditukar:", teks_swapcase)
```

### 5. Fungsi bawaan String : Memeriksa Isi String
1. `startswith(sub)`: Mengembalikan `True` jika string dimulai dengan substring `sub`.
2. `endswith(sub)`: Mengembalikan `True` jika string diakhiri dengan substring `sub`.
3. `isalpha()`: Mengembalikan `True` jika semua karakter dalam string adalah huruf.
4. `isdigit()`: Mengembalikan `True` jika semua karakter dalam string adalah angka.
5. `isalnum()`: Mengembalikan `True` jika semua karakter dalam string adalah alfanumerik (huruf atau angka).
6. `isspace()`: Mengembalikan `True` jika semua karakter dalam string adalah spasi kosong.
7. `isdecimal()` : Mengembalikan `True` jika semua karakter dalam sebuah string adalah angka-angka desimal.
8. `isupper()` : Mengembalikan `True` jika semua karakterdalam sebuah string adalah huruf besar
9. `islower()` : Mengembalikan `True` jika semua karakterdalam sebuah string adalah huruf kecil

ContohM0808.py adalah contoh penggunaan fungsi `startswith()`, `endswith()` `isalpha()`, `isdigit()`, `isalnum()`, `isspace()`, `isdecimal()`, `isupper()` dan `islower()` pada string.
##### ContohM0808.py
```python
teks1 = "Universitas Nusantara PGRI Kediri 123"
teks2, teks3 = "Teknik Informatika", "TeknikInformatika"
teks4 = "TeknikInformatika123"
teks5, teks6 = "12345", "678.9"
teks7 = "     " #hanya spasi
teks8, teks9 = "PGRI", "kediri"
print(f'teks1 : {teks1}\nteks2 : {teks2}\nteks3 : {teks3}\nteks4 : {teks4}\nteks5 : {teks5}')
print(f'teks6 : {teks6}\nteks7 : {teks7}\nteks8 : {teks8}\nteks9 : {teks9}\n')
print("Teks1 dimulai dengan 'Universitas':", teks1.startswith("Universitas"))
print("Teks1 dimulai dengan 'nusantara':", teks1.startswith("nusantara"))
print("Teks1 diakhiri dengan 'Kediri':", teks1.endswith("Kediri"))
print("Teks1 diakhiri dengan '123':", teks1.endswith("123"))
print("\nSemua karakter teks1 adalah huruf:", teks1.isalpha())
print("Semua karakter teks2 adalah huruf:", teks2.isalpha())
print("Semua karakter teks3 adalah huruf:", teks3.isalpha())
print("\nSemua karakter teks1 adalah angka:", teks1.isdigit())
print("Semua karakter teks5 adalah angka:", teks5.isdigit())
print("Semua karakter teks6 adalah angka:", teks6.isdigit())
print("\nSemua karakter teks1 adalah alfanumerik:", teks1.isalnum())
print("Semua karakter teks4 adalah alfanumerik:", teks4.isalnum())
print("Semua karakter teks5 adalah alfanumerik:", teks5.isalnum())
print("Semua karakter teks6 adalah alfanumerik:", teks6.isalnum())
print("\nSemua karakter teks2 adalah spasi:", teks2.isspace())
print("Semua karakter teks7 adalah spasi:", teks7.isspace())
print("\nSemua karakter teks4 adalah desimal:", teks4.isdecimal())
print("Semua karakter teks5 adalah desimal:", teks5.isdecimal())
print("Semua karakter teks6 adalah desimal:", teks6.isdecimal())
print("\nSemua karakter teks3 adalah huruf besar:", teks3.isupper())
print("Semua karakter teks8 adalah huruf besar:", teks8.isupper())
print("Semua karakter teks9 adalah huruf besar:", teks9.isupper())
print("\nSemua karakter teks3 adalah huruf kecil:", teks3.islower())
print("Semua karakter teks8 adalah huruf kecil:", teks8.islower())
print("Semua karakter teks9 adalah huruf kecil:", teks9.islower())
```

### 6. Fungsi bawaan String : Mencari dan Mengganti
1. `find(sub)`: Mengembalikan indeks pertama kemunculan substring `sub`. Jika tidak ditemukan, mengembalikan -1.
2. `rfind(sub)`: Sama seperti `find()`, tetapi mencari dari belakang.
3. `index(sub)`: Sama seperti `find()`, tetapi memunculkan error jika substring tidak ditemukan.
4. `rindex(sub)`: Sama seperti `rfind()`, tetapi memunculkan error jika substring tidak ditemukan.
5. `replace(old, new)`: Mengganti semua kemunculan substring `old` dengan `new`.
6. `max(teks)`: Mencari karakter dengan nilai ASCII tertinggi dalam string teks.
7. `min(teks)`: Mencari karakter dengan nilai ASCII terendah dalam string teks.

ContohM0809.py adalah contoh penggunaan fungsi `find()`, `rfind()`, `index()`, `rindex()`, `replace()`, `max()` dan `min()` pada string.
##### ContohM0809.py
```python
teks = "Teknik Informatika Universitas Nusantara PGRI Kediri"
teks_baru = teks.replace("PGRI", "Pendidikan")
print('teks :',teks)
print("\nPosisi pertama kemunculan 'ni':", teks.find("ni"))
print("Posisi pertama kemunculan 'Nusantara':", teks.find("Nusantara"))
print("Posisi pertama kemunculan 'pgri':", teks.find("pgri"))  # Jika tidak ditemukan, akan mengembalikan -1
print("\nPosisi terakhir kemunculan 'ni':", teks.rfind("ni"))
print("Posisi terakhir kemunculan 'Nusantara':", teks.rfind("Nusantara"))
print("Posisi terakhir kemunculan 'pgri':", teks.rfind("pgri"))
print("\nPosisi pertama kemunculan 'a':", teks.index("a"))
print("Posisi terakhir kemunculan 'a':", teks.rindex("a"))
print("Posisi pertama kemunculan 'ni':", teks.index("ni"))
print("Posisi terakhir kemunculan 'ni':", teks.rindex("ni"))
print("\nKarakter terbesar:", max(teks))
print("Karakter terkecil:", min(teks))
print("\nTeks setelah mengganti 'PGRI':", teks_baru)
```

### 7. Fungsi bawaan String : Memotong dan Menggabungkan String
1. `split(sep)`: Membagi string menjadi list berdasarkan pemisah `sep`.
2. `join(iterable)`: Menggabungkan elemen dalam `iterable` menjadi sebuah string dengan menggunakan string sebagai pemisah.
3. `strip()`: Menghapus spasi kosong di awal dan akhir string.
4. `lstrip()`: Menghapus spasi kosong di awal string.
5. `rstrip()`: Menghapus spasi kosong di akhir string.

ContohM0810.py adalah contoh penggunaan fungsi `split()`, `join()`, `strip()`, `lstrip()` dan `rstrip()` pada string.
##### ContohM0810.py
```python
teks = "   Universitas Nusantara PGRI Kediri   "
kata_kata = teks.split()
kata_kata.insert(0, 'Teknik Informatika')
huruf_vokal = "aiueo"
teks_baru = huruf_vokal.join(kata_kata)
teks_tanpa_spasi = teks.strip()
teks_tanpa_spasi_kiri = teks.lstrip()
teks_tanpa_spasi_kanan = teks.rstrip()
kalimat = "apel,mangga,jeruk"
buah = kalimat.split(",")
teks_dengan_tanda_baca = "  Hello, World!  "
teks_tanpa_tanda_baca = teks_dengan_tanda_baca.strip(" ,!")

print("Membagi teks menjadi kata-kata:", kata_kata)
print("Menggabungkan kata-kata dengan huruf vokal:", teks_baru)
print("Menghapus spasi di awal dan akhir:", teks_tanpa_spasi)
print("Menghapus spasi di awal          :", teks_tanpa_spasi_kiri)
print("Menghapus spasi di akhir         :", teks_tanpa_spasi_kanan)
print("Membagi kalimat berdasarkan koma :", buah)
print("Menghapus spasi, koma, dan tanda seru:", teks_tanpa_tanda_baca)
```

### 8. Fungsi bawaan String : Lain-lain
1. `len()`: Mengembalikan panjang string (jumlah karakter).
2. `count(sub)`: Menghitung jumlah kemunculan substring `sub` dalam string.
3. `center(width, fillchar)`: Mengembalikan string baru dengan panjang `width` dan string asli berada di tengah, diisi dengan karakter `fillchar`.
4. `ljust(width, fillchar)` : Mengembalikan string baru dengan panjang `width` dan string asli berada di kiri, diisi dengan karakter `fillchar`.
5. `rjust(width, fillchar)` : Mengembalikan string baru dengan panjang `width` dan string asli berada di kanan, diisi dengan karakter `fillchar`.
6. `zfill()` : Menambahkan karakter "0" (nol) di awal sebuah string hingga mencapai panjang tertentu yang telah ditentukan.

ContohM081.py adalah contoh penggunaan fungsi `len()`, `count()`, `center()`, `ljust()`, `rjust()` dan `zfill()` pada string.
##### ContohM0811.py
```python
teks1 = "Teknik Informatika Universitas Nusantara PGRI Kediri"
teks2 = "Teknik Informatika"
angka = "123"
panjang_teks = len(teks1)
jumlah_huruf_a = teks1.count('a')
jumlah_suku_ni = teks1.count('ni')
teks_tengah = teks2.center(26)
teks_kiri = teks2.ljust(26)
teks_kanan = teks2.rjust(26)
angka_dengan_nol = angka.zfill(6)
teks_tengah_dengan_karakter = teks2.center(26, '*')
teks_kiri_dengan_karakter = teks2.ljust(26, '-')
teks_kanan_dengan_karakter = teks2.rjust(26, '.')

print(f'teks1 :{teks1}\nteks2 :{teks2}\nangka :{angka}\n')
print("Panjang teks:", panjang_teks)
print("Jumlah huruf 'a'     :", jumlah_huruf_a)
print("Jumlah suku kata 'ni':", jumlah_suku_ni)
print(f"\nTeks ditengahkan          : |{teks_tengah}|")
print(f"Teks disejajarkan ke kiri : |{teks_kiri}|")
print(f"Teks disejajarkan ke kanan: |{teks_kanan}|")
print(f"Angka dengan pengisian nol: |{angka_dengan_nol}|")
print(f"\nTeks ditengahkan dengan karakter '*'          : |{teks_tengah_dengan_karakter}|")
print(f"Teks disejajarkan ke kiri dengan karakter '-' : |{teks_kiri_dengan_karakter}|")
print(f"Teks disejajarkan ke kanan dengan karakter '.': |{teks_kanan_dengan_karakter}|")
```