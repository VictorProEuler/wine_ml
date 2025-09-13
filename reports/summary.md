# Resumen VMF — Wine Quality (regresión)

## Métricas
- Baseline: MAE=0.7049, RMSE=0.8443, R²=-0.0063
- RF simple: MAE=0.4668, RMSE=0.6189, R²=0.4593

## Selección de modelo
- Elegido: **rf_simple**
- Motivo: menor MAE en test; tuning no mejora de forma significativa.
- Archivo: `models/model_prod.pkl`

## Importancia por permutación (top-3)
- alcohol: ΔMAE≈-0.1564 ± 0.0106
- sulphates: ΔMAE≈-0.0763 ± 0.0086
- volatile acidity: ΔMAE≈-0.0393 ± 0.0093

## Artefactos
- `reports/env.json`, `reports/requirements_freeze.txt`
- `reports/metrics.json`, `reports/model_selection.json`
- `reports/perm_importance_top10.json`, `reports/perm_importance_top10.png`

## Próximos pasos (opcionales)
- Validación externa o temporal si aplica.
- Chequeo de correlaciones y drift.
- Exportar pipeline para inferencia.
