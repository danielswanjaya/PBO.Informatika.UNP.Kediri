# DASAR PYTHON
## Tipe Data Kolektif (Set)
### 1. Membuat Set
Set atau Himpunan adalah objek yang bersifat mutable dengan data yang dikandungnya bersifat unik (tidak ada yang kembar) dan urutan data tidak penting, sama seperti Dictionary. Jika dibandingkan dengan List, Tuple & Dictionary, Set berbeda dalam hal indeks, pengurutan dan keunikan nilai. Set tidak memiliki indeks, sehingga tidak ada mekanisme pengurutan. Sehingga saat memasukan beberapa nilai ke dalam Set, posisi nilai tersebut bisa berada di mana saja, tidak persis seperti apa yang tertulis. Akibat tidak memiliki index, maka tidak memungkinkan menambah nilai baru ke dalam Set dengan cara menulis nomor indeks, seperti List, dan kita tidak bisa mengubah elemen yang sudah ada. Set biasa digunakan untuk :
- Operasi himpunan: Set mendukung operasi-operasi himpunan seperti union, intersection, difference, dan symmetric difference.
- Penghapusan duplikasi: Set dapat digunakan untuk menghapus elemen duplikat dari sebuah list.
- Cek keanggotaan: Anda dapat dengan cepat memeriksa apakah suatu elemen ada dalam set.

Ada 2 cara untuk membuat sebuah Set:
#### 1. Menggunakan Kurung Kurawal `{ }`
Cara paling umum untuk membuat set adalah dengan menggunakan kurung kurawal. Elemen-elemen di dalam set dipisahkan dengan koma. misalnya :
```python
contohSet = {1, 2, 3, "apple", "banana"}
basket = {'Andi','Ilham','Uki','Eko','Odin'}
```
Untuk membuat sebuah Set kosong tidak dapat menggunakan cara : `kosong = {}`, karena akan dianggap sebagai Dictionary.

#### 2. Menggunakan Fungsi set()
Anda juga bisa membuat set dari list, tuple, atau iterable lainnya menggunakan fungsi set(). Fungsi ini akan menghapus duplikat dan mengurutkan elemen-elemen secara acak. misalnya :
```python
kosong = set()
contohList = [1, 2, 2, 3, "apple"]
set1 = set(contohList)
contohTuple = (4, 2, 1, 3)
set2 = set(contohTuple)
contohString = 'Informatika'
set2 = set(contohString)
```

ContohM0601.py adalah contoh pembuatan Set dengan beberapa cara.
##### ContohM0601.py
```python
set1 = {}
set2 = set()
set3 = {1, 3, 5, 2, 4}
set4 = {'Andi','Ilham','Uki','Eko','Odin','Andi','Uki'}
set5 = set(['Mojoroto', 14, 24.6, 93010])
print(f'set1 : {set1} tipe : {type(set1)}')
print(f'set2 : {set2} tipe : {type(set2)}')
print(f'set3 : {set3}')
print(f'set4 : {set4}')
print(f'set4 : {set5}')
```

### 2. Menambah elemen Set 
Untuk menambahkan elemen ke dalam sebuah set, kita menggunakan metode `add()`. Untuk menambahkan beberapa elemen sekaligus, Anda bisa menggunakan metode `update()`. Metode ini menerima iterable (seperti list, tuple, atau set) sebagai argumen. ContohM0602.py adalah contoh penambahan elemen Set.
##### ContohM0602.py
```python
tim1 = {'Andi','Ilham','Uki'}
tim1.add('Eko')
tim1.add('Odin')
tim2 = {'Ali','Ilham','Udin'}
list1 = ['Udin','Eko','Oki']
tim2.update(list1)
print(f'tim 1 : {tim1}')
print(f'tim 2 : {tim2}')
tim3 = set()
print(f'tim 3 (awal) : {tim3}')
tim3.update(tim1)
print(f'tim 3 (update 1) : {tim3}')
tim3.update(tim2)
print(f'tim 3 (update 2) : {tim3}')
```

### 3. Hapus elemen Set
Pyton menyediakan 4 cara untuk  menghapus elemen Set, yaitu :
1. Fungsi `remove()` : Menghapus elemen yang spesifik. Jika elemen tidak ditemukan, maka akan menyebabkan KeyError. Misal :
```python
my_set = {1, 2, 3}
my_set.remove(2)
```
2. Fungsi `discard()` : Sama seperti `remove()`, tetapi tidak menimbulkan error jika elemen tidak ditemukan. Misal :
```python
my_set = {1, 2, 3}
my_set.discard(4)
```
3. Fungsi `pop()` : Menghapus dan mengembalikan elemen secara acak. Jika set kosong, akan menimbulkan KeyError. Misal :
```python
my_set = {1, 2, 3}
hasilPop = my_set.pop()
```
4. Fungsi `clear()` : Menghapus semua elemen dalam set. Misal :
```python
my_set = {1, 2, 3}
my_set.clear()
```

