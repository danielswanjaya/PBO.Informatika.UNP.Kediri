# DASAR PYTHON
## Tipe Data Kolektif Kompleks
### 1. Nested List
Nested list, atau list bersarang, adalah sebuah konsep di Python di mana sebuah list dapat berisi elemen yang juga merupakan list. Ini memungkinkan Anda untuk membuat struktur data yang lebih kompleks dan hierarkis. Bayangkan sebuah kotak yang berisi kotak-kotak kecil di dalamnya, dan kotak-kotak kecil itu juga bisa berisi kotak lagi.

Nested List biasa digunakan untuk :
- Representasi Data Multidimensi: Nested list sangat berguna untuk merepresentasikan data multidimensi seperti matriks, tabel, atau bahkan struktur data yang lebih kompleks seperti pohon.
- Organisasi Data: kita dapat mengelompokkan data yang terkait dalam list yang lebih kecil di dalam list yang lebih besar.

Untuk mengakses elemen dalam nested list, kita perlu menggunakan beberapa indeks. Indeks pertama menunjuk ke list luar, dan indeks kedua (atau lebih) menunjuk ke list dalam. ContohM0701.py adalah contoh penggunaan Nested List 2 dimensi.

##### ContohM0701.py
```python
peserta = [
    ['Andri', 20, 90],
    ['Beni', 22, 85],
    ['Catur', 19, 95],
    ['Desi', 21, 87],
]
print(f'peserta[0][0]: {peserta[0][0]}')
print(f'peserta[0][1]: {peserta[0][1]}')
print(f'peserta[0][2]: {peserta[0][2]}')
print(f'peserta[1][0]: {peserta[1][0]}')
print(f'peserta[1][1]: {peserta[1][1]}')
print(f'peserta[1][2]: {peserta[1][2]}')
print(f'peserta[2][0]: {peserta[2][0]}')
print(f'peserta[2][1]: {peserta[2][1]}')
print(f'peserta[2][2]: {peserta[2][2]}')
print(f'peserta[3][0]: {peserta[3][0]}')
print(f'peserta[3][1]: {peserta[3][1]}')
print(f'peserta[3][2]: {peserta[3][2]}\n')
print('-'*18)
print(f'|{'Nama':^6}|{'N':^4}|{'H':^4}|')
print('-'*18)
print(f'|{peserta[0][0]:<6}|{peserta[0][1]:>4}|{peserta[0][2]:>4}|')
print(f'|{peserta[1][0]:<6}|{peserta[1][1]:>4}|{peserta[1][2]:>4}|')
print(f'|{peserta[2][0]:<6}|{peserta[2][1]:>4}|{peserta[2][2]:>4}|')
print(f'|{peserta[3][0]:<6}|{peserta[3][1]:>4}|{peserta[3][2]:>4}|')
print('-'*18)
```

