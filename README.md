# ML-Predictive-model-Class-Imbalance-Data
Model predictivo de la permanencia de un cliente que mide el F1 y AUC-ROC. Se aplican técnicas de equilibrio de clases: Submuestreo y Ajuste de umbral.

# Descripcion del proyecto <a id='project_description'></a>
Los clientes de Beta Bank se están yendo, cada mes, poco a poco. Los banqueros descubrieron que es más barato salvar a los clientes existentes que atraer nuevos.

## Objetivo <a id='objective'></a>
Predecir si un cliente dejará el banco pronto. Tú tienes los datos sobre el comportamiento pasado de los clientes y la terminación de contratos con el banco.

Crea un modelo con el máximo valor *F1* posible. Para aprobar la revisión, necesitas un valor *F1* de al menos 0.59. Verifica F1 para el conjunto de prueba.

Además, debes medir la métrica *AUC-ROC* y compararla con el valor *F1*.

## Conclusiones <a id='end'></a>
1. En la etapa de inicializacion del proyecto, se revisaron los datos entregados donde se observo que habian valores nulos en la columna `tenure`; sin embargo, se valido que esto no impactaba en la proporcion de la columna objetivo por lo que se opto en depurar estos valores y asi tener un dataset limpio.
2. En la preparacion del dataset, se generaron las variables caracteristicas y objetivo, se transformaron todos los datos en numericos aplicando las tecnicas One-Hot y estandarizacion escalar y finalmente, se segmento el dataset en 3 conjuntos: entrenamiento, validacion y prueba.
3. Se valido que existia desequilibrio en las clases de entrenamiento en una proporcion de 80% = 0 y 20% = 1. Con este desequilibrio de datos entrenamos 3 modelos teniendo como resultado probabilidades de F1 no tan bajas pero con muchos errores de prediccion.
4. Para balancear las clases aplicamos 2 tecnicas: submuestreo y ajuste de umbral. Para cada una de las tecnicas entrenamos los 3 modelos donde el mejor modelo fue el de random forest aplicando el ajuste de umbral a 0.345 y n_estimators=100. Obteniendo un valor F1= 0.635262.
5. Finalmente, aplicamos el mejor modelo obtenido con el conjunto de pruebas logrando predicciones un poco mas correctas y el siguiente resultado: 
    - F1: 0.48
    - ROC_AUC: 0.73

![output](https://github.com/RitshuCrispin/ML-Predictive-model-Class-Imbalance-Data/assets/130596539/9be300bb-9afe-44fe-a3d5-235d78353c07)
