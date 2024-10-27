# FUNCTION
## Lambda, Fungsi Rekursif dan Standard Library Function
### 1. Lambda Function (Fungsi Tidak Bernama)
Suatu fungsi bisa didefinisikan tanpa nama dan dinamakan fungsi anonim (anonymous function) atau sering disebut Lambda Function. Jika fungsi biasa dalam Python didefinisikan menggunakan kata kunci `def` dan harus diberi nama, Lambda Function didefinisikan menggunakan kata kunci `lambda` dan tidak memerlukan nama. Alasan inilah yang menjadikannya lebih ringkas dan hemat waktu dalam penulisan kode. Dengan Format seperti berikut :
```python
lambda arg1 : ekspresi
# atau
lambda arg1, arg2 : ekspresi
```
Lambda Function sering digunakan untuk melakukan operasi yang sederhana dan cepat pada data, tanpa perlu mendefinisikan fungsi secara eksplisit. Cara kerja Lambda Function yaitu dengan membaca argumen yang diberikan, lalu melakukan operasi pada argumen tersebut dan mendapatkan hasil akhir. Lambda Function mengembalikan nilai, tetapi tidak memiliki return statement secara eksplisit. Nilai yang dikembalikan adalah hasil dari ekspresi yang diberikan. Tetapi Lambda Function hanya dapat digunakan untuk membuat satu function / expression, tidak cocok untuk fungsi yang membutuhkan banyak baris kode. Lambda Function sering digunakan sebagai argumen untuk fungsi-fungsi built-in seperti `map`, `filter`, dan `sorted`.

ContohM1201.py adalah contoh penggunaan Lambda Function dengan satu parameter, untuk operasi matematika sederhana.
#### ContohM1201.py
```python
kuadrat = lambda x: x**2
akar = lambda x: x**0.5
negate = lambda x: -x
is_odd = lambda x: x % 2 == 1
is_even = lambda x: x % 2 == 0

angka = int(input('Masukan sebuah bilangan:'))
print(f'Hasil Kuadrat: {kuadrat(angka)}')
print(f'Hasil Akar Kuadrat: {akar(angka)}')
print(f'Hasil Negasi: {negate(angka)}')
print(f'Apakah Ganjil? {'Ya' if is_odd(angka) else 'Tidak'}')
print(f'Apakah Genap? {'Ya' if is_even(angka) else 'Tidak'}')
```

ContohM1202.py adalah contoh penggunaan Lambda Function dengan dua parameter, untuk operasi matematika sederhana.
#### ContohM1202.py
```python
add = lambda x, y: x + y
subtract = lambda x, y: x - y
multiply = lambda x, y: x * y
greater_than = lambda x, y: x > y
less_than = lambda x, y: x < y

angka1 = int(input('Masukan bilangan pertama:'))
angka2 = int(input('Masukan bilangan kedua  :'))
print(f'{angka1} + {angka2} = {add(angka1, angka2)}')
print(f'{angka1} - {angka2} = {subtract(angka1, angka2)}')
print(f'{angka1} * {angka2} = {multiply(angka1, angka2)}')
print(f'{angka1} > {angka2} = {greater_than(angka1, angka2)}')
print(f'{angka1} < {angka2} = {less_than(angka1, angka2)}')
```

ContohM1203.py adalah contoh penggunaan Lambda Function untuk mengolah 2 String.
#### ContohM1203.py
```python
join_strings = lambda s1, s2, separator: s1 + separator + s2
compare_length = lambda s1, s2: s1 if len(s1) > len(s2) else s2
ejaan = lambda s1, s2 : set(s1.lower()) == set(s2.lower())
huruf_sama = lambda s1, s2: set(s1.lower()).intersection(set(s2.lower()))

kata1 = input('Masukan kata pertama:')
kata2 = input('Masukan kata kedua  :')
print(f'Gabungan: {join_strings(kata1,kata2,' & ')}')
print(f'"{kata1}" lebih panjang dari "{kata2}" = {compare_length(kata1,kata2)}')
print(f'Apakah Huruf penyusunnya yang sama? {'Ya' if huruf_sama(kata1,kata2) else 'Tidak'}')
print(f'Huruf penyusun yang sama: {huruf_sama(kata1,kata2)}')
```

