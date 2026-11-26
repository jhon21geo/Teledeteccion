# Teledetección — prospectividad Sentinel-2 (solo Colab)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhon21geo/Teledeteccion/blob/main/prospectividad_sentinel2.ipynb)

**Enlace directo:** <https://colab.research.google.com/github/jhon21geo/Teledeteccion/blob/main/prospectividad_sentinel2.ipynb>

Este repositorio es un **cuaderno de Google Colab**. No hace falta instalar Python, GDAL ni rasterio en tu computadora.

## Cómo ejecutarlo

1. Abre el [enlace directo a Colab](https://colab.research.google.com/github/jhon21geo/Teledeteccion/blob/main/prospectividad_sentinel2.ipynb).
2. En Colab: **Entorno de ejecución → Ejecutar todo**.
3. La primera celda comprueba que estás en Colab, instala `rasterio` y clona este repo (imagen de ejemplo).
4. Para tu zona, en **Parámetros** cambia `MODO`, `LON`, `LAT` y vuelve a ejecutar.

| `MODO` | Qué hace |
|---|---|
| `ejemplo` | Usa `data/prospectividad_sentinel2.tif` (ya viene en el repo) |
| `descargar` | Sentinel-2 L2A de tu `LON, LAT` (AWS Earth Search, sin cuenta) |
| `subir` | Selector de Colab — bien para archivos chicos |
| `drive` | GeoTIFF grande (p. ej. **200 MB**) desde Google Drive |

Al terminar se descarga `prospectividad_resultados.zip` (GeoJSON, KMZ, CSV, GeoTIFF).

## Imagen de 200 MB

GitHub rechaza archivos de más de **100 MB** en `data/`. No subas el TIF de 200 MB al repo.

1. Súbelo a Google Drive (`Mi unidad/teledeteccion/mi_escena.tif`).
2. En Colab, Parámetros: `MODO = 'drive'` y `RUTA_DRIVE = '/content/drive/MyDrive/teledeteccion/mi_escena.tif'`.
3. Ejecutar todo (la primera vez Colab pide acceso a Drive).

## Contenido

| Archivo | Rol |
|---|---|
| `prospectividad_sentinel2.ipynb` | Cuaderno (ábrelo solo en Colab) |
| `data/prospectividad_sentinel2.tif` | Escena de ejemplo, Sentinel-2 L2A, 10 m, 6 bandas |
| `requirements-colab.txt` | Paquetes que Colab instala en la primera celda |

## Alcance

Sentinel-2 ve **arcillas/hidroxilos** y **óxidos de Fe**. No separa argílica avanzada, fílica ni propilítica. Las zonas son hipótesis de priorización, no blancos confirmados.

Datos Sentinel-2 © Copernicus/ESA. DEM Copernicus GLO-30.
