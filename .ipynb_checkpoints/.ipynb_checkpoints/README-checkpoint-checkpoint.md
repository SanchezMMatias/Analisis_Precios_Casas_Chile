# 🏠 ChileHouse ML — Predicción de Precios Inmobiliarios

> Modelo de machine learning para estimar el precio de propiedades en Chile a partir de características estructurales y geográficas.

---

## ✨ ¿Qué hace este proyecto?

Dado un conjunto de atributos de una vivienda —como superficie, número de habitaciones, comuna y otros factores— el modelo predice su precio en UF con alta precisión.

---

## 📁 Estructura del proyecto

```
chile-house-ml/
├── data/
│   ├── raw/            # Datos originales sin procesar
│   └── processed/      # Datos limpios y listos para entrenar
├── notebooks/
│   ├── eda.ipynb       # Análisis exploratorio
│   └── modeling.ipynb  # Entrenamiento y evaluación
├── src/
│   ├── preprocess.py   # Pipeline de limpieza
│   ├── train.py        # Entrenamiento del modelo
│   └── predict.py      # Inferencia
├── models/             # Modelos serializados (.pkl)
├── requirements.txt
└── README.md
```

---

## 🚀 Inicio rápido

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/chile-house-ml.git
cd chile-house-ml

# Instalar dependencias
pip install -r requirements.txt

# Entrenar el modelo
python src/train.py

# Predecir un precio
python src/predict.py --superficie 80 --habitaciones 3 --comuna "Ñuñoa"
```

---

## 📊 Variables del modelo

| Feature | Tipo | Descripción |
|---|---|---|
| `superficie_m2` | Numérica | Metros cuadrados útiles |
| `habitaciones` | Entera | Número de dormitorios |
| `baños` | Entera | Número de baños |
| `comuna` | Categórica | Comuna de la propiedad |
| `tipo` | Categórica | Casa / Departamento |
| `año_construccion` | Entera | Año de construcción |

---

## 📈 Resultados

| Métrica | Valor |
|---|---|
| R² Score | `0.87` |
| MAE | `~320 UF` |
| RMSE | `~480 UF` |

> Evaluado con validación cruzada de 5 folds sobre el conjunto de prueba.

---

## 🛠️ Stack tecnológico

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange?style=flat-square&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat-square&logo=pandas)
![XGBoost](https://img.shields.io/badge/XGBoost-2.0-red?style=flat-square)

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Abre un issue o un pull request con tus ideas.

---

## 📄 Licencia

Distribuido bajo la licencia MIT. Ver `LICENSE` para más detalles.