ContohM0702.py adalah contoh penggunaan Nested List 3 dimensi.
##### ContohM0702.py
```python
gambar = [
    [[255, 0, 0], [0, 255, 0], [0, 0, 255], [255, 255, 255]], 
    [[0, 255, 255], [255, 0, 255], [0, 255, 0], [255, 0, 0]], 
    [[255, 255, 0], [0, 0, 255], [255, 255, 255], [0, 255, 0]], 
    [[0, 255, 255], [255, 0, 255], [0, 255, 0], [255, 0, 0]],
    [[0, 0, 0], [255, 255, 255], [0, 255, 0], [255, 0, 255]] 
]
print('Pixel Red')
print(f'|{gambar[0][0][0]:>5}|{gambar[0][1][0]:>5}|{gambar[0][2][0]:>5}|{gambar[0][3][0]:>5}|')
print(f'|{gambar[1][0][0]:>5}|{gambar[1][1][0]:>5}|{gambar[1][2][0]:>5}|{gambar[1][3][0]:>5}|')
print(f'|{gambar[2][0][0]:>5}|{gambar[2][1][0]:>5}|{gambar[2][2][0]:>5}|{gambar[2][3][0]:>5}|')
print(f'|{gambar[3][0][0]:>5}|{gambar[3][1][0]:>5}|{gambar[3][2][0]:>5}|{gambar[3][3][0]:>5}|')
print(f'|{gambar[4][0][0]:>5}|{gambar[4][1][0]:>5}|{gambar[4][2][0]:>5}|{gambar[4][3][0]:>5}|')
print('\nPixel Green')
print(f'|{gambar[0][0][1]:>5}|{gambar[0][1][1]:>5}|{gambar[0][2][1]:>5}|{gambar[0][3][1]:>5}|')
print(f'|{gambar[1][0][1]:>5}|{gambar[1][1][1]:>5}|{gambar[1][2][1]:>5}|{gambar[1][3][1]:>5}|')
print(f'|{gambar[2][0][1]:>5}|{gambar[2][1][1]:>5}|{gambar[2][2][1]:>5}|{gambar[2][3][1]:>5}|')
print(f'|{gambar[3][0][1]:>5}|{gambar[3][1][1]:>5}|{gambar[3][2][1]:>5}|{gambar[3][3][1]:>5}|')
print(f'|{gambar[4][0][1]:>5}|{gambar[4][1][1]:>5}|{gambar[4][2][1]:>5}|{gambar[4][3][1]:>5}|')
print('\nPixel Blue')
print(f'|{gambar[0][0][2]:>5}|{gambar[0][1][2]:>5}|{gambar[0][2][2]:>5}|{gambar[0][3][2]:>5}|')
print(f'|{gambar[1][0][2]:>5}|{gambar[1][1][2]:>5}|{gambar[1][2][2]:>5}|{gambar[1][3][2]:>5}|')
print(f'|{gambar[2][0][2]:>5}|{gambar[2][1][2]:>5}|{gambar[2][2][2]:>5}|{gambar[2][3][2]:>5}|')
print(f'|{gambar[3][0][2]:>5}|{gambar[3][1][2]:>5}|{gambar[3][2][2]:>5}|{gambar[3][3][2]:>5}|')
print(f'|{gambar[4][0][2]:>5}|{gambar[4][1][2]:>5}|{gambar[4][2][2]:>5}|{gambar[4][3][2]:>5}|')
```

### 2. Nested Tuple
Sama seperti list, tuple di Python juga dapat berisi elemen yang merupakan tuple lainnya. Ini disebut sebagai nested tuple atau tuple bersarang. Konsep ini memungkinkan kita untuk membuat struktur data yang lebih kompleks dan hierarkis. ContohM0703.py adalah contoh penggunaan Nested Tuple 2 dimensi.
##### ContohM0703.py
```python
kodewilayah = (
    ('35.71.01.1001','Bandar Lor'),
    ('35.71.01.1002','Bandar Kidul'),
    ('35.71.01.1003','Banjar Mlati'),
    ('35.71.01.1004','Pojok'),
    ('35.71.01.1005','Sukorame'),
    ('35.71.01.1006','Bujel'),
    ('35.71.01.1007','Gayam'),
    ('35.71.01.1008','Mrican'),
    ('35.71.01.1009','Dermo'),
    ('35.71.01.1010','Ngampel'),
    ('35.71.01.1011','Mojoroto'),
    ('35.71.01.1012','Campurejo'),
    ('35.71.01.1013','Lirboyo'),
    ('35.71.01.1014','Tamanan')
)
print('Kode Wilayah, Kecamatan Mojoroto')
print(f'|{'Kode':^15}|{'Kelurahan':^14}|')
print('-'*32)
print(f'|{kodewilayah[0][0]:^15}|{kodewilayah[0][1]:<14}|')
print(f'|{kodewilayah[1][0]:^15}|{kodewilayah[1][1]:<14}|')
print(f'|{kodewilayah[2][0]:^15}|{kodewilayah[2][1]:<14}|')
print(f'|{kodewilayah[3][0]:^15}|{kodewilayah[3][1]:<14}|')
print(f'|{kodewilayah[4][0]:^15}|{kodewilayah[4][1]:<14}|')
print(f'|{kodewilayah[5][0]:^15}|{kodewilayah[5][1]:<14}|')
print(f'|{kodewilayah[6][0]:^15}|{kodewilayah[6][1]:<14}|')
print(f'|{kodewilayah[7][0]:^15}|{kodewilayah[7][1]:<14}|')
print(f'|{kodewilayah[8][0]:^15}|{kodewilayah[8][1]:<14}|')
print(f'|{kodewilayah[9][0]:^15}|{kodewilayah[9][1]:<14}|')
print(f'|{kodewilayah[10][0]:^15}|{kodewilayah[10][1]:<14}|')
print(f'|{kodewilayah[11][0]:^15}|{kodewilayah[11][1]:<14}|')
print(f'|{kodewilayah[12][0]:^15}|{kodewilayah[12][1]:<14}|')
```

