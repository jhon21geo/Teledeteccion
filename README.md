# Prospectividad por alteración hidrotermal con Sentinel-2 (cuaderno Colab)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhon21geo/geoia-apps/blob/main/prospectividad/colab/prospectividad_sentinel2.ipynb)

Flujo reproducible en 4 pasos, equivalente a una parte de la app web [Prospectividad](https://geoia.site/prospectividad/):

1. **Datos** — imagen de ejemplo, descarga Sentinel-2 L2A de tu zona (AWS Earth Search, sin cuenta) o sube tu GeoTIFF.
2. **Análisis espectral** — M1 índices de bandas · M2 PCA dirigido (Crosta) · M3 ángulo espectral (SAM) → consenso ≥ 2 de 3.
3. **Lineamientos** — Canny + Hough (opcional con DEM Copernicus 30 m) y diagrama de rosa.
4. **Zonas prioritarias** — puntaje = alteración + densidad de lineamientos → GeoJSON, KMZ, CSV y GeoTIFF.

## Usar tu propia imagen
* **Descargar:** `MODO = 'descargar'` y cambia `LON, LAT`, `LADO_KM`, `FECHAS`.
* **Subir:** `MODO = 'subir'` con un GeoTIFF de 6 bandas en orden **B2, B3, B4, B8, B11, B12** (reflectancia 0–1 o entero ×10 000).

## Contenido
| Archivo | Descripción |
|---|---|
| `prospectividad_sentinel2.ipynb` | Cuaderno (ya ejecutado, se ven los resultados) |
| `data/prospectividad_sentinel2.tif` | Imagen de ejemplo (Sentinel-2 L2A, 10 m, 6 bandas) |

## Alcance y límites
Sentinel-2 distingue **arcillas/hidroxilos** y **óxidos de Fe**; no separa argílica avanzada, fílica ni propilítica (requiere SWIR fino: ASTER, WorldView-3, EMIT, EnMAP, PRISMA). Las zonas son hipótesis de priorización, no blancos confirmados. La validación con muestras de campo es opcional y solo concluyente con ≥ 30 puntos por clase.

Datos Sentinel-2 © Copernicus/ESA (acceso abierto). DEM Copernicus GLO-30.
