#Análisis de Segmentación y Precios con PySpark
Este proyecto realiza un análisis de segmentación y precios utilizando PySpark en un entorno de Google Colab. Los datos provienen de dos archivos CSV: Segmentacion.csv y Precios.csv, alojados en Google Drive.

##Objetivos del Análisis
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