ContohM0704.py adalah contoh penggunaan Nested Tuple 3 dimensi.
##### ContohM0704.py
```python
kecamatan = ('Mojoroto','Kota','Pesantren')
tahun = (2020, 2021, 2022, 2023)
penduduk = (
    ((55870, 56367), (56117, 56752), (56645, 57442), (57644, 58427)),
    ((44344, 45489), (44089, 45406), (44218, 45444), (44636, 45877)),
    ((44957, 45235), (44939, 45294), (45329, 45614), (46016, 46220))
)
print(f'Jumlah Penduduk Kecamatan {kecamatan[0]} :')
print(f'|{'Tahun':^7}|{'Pria':^6}|{'Wanita':^8}|{'Total':^7}|')
print(f'|{tahun[0]:^7}|{penduduk[0][0][0]:>6}|{penduduk[0][0][1]:>8}|{(penduduk[0][0][0] + penduduk[0][0][1]):>7}|')
print(f'|{tahun[1]:^7}|{penduduk[0][1][0]:>6}|{penduduk[0][1][1]:>8}|{(penduduk[0][1][0] + penduduk[0][1][1]):>7}|')
print(f'|{tahun[2]:^7}|{penduduk[0][2][0]:>6}|{penduduk[0][2][1]:>8}|{(penduduk[0][2][0] + penduduk[0][2][1]):>7}|')
print(f'|{tahun[3]:^7}|{penduduk[0][3][0]:>6}|{penduduk[0][3][1]:>8}|{(penduduk[0][3][0] + penduduk[0][3][1]):>7}|')
print(f'\nJumlah Penduduk Kecamatan {kecamatan[1]} :')
print(f'|{'Tahun':^7}|{'Pria':^6}|{'Wanita':^8}|{'Total':^7}|')
print(f'|{tahun[0]:^7}|{penduduk[1][0][0]:>6}|{penduduk[1][0][1]:>8}|{(penduduk[1][0][0] + penduduk[1][0][1]):>7}|')
print(f'|{tahun[1]:^7}|{penduduk[1][1][0]:>6}|{penduduk[1][1][1]:>8}|{(penduduk[1][1][0] + penduduk[1][1][1]):>7}|')
print(f'|{tahun[2]:^7}|{penduduk[1][2][0]:>6}|{penduduk[1][2][1]:>8}|{(penduduk[1][2][0] + penduduk[1][2][1]):>7}|')
print(f'|{tahun[3]:^7}|{penduduk[1][3][0]:>6}|{penduduk[1][3][1]:>8}|{(penduduk[1][3][0] + penduduk[1][3][1]):>7}|')
print(f'\nJumlah Penduduk Kecamatan {kecamatan[2]} :')
print(f'|{'Tahun':^7}|{'Pria':^6}|{'Wanita':^8}|{'Total':^7}|')
print(f'|{tahun[0]:^7}|{penduduk[2][0][0]:>6}|{penduduk[2][0][1]:>8}|{(penduduk[2][0][0] + penduduk[2][0][1]):>7}|')
print(f'|{tahun[1]:^7}|{penduduk[2][1][0]:>6}|{penduduk[2][1][1]:>8}|{(penduduk[2][1][0] + penduduk[2][1][1]):>7}|')
print(f'|{tahun[2]:^7}|{penduduk[2][2][0]:>6}|{penduduk[2][2][1]:>8}|{(penduduk[2][2][0] + penduduk[2][2][1]):>7}|')
print(f'|{tahun[3]:^7}|{penduduk[2][3][0]:>6}|{penduduk[2][3][1]:>8}|{(penduduk[2][3][0] + penduduk[2][3][1]):>7}|')
```

