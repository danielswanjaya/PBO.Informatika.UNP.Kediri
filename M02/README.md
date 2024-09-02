# DASAR PYTHON
## Dasar pemrograman Python
### 1. Mencetak Informasi di Console
Penyampaian informasi ke layar monitor bisa dilakukan melalui dua media, Console dan Graphical User Interface. Pada pembelajaran awal masih tampilan menggunakan Console dalam hal ini Command Prompt. Pada Python perintah yang digunakan untuk menampilkan informasi ke layar monitor adalah print, seperti gambar 1. File ContohM0201.py adalah contoh lain penggunaan perintah `print`. Untuk mengetikan program tersebut, gunakan aplikasi Visual Studio Code.

![<alt text>](img/Screenshot01.png)<br>Gambar 1. Contoh penggunaan perintah print

ContohM0201.py|
|-:|
```python
print ("Aku belajar dasar Python") 
print ("Aku pasti bisa")
```

Terdapat beberapa karakter khusus atau biasa disebut dengan escape character, merupakan karakter yang ditulis setelah tanda backslash (\) dan memiliki fungsi tertentu sesuai dengan kode karakter masing-masing,  seperti pada tabel 1. Contoh penggunaannya seperti pada file ContohM0202.py.

| Notasi |	Deskripsi                           |
| ------ |:------------------------------------:|
| `\b`   | Backspace                            |
| `\n`   | Newline                              |
| `\t`   | Tab                                  |
| `\‘`   | Petik Tunggal (Single Quote)         |
| `\”`   | Petik Ganda (Double Quote)           |
| `\\`   | Backslash                            |
| `\ooo` | Octal value                          |
| `\xhh` | Hexa value                           |
| `\u`   | Format pencetakkan (termasuk simbol) |

ContohM0202.py|
|-:|
```python
print ("Selamat\b Pagi")
print ("Selamat\n Siang")
print ("Selamat\t Sore")
print ("Hari Jum\'at")
print ("\\(\"o\")/")
print ("\113\105\104\111\122\111")
print ("\x48\x41\x52\x4D\x4F\x4E\x49")
print ("x\u00b2")
```

### 2. Komentar
Komentar (comment) adalah kode di dalam script Python yang tidak dieksekusi atau tidak dijalankan mesin. Komentar hanya digunakan untuk menandai atau memberikan keterangan tertulis pada script. Komentar biasa digunakan untuk membiarkan orang lain memahami apa yang dilakukan script. atau untuk mengingatkan kepada programmer sendiri jika suatu saat kembali mengedit script tersebut. Untuk menggunakan komentar terdapat 2 cara yaitu satu baris dan beberapa baris. Semua karakter yang ditulis setelah lambang #, sampai akhir baris, menunjukkan bahwa baris tersebut merupakan keterangan. Interpreter dari Python tidak menganggap baris itu ada (sebagai komentar saja). Komentar yang lebih dari satu baris dapat juga ditulis di dalam tanda petik, dengan menggunakan string literal yang dibuka dan ditutup dengan """. File ContohM0203.py adalah contoh pemberian komentar pada script program Python.

ContohM0203.py|
|-:|
```python
# Nama File : ContohM203.py
"""
Program ini memberikan contoh bagaimana membuat komentar
pada script program Python
"""
print ("Komentar di Python")
```

### 3. Kata Kunci (Keyword)
Di Python terdapat kata-kata yang berlaku sebagai kata-kunci. Kata-kata yang tergolong sebagai kata-kunci digunakan secara khusus oleh Python dan tidak boleh digunakan misalnya untuk nama variabel atau fungsi. Sebagai contoh, True menyatakan nilai benar dan False menyatakan nilai salah. Gambar 2 mencantumkan kata-kunci yang terdapat pada Python.

![alt text](img/Screenshot02.png)<br>Gambar 2. Keyword di Python

### 4. Pengenal (Identifier)
Pengenal adalah nama yang digunakan untuk variabel, fungsi, kelas, dan lain-lain. Pemberian nama pengenal harus mengikuti aturan yang berlaku di Python. Berikut adalah aturannya :
1.	Pengenal dapat mengandung huruf (A-Z, a-z), angka (0-9), dan garis-bawah (_).
2.	Pengenal tidak boleh berawalan angka.
3.	Huruf kecil dan huruf kapital dibedakan (Case Sensitif). Dengan demikian, lebar dan LEBAR menyatakan pengenal yang berbeda.
4.	Pengenal tidak diperkenankan menggunakan kata-kunci, misalnya for dan true.

