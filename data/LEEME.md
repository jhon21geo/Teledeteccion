# Datos

`prospectividad_sentinel2.tif` es la escena de **ejemplo** (~10 MB). GitHub **no acepta** un GeoTIFF de 200 MB en esta carpeta (límite 100 MB por archivo).

Para una imagen grande, en Colab:

1. Súbela a [Google Drive](https://drive.google.com) (por ejemplo `Mi unidad/teledeteccion/mi_escena.tif`).
2. En el cuaderno, celda **Parámetros**:
   - `MODO = 'drive'`
   - `RUTA_DRIVE = '/content/drive/MyDrive/teledeteccion/mi_escena.tif'`
3. **Ejecutar todo**. Colab pide permiso de Drive una vez.

Seis bandas, en este orden: **B2, B3, B4, B8, B11, B12**.