### 3. Nested Dictionary
Nested dictionary atau kamus bersarang adalah sebuah konsep di Python di mana sebuah kamus dapat berisi nilai yang juga merupakan kamus. Ini memungkinkan kita untuk membuat struktur data yang lebih kompleks dan hierarkis. Bayangkan sebuah kotak yang berisi kotak-kotak kecil di dalamnya, dan kotak-kotak kecil itu juga bisa berisi kotak lagi. ContohM0705.py adalah contoh penggunaan Nested Dictionary untuk menyimpan data buku.
##### ContohM0705.py
```python
buku = {
    'buku1': dict(
        judul='Laskar Pelangi',
        pengarang='Andrea Hirata',
        tahun_terbit=2005,
        genre='Fiksi'
    ),
    'buku2': {
        'judul': 'Negeri 5 Menara',
        'pengarang': 'Andrea Hirata',
        'tahun_terbit': 2007,
        'genre': 'Fiksi'
    },
    'buku3': dict([
        ('judul','Bumi Manusia'),
        ('pengarang','Pramoedya Ananta Toer'),
        ('tahun_terbit',1980),
        ('genre','Fiksi Sejarah')
    ]),
    'buku4': {
        'judul': 'Anak Semua Bangsa',
        'pengarang': 'Pramoedya Ananta Toer',
        'tahun_terbit': 1980,
        'genre': 'Fiksi Sejarah'
    },
    'buku5': dict(
        judul='Filosofi Teras',
        pengarang='Heru Prasetya',
        tahun_terbit=2016,
        genre='Filsafat'
    )
}
print(f'|{'Judul':^18}|{'Pengarang':^22}|{'Tahun Terbit':^14}|{'Genre':^14}|')
print('-'*73)
print(f'|{(buku.get('buku1')).get('judul'):<18}|{(buku.get('buku1')).get('pengarang'):<22}',
      f'|{(buku.get('buku1')).get('tahun_terbit'):^14}|{(buku.get('buku1')).get('genre'):<14}|')
print(f'|{(buku.get('buku2')).get('judul'):<18}|{(buku.get('buku2')).get('pengarang'):<22}',
      f'|{(buku.get('buku2')).get('tahun_terbit'):^14}|{(buku.get('buku2')).get('genre'):<14}|')
print(f'|{(buku.get('buku3')).get('judul'):<18}|{(buku.get('buku3')).get('pengarang'):<22}',
      f'|{(buku.get('buku3')).get('tahun_terbit'):^14}|{(buku.get('buku3')).get('genre'):<14}|')
print(f'|{(buku.get('buku4')).get('judul'):<18}|{(buku.get('buku4')).get('pengarang'):<22}',
      f'|{(buku.get('buku4')).get('tahun_terbit'):^14}|{(buku.get('buku4')).get('genre'):<14}|')
print(f'|{(buku.get('buku5')).get('judul'):<18}|{(buku.get('buku5')).get('pengarang'):<22}',
      f'|{(buku.get('buku5')).get('tahun_terbit'):^14}|{(buku.get('buku5')).get('genre'):<14}|')
```