ontohM1204.py adalah contoh penggunaan Lambda Function untuk mengolah sebuah List.
#### ContohM1204.py
```python
numbers = [range(1,11)]

squared_numbers = list(map(lambda x: x**2, numbers))
odd_numbers = list(filter(lambda x: x % 2 == 1, numbers))
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

print('Kuadrat:',squared_numbers)
print('Ganjil:',odd_numbers)
print('Genap:',even_numbers)
```

Fungsi `map()` adalah salah satu fungsi bawaan (built-in) dalam Python yang sangat berguna untuk menerapkan suatu fungsi pada setiap elemen dari suatu iterable (seperti list, tuple, atau string) dan mengembalikan hasil sebagai objek map. Objek map ini kemudian dapat diubah menjadi list, tuple, atau tipe data iterable lainnya jika diperlukan. Fungsi `map()` memiliki 2 parameter : `function` & `iterable`. `function` adalah fungsi yang akan diterapkan pada setiap elemen iterable. `iterable` adalah Iterable (seperti list, tuple, string, dll.) yang berisi elemen-elemen yang akan diproses. Cara kerja fungsi map adalah :
1. Fungsi `map()` akan mengambil setiap elemen dari `iterable`.
2. Setiap elemen tersebut akan dijadikan argumen untuk fungsi yang diberikan.
3. Hasil dari penerapan fungsi pada setiap elemen akan disimpan dalam objek map.
4. Objek map ini dapat diubah menjadi tipe data lain yang diinginkan, seperti list atau tuple.

Fungsi `filter()` adalah fungsi bawaan (built-in) dalam Python yang digunakan untuk menyaring elemen-elemen dari suatu iterable (seperti list, tuple, atau string) berdasarkan kondisi tertentu. Fungsi ini akan mengembalikan sebuah objek filter yang berisi elemen-elemen yang memenuhi kondisi tersebut. Argumen dan cara kerjanya sama dengan fungsi `map()`.

ContohM1205.py adalah contoh penggunaan Function dengan return value dan Lambda Function untuk konversi suhu Celcius ke Fahrenheit, Reamur, dan Kelvin.
#### ContohM1205.py
```python
import random

def konversi_suhu(celsius):
    """
    Fungsi untuk mengkonversi suhu dari Celcius ke Fahrenheit, Reamur, dan Kelvin.
    Args:
        celsius: Suhu dalam Celcius.
    Returns:
        Tuple yang berisi suhu dalam Fahrenheit, Reamur, dan Kelvin.
    """
    fahrenheit = lambda c: (c * 9/5) + 32
    reamur = lambda c: (c * 4/5)
    kelvin = lambda c: c + 273.15
    return celsius, fahrenheit(celsius), reamur(celsius), kelvin(celsius)

if __name__ == "__main__":
    jumlah_data = int(input("Masukkan jumlah data yang ingin dikonversi: "))
    data_celcius = [random.random() * 100 for _ in range(jumlah_data)]
    hasil_konversi = list(map(konversi_suhu, data_celcius))

    print("-" * 42)
    print("| Celcius | Fahrenheit | Reamur | Kelvin |")
    print("-" * 42)
    for celsius, fahrenheit, reamur, kelvin in hasil_konversi:
        print(f"| {celsius:7.2f} | {fahrenheit:10.2f} | {reamur:6.2f} | {kelvin:6.2f} |")
    print("-" * 42)
```

ContohM1206.py adalah contoh pembuatan fungsi untuk 
#### ContohM1206.py
```python
data = [('Alice', 30), ('Wati', 29), ('Bob', 25), ('Charlie', 30), ('Joko', 31), ('David', 28)]

data_sorted_biasa = sorted(data)
data_sorted_lambda = sorted(data, key=lambda x: (-x[1], x[0]))

print('PENGURUTAN DATA')
print('data_sorted_biasa :',data_sorted_biasa)
print('data_sorted_lambda:',data_sorted_lambda)
```

