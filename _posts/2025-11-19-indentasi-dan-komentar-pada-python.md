---
title: 'Indentasi dan Komentar Pada Python'
date: 2025-11-19
permalink: /posts/2025/11/indentasi-dan-komentar-pada-python/
tags:
  - python
  - dasar
  - tutorial
---


Dalam Python, **indentasi** dan **komentar** bukan hanya soal gaya penulisan—keduanya memiliki fungsi penting dalam struktur dan dokumentasi kode. 

Indentasi dalam Python
======

- **Indentasi** mengacu pada spasi atau tab di awal baris kode.
- Berbeda dengan bahasa pemrograman lain yang menggunakan kurung kurawal (`{}`) untuk menandai blok kode, Python **mengandalkan indentasi** untuk menentukan struktur logika program.
- Semua baris dalam satu blok kode harus memiliki **tingkat indentasi yang konsisten**. Jika tidak, Python akan menghasilkan **`IndentationError`**.

Contoh Penggunaan Indentasi yang Benar
======

```python
for i in range(5):
    # Blok ini di-indentasi
    print(i)
# Baris ini berada di luar blok for
print("Loop finished")
```

**Output**
```bash
0
1
2
3
4
Loop finished
```

Contoh Kesalahan Indentasi
===

```python
for i in range(5):
print(i)  # ← Error! Tidak di-indentasi
```

**Error yang muncul**

```bash
IndentationError: expected an indented block after 'for' statement on line 2
```

> 💡 **Tips**: Gunakan 4 spasi sebagai standar indentasi sesuai panduan [PEP 8](https://peps.python.org/pep-0008/), dan hindari mencampur spasi dengan tab.


Komentar dalam Python
===

Komentar digunakan untuk **menjelaskan kode**, memberi catatan, atau **menonaktifkan kode sementara** saat pengujian. Komentar **tidak dieksekusi** oleh interpreter.

### Komentar Satu Baris
- Dimulai dengan tanda `#`.
- Bisa ditempatkan di awal baris atau di akhir baris kode.

```python
# Ini adalah komentar satu baris
print("Intensity Coding")  # Komentar juga bisa di akhir baris
```

Anda juga bisa menonaktifkan baris kode:
```python
# variable = 42  # Baris ini tidak dieksekusi
```

### Komentar Multi-Baris

Python **tidak memiliki sintaks khusus** untuk komentar multi-baris seperti bahasa lain, namun ada dua pendekatan umum:

1. Gunakan `#` di tiap baris

```python
# Ini adalah
# komentar
# multi-baris
```

2. Gunakan string multi-baris dengan triple quote (`'''` atau `"""`):

```python
'''
Ini adalah string multi-baris
yang tidak ditugaskan ke variabel,
sehingga diabaikan oleh Python
dan berfungsi seperti komentar.
'''
```
> ⚠️ Catatan: Meskipun string multi-baris sering dipakai sebagai komentar, secara teknis ini tetap string literal. Namun, jika tidak digunakan, Python akan mengabaikannya. 

Docstring (Dokumentasi Fungsi)
===

**Docstring** adalah komentar khusus yang digunakan untuk **mendokumentasikan fungsi, kelas, atau modul**. Ditulis menggunakan **triple quote** (`"""` atau `'''`) tepat setelah deklarasi.

```python
def tambah(a, b):
    """
    Fungsi ini menjumlahkan dua angka.
    
    Parameter:
        a (int): Angka pertama
        b (int): Angka kedua
    
    Returns:
        int: Hasil penjumlahan a dan b
    """
    return a + b

# Menampilkan docstring
print(tambah.__doc__)
```

Docstring dapat diakses melalui atribut `__doc__` dan digunakan oleh alat seperti `help()`.

Beberapa Pernyataan dalam Satu Baris
===

Anda dapat menulis beberapa pernyataan dalam satu baris dengan memisahkannya menggunakan titik koma (`;`):

```python
x = 5; y = 10; z = x + y
```
> ⚠️ Hindari penggunaan berlebihan karena dapat mengurangi keterbacaan kode. 

Pernyataan Multi-Baris
===

Jika baris kode terlalu panjang, Anda bisa membaginya ke beberapa baris dengan dua cara:

1. Menggunakan Backslash (`\`)

```python
total = item_satu + \
        item_dua + \
        item_tiga
```
2. Menggunakan Tanda Kurung (`()`, `[]`, `{}`)
Tidak perlu backslash—Python otomatis mengenali bahwa pernyataan belum selesai selama tanda kurung belum ditutup.

```python
angka = [1, 2, 3,
         4, 5, 6]

hasil = (a + b +
         c * d)
```

Kutipan dalam Python
===

Python mendukung tiga jenis tanda kutip untuk membuat string:

- Single quote: `'Halo'`
- Double quote: `"Halo"`
- Triple quote (untuk string multi-baris):

```python
'''String
multi-baris'''

"""String
multi-baris juga"""
```
Pemilihan jenis kutipan tergantung pada isi string—misalnya, gunakan double quote jika string mengandung petik tunggal, dan sebaliknya.

Kesimpulan
===

- **Indentasi** adalah bagian esensial dari sintaks Python—jaga konsistensi!
- **Komentar** membantu menjelaskan logika kode dan mempermudah kolaborasi.
- Gunakan **docstring** untuk dokumentasi profesional.
- Manfaatkan fitur **multi-baris** dan **kutipan fleksibel** untuk meningkatkan keterbacaan kode.

Dengan memahami konsep ini, Anda tidak hanya menulis kode yang berjalan, tetapi juga kode yang **bersih, rapi, dan mudah dipelihara**.

------