ContohM0706.py adalah contoh penggunaan Nested Dictionary untuk menyimpan data mahasiswa dan nilainya.
##### ContohM0706.py
```python
mhs = {
    'M001': {
        'npm': '2013020003','nama': 'Ibnu Al Ikrom',
        'nilai': {
            'Algoritma': 85, 'Struktur Data': 90,
            'Basis Data': 75, 'Pemrograman Web': 80
        }
    },
    'M002': {
        'npm': '2013020007', 'nama': 'Moh. Khamdanni',
        'nilai': {
            'Algoritma': 70, 'Struktur Data': 85,
            'Basis Data': 95, 'Pemrograman Web': 85
        }
    },
    'M003': {
        'npm': '2013020012', 'nama': 'Donny Firdani',
        'nilai': {
            'Algoritma': 90, 'Struktur Data': 80,
            'Basis Data': 85, 'Pemrograman Web': 95
        }
    },
    'M004': {
        'npm': '2013020022', 'nama': 'Andry Firdiansyah',
        'nilai': {
            'Algoritma': 75, 'Struktur Data': 75,
            'Basis Data': 80, 'Pemrograman Web': 85
        }
    },
    'M005': {
        'npm': '2013020081', 'nama': 'Rasio Fernandis',
        'nilai': {
            'Algoritma': 80, 'Struktur Data': 95,
            'Basis Data': 90, 'Pemrograman Web': 75
        }
    }
}
print(f'|{'NPM':^12}|{'Nama Mahasiswa':^18}|{'Algoritma':^11}|{'Struktur Data':^15}|{'Basis Data':^12}|{'Pemrograman Web':^17}|')
print('-'*92)
print(f'|{(mhs.get('M001')).get('npm'):^12}|{(mhs.get('M001')).get('nama'):<17}',
      f'|{((mhs.get('M001')).get('nilai')).get('Algoritma'):>10}',
      f'|{((mhs.get('M001')).get('nilai')).get('Struktur Data'):>14}',
      f'|{((mhs.get('M001')).get('nilai')).get('Basis Data'):>11}',
      f'|{((mhs.get('M001')).get('nilai')).get('Pemrograman Web'):>16} |')
print(f'|{(mhs.get('M002')).get('npm'):^12}|{(mhs.get('M002')).get('nama'):<17}',
      f'|{((mhs.get('M002')).get('nilai')).get('Algoritma'):>10}',
      f'|{((mhs.get('M002')).get('nilai')).get('Struktur Data'):>14}',
      f'|{((mhs.get('M002')).get('nilai')).get('Basis Data'):>11}',
      f'|{((mhs.get('M002')).get('nilai')).get('Pemrograman Web'):>16} |')
print(f'|{(mhs.get('M003')).get('npm'):^12}|{(mhs.get('M003')).get('nama'):<17}',
      f'|{((mhs.get('M003')).get('nilai')).get('Algoritma'):>10}',
      f'|{((mhs.get('M003')).get('nilai')).get('Struktur Data'):>14}',
      f'|{((mhs.get('M003')).get('nilai')).get('Basis Data'):>11}',
      f'|{((mhs.get('M003')).get('nilai')).get('Pemrograman Web'):>16} |')
print(f'|{(mhs.get('M004')).get('npm'):^12}|{(mhs.get('M004')).get('nama'):<17}',
      f'|{((mhs.get('M004')).get('nilai')).get('Algoritma'):>10}',
      f'|{((mhs.get('M004')).get('nilai')).get('Struktur Data'):>14}',
      f'|{((mhs.get('M004')).get('nilai')).get('Basis Data'):>11}',
      f'|{((mhs.get('M004')).get('nilai')).get('Pemrograman Web'):>16} |')
print(f'|{(mhs.get('M005')).get('npm'):^12}|{(mhs.get('M005')).get('nama'):<17}',
      f'|{((mhs.get('M005')).get('nilai')).get('Algoritma'):>10}',
      f'|{((mhs.get('M005')).get('nilai')).get('Struktur Data'):>14}',
      f'|{((mhs.get('M005')).get('nilai')).get('Basis Data'):>11}',
      f'|{((mhs.get('M005')).get('nilai')).get('Pemrograman Web'):>16} |')
```

