# DASAR PYTHON
## Tipe Data Kolektif (Tuple)
### 1. Membuat Tuple
Tuple adalah salah satu tipe data koleksi dalam Python yang mirip dengan list, namun dengan satu perbedaan utama yaitu tuple bersifat **immutable**. Artinya, setelah sebuah tuple dibuat, elemen-elemen di dalamnya **tidak dapat diubah**, ditambahkan, atau dihapus. Tupel menggunakan
symbol tanda kurung `( )` (Namun bisa juga tanpa tanda kurung), sedangkan List Python menggunakan tanda kurung siku `[ ]`. Elemen Tuple bisa berupa tipe data apa pun. Berikut contoh pembuatan Tuple :

```python
kosong = ()
label1 = ('Prodi','Fakultas','Universitas')
label2 = 'Teknik Informatika','Teknik & Ilmu Komputer','Universitas Nusantara PGRI Kediri'
tahun = (2020, 2021, 2022, 2024, 2025)
biodata = ('2013020012', 'Donny Firdani', 160.5, 83, True)
anggota = ('Andi',)
nomor = (1,)
```

### 2. Indexing pada Tuple
Indexing pada Tuple sama seperti pada List. Data indeks idx dari Tuple `TUPLE` dapat diakses dengan cara `TUPLE[idx]`. ContohM0401.py adalah contoh pembuatan Tuple dan pengaksesan nilai dalam Tuple.

##### ContohM0401.py
```python
label = ('Prodi','Fakultas','Universitas')
isi = 'Teknik Informatika','Teknik & Ilmu Komputer','Universitas Nusantara PGRI Kediri'
print(label)
print(isi)
print(label[0],':',isi[-3])
print(label[1],':',isi[-2])
print(label[2],':',isi[-1])
```

### 3. Slicing pada Tuple
Sama seperti list, slicing pada Tuple menggunakan notasi [start:stop:step]. 
ContohM0402.py adalah beberapa contoh penggunaan Slicing pada List.
##### ContohM0402.py
```python
fruits = ('Apple','Banana','Orange','Grape','Strawberry','Mango','Pineapple','Watermelon','Avocado','Cherry','Pear')
print('Tes 01: ',fruits[2:8:2])
print('Tes 02: ',fruits[-9:-3:2])
print('Tes 03: ',fruits[8:2:-2])
print('Tes 04: ',fruits[-3:-9:-2])
print('Tes 05: ',fruits[3:])
print('Tes 06: ',fruits[3::])
print('Tes 07: ',fruits[-8::])
print('Tes 08: ',fruits[:3])
print('Tes 09: ',fruits[:3:])
print('Tes 10: ',fruits[:-8:])
print('Tes 11: ',fruits[::3])
print('Tes 12: ',fruits[::-3])
print('Tes 13: ',fruits[-5::-2])
print('Tes 14: ',fruits[-2::-5])
print('Tes 15: ',fruits[2:8])
print('Tes 16: ',fruits[-9:-3])
print('Tes 17: ',fruits[8:2])
print('Tes 18: ',fruits[-3:-9])
```

### 4. Penyalinan Tuple
Proses penyalinan suatu Tuple dapat menggunakan 2 cara berikut :
- Cara ke-1 : `TupleA = TupleB`
- Cara ke-2 : `TupleA = TupleB[:]`

Karena elemen pada Tuple tidak dapat diubah, maka kedua cara tersebut tidak memiliki perbedaan seperti pada List. ContohM0403.py adalah contoh penyalinan Tuple.
##### ContohM0402.py
```python
fruits = ('Apple','Banana','Orange','Grape','Strawberry')
copy1 = fruits[:]
copy2 = fruits
print('copy1 =',copy1)
print('copy3 =',copy2)
```

### 5. Metode bawaan Tuple
Karena Tuple adalah tipe data yang tidak dapat diubah (immutable), Python hanya menyediakan beberapa fungsi bawaan yang berguna untuk memanipulasi dan mendapatkan informasi dari Tuple, seperti pada Tabel 1.

