# analizador dashboard
Sistema web para cargar, analizar y visualizar archivos CSV mediante dashboards interactivos.

# Analizador de CSV y Generador de Dashboards

Sistema web desarrollado en Python con Streamlit para cargar archivos CSV, revisar su estructura, limpiar columnas marcadas para eliminación, explorar datos y generar dashboards con gráficos.

## Funciones principales

- Carga de archivos CSV desde el navegador.
- Detección automática de separador y codificación.
- Resumen del archivo: filas, columnas, encoding y separador.
- Vista previa de registros.
- Perfil de columnas: valores vacíos, valores únicos y ejemplos.
- Limpieza de columnas marcadas como `ELIMINAR COLUMNA`.
- Dashboard automático para preguntas específicas de análisis.
- Gráficos manuales: barras, circular, histograma, barras cruzadas, línea por fecha y dispersión.
- Módulo de consultas guiadas.
- Exportación de CSV limpio.
- SQL sugerido para crear tabla en MySQL.

## Requisitos previos

- Python 3.10 o superior.
- Git, si se descargará desde GitHub.
- Internet para instalar dependencias la primera vez.

Verificar Python:

```powershell
python --version
```

Si no funciona:

```powershell
py --version
```

## Descargar desde GitHub

```powershell
git clone URL_DEL_REPOSITORIO
cd analizador_csv_dashboard
```

También se puede descargar como ZIP desde GitHub: **Code > Download ZIP**, descomprimir y abrir PowerShell dentro de la carpeta.

## Instalación rápida

```powershell
python -m pip install -r requirements.txt
```

Si no funciona:

```powershell
py -m pip install -r requirements.txt
```

## Ejecución

```powershell
python -m streamlit run app.py
```

Si no funciona:

```powershell
py -m streamlit run app.py
```

Luego se abrirá el navegador. Si no se abre, entrar manualmente a:

```text
http://localhost:8501
```

## Instalación recomendada con entorno virtual

Crear entorno virtual:

```powershell
python -m venv .venv
```

Activar entorno:

```powershell
.\.venv\Scripts\Activate.ps1
```

Si PowerShell bloquea la activación:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

Instalar dependencias:

```powershell
python -m pip install -r requirements.txt
```

Ejecutar:

```powershell
python -m streamlit run app.py
```

Salir del entorno:

```powershell
deactivate
```

## Uso del sistema

1. Ejecutar el programa.
2. Subir un archivo `.csv`.
3. Revisar resumen de filas, columnas, separador y codificación.
4. Revisar perfil de columnas.
5. Entrar a **Dashboard por preguntas** para generar visualizaciones automáticas.
6. Entrar a **Gráficos manuales** para crear visualizaciones personalizadas.
7. Entrar a **Consultas guiadas** para escribir preguntas sobre el dataset.
8. Exportar el CSV limpio si se necesita.

## Preguntas de prueba

```text
¿Cuántos pacientes han fallecido por cada estatus del caso?
```

```text
¿Cuántos pacientes con hipertensión hay por cada dictamen?
```

```text
¿Cuánto es el total de pacientes confirmados por cada entidad de residencia?
```

```text
¿Cuál es la fecha de actualización más reciente?
```

```text
¿Cuántos pacientes confirmados padecen diabetes y cuántos no?
```

## Errores comunes

### `streamlit` no se reconoce

Usar:

```powershell
python -m streamlit run app.py
```

O reinstalar:

```powershell
python -m pip install streamlit pandas plotly
```

### No se puede activar el entorno virtual

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

### No encuentra `requirements.txt`

Verificar que se está dentro de la carpeta correcta:

```powershell
dir
```

Deben aparecer:

```text
app.py
requirements.txt
README.md
```

## Nota sobre datasets

No se recomienda subir archivos CSV grandes o sensibles al repositorio.  
Cada usuario puede cargar su propio CSV desde la interfaz del sistema.
