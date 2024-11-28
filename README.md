# Análisis de Segmentación y Precios con PySpark
Este proyecto realiza un análisis de segmentación y precios utilizando PySpark en un entorno de Google Colab. Los datos provienen de dos archivos CSV: Segmentacion.csv y Precios.csv, alojados en Google Drive.

## Objetivos del Análisis
- Validar cuántos registros tienen ambos archivos (Segmentacion y Precios).
- Realizar una partición de la matriz de precios por familia (FAM) y subfamilia (SUBFAM).
- Validar que los márgenes (VALUE) se mantengan entre 0.1 y 1.
- Contabilizar el promedio de clientes únicos (RUT_CLI) por grupos (GROUPM).
- Calcular márgenes máximos, promedios y mínimos para un cliente específico (RUT_CLI = 66666666).
##Requisitos Previos
- Google Colab: Ejecutar el script en un entorno de Google Colab.
- PySpark: Instalado automáticamente en el entorno de Colab.
- Archivos de Datos:
  - Segmentacion.csv: Contiene la información de los grupos.
  - Precios.csv: Contiene información de clientes (RUT_CLI) y sus segmentos (SEGMENTO).
  - Google Drive: Los archivos deben estar almacenados en una carpeta accesible desde Google Drive.

## Estructura de los Datos
### Segmentacion.csv
| **Columna** | **Descripción**                  |
|-------------|----------------------------------|
| GROUPM      | Grupo de segmentación           |
| FAM         | Familia del grupo               |
| SUBFAM      | Subfamilia dentro de la familia |
| VALUE       | Valor asociado al grupo         |

### Precios.csv
| **Columna** | **Descripción**                  |
|-------------|----------------------------------|
| RUT_CLI     | Identificador único del cliente |
| SEGMENTO    | Segmento al que pertenece       |


## Instrucciones de Uso
1. Montar Google Drive
El script monta Google Drive para acceder a los archivos de datos:

```python
from google.colab import drive
drive.mount('/content/drive')
```
2. Configurar Rutas
Asegúrate de que los archivos Segmentacion.csv y Precios.csv estén en una carpeta llamada Datos dentro de tu Google Drive.

python

```python
ruta_segmentacion = "/content/drive/My Drive/Datos/Segmentacion.csv"
ruta_precios = "/content/drive/My Drive/Datos/Precios.csv"
```

3. Ejecutar el Script
Copia y pega el código en Google Colab y ejecútalo. El análisis incluye:

- Conteo de registros en ambos archivos.
- Validación y partición por FAM y SUBFAM.
- Verificación de márgenes en el rango [0.1, 1].
- Cálculo de clientes únicos por grupo y su promedio.
- Cálculo de márgenes (máximo, promedio y mínimo) para RUT_CLI = 66666666.

4. Resultados
Los resultados incluyen:

- El número de registros en ambos archivos.
- Clientes únicos por grupo y promedio.
- Validación de márgenes en el rango deseado.
- Estadísticas de márgenes para un cliente específico.