##### Tabel 1. Metode bawaan untuk mengolah Tuple
|Fungsi|Keterangan|
|-|-|
|`len(T)`|Mengembalikan jumlah elemen dalam tuple T.|
|`min(T)`|Mengembalikan nilai terkecil dalam tuple T.<br>Hanya bisa digunakan untuk tuple yang berisi elemen yang dapat dibandingkan (angka, karakter).|
|`max(T)`|Mengembalikan nilai terbesar dalam tuple T.<br>Sama seperti `min()`, hanya bisa digunakan untuk elemen yang dapat dibandingkan.|
|`sum(T)`|Menghitung jumlah semua elemen dalam tuple T.<br>Hanya bisa digunakan untuk tuple yang berisi angka.|
|`T.count(var)`|Menghitung jumlah kemunculan elemen var dalam tuple T.|
|`sorted(T)`|Mengembalikan **list** baru yang berisi elemen-elemen tuple T yang telah diurutkan.<br>Tuple asli tidak berubah.|
|`reversed(T)`|Mengembalikan iterator yang iterasi melalui elemen-elemen tuple T dalam urutan terbalik.|
|`tuple(iterable)`|Mengubah iterable (seperti list, string) menjadi tuple.|
|`T.index(var)`|Mengembalikan indeks pertama dari var yang pertama ditemukan dalam tuple T.|
|`T.index(var,idx)`|Mengembalikan indeks pertama dari item yang pertama ditemukan dalam tuple T, pencarian dimulai dari indeks `idx`.|
|`T.index(var,idx1,idx2)`|Mengembalikan indeks pertama dari item yang pertama ditemukan dalam tuple T, pencarian dilakukan dari indeks `idx` hingga indeks ke-(`idx2`-1).|

ContohM0404.py adalah contoh penggunaan metode len(), count(), max(), min() dan sum().
##### ContohM0404.py
```python
data = (1, 2, 3, 4, 3, 5, 3, 2, 1, 3)
panjang_tuple = len(data)
banyak_tiga = data.count(3)
nilai_maks = max(data)
nilai_min = min(data)
total = sum(data)
print('data = ',data)
print("Panjang tuple:", panjang_tuple)
print("Banyak angka 3:", banyak_tiga)
print("Nilai maksimum:", nilai_maks)
print("Nilai minimum:", nilai_min)
print("Jumlah semua elemen:", total)
```

ContohM0405.py adalah contoh penggunaan metode sorted(), reversed() & tuple().
##### ContohM0404.py
```python
fruits = ('apple', 'banana', 'cherry', 'plums', 'apple', 'banana', 'cherry', 'apple', 'banana')
fruits1 = sorted(fruits)
fruits2 = sorted(fruits, reverse=True)
fruits3 = tuple(reversed(fruits))
print('fruits = ', fruits)
print('fruits1 = ', fruits1)
print('fruits2 = ', fruits2)
print('fruits3 = ', fruits3)
```

ContohM0406.py adalah contoh penggunaan metode index().
##### ContohM0406.py
```python
fruits = ['apple', 'banana', 'cherry', 'plums', 'apple', 'banana', 'cherry', 'apple', 'banana']
print(fruits.index('apple'))
print(fruits.index('apple',3))
print(fruits.index('apple',5,8))
```

ContohM0407.py adalah contoh penggunaan metode tuple(), untuk mengubah setiap karakter dalam string akan menjadi elemen dalam tuple & mengubah hasil dari fungsi range() akan menjadi elemen dalam tuple.
##### ContohM0407.py
```python
teks = 'Informatika'
tupleTeks = tuple(teks)
tupleRange = tuple(range(10,50,5))
print('tupleTeks = ',tupleTeks)
print('tupleRange = ',tupleRange)
```

### 6. operator `+`, `in`, `not in`, `*` dan `==`
Sama seperti List, 
- operator `+` digunakan untuk menggabung 2 tuple, menjadi 1 tuple baru
- operator `in` dan `not in` digunakan untuk memeriksa apakah suatu elemen ada atau tidak ada dalam sebuah tuple di Python.
- Operator `*` pada tuple di Python digunakan untuk mengulang suatu tuple sebanyak n kali, di mana n adalah angka yang dikalikan dengan tuple tersebut.
- Operator `==` pada list digunakan untuk membandingkan apakah dua buah tuple memiliki elemen yang sama dalam urutan yang sama.

