# Analizador de CSV y Generador de Dashboards

Sistema web desarrollado en Python con Streamlit para cargar archivos CSV, revisar su estructura, limpiar columnas marcadas para eliminación, explorar datos y generar dashboards con gráficos.

Este proyecto permite analizar archivos CSV desde una interfaz web, generar visualizaciones automáticas y crear gráficos personalizados.

---

## Funciones principales

* Carga de archivos CSV desde el navegador.
* Detección automática de separador y codificación.
* Resumen del archivo: filas, columnas, encoding y separador.
* Vista previa de registros.
* Perfil de columnas: valores vacíos, valores únicos y ejemplos.
* Limpieza de columnas marcadas como `ELIMINAR COLUMNA`.
* Dashboard automático para preguntas específicas de análisis.
* Gráficos manuales:

  * conteo por categoría,
  * gráfico circular,
  * histograma,
  * barras cruzadas,
  * línea por fecha,
  * dispersión.
* Módulo de consultas guiadas.
* Exportación de CSV limpio.
* SQL sugerido para crear tabla en MySQL.

---

## Archivos incluidos

```text
analizador_csv_dashboard/
│
├── app.py
├── requirements.txt
├── README.md
├── INSTALACION_USO.md
├── .gitignore
├── instalar_dependencias.bat
└── ejecutar.bat
```

| Archivo                     | Función                                                     |
| --------------------------- | ----------------------------------------------------------- |
| `app.py`                    | Código principal del sistema.                               |
| `requirements.txt`          | Librerías necesarias para ejecutar el proyecto.             |
| `README.md`                 | Documentación principal.                                    |
| `INSTALACION_USO.md`        | Guía rápida de instalación y ejecución.                     |
| `.gitignore`                | Evita subir archivos innecesarios o datasets grandes.       |
| `instalar_dependencias.bat` | Verifica Python, instala dependencias y prepara el entorno. |
| `ejecutar.bat`              | Ejecuta el sistema en Windows.                              |

---

## Instalación recomendada en Windows

### 1. Instalar dependencias automáticamente

Dar doble clic en:

```text
instalar_dependencias.bat
```

Este archivo realiza lo siguiente:

1. Verifica si Python está instalado.
2. Si Python no está instalado, intenta instalarlo con `winget`.
3. Si Python ya está instalado, intenta actualizarlo cuando sea posible.
4. Crea un entorno virtual local llamado `.venv`.
5. Actualiza `pip`.
6. Instala las dependencias del proyecto.

Dependencias utilizadas:

```text
streamlit
pandas
plotly
```

---

### 2. Ejecutar el sistema

Dar doble clic en:

```text
ejecutar.bat
```

Si todo está correcto, se abrirá el navegador con la aplicación.

Si no se abre automáticamente, ingresar manualmente a:

```text
http://localhost:8501
```

---

## Instalación manual

Abrir PowerShell dentro de la carpeta del proyecto y ejecutar:

```powershell
python -m pip install -r requirements.txt
```

Si `python` no funciona, usar:

```powershell
py -m pip install -r requirements.txt
```

Luego ejecutar:

```powershell
python -m streamlit run app.py
```

Si `python` no funciona, usar:

```powershell
py -m streamlit run app.py
```

---

## Uso del sistema

1. Ejecutar el programa.
2. Subir un archivo `.csv`.
3. Revisar el resumen de filas, columnas, separador y codificación.
4. Revisar el perfil de columnas.
5. Entrar a **Dashboard por preguntas** para generar visualizaciones automáticas.
6. Entrar a **Gráficos manuales** para crear visualizaciones personalizadas.
7. Entrar a **Consultas guiadas** para escribir preguntas sobre el dataset.
8. Exportar el CSV limpio si se necesita.

---

## Preguntas de prueba

Después de subir un dataset compatible, se pueden probar preguntas como:

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

También se pueden usar preguntas generales como:

```text
Grafica diabetes
```

```text
Muestra un conteo por dictamen
```

```text
Grafica entidad_res_desc
```

---

## Subir a GitHub

Para subir el proyecto a GitHub:

```powershell
git init
git add .
git commit -m "Primer commit - analizador CSV dashboard"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

---

## Nota sobre datasets

No se recomienda subir archivos CSV grandes o sensibles al repositorio.

El archivo `.gitignore` está configurado para ignorar archivos como:

```text
*.csv
*.xlsx
*.xls
```

Cada usuario puede cargar su propio CSV desde la interfaz del sistema.
