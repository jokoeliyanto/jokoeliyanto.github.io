---
title: 'Pengenalan Python untuk Analisis Data'
date: 2025-08-14
permalink: /free_course/data-analyst-python/pengenalan-python/
tags:
  - python
  - data-analysis
  - tutorial
youtube_id: '29NQmFtV9BM'
colab_link: 'https://colab.research.google.com/drive/example'
excerpt: 'Mulai belajar Python dengan fokus pada analisis data menggunakan pandas dan numpy'
---

## Video Pembelajaran

{% if page.youtube_id %}
<div class="video-container" style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin-bottom: 20px;">
  <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/{{ page.youtube_id }}" frameborder="0" allowfullscreen></iframe>
</div>
{% endif %}

## Materi Pembelajaran

### Pengenalan Python untuk Analisis Data

Python adalah bahasa pemrograman yang sangat populer untuk data analysis. Dalam modul ini kamu akan belajar:

- Setup environment Python
- Library pandas, numpy, matplotlib
- Membaca dan manipulasi data
- Visualisasi data dasar

### Library Penting

#### NumPy
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(np.mean(arr))
```

#### Pandas
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.head())
```

#### Matplotlib
```python
import matplotlib.pyplot as plt
plt.plot([1, 2, 3], [1, 4, 9])
plt.show()
```

### Membaca Data

```python
df = pd.read_csv('data.csv')
df.describe()
df.info()
```

### Visualisasi Data

```python
df.plot(kind='bar')
plt.show()
```

## Google Colab

Untuk praktik interaktif, gunakan link di bawah:

{% if page.colab_link %}
[Buka di Google Colab →]({{ page.colab_link }})
{% endif %}
