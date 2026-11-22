---
title: 'Pengenalan Excel untuk Analisis Data'
date: 2025-08-14
permalink: /free_course/data-analyst-excel/pengenalan-excel/
tags:
  - excel
  - data-analysis
  - tutorial
youtube_id: '29NQmFtV9BM'
colab_link: 'https://colab.research.google.com/drive/example'
excerpt: 'Pelajari dasar-dasar Excel untuk analisis data, dari fungsi dasar hingga visualisasi'
---

## Video Pembelajaran

{% if page.youtube_id %}
<div class="video-container" style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin-bottom: 20px;">
  <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/{{ page.youtube_id }}" frameborder="0" allowfullscreen></iframe>
</div>
{% endif %}

## Materi Pembelajaran

### Pengenalan Excel untuk Analisis Data

Excel adalah tools yang powerful untuk analisis data dasar. Dalam kursus ini, kamu akan mempelajari:

- Fungsi-fungsi dasar Excel
- Pivot Table
- Visualisasi data dengan Chart
- Formula untuk analisis

### Fungsi-Fungsi Penting

#### SUM, AVERAGE, COUNT
```
=SUM(A1:A10)
=AVERAGE(B1:B10)
=COUNT(C1:C10)
```

#### VLOOKUP
```
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

### Membuat Pivot Table

1. Pilih data
2. Insert → Pivot Table
3. Drag field ke area yang sesuai
4. Analisis data

### Visualisasi Data

Gunakan Chart untuk memvisualisasikan data:
- Column Chart
- Line Chart
- Pie Chart
- Scatter Plot

## Google Colab

Untuk praktik interaktif, gunakan link di bawah:

{% if page.colab_link %}
[Buka di Google Colab →]({{ page.colab_link }})
{% endif %}
