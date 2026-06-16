# Proceso de construccion del dashboard en Excel

## 1) Objetivo de analisis

Construir un dashboard interactivo para explorar patrones de consumo musical global:

- preferencias por genero
- variaciones por pais
- comportamiento por plataforma
- relacion entre uso premium, tiempo de escucha y repeticion de canciones

## 2) Preparacion de datos

Fuente: [Global Music Streaming Trends & Listener Insights (Kaggle)](https://www.kaggle.com/datasets/atharvasoundankar/global-music-streaming-trends-and-listener-insights)

El dataset contiene **50,000 registros** con informacion de oyentes, generos musicales, paises, plataformas de streaming y metricas de comportamiento.

Flujo recomendado en Power Query:

1. Importar CSV desde Kaggle.
2. Revisar tipos de datos por columna (texto, numerico, fecha).
3. Estandarizar categorias (por ejemplo nombres de plataforma/genero).
4. Tratar valores nulos o inconsistentes.
5. Cargar modelo limpio a hoja de datos o modelo de datos.

Hojas del archivo `dashboard/global-music-streaming-dashboard.xlsx`:

| Hoja | Proposito |
|------|-----------|
| `Global_Music_Streaming_Listener` | Datos base importados desde Kaggle |
| `calculator` | Calculos y KPIs del dashboard |
| `platform` | Agregacion por plataforma de streaming |
| `country` | Agregacion por pais |
| `country_dashboard` | Vista de mapa y metricas por pais |
| `avg minutes` | Metricas de tiempo de escucha |

## 3) Construccion del dashboard

Elementos principales:

- Grafico de barras: Top Genero
- Mapa: Distribucion por pais
- Grafico de barras: Uso por plataforma
- Tarjetas KPI:
  - Avg Listening Time
  - Premium Users
  - Repeat Song Rate

Interaccion:

- Segmentador de pais
- Segmentador de plataforma

## 4) Formulas y logica en Excel (ejemplos)

> Ajustar nombres de columnas/tablas segun el archivo final.

- Promedio de escucha:

```excel
=PROMEDIO(TablaDatos[ListeningTimeHours])
```

- Porcentaje de usuarios premium:

```excel
=CONTAR.SI(TablaDatos[IsPremium],"Yes")/CONTARA(TablaDatos[UserId])
```

- Tasa de repeticion:

```excel
=PROMEDIO(TablaDatos[RepeatRate])
```

- Conteo por genero (si aplica fuera de tabla dinamica):

```excel
=CONTAR.SI(TablaDatos[Genre],A2)
```

## 5) Evidencia visual

Se grabo un GIF (`docs/screenshots/dashboard.gif`) que documenta la manipulacion del dashboard: aplicacion de filtros por pais, plataforma y genero, y la reaccion de los KPIs sobre el conjunto de 50,000 registros.

El GIF se muestra en el `README.md` como demostracion interactiva del proyecto.

## 6) Notas para publicacion en GitHub

- Subir solo el archivo final `.xlsx` y documentacion.
- No subir el CSV crudo si prefieres mantener el repo liviano.
- Mantener referencia directa al dataset de Kaggle en el README.
