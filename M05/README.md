# DASAR PYTHON
## Tipe Data Kolektif (Dictionary)
### 1. Membuat Dictionary
Dictionary atau Kamus di Python dapat dibayangkan seperti kamus yang kita gunakan sehari-hari; misalnya, kamus Bahasa Inggris ke Bahasa Indonesia. Kata dalam bahasa Inggris bertindak sebagai kata-kunci. Melalui kata-kunci ini, arti dalam Bahasa Indonesia bisa ditemukan. Demikian halnya pada Dictionary di Python. Dictionary mengandung nol, satu atau sejumlah elemen, dengan setiap item mengandung kunci dan nilai secara berpasangan. Dalam hal ini, kunci bersifat unik (tidak ada yang kembar). Perlu diketahui, Dictionary bersifat mutable, seperti List. Tetapi Dictionary tidak memiliki indeks sehingga tidak memiliki urutan. Dictionary dipisahkan menggunakan tanda koma dan diapit dengan tanda kurung kurawal `{ }`. Data dinyatakan sebagai pasangan key & value, dimana tipe data dari key dan value sesuai dengan keperluan, dituliskan dalam format `key:value`. Berikut contoh pembuatan Dictionary :
```python
kosong = {}
matkul = {'kode':'INF1011', 'nama':'Pemrograman Berorientasi Obyek'}
kodeFakultas = {
    1:'Fakultas Keguruan dan Ilmu Penddikan'
    2:'Fakultas Ekonomi dan Bisnis'
    3:'Fakultas Teknik dan Ilmu Komputer'
    4:'Fakultas Ilmu Kesehatan dan Sains'
}
infoku = {
    'nama':'Dwi Kusuma Dewi',
    'npm':'2213020777',
    'prodi':'Teknik Informatika',
    'fakultas':'Teknik dan Ilmu Komputer',
    'universitas':'Universitas Nusantara PGRI Kediri'
}
```

Dictionary bisa juga dibuat menggunakan fungsi `dict()`, seperti berikut :
```python
matkul = dict(kode='INF1011', nama='Pemrograman Berorientasi Obyek',sks = 3)
infoku = dict([('nama','Dwi Kusuma Dewi'),('npm','2213020777'),('prodi','Teknik Informatika')])
```

Selain itu, Dictionary juga bisa dibuat menggunakan fungsi `enumerate()`. Fungsi `enumerate()` sangat berguna untuk membuat dictionary baru, terutama ketika kita ingin menggunakan indeks sebagai kunci dari dictionary tersebut. Fungsi `enumerate()` menghasilkan pasangan (indeks, nilai) dari sebuah iterable (seperti list, tuple, atau string). misal :
```python
fruits1 = ['Apple','Pineapple','Mango','Guava','Blueberry']
dict1 = dict(enumerate(fruits1))

fruits2 = ('Banana','Watermelon','Avocado','Strawberry')
dict2 = dict(enumerate(fruits2))

fruit = 'Apple'
dict3 = dict(enumerate(fruit))
```

### 2. Akses Nilai dalam Dictionary
Untuk mengakses value tidak bisa menggunakan indeks seperti List & Tuple, tetapi harus menggunakan key-nya dengan format `dict['key']`. ContohM0501.py adalah contoh pembuatan dan akses nilai dalam Dictionary
##### ContohM0501.py
```python
infoku = {
    'nama':'Dwi Kusuma Dewi',
    'npm':'2213020777',
    'prodi':'Teknik Informatika',
    'fakultas':'Teknik dan Ilmu Komputer',
    'universitas':'Universitas Nusantara PGRI Kediri'
}
print(infoku)
print('NPM      :',infoku['npm'])
print('Nama     :',infoku['nama'])
print('Prodi    :',infoku['prodi'])
print('Fakultas :',infoku['fakultas'])
print('Kampus   :',infoku['universitas'])
```

Jika terdapat key yang sama dengan value yang berbeda, maka value dari pasangan key yang terakhir yang akan digunakan, misal Dictionary `infoku` kita buat menjadi seperti :

```python
infoku = {
    'nama':'Dwi Kusuma Dewi',
    'npm':'2213020777',
    'prodi':'Teknik Informatika',
    'fakultas':'Teknik dan Ilmu Komputer',
    'nama':'Daniel Swanjaya',
    'universitas':'Universitas Nusantara PGRI Kediri'
}
```
Maka saat Dictionary `infoku` kita cetak, maka pada bagian nama yang muncul `Daniel Swanjaya`, bukan `Dwi Kusuma Dewi`.