Perlu diingatkan bahwa dalam penamaan (identifier) sebaiknya menggunakan nama yang deskriptif. Hal ini memudahkan kita dalam mengingat penamaan, contohnya `kmp=”UNP Kediri”` adalah benar, hanya saja ini tidak deskriptif, bagusnya dalam penamaan menggunakan `kampus=”UNP Kediri”`.

### 5. Variabel
Variabel adalah lokasi memori yang dicadangkan untuk menyimpan nilai-nilai. Ini berarti bahwa ketika Anda membuat sebuah variabel Anda memesan beberapa ruang di memori. Variabel menyimpan data yang dilakukan selama program dieksekusi (Gambar 3), yang nantinya isi dari variabel tersebut dapat diubah oleh operasi-operasi tertentu pada program yang menggunakan variabel. Variabel dapat menyimpan berbagai macam tipe data. Di dalam pemrograman Python, variabel mempunyai sifat yang dinamis, artinya variabel Python tidak perlu didekralasikan tipe data tertentu dan variabel Python dapat diubah saat program dijalankan. Pemberian nama pengenal harus mengikuti aturan penamaan Identifier.

![alt text](img/Screenshot03.png)<br>Gambar 3. Ilustrasi Variabel dan Data

Berbeda dengan bahasa lain, seperti C ataupun C++, variabel di Python tidak perlu dideklarasikan. Deklarasi variabel itu bertujuan untuk menentukan tipe data yang diwakili oleh suatu variabel sehingga deklarasi variabel dapat dilakukan tanpa memberikan nilai ke variabel. Di Python, variabel tidak perlu dideklarasikan terlebih dahulu karena memang variabel itu tidak mempunyai tipe; yang mempunyai tipe data adalah nilai yang dinyatakannya. Itulah sebabnya, satu variabel di Python dapat menyatakan data bertipe bilangan pada suatu saat dan menyatakan data bertipe string pada waktu yang lain. Contoh pemberian nilai (Assignment) ke variabel adalah seperti file ContohM0204.py.

ContohM0204.py|
|-:|
```python
# Cara pertama
NilaiA = 10
NilaiB = 10
NilaiC = 10
print("NilaiA = ",NilaiA); print("NilaiB = ",NilaiB) ; print("NilaiC = ",NilaiC)
# Cara Kedua
NilaiD = NilaiE = NilaiF = 20
print("NilaiD = ",NilaiD); print("NilaiE = ",NilaiE) ; print("NilaiE = ",NilaiE)
# Cara ketiga
NilaiG, NilaiH, NilaiI = 15, 17, 19
print("NilaiG = ",NilaiG); print("NilaiH = ",NilaiH) ; print("NilaiI = ",NilaiI)
# Tukar isi
NilaiA, NilaiD = NilaiD, NilaiA
print("Setelah penukaran :")
print("NilaiA = ",NilaiA) ; print("NilaiD = ",NilaiD)
```

Pada assignment cara pertama, baris ke-2 sampai dengan 4, adalah cara umum yang digunakan untuk pemberian nilai. Cara kedua, baris ke-7, adalah cara lain jika terdapat beberapa Variabel yang mempunyai nilai yang sama. Cara ketiga, baris ke-10, adalah cara untuk memberi nilai pada beberapa Variabel secara bersamaan. Cara ketiga juga bisa digunakan untuk menukar isi beberapa Variabel seperti pada baris ke-13. Output dari Contoh0204.py, jika bagian nilai variabel diperhatikan, terdapat spasi tambahan, misal NilaiA =  10, dimana setelah tanda sama dengan terdapat 2 spasi, padahal pada perintah cetaknya tidak ada 2 spasi. Hal ini disebabkan oleh arti tanda koma pada perintah print adalah separator default antar teks berupa spasi, misal terdapat perintah berikut :
```python
print("Teknik","Informatika","Universitas","Nusantara","PGRI","Kediri")
```
Maka hasilnya adalah Teknik Informatika Universitas Nusantara PGRI Kediri. Tetapi separator antar teks dapat diganti dengan lainnya, misal kita ganti dengan karakter sep="->", maka perintah cetaknya menjadi :
```python
print("Teknik","Informatika","Universitas","Nusantara","PGRI","Kediri", sep="->")
```
Sehingga hasilnya menjadi Teknik->Informatika->Universitas->Nusantara->PGRI->Kediri.

