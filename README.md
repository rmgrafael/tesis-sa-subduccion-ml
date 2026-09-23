# Repositorio computacional de la tesis — candidato público v1

## Finalidad
Este paquete reúne el código computacional preservado que puede ponerse a disposición pública para consulta y reproducibilidad académica de la tesis sobre estimación de Sa(T=1.0 s) mediante aprendizaje automático en sismos de interfaz de subducción sudamericanos.

**Estado:** candidato previo a publicación. No contiene aún una URL pública ni DOI.

## Regla de integridad
Las copias `*_PUBLICO.ipynb` conservan **sin modificación el tipo y el contenido fuente de cada celda**. Para publicación se eliminaron únicamente:
- salidas ejecutadas (`outputs`);
- números de ejecución;
- metadatos por celda de Google Colab, incluidos identificadores de usuario y ejecución.

El archivo `06_MANIFIESTOS/MANIFIESTO_CODIGO_PUBLICO.csv` registra el SHA-256 del original, el SHA-256 del código fuente y el SHA-256 de la copia pública.

## Estructura
- `01_CODIGO_PRINCIPAL/`: notebook maestro del desarrollo y evaluación interna.
- `02_VALIDACIONES_EXTERNAS/`: material computacional preservado de Valparaíso 2017, Acarí/Lomas 2018, Vallenar 2020 y Yauca/Caravelí 2024.
- `03_ANALISIS_MULTIEVENTO/`: análisis multievento y correcciones estadísticas.
- `04_CODIGO_COMPLEMENTARIO/`: reconstrucciones auditadas que deben leerse con su estado de procedencia.
- `05_ENTORNO_REPRODUCIBLE/`: versiones exactas registradas de Python y bibliotecas principales.
- `06_MANIFIESTOS/`: hashes, comparación de versiones e inventario de publicación.

## Entorno registrado
- Python 3.13.15
- pandas 2.2.3
- NumPy 2.1.3
- scikit-learn 1.6.1
- XGBoost 3.4.1
- SHAP 0.52.0
- semilla global: 42

## Datos fuente no incluidos
La base NGA-Sub original **no se redistribuye en este candidato**. Debe obtenerse de su fuente oficial y verificarse contra la identificación y hashes documentados en el Anexo B. Tampoco se incluyen automáticamente registros acelerográficos RAW, grillas, StationXML, geometrías de ruptura u otros archivos de terceros hasta verificar sus condiciones de redistribución.

## Estado de las validaciones externas
- **G — Valparaíso 2017:** oficial/verificado/completo.
- **H — Acarí/Lomas 2018:** oficial/verificado/completo.
- **I — Vallenar 2020:** cadena tardía preservada; brecha histórica de originales RAW/FFM/FSP/PARAM documentada.
- **J — Yauca/Caravelí 2024:** resultados finales preservados; cadena raw→freeze completa no certificada para las 44 estaciones.
- **K — Multievento:** oficial/verificado/completo.
- **F — Dominio Lima:** reconstrucción auditada con bloqueo de certificación en el entorno exacto; no se presenta como artefacto histórico original.

## Rutas de Google Drive en el código
Los notebooks preservan las rutas empleadas durante la ejecución original (`/content/drive/MyDrive/Tesis/...`). Estas rutas no contienen credenciales, pero un tercero deberá adaptar la ubicación de los archivos a su propio entorno. La adaptación de rutas no debe alterar filtros, parámetros, semillas ni decisiones metodológicas.

## Licencia
No se ha asignado todavía una licencia de reutilización. Antes de publicar en GitHub/Zenodo debe decidirse expresamente la licencia del código y comprobar las condiciones de redistribución de cada fuente de datos externa.