Jika kita menambahkan baris berikut pada ContohM0501.py maka akan memunculkan pesan error. 
```python
print('Alamat   :',infoku['alamat'])
```
Karena jika key tidak ditemukan dalam Dictionary, maka Python akan memunculkan pesan error saat dieksekusi. Untuk mengatasi hal ini terdapat alternatif untuk mendapatkan nilai berdasarkan suatu kunci yaitu menggunakan metode `get()`. Dengan cara ini error tidak akan terjadi seandainya key yang dicari tidak ada, melainkan nilai balik None yang akan diberikan. Cara ini lebih disarankan daripada akses langsung. Sehingga ContohM0501.py lebih disarankan diubah seperti berikut :
```python
infoku = {
    'nama':'Dwi Kusuma Dewi',
    'npm':'2213020777',
    'prodi':'Teknik Informatika',
    'fakultas':'Teknik dan Ilmu Komputer',
    'universitas':'Universitas Nusantara PGRI Kediri'
}
print(infoku)
print('NPM      :',infoku.get('npm'))
print('Nama     :',infoku.get('nama'))
print('Prodi    :',infoku.get('prodi'))
print('Fakultas :',infoku.get('fakultas'))
print('Kampus   :',infoku.get('universitas'))
print('Alamat   :',infoku.get('alamat'))
```

Kita juga bisa memberikan pesan seandainya key yang dicari tidak ada, yaitu dengan menambahkan argumen kedua pada metode `get()`, seperti berikut :
```python
print('Alamat   :',infoku.get('alamat','Data tidak ditemukan'))
```
Sehingga teks yang muncul bukan 'None' tetapi 'Data tidak ditemukan'.

### 3. Update Nilai dalam Dictionary
Kita dapat memperbarui Dictionary dengan menambahkan entri baru atau pasangan nilai kunci, memodifikasi entri yang ada, atau menghapus entri yang ada seperti ditunjukkan pada ContohM0502.py. Untuk mengubah nilai dapat menggunakan 2 cara yaitu :
- Akses langsung berdasarkan key
- Metode `update()` untuk meng-update satu atau beberapa nilai sekaligus atau menggabungkan dua dictionary.
##### ContohM0502.py
```python
infoku = {
    'nama':'Dwi Kusuma Dewi',
    'npm':'2213020777',
    'prodi':'Teknik Informatika',
    'fakultas':'Teknik dan Ilmu Komputer',
    'universitas':'Universitas Nusantara PGRI Kediri'
}
infoku['npm'] = '2213020888'
infoku.update({'nama':'Duwi Kusuma Dewi'})
infoku.update({'alamat':'Jl. Kilisuci No.100 Kediri'})
print('NPM      :',infoku.get('npm'))
print('Nama     :',infoku.get('nama'))
print('Prodi    :',infoku.get('prodi'))
print('Fakultas :',infoku.get('fakultas'))
print('Kampus   :',infoku.get('universitas'))
print('Alamat   :',infoku.get('alamat'))
```

Baris ke-9 dan 10 dapat disatukan dengan cara berikut :
```python
infoku.update({'nama':'Duwi Kusuma Dewi','alamat':'Jl. Kilisuci No.100 Kediri'})
```
Key suatu Dictionary tidak bisa diubah, hanya value saja  yang bisa diubah. Setelah key ditetapkan untuk item tertentu, kita tidak bisa mengubah key tersebut. Namun, kamu bisa mengubah value yang terkait dengan key.
Nilai dalam dictionary bisa berupa tipe data apa pun, seperti string, angka, list, atau bahkan dictionary lain. Namun, key biasanya terbatas pada tipe data yang tidak berubah seperti string, angka, atau tuple.