### 6. Tipe Data
Secara umum, tipe data primitif dalam python dibagi menjadi tiga jenis, Numerik/Bilangan, Teks/String dan Boolean/Logika. Meskipun variabel di Python tidak perlu dideklarasikan, tetapi setiap tipe data punya aturan penulisannya masing-masing.
#### 1. Numerik/Bilangan
Tipe data numerik adalah jenis data Python yang bersifat angka yang bisa ditambah, dikurangi, dikali maupun dibagi. Beberapa tipe data yang dimiliki data numerik pada Python seperti:
- Integer : Tipe data integer adalah tipe data numerik yang menampung bilangan bulat. Contohnya bilangan 1,2,3 dan seterusnya. Sehingga setiap variabel yang memiliki nilai bilangan bulat, maka ia akan dikategorikan sebagai integer. Dalam bahasa Python, panjang dari data integer dibatasi oleh besarnya memori yang tersedia
- Float : Tipe data float dipergunakan untuk variabel-variabel yang memiliki nilai pecahan / desimal. Tipe data float juga termasuk ke dalam tipe data numerik karena jenis data ini menyimpan bilangan pecahan atau disebut juga dengan bilangan real. Pemisah dari bilangan desimal menggunakan tanda titik (.) bukan koma (,).
- Complex : Tipe data Complex merepresentasikan nilai imajiner. Bilangan imajiner merupakan suatu simbol sehingga pada dasarnya tidak ada dan hanya dituliskan saja sebagai bahasa komputasi, misal 5i yang berarti 5×√(-1). bilangan ini tidak banyak digunakan pada operasi matematika, sehingga jarang digunakan pada pemrograman. Bilangan kompleks adalah bilangan riil “ditambah” dengan bilangan imajiner, misal 2+5i yang berarti 2+(5×√(-1)), jika dituliskan pada Python menjadi 2 + 5j, dimana j sama artinya dengan simbol i pada notasi matematika.
#### 2.	Teks/String
Tipe data ini digunakan untuk menyimpan sebuah teks, seperti huruf, tanda baca, dan karakter spesial lainnya. Data yang bertipe string harus diapit oleh tanda kutip, baik tanda kutip satu ( ' ) maupun tanda kutip dua ( " ) setelah karakter sama dengan ( = ). Tanda kutip pembuka dan penutup harus sama, tidak boleh berbeda. Seperti berikut :
```python
prodi = 'Teknik Informatika'
univ = "UNiversitas Nusantara PGRI Kediri"
```
Adapun penulisan seperti 'Teknik Informatika", yang menggunakan awalan berupa petik tunggal dan akhiran petik ganda tidak diperkenankan. Jika hendak menuliskan string Jum’at, maka bisa dilakukan dengan 2 cara yaitu :

```python
Hari1 = 'Jum\'at'
Hari2 = "Jum'at"
```

ContohM0205.py merupakan contoh penulisan beberapa nilai dengan tipe data yang berbeda, beserta cara mengetahui tipe dari nilai tersebut, dengan mengingat bahwa yang memiliki tipe bukan variabelnya tetapi nilai yang dirujuk suatu variabel.

ContohM0205.py|
|-:|
```python
vari = 17; print(vari, type(vari))
vari = 17.08 ;print(vari, type(vari))
vari = '17.08.1945'; print(vari, type(vari))
vari = 0xABC; print(vari, type(vari)) 
vari = 0o77; print(vari, type(vari))
vari = 0b110011; print(vari, type(vari))
vari = 30.5e3; print(vari, type(vari))
vari = 2 + 5j; print(vari, type(vari))
```
Pada baris ke-4 sampai 6 adalah cara penulisan bilangan Heksadesimal (basis-16), Oktadesimal (basis-8) dan Biner (basis-2), tetapi saat dicetak akan diubah dalam bentuk desimal. Tetapi jika menghendaki nilai yang dicetak dalam bentuk tertentu, maka kita bisa menggunakan fasilitas format di Python, seperti berikut :
```python
vari = 0xABC
print(format(vari,'04x'))
vari = 0o77
print(format(vari,'05o'))
vari = 0b110011
print(format(vari,'08b'))
```
Dimana `'04x'` berarti nilainya akan diformat ke bentuk 4 digit Heksadesimal, `'05o'` berarti nilainya akan diformat ke bentuk 5 digit Oktadesimal, dan `'08b'` berarti nilainya akan diformat ke bentuk 8 digit biner. Selain digunakan untuk mengkonversi bentuk bilangan, format juga bisa digunakan untuk memperpendek perintah pencetakan, misalnya dari ContohM0204.py. baris ke-5 bisa diganti menjadi :
```python
print("NilaiA = %d\nNilaiB = %d\nNilaiC = %d" %(NilaiA,NilaiB,NilaiC))
```
Dimana %d akan digantikan dengan variabel pertama pada runtutan variabel yang ada di akhir perintah print, dalam hal ini %(NilaiA,NilaiB,NilaiC). Tanda %d pertama akan digantikan nilai variabel NilaiA, tanda %d kedua akan digantikan nilai variabel NilaiB dan tanda %d ketiga akan digantikan nilai variabel NilaiC. Tanda %d mewakili integer, %f mewakili float dan %s mewakili string. Untuk membuat n angka di belakang koma, gunakan %.nf, misal %.3f, yang berarti nilai variabel akan memiliki 3 digit dibelakang koma.

Selain menggunakan format integer, float dan string, bisa juga menggunakan perintah format seperti berikut :
```python
print('NilaiA = {}\nNilaiB = {}\nNilaiC = {}\n'.format(NilaiA, NilaiB, NilaiC))
```
Dalam format ini, kita bisa mengatur urutan variabel yang ditampilkan, sehingga tidak harus sesuai dengan urutan pada bagian format, misalnya perintahnya diubah menjadi :
```python
print('NilaiA = {2}\nNilaiB = {0}\nNilaiC = {1}\n'.format(NilaiB, NilaiC, NilaiA))
```

### 7. Input
Input atau inputan (dalam konteks pemrograman) merupakan sebuah data, informasi, atau nilai apa pun yang dikirimkan oleh user kepada komputer untuk diproses lebih lanjut. Dalam Python untuk keperluan pemasukkan data dari pengguna dapat dilakukan dengan memanfaatkan fungsi input. Nilai yang didapat dari fungsi input berupa String, sehingga jika kita perlu nilai bertipe selain integer, maka kita perlu mengkonversi tipe data string menjadi tipe yang diperlukan, misalnya jika ingin mengkonversi ke tipe integer, maka dapat diubah menggunakan fungsi int(). jika ingin mengkonversi ke tipe integer, maka dapat diubah menggunakan fungsi float(). Contoh M0206.py adalah contoh penggunaan fungsi input, int() dan float().
ContohM0205.py|
|-:|
```python
panjang = int(input("Panjang = "))
lebar = int(input("Lebar = "))
tinggi = float(input("Tinggi = "))
luas = panjang * lebar
volume = luas * tinggi
print('Luas Alas =', luas)
print('Volume =', volume)
```

Tetapi terkadang karena kebiasaan orang Indonesia menuliskan pecahan menggakan tanda koma bukan titik, maka hal ini bisa menyebabkan terjadinya runtime error atau kesalahan saat program dijalankan, seperti gambar 9. Untuk mengatasi hal ini gunakan exception handling, yaitu kemampuan program Python untuk menangani kesalahan. Contoh0207.py adalah contoh penggunaan Exception Handling di Python.

![alt text](img/Screenshot04.png)<br>Gambar 4. Runtime Error karena kesalahan penulisan pemisah desimal

ContohM0205.py|
|-:|
```python
panjang = int(input("Panjang = "))
lebar = int(input("Lebar = "))
try :
    tinggi = float(input("Tinggi = "))
except :
    print('terjadi kesalahan, maka tinggi = 1.')
    tinggi = 1
luas = panjang * lebar
volume = luas * tinggi
print('Luas Alas =', luas)
print('Volume =', volume)
```

Setelah penggunaan try-except maka ketika terjadi kesalahan, maka program tidak akan berhenti, tetapi mengeksekusi bagian except (baris ke-6 dan 7), kemudian melanjutkan script program berikutnya, baris ke-8 sampai 11.
Pada baris ke 4, 6 & 7 terlihat bagian script yang menjorok ke dalam, hal ini disebut sebagai indentasi, Indentasi digunakan untuk mengindikasi tingkatan kode pada Python atau biasa disebut sebagai blok program. Karakter  white space yang bisa digunakan untuk indentasi baris adalah spasi atau tab (pada bahasa pemrograman lainnya biasanya menggunakan tanda kurung kurawal atau kata kunci). Tetapi karakter white space yang digunakan untuk indentasi harus konsisten dalam satu file program Python. Jika karakter white space yang digunakan berbeda, maka Python akan memberikan pesan kesalahan.