ContohM1207.py adalah contoh penggunaan Lambda Function untuk membuat fungsi yang lebih dinamis, dimana fungsi yang menerima operator aritmatika sebagai parameter.
#### ContohM1207.py
```python
def apply_operation(x, y, operator):
    """
    Menerapkan operasi aritmatika pada dua bilangan.
    Args:
        x: Bilangan pertama.
        y: Bilangan kedua.
        operator: Operator aritmatika (+, -, *, /).
    Returns:
        Hasil operasi.
    Raises:
        ValueError: Jika operator tidak valid.
    """
    operations = {
        '+': lambda x, y: x + y,
        '-': lambda x, y: x - y,
        '*': lambda x, y: x * y,
        '/': lambda x, y: x / y
    }
    if operator not in operations:
        raise ValueError("Operator tidak valid")

    return operations[operator](x, y)

print('OPERASI ARITMATIKA')
print('apply_operation(5, 3, "+") =',apply_operation(5, 3, '+'))
print('apply_operation(17, 8, "-")=',apply_operation(17, 8, '-'))
print('apply_operation(10, 2, "/")=',apply_operation(10, 2, '/'))
print('apply_operation(7, 4, "*") =',apply_operation(7, 4, '*'))

print('apply_operation(2, 3, "^") =',end=' ')
try:
  print(apply_operation(2, 3, '^'))
except ValueError as e:
  print(e)
```
Pada baris ke-20 terdapat keyword `raise`, Keyword `raise` dalam Python digunakan untuk secara sengaja memunculkan sebuah pengecualian (exception). Pengecualian adalah suatu peristiwa yang mengganggu aliran normal eksekusi program. Ketika sebuah pengecualian terjadi, Python akan mencari blok try...except yang sesuai untuk menangani pengecualian tersebut. Jika tidak ditemukan, program akan berhenti dengan pesan kesalahan. (Lihat kembali [M02](../M02/README.md) bagian ContohM0207.py). Keyword `raise` biasa digunakan untuk:
* Menandai Kondisi Error: Ketika suatu kondisi yang tidak diharapkan terjadi, kita bisa menggunakan `raise` untuk menandainya sebagai sebuah error.
* Membuat Fungsi yang Lebih Robust: Dengan menggunakan `raise`, kita dapat membuat fungsi yang lebih aman dengan cara membatasi input yang valid dan memunculkan pengecualian jika input tidak sesuai.
* Mengontrol Aliran Program: Kita bisa menggunakan `raise` untuk mengontrol aliran program secara eksplisit, misalnya untuk keluar dari sebuah loop atau fungsi ketika kondisi tertentu terpenuhi.

Sintaks umum :
```python
raise ExceptionType("Pesan error")
```
dimana :
* `ExceptionType`: Jenis pengecualian yang ingin dibangkitkan. Ini bisa berupa pengecualian bawaan Python seperti ValueError, TypeError, IndexError, atau pengecualian yang kita definisikan sendiri.
* `"Pesan error"`: Pesan yang akan ditampilkan ketika pengecualian terjadi. Pesan ini akan membantu kita dalam men-debug program.

Misal pada ContohM1207 baris ke-7, fungsi `apply_operation` akan memunculkan pengecualian `ValueError` jika karakter `operator` selain `+`, `-`, `*` dan `/`. Blok try...except (baris ke-31 s.d 34) digunakan untuk menangkap pengecualian yang mungkin terjadi. Jika terjadi `ValueError`, pesan error yang kita definisikan akan ditampilkan.

ContohM1208.py adalah contoh penggunaan Lambda Function untuk menghitung Permutasi dan Kombinasi (modifikasi dari ContohM1112.py)
#### ContohM1208.py
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

permutasi = lambda n, r:faktorial(n)/faktorial(n-r)
kombinasi = lambda n, r:faktorial(n)/(faktorial(r)*faktorial(n-r))

print('HITUNG NILAI PERMUTASI DAN KOMBINASI')
n = int(input('Total Elemen:'))
r = int(input('Banyak Elemen yang dipilih:'))

hasil_permutasi = permutasi(n, r)
hasil_kombinasi = kombinasi(n, r)

print("Permutasi P(", n, ",", r, ") = ", hasil_permutasi)
print("Kombinasi C(", n, ",", r, ") = ", hasil_kombinasi)
```

ContohM1209.py adalah contoh penggunaan Lambda Function untuk menghitung jarak 2 titik koordinat, dan penerapannya untuk mencari pasangan titik yang mempunyai jarak paling dekat.
#### ContohM1209.py
```python
import random
import math

def buat_titik_acak(N):
    """
    Membuat N titik koordinat kartesius secara acak dalam rentang 0 hingga 10.
    Hasil dikembalikan dalam bentuk dictionary, dengan key berupa huruf alfabet dan
    value berupa tuple koordinat.
    Args:
        N (int): Jumlah titik yang akan dibuat.
    Returns:
        dict: Dictionary yang berisi titik-titik dengan nama dan koordinatnya.
    """
    titik = {}
    huruf = [chr(i) for i in range(ord('A'), ord('Z')+1)]
    for i in range(N):
        if i < 26:
            nama_titik = huruf[i]
        else:
            index_utama = (i - 26) // 26
            index_tambahan = (i - 26) % 26
            nama_titik = huruf[index_utama] + huruf[index_tambahan]
        koordinat = (random.randint(0, 100), random.randint(0, 100))
        titik[nama_titik] = koordinat
    return titik