### 4. Hapus Elemen Dictionary
Kita dapat menghapus elemen Dictionary individual atau menghapus keseluruhan isi Dictionary. kita juga dapat menghapus seluruh Dictionary dalam satu operasi.
- Untuk menghapus elemen dalam dictionary, kita dapat menggunakan keyword `del`. Setelah elemen dihapus, kita tidak dapat lagi mengaksesnya. Penggunaannya seperti berikut :
```python
del infoku['alamat']
```
- metode `pop()` akan Menghapus elemen dan mengembalikan nilai yang dihapus. Jika key tidak ditemukan, akan muncul error. Penggunaannya seperti berikut :
```python
infoku.pop('alamat')
#atau
infoku.pop('alamat', 'Data tidak ditemukan')
```
- metode `popitem()` akan menghapus elemen terakhir pada Dictionary dan memberikan nilai balik berupa pasangan kunci dan nilainya dalam bentuk tupel. Penggunaannya seperti berikut :
```python
infoku.popitem()
```
- Untuk menghapus seluruh isi dalam dictionary, kita juga dapat menggunakan keyword `del`. Namun, kali ini kita akan menghapus seluruh dictionary itu sendiri. Penggunaannya seperti berikut :
```python
del infoku
```
- Selain del, kita juga bisa menggunakan metode clear() untuk menghapus semua elemen dalam dictionary, tetapi dictionary itu sendiri tetap ada (hanya menjadi kosong). Penggunaannya seperti berikut :
```python
infoku.clear()
```
Perbedaan `del` dan `clear()` :
- `del`: Menghapus seluruh dictionary atau elemen spesifik. Setelah dihapus, variabel tidak lagi menunjuk ke dictionary.
- `clear()`: Menghapus semua elemen dalam dictionary, tetapi dictionary itu sendiri masih ada (menjadi kosong). Variabel masih menunjuk ke dictionary kosong.

ContohM0503.py adalah contoh penggunaan `del`, `pop()`, `popitem()` dan `clear()`.
##### ContohM0503.py
```python
Mahasiswa = {
    '2313020200':'Darmo Wiyono',
    '2313020222':'Jonatan Arya Santosa',
    '2313020240':'Rivaldo Oktavian Rahmadani',
    '2313020255':'Nazwa Hardiana Gisanov',
    '2313020075':'Aditya Maulana Kurniawan',
    '2313020166':'Sutan Zakaria',
    '2313020110':'Syahrul Putra Mulyana',
    '2313020115':'Puttra Hatti Imanna',
    '2313020213':'Ihza Oka Mahesa',
    '2313020243':'Laila Nabila Rahmanisa'
}
print('Mahasiswa 1:\n',Mahasiswa)
del Mahasiswa['2313020075']
print('Mahasiswa 2:\n',Mahasiswa)
hasilPop1 = Mahasiswa.pop('2313020200')
print('hasilPop1:',hasilPop1)
print('Mahasiswa 3:\n',Mahasiswa)
hasilPop2 = Mahasiswa.pop('2313020200', 'NPM tidak ditemukan')
print('hasilPop2:',hasilPop2)
print('Mahasiswa 4:\n',Mahasiswa)
hasilPop3 = Mahasiswa.popitem()
print('hasilPopitem:',hasilPop3)
print('Tes 5:\n',Mahasiswa)
copyMahasiswa = Mahasiswa.copy()
print('copyMahasiswa 1:\n',copyMahasiswa)
del Mahasiswa
copyMahasiswa.clear()
print('copyMahasiswa 2:\n',copyMahasiswa)
print('Mahasiswa 5:\n',Mahasiswa)
```

Baris ke-30 akan menyebabkan error NameError, karena efek dari perintah `del Mahasiswa`. Sebagaimana telah disampaikan sebelumnya bahwa efek dari perintah `del` akan menyebabkan seluruh dictionary dihapus dan variabel `Mahasiswa` tidak lagi menunjuk ke dictionary.

### 5. Fungsi item(), keys() dan values()
Fungsi `items()` pada dictionary digunakan untuk mengembalikan view object yang berisi pasangan (key, value) dalam bentuk Tuple. Masing-masing elemen dalam view object ini adalah sebuah Tuple yang terdiri dari dua elemen: key dan value-nya. `items()` dapat digunakan untuk membuat dictionary baru berdasarkan pasangan key-value yang ada.

Fungsi `keys()` dan `values()` sangat berguna untuk mengekstrak semua key atau value dari sebuah dictionary dalam bentuk objek yang dapat diiterasi (biasanya berupa `dict_keys` atau `dict_values`). `dict_keys` dan `dict_values`, merupakan view dari dictionary, artinya perubahan pada dictionary akan tercermin pada objek ini. Namun, kita tidak bisa mengubah elemen secara langsung pada objek ini.

Perbedaan `items()`, `keys()` dan `values()`
- `keys()`: Hanya mengembalikan key.
- `values()`: Hanya mengembalikan value.
- `items()`: Mengembalikan pasangan (key, value) dalam bentuk tuple.