ContohM0408.py adalah contoh penggunaan Operator `in`, `not in`, `*` dan `==`.
##### ContohM0408.py
```python
fruits = ('apple', 'avocados', 'banana', 'cherry', 'plums', 'kiwis', 'lemons')
fruits1 = ('apple', 'avocados', 'banana') + ('cherry', 'plums', 'kiwis', 'lemons')
fruits2 = ('orange',) * 3
fruits3 = ('orange','lemons') * 2
fruits4 = ('apple', 'banana', 'cherry')
cari1 = 'apple'
cari2 = 'orange'
cek1 = ('apple', 'banana')
cek2 = ('apple', 'banana', 'cherry')
cek3 = ('banana', 'cherry', 'apple')
print('fruits: ',fruits)
print(f'Apakah "{cari1}" ADA di dalam tuple ? {(cari1 in fruits)}')
print(f'Apakah "{cari1}" TIDAK ADA di dalam tuple ? {(cari1 not in fruits)}')
print(f'Apakah "{cari2}" ADA di dalam tuple ? {(cari2 in fruits)}')
print(f'Apakah "{cari2}" TIDAK ADA di dalam tuple ? {(cari2 not in fruits)}')
print('fruits1: ',fruits1)
print('fruits2: ',fruits2)
print('fruits3: ',fruits3)
print('fruits4: ',fruits4)
print('cek1: ',cek1)
print('cek2: ',cek2)
print('cek3: ',cek3)
print('cek1 == fruits2: ',(cek1 == fruits4))
print('cek2 == fruits2: ',(cek2 == fruits4))
print('cek3 == fruits2: ',(cek3 == fruits4))
```

### 7. Modifikasi elemen tuple
Sifat dasar dari tuple, yaitu bersifat immutable atau tidak dapat diubah setelah dibuat. Berbeda dengan list yang bersifat mutable dan memungkinkan elemennya diubah, tuple dirancang untuk menyimpan data yang tidak perlu diubah setelah dibuat. Akan tetapi, jika kita ingin mengubah data dalam tuple, berikut beberapa alternatif yang mungkin bisa dilakukan :
#### 1. Bantuan List
Alternatif ini cocok untuk kasus dimana tuple perlu proses penghapusan dan pengubahan.
1. Ekstrak elemen yang ingin diubah: Gunakan slicing untuk mengambil bagian dari tuple yang ingin diubah.
2. Buat list baru: Ubah hasil slicing menjadi list.
3. Modifikasi list: Ubah elemen yang diinginkan dalam list.
4. Ubah kembali menjadi tuple: Ubah list yang sudah dimodifikasi menjadi tuple baru.

ContohM0409.py adalah contoh modifikasi tuple dengan bantuan list
##### ContohM0409.py
```python
fruits = ('Apple','Banana','Orange','Grape','Strawberry','Mango','Pineapple','Watermelon','Avocado','Cherry','Pear')
listFruits = list(fruits)
listFruits.remove('Strawberry')
listFruits.remove('Pineapple')
listFruits.remove('Watermelon')
listFruits.insert(2, 'Citrus')
listFruits.insert(5, 'Melons')
listFruits.append('Guava')
fruitsNew = tuple(fruits)
print('fruits: ',fruits)
print('listFruits: ',listFruits)
print('fruitsNew: ',fruitsNew)
```
#### 2. Tuple baru hasil penggabungan slicing
Alternatif ini cocok untuk kasus dimana tuple hanya perlu penyisipan atau penambahan elemen. ContohM0410.py adalah contoh modifikasi tuple dengan penggabungan slicing.
##### ContohM0410.py
```python
fruits = ('Apple','Banana','Orange','Grape')
print('Awal :\n',fruits)
fruits = fruits + ('Mango','Pineapple','Watermelon','Avocado','Cherry','Pear')
print('Setelah penambahan :\n',fruits)
fruits = fruits[:4] + ('Strawberry',) + fruits[4:]
print('Setelah penyisipan :\n',fruits)
```

### 8. Swapping
Swapping pada Tuple tidak sebebas pada List. Karena Tuple di Python bersifat immutable atau tidak dapat diubah setelah dibuat. Sehingga kita hanya bisa menukar nilai dari dua variabel secara simultan. Dalam hal ini berarti kita akan menukar seluruh konten dari tuple pertama dengan kedua, dan sebaliknya. ContohM0411.py adalah contoh swapping dari 2 buah tuple.

##### ContohM0411.py
```python
fruits1 = ('Apple','Pineapple','Mango','Guava','Blueberry')
fruits2 = ('Banana','Watermelon','Avocado','Strawberry')
print(f'Awal\nfruits1: {fruits1}\nfruits2: {fruits2}')
fruits1, fruits2 = fruits2, fruits1
print(f'Setelah swapping\nfruits1: {fruits1}\nfruits2: {fruits2}')
```

|[# Awal](../README.md)<br>[# Materi Sebelumnya](../M03/README.md)<br>[# Materi Berikutnya](../M05/README.md)|
|-|