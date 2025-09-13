# VMF a Producción — Wine Quality

## Estado
- Aprobado: MAE_global ≤ 0.50, Hit±1 ≥ 0.80, slices OK, monotonicidad OK.

## Artefactos
- Modelo prod: models/model_prod.pkl
- Features y medianas: reports/features.json, reports/medians.json
- Métricas: reports/metrics.json, reports/model_selection.json
- Explicabilidad: reports/perm_importance_top10.(json|png)

## Inferencia
- Desde notebook: predict_one(dict) o predict_from_csv(entrada.csv, salida.csv)

## Operación
- Usar para ranking y alertas. Comunicar ±0.5 como rango típico.
- Monitoreo mensual: MAE, Hit±1, drift en alcohol y volatile acidity.
