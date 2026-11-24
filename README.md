# Turbidity of the Maro River Estuary and Merauke Coastal Waters 2013–2025 (P07)

Code, data and results for the study *"Turbidity of the Maro River Estuary and Merauke Coastal Waters, Indonesia, 2013–2025 from Landsat 8/9 and Sentinel-2: Seasonal Patterns, Trends, Rainfall Links and k-Means Zoning"*.

> **Ringkasan (ID):** Repositori ini berisi notebook, data, dan tabel hasil pemetaan kekeruhan bulanan muara Sungai Maro dan perairan pesisir Merauke 2013–2025 dari Landsat 8/9 dan Sentinel-2 (algoritma Dogliotti et al., 2015), tanpa pengukuran lapangan: pola musim, tren Mann-Kendall, hubungan dengan hujan DAS (CHIRPS), dan zonasi rezim k-means. Semua tabel dan gambar tersedia dalam versi Indonesia (_ID) dan Inggris (_EN).

## Study design

| Item | Value |
|---|---|
| Study area | Merauke city coast and Arafura Sea in front (140.15–140.75° E, 8.30–8.80° S), 100 m grid |
| River mouth & catchment | Max HydroSHEDS flow accumulation near Merauke; HydroBASINS level 8 traced upstream via NEXT_DOWN |
| Data | Landsat 8/9 C2 L2 (2013–2025), Sentinel-2 SR + Cloud Score+ (2019–2025), JRC GSW, CHIRPS |
| Turbidity | Dogliotti et al. (2015) red/NIR switching algorithm after SWIR2 subtraction; monthly medians |
| Analyses | Sensor agreement; zones 0–5/5–15/15–30 km; wet vs dry season; Otsu plume; Mann-Kendall + Sen trends; lagged rainfall correlation; leave-one-year-out Random Forest; k-means regimes (silhouette) |

## Main results

| Item | Result |
|---|---|
| Maro mouth / catchment | 140.363° E, 8.465° S; 8,100 km² (HydroBASINS level 8) |
| Spatial pattern | Shore-parallel turbid band, sharp decline seaward (not a point-source river plume) |
| Season, 0–5 km zone | Dry > wet: Landsat 237 vs 63 FNU; Sentinel-2 221 vs 44 FNU (p < 0.01); peak July–August |
| Trend 2014–2025 | None significant (zones p ≥ 0.54; 1.4% of pixels significant) |
| Rainfall link | Negative same-month correlation (ρ = −0.36, 0–5 km); RF leave-one-year-out R² = 0.17, seasonal cycle most important |
| k-means regimes | k = 2 (silhouette 0.51): turbid coastal band 515 km², 26.6 FNU; clear offshore 700 km², 1.4 FNU |
| Sensor agreement | Spearman ρ = 0.66; Sentinel-2 ≈ 2 × Landsat (treat FNU as a relative index) |

## Repository structure

```
notebooks/P07_notebook.ipynb   full pipeline (Google Colab + Earth Engine + scikit-learn)
data/                          monthly zone series, rainfall/plume table, maps (.npz), catchment and mouth
results/tables/                result tables and P07_hasil_ringkas.json
results/figures/               figures used in the manuscript
docs/diagrams/                 flowchart, context diagram, level-1 DFD (ID & EN)
```

## License

Code: MIT (`LICENSE`). Data, results and figures: CC BY 4.0.