ContohM0603.py adalah contoh penghapusan elemen Set.
##### ContohM0603.py
```python
nama = {'Ilham', 'Eko', 'Udin', 'Oki', 'Ali', 'Andi', 'Odin', 'Uki'}
print(f'nama (awal) : {nama}')
nama.remove('Udin')
print(f'nama (setelah remove) : {nama}')
nama.discard('Eka')
nama.discard('Eko')
print(f'nama (setelah discard) : {nama}')
hasilPop = nama.pop()
print(f'hasil pop : {hasilPop}')
print(f'nama (setelah pop) : {nama}')
nama.clear()
print(f'nama (setelah clear) : {nama}')
```

### 4. Fungsi `len()` dan `copy()`
Fungsi `len()` digunakan untuk menghitung jumlah elemen dalam sebuah set. Fungsi ini mengembalikan bilangan bulat yang menunjukkan jumlah elemen dalam set. Fungsi `copy()` digunakan untuk membuat salinan dari sebuah set. Fungsi ini mengembalikan salinan dangkal dari set tersebut. ContohM0606.py adalah contoh penggunaan fungsi `len()` dan `copy()`. Proses penyalinan Set sama seperti pada List, terdapat 2 cara yaitu assignment langsung `=` dan fungsi `copy()`. Akan tetapi lebih disarankan menggunakan fungsi `copy()`, supaya tidak terjadi salah pemberian nilai. ContohM0604.py adalah contoh penggunaan fungsi `len()` dan proses penyalinan Set.
##### ContohM0604.py
```python
nama = {'Andi','Ilham','Uki','Eko','Odin'}
print(f'nama (awal) :\n{nama} ; panjang = {len(nama)}')
copyNama1 = nama.copy()
print(f'copyNama1 (awal) :\n{copyNama1} ; panjang = {len(copyNama1)}')
copyNama1.add('Hari')
print(f'nama (setelah copyNama1.add) :\n{nama} ; panjang = {len(nama)}')
print(f'copyNama1 (setelah copyNama1.add) :\n{copyNama1} ; panjang = {len(copyNama1)}')
copyNama2 = nama
print(f'copyNama2 (awal) :\n{copyNama2} ; panjang = {len(copyNama2)}')
copyNama2.add('Doni')
print(f'nama (setelah copyNama2.add) :\n{nama} ; panjang = {len(nama)}')
print(f'copyNama2 (setelah copyNama2.add) :\n{copyNama2} ; panjang = {len(copyNama2)}')
```

### 5. Operasi himpunan
Set dalam Python sangat berguna untuk melakukan operasi himpunan seperti yang kita pelajari dalam matematika. Operasi himpunan ini sering digunakan untuk memanipulasi data dan memecahkan masalah yang berkaitan dengan keanggotaan dan relasi antara kumpulan data. Operasi Himpunan Utama yang ada yaitu :
1. Union (Gabungan): Menggabungkan semua elemen dari dua set menjadi satu set baru tanpa duplikasi. Gambar 1 adalah Diagram Venn untuk operasi Union. Untuk operasi Union dapat menggunakan fungsi `union()` dan operator `|`. ContohM0605.py adalah contoh operasi Union pada 2 himpunan.

