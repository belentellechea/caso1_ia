# Ames Housing - datos del Caso de Estudio

Estos archivos contienen una partición docente del `train.csv` original de la
competencia *House Prices: Advanced Regression Techniques*. Se distribuyen en
dos momentos para mantener el test reservado hasta la apertura del podio.

## Archivos

- `train.csv`: 1022 viviendas con `SalePrice` (entrega de desarrollo).
- `validation.csv`: 219 viviendas con `SalePrice` (entrega de desarrollo).
- `test.csv`: 219 viviendas sin `SalePrice` (entrega posterior del podio).
- `sample_submission.csv`: formato de entrega `Id,SalePrice` para las 219
  viviendas de test. Los valores incluidos forman un baseline constante y
  deben sustituirse por las predicciones del modelo.
- `data_description.txt`: descripción original de las variables.

El primer ZIP contiene solo train, validation y la descripción. El segundo ZIP
contiene test y el formato de submission; debe publicarse recién cuando el
equipo docente abra la etapa del podio.

## Uso esperado

1. Desarrollen y comparen modelos únicamente con `train.csv` y
   `validation.csv`.
2. Ajusten todo preprocesamiento solo con los datos correspondientes al
   entrenamiento de cada evaluación.
3. Congelen el pipeline y los hiperparámetros antes de predecir `test.csv`.
4. Entreguen un CSV con exactamente las columnas `Id,SalePrice`, una fila por
   `Id` del test y sin valores faltantes.

La métrica indicada en el documento del caso es RMSE; informen también MAE en
dólares. Un valor menor es mejor.

## Integridad académica

Los identificadores fueron reemplazados para esta edición. No está permitido
buscar, reconstruir o usar etiquetas externas del test ni otros archivos de
Ames obtenidos fuera de la entrega docente.

La semilla del split es `2026`. El equipo docente conserva por separado las
etiquetas del test.
