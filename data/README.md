# Dataset P07 — Kekeruhan muara Maro 2013–2025

Dihasilkan oleh notebook (`P07_hasil.zip` → `07_dataset/`).

| Berkas | Isi |
|---|---|
| `P07_deret_bulanan_zona.csv` | Median kekeruhan bulanan (FNU) zona 0–5, 5–15, 15–30 km dari muara; `sensor` (Landsat 8/9 atau Sentinel-2) |
| `P07_bulanan_hujan_plume.csv` | Per bulan: kekeruhan zona 0–5 km, persentase plume, hujan DAS (mm) jeda 0–2 bulan |
| `P07_peta.npz` | Grid 100 m UTM 54S (`X0`, `Y0` = pojok kiri atas): kemiringan Sen (FNU/thn), tren signifikan, rezim k-means, median musim hujan dan kemarau |
| `P07_DAS_dan_muara.geojson` | Batas DAS Maro (HydroBASINS level 8) dan titik muara |

Kekeruhan dihitung dengan algoritma Dogliotti et al. (2015) tanpa kalibrasi lokal; baca sebagai indeks relatif. Lisensi CC BY 4.0.

**EN.** Monthly turbidity per distance zone, monthly plume and catchment rainfall, trend/regime/season maps and the Maro catchment boundary. Turbidity from the Dogliotti et al. (2015) algorithm without local calibration; treat as a relative index. Licence CC BY 4.0.