ContohM0503.py adalah contoh penggunaan `items()`, `keys()` dan `values()`.
##### ContohM0504.py
```python
Mahasiswa1 = {
    '2313020200':'Darmo Wiyono',
    '2313020222':'Jonatan Arya Santosa',
    '2313020240':'Rivaldo Oktavian Rahmadani',
    '2313020255':'Nazwa Hardiana Gisanov',
    '2313020075':'Aditya Maulana Kurniawan'
}
Mahasiswa2 = {
    '2313020166':'Sutan Zakaria',
    '2313020110':'Syahrul Putra Mulyana',
    '2313020115':'Puttra Hatti Imanna',
    '2313020213':'Ihza Oka Mahesa',
    '2313020243':'Laila Nabila Rahmanisa'
}
list_item1 = list(Mahasiswa1.items())
list_item2 = list(Mahasiswa2.items())
print('list_item1:\n',list_item1)
print('list_item2:\n',list_item2)
Mahasiswa = {}
Mahasiswa.update(Mahasiswa1.items())
Mahasiswa.update(Mahasiswa2.items())
print('Mahasiswa:\n',Mahasiswa)
list_key = list(Mahasiswa.keys())
print('list_key:\n',list_key)
list_value = list(Mahasiswa.values())
print('list_value:\n',list_value)
```

### 6. Operator `in`, `not in` dan `==`
Sama seperti List dan Tuple, operator `in` dan `not in` digunakan untuk memeriksa apakah suatu elemen ada atau tidak ada dalam sebuah Dictionary. Operator `in` mengembalikan True jika key ada sebagai key dalam dictionary, False jika tidak ada. Operator `not in` mengembalikan True jika suatu key atau value tidak ada dalam dictionary.

Operator `==` pada Dictionary akan Mengembalikan True jika kedua dictionary memiliki pasangan key-value yang sama persis, termasuk urutannya.

ContohM0505.py adalah contoh penggunaan operator `in`, `not in` dan `==`.
##### ContohM0505.py
```python
mk1 = dict(kode='INF1011', nama='Pemrograman Berorientasi Obyek')
mk2 = dict(nama='Pemrograman Berorientasi Obyek',kode='INF1011')
mk3 = dict(kode='INF1010', nama='Basis Data II', sks=3)
mk4 = dict(kode='INF1010', nama='Basis Data II', sks=3)
mk5 = dict(kode='INF1010', nama='Basis Data II', sks=2)
cari = 'sks'
print(f'mk1 : {mk1}\nmk2 : {mk2}\nmk3 : {mk3}\nmk4 : {mk4}\nmk5 : {mk5}')
print(f'apakah key "{cari}" ADA di mk1 ? {cari in mk1}')
print(f'apakah key "{cari}" ADA di mk3 ? {cari in mk3}')
print(f'apakah key "{cari}" TIDAK ADA di mk1 ? {cari not in mk1}')
print(f'apakah key "{cari}" TIDAK ADA di mk3 ? {cari not in mk3}')
print('apakah mk1 == mk2 ?', mk1 == mk2)
print('apakah mk3 == mk4 ?', mk3 == mk4)
print('apakah mk3 == mk5 ?', mk3 == mk5)
```

### 7. fungsi `len()`
Fungsi `len()` pada Python digunakan untuk menghitung jumlah elemen dalam suatu objek yang dapat diiterasi, seperti list, tuple, string, dan tentu saja, dictionary. Ketika diterapkan pada dictionary, fungsi `len()` akan menghitung jumlah pasangan key-value yang ada di dalam dictionary tersebut.

ContohM0506.py adalah contoh penggunaan fungsi `len()`.
##### ContohM0506.py
```python
Mahasiswa = {
    '2313020200':'Darmo Wiyono',
    '2313020222':'Jonatan Arya Santosa',
    '2313020240':'Rivaldo Oktavian Rahmadani',
    '2313020255':'Nazwa Hardiana Gisanov',
    '2313020075':'Aditya Maulana Kurniawan',
    '2313020166':'Sutan Zakaria',
    '2313020110':'Syahrul Putra Mulyana',
    '2313020115':'Puttra Hatti Imanna',
    '2313020213':'Ihza Oka Mahesa',
    '2313020243':'Laila Nabila Rahmanisa'
}
print('Banyak pasangan key-value = ',len(Mahasiswa))
```

|[# Awal](../README.md)<br>[# Materi Sebelumnya](../M04/README.md)<br>[# Materi Berikutnya](../M06/README.md)|
|-|