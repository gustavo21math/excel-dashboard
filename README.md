# Global Music Streaming Analytics (Excel Dashboard)

Este proyecto documenta un dashboard en Excel construido con datos de Kaggle sobre tendencias globales de streaming musical y comportamiento de oyentes.

## Entregables

- Dashboard final en Excel: `dashboard/global-music-streaming-dashboard.xlsx`
- Documentacion del proceso: `docs/process.md`
- Capturas del dashboard: `docs/screenshots/`

## Fuente de datos

- Dataset: **Global Music Streaming Trends & Listener Insights** (Kaggle)
- Enlace: [Global Music Streaming Trends & Listener Insights](https://www.kaggle.com/datasets/atharvasoundankar/global-music-streaming-trends-and-listener-insights)
- Autor del dataset: Atharva Soundankar
- Volumen de datos: **50,000 registros** de oyentes y sesiones de streaming
- Nota: el CSV no se versiona en este repositorio; solo se referencia la fuente.

## Que muestra el dashboard

- Top Genero musical
- Pais (vista geoespacial)
- Plataforma de streaming
- KPI de tiempo promedio de escucha
- KPI de usuarios premium
- KPI de tasa de repeticion de canciones

## Demostracion interactiva

El siguiente GIF muestra la manipulacion del dashboard en tiempo real: filtros por pais, plataforma y genero, y la actualizacion de los KPIs sobre los **50,000 registros** del dataset.

![Demostracion del dashboard](docs/screenshots/dashboard.gif)

## Reproducibilidad en Excel

1. Descargar el dataset desde Kaggle.
2. Abrir `dashboard/global-music-streaming-dashboard.xlsx`.
3. Ir a **Data > Get Data > From Text/CSV** para reconectar el origen si es necesario.
4. Actualizar consultas con **Refresh All**.
5. Verificar tablas dinamicas, segmentadores y graficos en la hoja de dashboard.

## Herramientas utilizadas

- Microsoft Excel (Power Query, tablas dinamicas, segmentadores, mapas y tarjetas KPI)
- Git + GitHub para versionado y publicacion
