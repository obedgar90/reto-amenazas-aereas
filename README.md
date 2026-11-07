<p align="right"><b><span style="color:#2E7D32">Pública</span></b></p>

# Detección de amenazas aéreas con redes neuronales profundas

Clasificación de imágenes de **6 clases de objetos aéreos** (avión, cohete, dron, helicóptero, jet y misil) con TensorFlow/Keras. Reto DS_C7_SC3.

## Contenido

| Archivo | Descripción |
|---|---|
| `DS_C7_SC3_NombreCompleto.ipynb` | Cuaderno con la solución completa del reto |

## Qué hace el cuaderno

1. **Exploración y limpieza** de 8,530 imágenes con formatos, modos de color y tamaños heterogéneos. Se detectan duplicados exactos (MD5) y se eliminan las imágenes repetidas en clases distintas. Quedan 7,099 imágenes.
2. **Estandarización** a RGB de 224 × 224 píxeles y división estratificada en entrenamiento (80 %) y prueba (20 %), sin imágenes compartidas entre ambos conjuntos.
3. **Modelo 1:** CNN diseñada desde cero, con aumento de datos y búsqueda de hiperparámetros.
4. **Modelo 2:** transferencia de aprendizaje con MobileNetV2 (extracción de características y ajuste fino).
5. **Modelo 3:** modelo de Teachable Machine entrenado solo con el conjunto de entrenamiento.
6. **Comparación** de los tres modelos con el mismo conjunto de prueba (exactitud, F1 y matriz de confusión), selección del mejor y exportación a `.keras` y TensorFlow Lite.

## Cómo ejecutarlo

1. Coloca la base de datos en `datos/objetos/<clase>/` junto al cuaderno (no se incluye en el repositorio por su tamaño).
2. Instala las dependencias: `pip install tensorflow tf_keras seaborn scikit-learn tqdm pillow` (la primera celda del cuaderno lo hace).
3. Ejecuta todas las celdas. Los datos preparados se generan en `datos_preparados/` y los modelos en `resultados/modelos/`.
4. Para el modelo 3, sigue las instrucciones de la sección 8 del cuaderno.

<p align="right"><b><span style="color:#2E7D32">Pública</span></b></p>