def buat_matriks_adjacency(titik):
    """
    Membuat matriks adjacency dari dictionary titik.
    Args:
        titik (dict): Dictionary yang berisi titik-titik dengan nama dan koordinatnya.
    Returns:
        list: Matriks adjacency di mana elemennya adalah jarak antara dua titik.
    """
    N = len(titik)
    matriks = [[0] * N for _ in range(N)]
    jarak_titik = lambda titik1, titik2: math.sqrt((titik2[0] - titik1[0])**2 + (titik2[1] - titik1[1])**2)
    for i, nama_i in enumerate(titik):
        for j, nama_j in enumerate(titik):
            if i < j:
                matriks[i][j] = matriks[j][i] = round(jarak_titik(titik[nama_i], titik[nama_j]),3)
    return matriks

def cari_pasangan_terdekat(matriks):
    """
    Mencari pasangan titik terdekat dalam matriks adjacency.
    Args:
        matriks (list): Matriks adjacency.
    Returns:
        tuple: Tuple berisi indeks baris dan kolom pasangan titik terdekat serta jaraknya.
    """
    N = len(matriks)
    jarak_min = float('inf')
    for i in range(N):
        for j in range(i+1, N):
            if 0 < matriks[i][j] < jarak_min:
                jarak_min = matriks[i][j]
                indeks_min = (i, j)
    return indeks_min, jarak_min

def cetak_titik(titik):
    """
    Mencetak semua titik dalam format (nama, x, y).
    Args:
        titik (dict): Dictionary yang berisi titik-titik dengan nama dan koordinatnya.
    """
    for nama, koordinat in titik.items():
        print(f"Titik {nama}: {koordinat}")

if __name__ == "__main__":
    N = int(input("Masukkan jumlah titik: "))
    titik = buat_titik_acak(N)
    print("Semua titik:")
    cetak_titik(titik)
    matriks = buat_matriks_adjacency(titik)
    indeks, jarak = cari_pasangan_terdekat(matriks)
    nama_titik1 = list(titik.keys())[indeks[0]]
    nama_titik2 = list(titik.keys())[indeks[1]]
    print(f"Pasangan titik terdekat: {nama_titik1} {titik[nama_titik1]} dan {nama_titik2} {titik[nama_titik2]}")
    print("Jarak terdekat:", jarak)
```

ContohM1210.py adalah contoh penggunaan Lambda Function untuk penjumlahan dan pengurangan 2 matriks.
#### ContohM1210.py
```python
import random

def generate_matrix(rows, cols):
    """Membuat matriks dengan ukuran rows x cols dengan elemen acak"""
    return [[random.randint(-10, 10) for _ in range(cols)] for _ in range(rows)]

def tambah_matriks(matriks1, matriks2):
    """Menjumlahkan dua matriks menggunakan fungsi lambda"""
    return list(map(lambda baris1, baris2: list(map(lambda x, y: x+y, baris1, baris2)), matriks1, matriks2))

def kurang_matriks(matriks1, matriks2):
    """Mengurangi dua matriks menggunakan fungsi lambda"""
    return list(map(lambda baris1, baris2: list(map(lambda x, y: x-y, baris1, baris2)), matriks1, matriks2))

def cetak(nama, matriks):
    print(nama)
    for row in matriks:
        for col in row:
            print(f'{col:>3}',end=' ')
        print()
    print()

if __name__ == "__main__":
    rows = int(input("Masukkan jumlah baris: "))
    cols = int(input("Masukkan jumlah kolom: "))

    matrixA = generate_matrix(rows, cols)
    matrixB = generate_matrix(rows, cols)
    hasil_tambah = tambah_matriks(matrixA, matrixB)
    hasil_kurang = kurang_matriks(matrixA, matrixB)

    cetak("Matriks A:",matrixA)
    cetak("Matriks B:",matrixB)
    cetak("Hasil penjumlahan:",hasil_tambah)
    cetak("Hasil pengurangan:",hasil_kurang)
```

### 2. Fungsi Rekursif

ContohM1210.py adalah contoh pembuatan fungsi untuk 
#### ContohM1211.py
```python
```

### 3. Standard Library Function (Built-in Function)