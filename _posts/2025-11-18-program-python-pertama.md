---
title: 'Program Python Pertama'
date: 2025-11-18
permalink: /posts/2025/11/program-python-pertama/
tags:
  - python
  - dasar
  - tutorial
---


Saat mempelajari Python, langkah pertama yang sangat umum adalah menulis program sederhana yang hanya menampilkan pesan di layar. Tradisi klasik adalah mencetak **“Assalamualaikum!”** — ini menjadi tanda bahwa instalasi Python kamu sudah benar dan berjalan dengan baik.

Contoh Program Pertama
===

```python
# Ini adalah komentar. Python mengabaikan semua yang setelah simbol '#'.  
# Gunakan komentar untuk menjelaskan apa yang dilakukan kode — agar lebih mudah dibaca.

# Cetak "Assalamualaikum!" ke layar
print("Assalamualaikum!")
```

Mode Script (Berkas .py)
===

Langkah Membuat dan Menjalankan Script:

1. Pastikan Python sudah terinstal.
2. Buat file `.py`.
3. Tulis skrip berikut:

```python
number = float(input("Masukkan sebuah angka: "))
square = number ** 2
print(f"Kuadrat dari {number} adalah {square}")
```

4. Simpan file (`square_calculator.py`)
5. Jalankan di terminal:

```bash
python square_calculator.py
```

Mode Notebook (Jupyter Notebook / Google Colab)
===

Jika kamu menggunakan Jupyter Notebook atau Google Colab, cara kerjanya sedikit berbeda dibandingkan mode script. Kamu mengeksekusi kode secara bertahap dalam cell.

Langkah Menulis Kode Pertama di Notebook

1. Buka Jupyter Notebook atau Google Colab.
2. Buat sebuah Code Cell.
3. Tulis kode berikut:

```python
# Ini adalah komentar. Python mengabaikan semua yang setelah simbol '#'.  
# Gunakan komentar untuk menjelaskan apa yang dilakukan kode — agar lebih mudah dibaca.

# Cetak "Assalamualaikum!" ke layar
print("Assalamualaikum!")
```

4. Jalankan cell dengan menekan Ctrl + Enter.

Identifier di Python
===

Aturan penamaan:

- Harus diawali huruf atau `_`
- Tidak boleh menggunakan karakter khusus seperti `@`, `$`, `%`
- Peka huruf besar/kecil
- Tidak boleh memakai kata kunci Python


Membaca Input
===

```python
nama = input("Masukkan nama: ")
print("Halo,", nama)
```


Menampilkan Output
===

Menggunakan `print()`:

```python
print("Hello, World!")
```

Ringkasan
===

- Mulai dari program sederhana memastikan Python berjalan baik.
- Mode skrip memungkinkan program lebih kompleks.
- Input (`input()`) dan output (`print()`) adalah dasar interaksi program.

