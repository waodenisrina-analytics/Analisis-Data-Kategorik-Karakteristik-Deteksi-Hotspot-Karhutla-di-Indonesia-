# 🔥🪾 Analisis Data Kategorik Hotspot Karhutla Indonesia 🪾🔥

Analisis karakteristik deteksi hotspot karhutla berdasarkan satelit, sesi waktu
(siang/malam), dan wilayah pulau terhadap tingkat kepercayaan (*confidence*:
Low/Medium/High).

## Data 📃
Sheet *Detail* pada `sebaran-hotspot.xlsx`: 3.350 titik hotspot, 33 provinsi,
184 kabupaten/kota, periode 11-12 November 2026.

## Metode 📊
- Uji chi-square independensi (Cramér's V, residual terstandarisasi)
- Regresi logistik biner (hotspot berkepercayaan rendah)
- Regresi logistik multinomial (Low / Medium / High)
- Galat baku cluster-robust per kabupaten/kota
- Analisis sensitivitas tanpa Kabupaten Merauke

## Temuan utama 📌
- Deteksi siang hari dan satelit NASA-MODIS berkaitan kuat dengan hotspot
  berkepercayaan rendah, dan temuan ini stabil terhadap analisis sensitivitas.
- Efek NOAA20 dan Maluku-Papua pada model penuh didorong oleh Kabupaten
  Merauke (30,7% dari seluruh titik).
- Hasil menunjukkan asosiasi, bukan sebab-akibat.

Software : Rstudio
Paket R: readxl, dplyr, ggplot2, knitr, car, sandwich, lmtest, pROC, nnet, gridExtra
