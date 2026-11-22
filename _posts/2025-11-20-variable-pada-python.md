---
title: 'Variable pada Python'
date: 2025-11-20
permalink: /posts/2025/11/variable-pada-python/
tags:
  - python
  - variable
  - tutorial
---

Dalam pemrograman, variable adalah tempat penyimpanan data atau nilai. Variable memungkinkan kita untuk menyimpan, memanipulasi, dan mengakses data dengan mudah. Mari kita pelajari lebih lanjut tentang variable pada Python.

Apa itu Variable?
===

Variable adalah sebuah nama yang mengacu pada suatu nilai atau data dalam memori komputer. Variable berfungsi sebagai "kotak penyimpanan" yang menyimpan informasi saat program berjalan.

Contoh sederhana:
```python
nama = "Joko"
umur = 25
tinggi = 170.5
```

Pada contoh di atas, `nama`, `umur`, dan `tinggi` adalah variable yang menyimpan nilai masing-masing.

Aturan Penamaan Variable
===

Ketika membuat variable di Python, ada beberapa aturan yang harus diikuti:

1. **Karakter pertama** harus berupa huruf (a-z, A-Z) atau underscore (_)
2. **Tidak boleh dimulai dengan angka**
3. Hanya boleh menggunakan **huruf, angka, dan underscore** (a-z, A-Z, 0-9, _)
4. **Peka terhadap huruf besar/kecil** (case-sensitive) - `nama` dan `Nama` adalah variable berbeda
5. Hindari penggunaan **keyword Python** sebagai nama variable (seperti `if`, `while`, `for`, `class`, dsb.)

Contoh penamaan yang benar:
```python
nama = "Joko"
nama_lengkap = "Joko Eliyanto"
_umur = 25
umur2 = 26
NamaDepan = "Joko"
```

Contoh penamaan yang salah:
```python
2nama = "Joko"  # Dimulai dengan angka
nama-lengkap = "Joko"  # Menggunakan tanda hubung
nama lengkap = "Joko"  # Mengandung spasi
class = "Kelas 1"  # Menggunakan keyword Python
```

Tipe-Tipe Data Python
===

Python mendukung berbagai tipe data. Berikut adalah tipe data yang paling umum:

### 1. String (str)
Digunakan untuk menyimpan teks atau karakter.

```python
nama = "Joko Eliyanto"
alamat = "Jakarta, Indonesia"
```

### 2. Integer (int)
Digunakan untuk menyimpan bilangan bulat (tanpa desimal).

```python
umur = 25
tahun_lahir = 2000
jumlah_siswa = 45
```

### 3. Float (float)
Digunakan untuk menyimpan bilangan desimal.

```python
tinggi = 170.5
berat = 65.2
nilai_rata = 85.75
```

### 4. Boolean (bool)
Digunakan untuk menyimpan nilai kebenaran: `True` atau `False`.

```python
adalah_pelajar = True
sudah_lulus = False
```

### 5. List (list)
Digunakan untuk menyimpan kumpulan data dalam satu variable.

```python
hobi = ["membaca", "menulis", "coding"]
angka = [1, 2, 3, 4, 5]
```

### 6. Dictionary (dict)
Digunakan untuk menyimpan data dengan pasangan kunci-nilai.

```python
profil = {"nama": "Joko", "umur": 25, "kota": "Jakarta"}
```

Cara Mendeklarasikan Variable
===

Di Python, cara mendeklarasikan variable sangat mudah. Kita hanya perlu menulis nama variable, tanda sama dengan (=), dan nilai yang ingin disimpan.

```python
# Deklarasi satu variable
nama = "Joko"

# Deklarasi multiple variable sekaligus
umur, tinggi, berat = 25, 170.5, 65.2

# Deklarasi multiple variable dengan nilai yang sama
x = y = z = 0
```

Mengubah Nilai Variable
===

Nilai variable dapat diubah kapan saja selama program berjalan.

```python
nama = "Joko"
print(nama)  # Output: Joko

nama = "Eliyanto"
print(nama)  # Output: Eliyanto
```

Menampilkan Nilai Variable
===

Untuk menampilkan nilai variable, kita dapat menggunakan fungsi `print()`.

```python
nama = "Joko Eliyanto"
umur = 25
tinggi = 170.5

print(nama)  # Output: Joko Eliyanto
print(umur)  # Output: 25
print(tinggi)  # Output: 170.5

# Menampilkan multiple variable
print(nama, umur, tinggi)  # Output: Joko Eliyanto 25 170.5
```

Mengecek Tipe Data Variable
===

Untuk mengetahui tipe data dari suatu variable, kita dapat menggunakan fungsi `type()`.

```python
nama = "Joko"
umur = 25
tinggi = 170.5
adalah_pelajar = True

print(type(nama))  # Output: <class 'str'>
print(type(umur))  # Output: <class 'int'>
print(type(tinggi))  # Output: <class 'float'>
print(type(adalah_pelajar))  # Output: <class 'bool'>
```

Konversi Tipe Data
===

Kita dapat mengubah tipe data dari satu ke tipe lain menggunakan fungsi konversi.

```python
# Konversi ke String
umur = 25
umur_str = str(umur)
print(umur_str)  # Output: 25
print(type(umur_str))  # Output: <class 'str'>

# Konversi ke Integer
nilai_str = "30"
nilai_int = int(nilai_str)
print(nilai_int)  # Output: 30
print(type(nilai_int))  # Output: <class 'int'>

# Konversi ke Float
angka = 10
angka_float = float(angka)
print(angka_float)  # Output: 10.0
print(type(angka_float))  # Output: <class 'float'>

# Konversi ke Boolean
nilai = 1
bool_nilai = bool(nilai)
print(bool_nilai)  # Output: True
```

Konstanta
===

Meskipun Python tidak memiliki keyword untuk membuat konstanta sejati, secara konvensi konstanta ditulis dengan **huruf kapital semua** untuk menunjukkan bahwa nilai tidak boleh diubah.

```python
PI = 3.14159
KECEPATAN_CAHAYA = 299792458
NAMA_APLIKASI = "Portfolio Joko"

# Meskipun dapat diubah, konvensi ini menunjukkan bahwa nilai seharusnya tetap sama
```

Scope Variable
===

Scope adalah area di mana variable dapat diakses. Ada dua jenis scope utama:

### 1. Global Scope
Variable yang dideklarasikan di luar fungsi dapat diakses di seluruh program.

```python
nama = "Joko"  # Global variable

def tampilkan_nama():
    print(nama)  # Dapat mengakses global variable

tampilkan_nama()  # Output: Joko
```

### 2. Local Scope
Variable yang dideklarasikan di dalam fungsi hanya dapat diakses dalam fungsi tersebut.

```python
def tampilkan_info():
    nama = "Eliyanto"  # Local variable
    print(nama)

tampilkan_info()  # Output: Eliyanto
print(nama)  # Error: nama is not defined
```

Kesimpulan
===

Variable adalah elemen fundamental dalam pemrograman Python. Pemahaman yang baik tentang variable, tipe data, dan cara menggunakannya akan membantu Anda dalam menulis program yang lebih baik. Pastikan untuk mengikuti aturan penamaan variable dan memahami konsep scope agar kode Anda lebih terstruktur dan mudah dipahami.