### 4. Campuran Tipe Data Kolektif
Python menawarkan fleksibilitas yang tinggi dalam mencampur berbagai tipe data kolektif (seperti list, tuple, dan dictionary) dalam satu struktur data. Hal ini memungkinkan kita untuk membuat struktur data yang lebih kompleks dan sesuai dengan kebutuhan spesifik suatu permasalahan.

Campuran Tipe Data Kolektif biasa digunakan untuk :
- Representasi Data yang Lebih Akurat: Dengan menggabungkan berbagai tipe data, kita dapat merepresentasikan data yang memiliki struktur hierarkis atau kompleks dengan lebih baik.
- Peningkatan Fleksibilitas: Kita dapat dengan mudah menambahkan atau mengubah struktur data tanpa harus mengubah seluruh kode.
- Peningkatan Efisiensi: Dalam beberapa kasus, menggunakan campuran tipe data dapat meningkatkan efisiensi pemrosesan data.

ContohM0707.py adalah contoh penggunaan Nested Dictionary untuk menyimpan data mahasiswa dan nilainya.
##### ContohM0707.py
```python
laptops = {
    'A1': {
        'tipe':'XB450K', 'harga': 8000000,
        'spesifikasi': {
            'processor': 'Intel Core i5', 'RAM': '8 GB', 'storage': '256 GB SSD'
        },
        'penjualan': [
            {'tanggal': '2023-11-24', 'jumlah': 2},
            {'tanggal': '2023-11-25', 'jumlah': 3}
        ]
    },
    'A2': {
        'tipe':'JT570M', 'harga': 10000000,
        'spesifikasi': {
            'processor': 'AMD Ryzen 7', 'RAM': '16 GB', 'storage': '512 GB SSD'
        },
        'penjualan': [
            {'tanggal': '2023-11-26', 'jumlah': 1}
        ]
    },
     'A3': {
        'tipe':'KT239L', 'harga': 7000000,
        'spesifikasi': {
            'processor': 'Intel Core i3', 'RAM': '4 GB', 'storage': '256 GB HDD'
        },
        'penjualan': [
            {'tanggal': '2023-11-27', 'jumlah': 5},
            {'tanggal': '2023-11-29', 'jumlah': 3}
        ]
    },
    'A4': {
        'tipe':'FB831P', 'harga': 12000000,
        'spesifikasi': {
            'processor': 'Apple M2', 'RAM': '16 GB', 'storage': '512 GB SSD'
        },
        'penjualan': [
            {'tanggal': '2023-11-26', 'jumlah': 3},
            {'tanggal': '2023-11-28', 'jumlah': 2},
            {'tanggal': '2023-11-30', 'jumlah': 4}
        ]
    }
}
print(f'|{'Kode':^6}|{'Tipe':^8}|{'Harga':^10}|{'Spesifikasi':^35}|{'Penjualan':^21}|')
print(f'|{' ':^6}|{' ':^8}|{' ':^10}|{'Processor':^15}|{'RAM':^7}|{'Storage':^11}|{'Tanggal':^12}|{'Jumlah':^8}|')
print('-'*88)
print(f'|{'A1':^6}|{(laptops.get('A1')).get('tipe'):^8}',
      f'|{(laptops.get('A1')).get('harga'):>10}',
      f'|{((laptops.get('A1')).get('spesifikasi')).get('processor'):<15}',
      f'|{((laptops.get('A1')).get('spesifikasi')).get('RAM'):>7}',
      f'|{((laptops.get('A1')).get('spesifikasi')).get('storage'):>11}',
      f'|{((laptops.get('A1')).get('penjualan')[0]).get('tanggal'):^12}',
      f'|{((laptops.get('A1')).get('penjualan')[0]).get('jumlah'):>8}|',sep='')
print(f'|{'':^6}|{'':^8}|{'':>10}|{'':<15}|{'':<7}|{'':<11}',
      f'|{((laptops.get('A1')).get('penjualan')[1]).get('tanggal'):^12}',
      f'|{((laptops.get('A1')).get('penjualan')[1]).get('jumlah'):>8}|',sep='')
print(f'|{'A2':^6}|{(laptops.get('A2')).get('tipe'):^8}',
      f'|{(laptops.get('A2')).get('harga'):>10}',
      f'|{((laptops.get('A2')).get('spesifikasi')).get('processor'):<15}',
      f'|{((laptops.get('A2')).get('spesifikasi')).get('RAM'):>7}',
      f'|{((laptops.get('A2')).get('spesifikasi')).get('storage'):>11}',
      f'|{((laptops.get('A2')).get('penjualan')[0]).get('tanggal'):^12}',
      f'|{((laptops.get('A2')).get('penjualan')[0]).get('jumlah'):>8}|',sep='')
print(f'|{'A3':^6}|{(laptops.get('A3')).get('tipe'):^8}',
      f'|{(laptops.get('A3')).get('harga'):>10}',
      f'|{((laptops.get('A3')).get('spesifikasi')).get('processor'):<15}',
      f'|{((laptops.get('A3')).get('spesifikasi')).get('RAM'):>7}',
      f'|{((laptops.get('A3')).get('spesifikasi')).get('storage'):>11}',
      f'|{((laptops.get('A3')).get('penjualan')[0]).get('tanggal'):^12}',
      f'|{((laptops.get('A3')).get('penjualan')[0]).get('jumlah'):>8}|',sep='')
print(f'|{'':^6}|{'':^8}|{'':>10}|{'':<15}|{'':<7}|{'':<11}',
      f'|{((laptops.get('A3')).get('penjualan')[1]).get('tanggal'):^12}',
      f'|{((laptops.get('A3')).get('penjualan')[1]).get('jumlah'):>8}|',sep='')
print(f'|{'A4':^6}|{(laptops.get('A4')).get('tipe'):^8}',
      f'|{(laptops.get('A4')).get('harga'):>10}',
      f'|{((laptops.get('A4')).get('spesifikasi')).get('processor'):<15}',
      f'|{((laptops.get('A4')).get('spesifikasi')).get('RAM'):>7}',
      f'|{((laptops.get('A4')).get('spesifikasi')).get('storage'):>11}',
      f'|{((laptops.get('A4')).get('penjualan')[0]).get('tanggal'):^12}',
      f'|{((laptops.get('A4')).get('penjualan')[0]).get('jumlah'):>8}|',sep='')
print(f'|{'':^6}|{'':^8}|{'':>10}|{'':<15}|{'':<7}|{'':<11}',
      f'|{((laptops.get('A4')).get('penjualan')[1]).get('tanggal'):^12}',
      f'|{((laptops.get('A4')).get('penjualan')[1]).get('jumlah'):>8}|',sep='')
print(f'|{'':^6}|{'':^8}|{'':>10}|{'':<15}|{'':<7}|{'':<11}',
      f'|{((laptops.get('A4')).get('penjualan')[1]).get('tanggal'):^12}',
      f'|{((laptops.get('A4')).get('penjualan')[1]).get('jumlah'):>8}|',sep='')
```

|[# Awal](../README.md)<br>[# Materi Sebelumnya](../M06/README.md)<br>[# Materi Berikutnya](../M08/README.md)|
|-|