![Gambar 1](https://www.programiz.com/sites/tutorial2program/files/python-union.png)<br>Gambar 1. Diagram Venn untuk operasi Union.
##### ContohM0605.py
```python
tim1 = {'Andi','Ilham','Uki','Eko','Odin'}
tim2 = {'Ali','Ilham','Udin','Eko','Oki'}
tim3 = {'Nata','Soni','Catur','Feri','Heru'}
union1 = tim1 | tim2
union2 = tim1.union(tim3)
union3 = tim2.union(tim3)
print(f'tim1 : {tim1}\ntim2 : {tim2}\ntim3 : {tim3}')
print(f'union1 : {union1}\nunion2 : {union2}\nunion3 : {union3}')
```
2. Intersection (Irisan): Menemukan elemen-elemen yang sama di antara dua set. Gambar 2 adalah Diagram Venn untuk operasi Intersection. Untuk operasi Union dapat menggunakan fungsi `intersection()` dan operator `&`. ContohM0606.py adalah contoh operasi Intersection pada 2 himpunan.

![Gambar 2](https://www.programiz.com/sites/tutorial2program/files/python-intersection.png)<br>Gambar 2. Diagram Venn untuk operasi Intersection.
##### ContohM0606.py
```python
tim1 = {'Andi','Ilham','Uki','Eko','Odin'}
tim2 = {'Ali','Ilham','Udin','Eko','Oki'}
tim3 = {'Nata','Soni','Catur','Feri','Heru'}
irisan1 = tim1 & tim2
irisan2 = tim1.intersection(tim3)
irisan3 = tim2.intersection(tim3)
print(f'tim1 : {tim1}\ntim2 : {tim2}\ntim3 : {tim3}')
print(f'irisan1 : {irisan1}\nirisan2 : {irisan2}\nirisan3 : {irisan3}')
```
3. Difference (Selisih): Menemukan elemen-elemen yang ada di set pertama tetapi tidak ada di set kedua. Gambar 3 adalah Diagram Venn untuk operasi Difference. Untuk operasi Union dapat menggunakan fungsi `difference()` dan operator `-`. ContohM0607.py adalah contoh operasi Difference pada 2 himpunan.

![Gambar 3](https://www.programiz.com/sites/tutorial2program/files/python-difference.png)<br>Gambar 3. Diagram Venn untuk operasi Difference.
##### ContohM0607.py
```python
tim1 = {'Andi','Ilham','Uki','Eko','Odin'}
tim2 = {'Ali','Ilham','Udin','Eko','Oki'}
tim3 = {'Nata','Soni','Catur','Feri','Heru'}
selisih1a = tim1 - tim2
selisih1b = tim2 - tim1
selisih2a = tim1.difference(tim3)
selisih2b = tim3.difference(tim1)
selisih3a = tim2.difference(tim3)
selisih3b = tim3.difference(tim2)
print(f'tim1 : {tim1}\ntim2 : {tim2}\ntim3 : {tim3}')
print(f'selisih1a : {selisih1a}\nselisih1b : {selisih1b}')
print(f'selisih2a : {selisih2a}\nselisih2b : {selisih2b}')
print(f'selisih3a : {selisih3a}\nselisih3b : {selisih3b}')
```
4. Symmetric Difference (Selisih Simetris): Menemukan elemen-elemen yang ada di salah satu set tetapi tidak di keduanya. Gambar 4 adalah Diagram Venn untuk operasi Symmetric Difference. Untuk operasi Union dapat menggunakan fungsi `symmetric_difference()` dan operator `^`. ContohM0608.py adalah contoh operasi Symmetric Difference pada 2 himpunan.

![Gambar 4](https://www.programiz.com/sites/tutorial2program/files/python-symmetric-difference.png)<br>Gambar 4. Diagram Venn untuk operasi Symmetric Difference.
##### ContohM0608.py
```python
tim1 = {'Andi','Ilham','Uki','Eko','Odin'}
tim2 = {'Ali','Ilham','Udin','Eko','Oki'}
tim3 = {'Nata','Soni','Catur','Feri','Heru'}
selisih1 = tim1 ^ tim2
selisih2 = tim1.symmetric_difference(tim3)
selisih3 = tim2.symmetric_difference(tim3)
print(f'tim1 : {tim1}\ntim2 : {tim2}\ntim3 : {tim3}')
print(f'selisih1 : {selisih1}\nselisih2 : {selisih2}\nselisih3 : {selisih3}')
```
### 5. Operator `in`, `not in`, `==`, `!=`, `<`, `<=`, `>`, `>=` dan fungsi `isdisjoint()`
- Operator `in` digunakan untuk memeriksa apakah suatu elemen ada dalam sebuah set. Jika elemen tersebut ditemukan, operator in mengembalikan True, jika tidak, mengembalikan False.
- Operator `not in` adalah kebalikan dari `in`. Operator `not in` mengembalikan True jika suatu elemen tidak ditemukan dalam set, dan False jika ditemukan.
- Operator `==` : Mengecek apakah dua set memiliki elemen yang persis sama. Urutan elemen tidak penting.
- Operator `!=` : Kebalikan dari ==. Mengecek apakah dua set tidak sama persis.
- Operator `<` : Perintah `A < B` atau `A.issubset(B)` (A is a proper subset of B (A ⊂ B)) berarti A adalah subset dari B, tetapi A tidak sama dengan B. Atau, ada setidaknya satu elemen di B yang tidak ada di A. Dengan kata lain, himpunan A "terkandung sepenuhnya" dalam himpunan B, tetapi himpunan B memiliki elemen tambahan yang tidak dimiliki A.
- Operator `<=` : Perintah `A <= B` (A is a subset of B (A ⊆ B)) berarti setiap elemen yang ada di himpunan A juga pasti ada di himpunan B. Dengan kata lain, himpunan A "terkandung sepenuhnya" dalam himpunan B.
- Operator `>` : Perintah `A > B` atau `A.issuperset(B)` (A is a proper superset of B (A ⊃ B)) berarti A adalah superset dari B, tetapi B tidak sama dengan A. Atau, ada setidaknya satu elemen di A yang tidak ada di B. Dengan kata lain, himpunan B "terkandung sepenuhnya" dalam himpunan A, tetapi himpunan A memiliki elemen tambahan yang tidak dimiliki B.
- Operator `>=` : Perintah `A >= B` (A is a superset of B (A ⊇ B)) berarti setiap elemen yang ada di himpunan B juga pasti ada di himpunan A. Dengan kata lain, himpunan B "terkandung sepenuhnya" dalam himpunan A.
- Fungsi `isdisjoint()` : Perintah `A.isdisjoint(B)` atau `B.isdisjoint(A)` berarti himpunan A dan himpunan B tidak memiliki elemen yang sama. Dengan kata lain, irisan (intersection) dari himpunan A dan B adalah himpunan kosong.

ContohM0609.py adalah contoh penggunaan dari operator `in`, `not in`, `==`, `!=`, `<`, `<=`, `>`, `>=` dan fungsi `isdisjoint()`.
##### ContohM0609.py
```python
nama = {'Ilham', 'Eko', 'Udin', 'Oki', 'Ali', 'Andi', 'Odin', 'Uki'}
tim1 = {'Andi','Ilham','Uki','Eko','Odin'}
tim2 = {'Nata','Soni','Catur','Feri','Heru'}
tim3 = set()
cari1, cari2 = 'Eko', 'Soni'
print(f'nama: {nama}\ntim1: {tim1}\ntim2: {tim2}')
print(f'tim3: {tim3}\ncari1: {cari1}\ncari2: {cari2}\n')
print(f'apakah cari1 ADA di nama ? {cari1 in nama}')
print(f'apakah cari2 ADA di nama ? {cari2 in nama}')
print(f'apakah cari1 TIDAK ADA di nama ? {cari1 not in nama}')
print(f'apakah cari2 TIDAK ADA di nama ? {cari2 not in nama}\n')
print(f'tim1 < nama : {tim1 < nama} ; tim1.issubset(nama) : {tim1.issubset(nama)}')
print(f'tim2 < nama : {tim2 < nama} ; tim2.issubset(nama) : {tim2.issubset(nama)}')
print(f'tim3 < nama : {tim3 < nama} ; tim3.issubset(nama) : {tim3.issubset(nama)}\n')
print(f'nama > tim1 : {nama > tim1} ; nama.issuperset(tim1) : {nama.issuperset(tim1)}')
print(f'nama > tim2 : {nama > tim2} ; nama.issuperset(tim2) : {nama.issuperset(tim2)}')
print(f'nama > tim3 : {nama > tim3} ; nama.issuperset(tim3) : {nama.issuperset(tim3)}')
tim4 = {'Andi','Ilham','Feri','Heru'}
tim5 = tim1.copy()
print(f'\ntim4: {tim4}')
print(f'\ntim5: {tim5}')
print(f'tim1 == tim4 : {tim1 == tim5} ; tim1 != tim4 : {tim1 != tim5}')
print(f'tim1 == tim2 : {tim1 == tim2} ; tim1 != tim2 : {tim1 != tim2}')
print(f'tim1.isdisjoint(tim2): {tim1.isdisjoint(tim2)}')
print(f'tim4.isdisjoint(nama): {tim4.isdisjoint(nama)}')
print(f'tim1 < tim5 : {tim1 < tim5} ; tim1 <= tim5 : {tim1 <= tim5}')
print(f'tim1 > tim5 : {tim1 > tim5} ; tim1 >= tim5 : {tim1 >= tim5}')
tim6 = {'Andi','Eko'}
```

|[# Awal](../README.md)<br>[# Materi Sebelumnya](../M05/README.md)<br>[# Materi Berikutnya](../M07/README.md)|
|-|