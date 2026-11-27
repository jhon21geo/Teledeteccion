# Teledetección — prospectividad Sentinel-2

Cuaderno de **Google Colab**. Ábrelo, ejecuta todo y verás el plano de alteraciones (arcillas en amarillo, óxidos de Fe en rojo).

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhon21geo/Teledeteccion/blob/main/prospectividad_sentinel2.ipynb)

https://colab.research.google.com/github/jhon21geo/Teledeteccion/blob/main/prospectividad_sentinel2.ipynb

## Cómo ejecutarlo

1. Abre el enlace de Colab.
2. Menú **Entorno de ejecución → Ejecutar todo**.
3. El plano está en **Plano de alteraciones**. Al final se descarga un zip (PNG, GeoJSON, KMZ, CSV, GeoTIFF).

La imagen de ejemplo ya viene en el repo. No instales nada en tu PC.

Para **tu zona**, en la celda **Parámetros**:

- `MODO = 'descargar'` y tus `LON`, `LAT`, o
- `MODO = 'subir'` y elige un GeoTIFF de 6 bandas (`B2, B3, B4, B8, B11, B12`).

## Alcance

Sentinel-2 ve **arcillas/hidroxilos** y **óxidos de Fe**. No separa argílica avanzada, fílica ni propilítica. Las zonas son hipótesis de priorización, no blancos confirmados.

Datos Sentinel-2 © Copernicus/ESA. DEM Copernicus GLO-30.
