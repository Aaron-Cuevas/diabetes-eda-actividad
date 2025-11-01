# Diabetes EDA — Pima Indians (TC1002S)

Este repositorio contiene el análisis descriptivo y visual del dataset **Pima Indians Diabetes** (`diabetes.csv`).

## Requisitos
- Python 3.10+ (funciona en 3.14)
- Paquetes: `pandas`, `numpy`, `matplotlib`, `seaborn`, `jupyterlab`

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip
python -m pip install pandas numpy matplotlib seaborn jupyterlab
source .venv/bin/activate   # si creaste venv
jupyter lab
En el navegador, abre EstadisticaDescriptiva-bueno.ipynb y ejecuta todas las celdas (Kernel → Restart & Run All).

Contenido del cuaderno
	•	Carga y validación del dataset (nulos y tipos).
	•	Estadística descriptiva de Pregnancies, DiabetesPedigreeFunction (DPF) y Outcome.
	•	Visualizaciones:
	•	Barras: Outcome (clase 0/1).
	•	Boxplot: Pregnancies por Outcome (comparación de distribuciones).
	•	Heatmaps de correlación:
	•	Matriz completa (diagonal en 1).
	•	Enfoque en Outcome y submatriz DPF vs Outcome (2×2).
	•	Respuestas a: variables poco informativas, rangos, atípicos (IQR) y correlaciones relevantes.

Datos

Coloca data/diabetes.csv (Pima Indians Diabetes). Si no existe la carpeta:

Datos

Coloca data/diabetes.csv (Pima Indians Diabetes). Si no existe la carpeta:
mkdir -p data
# copia aquí tu diabetes.csv
(Opcional) Exportar a PDF

Requiere navegador headless:
python -m pip install -U "nbconvert[webpdf]" playwright
python -m playwright install chromium
jupyter nbconvert --to webpdf "EstadisticaDescriptiva-bueno.ipynb" --output-dir reports --output "EstadisticaDescriptiva-bueno"
El PDF quedará en reports/EstadisticaDescriptiva-bueno.pdf.

Estructura sugerida
diabetes-eda-actividad/
├─ data/diabetes.csv
├─ EstadisticaDescriptiva-bueno.ipynb
├─ reports/ (opcional)
│  └─ EstadisticaDescriptiva-bueno.pdf
└─ README.md
