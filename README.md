# Conclusiones del Análisis: Evaluación de Automóviles 🚗
Curso: Minería de datos - EDA | Grupo: 10.

Integrantes: Tello Mendez Nicolás, Buitrago Murcia Jersson Fabián.

# Introducción
Este proyecto se enfoca en la evaluación de la calidad de automóviles utilizando técnicas de minería de datos y análisis exploratorio de datos (EDA). El objetivo principal es desarrollar un modelo predictivo que permita clasificar la calidad de un automóvil en función de sus características técnicas y de seguridad, como precio de compra, costo de mantenimiento, número de puertas, capacidad de pasajeros, tamaño del baúl y nivel de seguridad. Este tipo de análisis es útil tanto para consumidores que buscan tomar decisiones informadas al comprar un automóvil, como para empresas que desean entender los factores que influyen en la percepción de calidad de sus productos.
## 1. Resumen del análisis

Se utilizó el dataset Car Evaluation (UCI), compuesto por 1,728 registros y 7 variables principales (compra, mantenimiento, puertas, personas, baúl, seguridad, clase). El análisis siguió los pasos estructurados: importación de librerías, carga y limpieza de datos, tratamiento de valores faltantes, conversión de variables categóricas, análisis descriptivo, visualización de distribuciones, análisis de correlación, test de normalidad, enfoque de predicción, modelado (regresión lineal) y evaluación de resultados.

## 2. Hallazgos principales

- Predominan los autos de la clase “Inaceptable” (unacc), lo que revela un fuerte desbalance en la variable objetivo
- La distribución usual es para autos de 2, 4 o 5 pasajeros, y puertas de 2, 3, 4 o 5, con pocos modelos minoritarios
- Se detectaron valores no numéricos en las variables persons y doors, corregidos durante la limpieza de datos
- Las variables compuestas presentan correlaciones altas con variables originales, aportando valor predictivo
- Ninguna variable numérica sigue una distribución normal

## 3. Respuesta a la pregunta de investigación
¿Es posible predecir la calidad de un auto usando sus características técnicas y de seguridad?

Sí, es posible predecir la calidad de un auto usando las variables seleccionadas. El modelo entrenado (regresión lineal normalizada) alcanzó MSE = 0.035 y R² = 0.53, mostrando capacidad media de predecir la clase de calidad a partir de las variables técnicas y de seguridad

## 4. Interpretación de resultados

Los modelos predictivos distinguen entre autos de diferente calidad, aunque con margen de error. El desbalance en la clase limita la sensibilidad, e influye en que los modelos tiendan a predecir la categoría mayoritaria. El valor de las variables compuestas sugiere que la combinación de atributos mejora la capacidad predictiva general del modelo
<img width="781" height="567" alt="image" src="https://github.com/user-attachments/assets/c6d7ae33-cbdf-4d3b-86bd-4a0a7f652b42" />

## 5. Limitaciones

- Desbalance fuerte hacia la categoría ‘unacc’
- Falta de normalidad afecta algunos algoritmos estadísticos.
- El resultado depende de la codificación empleada y variables incluidas.

## 6. Recomendaciones

- Aplicar técnicas de balanceo de clases para un mejor desempeño en clases minoritarias.
- Probar modelos no lineales o basados en árboles (Random Forest, boosting), robustos frente a variables no normales.
- Ampliar el análisis usando validación cruzada y métricas adicionales
- Explorar y comparar variable importance entre variables originales y compuestas
- Ampliar el dataset con variables externas (precios reales, ratings) si se dispone de ellas.

---
