# caso1_ia


## ¿Qué decisiones de preparación de datos y de modelado explican el mejor desempeño alcanzado, y con qué evidencia las sostienen?

Esta pregunta ordena el trabajo, pero sobre todo orienta la forma de la conclusión. Al cerrar el
informe el equipo debe poder responder, con evidencia propia y en lenguaje claro: 
- qué hace el modelo
- con qué precisión lo hace (en dólares, no solo en abstracto)
- qué no hace o en qué casos falla
- qué sugerirían como próximo paso si el trabajo continuara.

# Caso de estudio 1 — Predicción del precio de viviendas (Ames Housing)

Inteligencia Artificial I — Machine Learning clásico
Equipo: Julián Bevc, Lucía Olivera, Belén Tellechea

**Pregunta central:** ¿Qué decisiones de preparación de datos y de modelado
explican el mejor desempeño alcanzado, y con qué evidencia las sostienen?

Modelo final: Stacking de ElasticNet, SVR y Gradient Boosting (scikit-learn).

## Estructura del repositorio

- `src/Ames_Housing_Modeling_v3.ipynb`: notebook final (preparación, modelado,
  evaluación y predicciones de test).
- `src/EDA_Ames_Housing.ipynb`: análisis exploratorio.
- `src/deprecated-versions/`: versiones anteriores del notebook de modelado (v0 a v2).
- `ames-housing-desarrollo-estudiantes/`: datos entregados por la cátedra
  (`train.csv`, `validation.csv`, `data_description.txt`).

## Cómo ejecutar

1. Preparar un entorno con Python 3.10 o superior y scikit-learn (1.2 o superior),
   pandas, NumPy, SciPy y Matplotlib. No se instala nada desde el notebook.

   ```bash
   pip install scikit-learn pandas numpy scipy matplotlib jupyter
   ```

2. Verificar que `train.csv` y `validation.csv` estén en
   `ames-housing-desarrollo-estudiantes/` (ya vienen en el repositorio).
   El notebook también los busca en `data/` y en su propia carpeta.
3. Copiar el archivo de test en esa misma carpeta con el nombre `test.csv`
   (mismas columnas, sin `SalePrice`). La ruta está definida una sola vez, en
   `TEST_PATH`, en la primera celda de código.
4. Abrir `src/Ames_Housing_Modeling_v3.ipynb` y ejecutar todas las celdas en
   orden (Restart & Run All). Tarda unos 6 minutos en una máquina de 2 núcleos.
5. Las predicciones quedan en `src/predicciones_test.csv`, con las columnas
   `Id` y `SalePrice`.

No hay que editar código: si `test.csv` no está, el notebook igual corre
completo y ensaya el mismo flujo con la partición de validación.

## Reproducibilidad

- Semillas fijas (`random_state = 42`) en todos los pasos con azar.
- Rutas relativas; no se usan archivos intermedios.
- Versión ejecutada: Python 3.13.18, scikit-learn 1.9.1, pandas 3.0.5,
  NumPy 2.5.3, SciPy 1.18.1.
