# 🧠 Fundamentos de Machine Learning y Redes Neuronales

Este repositorio contiene una explicación detallada y los conceptos fundamentales detrás del proceso de desarrollo y entrenamiento de un modelo de **Inteligencia Artificial** o una **Red Neuronal** desde sus bases.

## 🚀 Proceso de Aprendizaje de una IA (El Ciclo Completo)

El entrenamiento de una IA se basa en un ciclo iterativo y sistemático cuyo objetivo es ajustar los parámetros internos del modelo para minimizar el error de predicción.

---

### 1. 📂 Preparación y División de Datos

El primer paso crucial es la gestión de los datos de entrada.

* **Dataset (Conjunto de Datos):** La totalidad de los datos disponibles se divide estratégicamente:
    * **Training Set (Conjunto de Entrenamiento):** Se utiliza para que el modelo **aprenda** y ajuste sus pesos (W) y sesgos (b).
    * **Test Set (Conjunto de Prueba):** Se mantiene separado para **evaluar** el rendimiento final del modelo con datos que nunca ha procesado.
    > *Este proceso asegura que el modelo pueda **generalizar** y no solo memorizar.*

---

### 2. 🎯 Función de Pérdida (Loss Function) 

[Image of Loss Function Parabola]


La función de pérdida es la métrica matemática que cuantifica el grado de **error** del modelo.

* **Definición:** Mide la distancia entre el valor predicho ($\hat{y}$) y el valor real ($y$).
* **Objetivo:** El entrenamiento busca encontrar los valores de pesos y sesgos que resulten en el **punto mínimo** de esta función. Un valor bajo significa una alta **precisión** (_accuracy_).

---

### 3. 📉 Optimización: Descenso del Gradiente (Gradient Descent)

El Descenso del Gradiente es el algoritmo usado para navegar la curva de pérdida y encontrar ese punto mínimo.

* **Gradiente:** Representa la pendiente de la función de pérdida. Indica la dirección y la intensidad del cambio que se necesita.
* **Ajuste:** La IA utiliza el gradiente para determinar cómo y cuánto debe **ajustar los pesos y sesgos** en cada iteración, moviéndose progresivamente hacia el punto de menor error.

---

### 4. ⚙️ Entrenamiento en la Red Neuronal

El entrenamiento se divide en dos fases que se ejecutan repetidamente por cada *epoch* (ciclo completo sobre el conjunto de entrenamiento):

#### A. Propagación Hacia Adelante (*Forward Pass*)
1.  Los datos pasan a través de las capas de la red.
2.  En cada neurona, la entrada se multiplica por el **Peso (W)** y se le suma el **Sesgo (b)**.
3.  El resultado se procesa mediante una **Función de Activación** (como la **Sigmoide** que convierte valores en probabilidades entre 0 y 1).
4.  La red genera una **predicción** ($\hat{y}$).

#### B. Retropropagación (*Backpropagation*) 
Esta es la fase de **aprendizaje** donde el error se propaga hacia atrás.

1.  Se calcula la **diferencia** entre la predicción y el valor real (el error).
2.  La retropropagación utiliza el **Cálculo de Gradientes** para determinar exactamente qué neurona o conexión contribuyó más al error.
3.  Esta información es utilizada por el **Descenso del Gradiente** para realizar la **actualización de pesos y sesgos**, cerrando el ciclo de aprendizaje y optimizando el modelo para la siguiente iteración.

---

### 5. ✅ Evaluación Final

Tras completar el entrenamiento, el modelo se valida con el **Test Set**.

* La **precisión** (_accuracy_) y otras métricas se calculan para determinar la capacidad real del modelo para hacer predicciones correctas en datos que no formaron parte de su entrenamiento.

## 🛠️ Conceptos Clave Adicionales

* **LLM (Large Language Model):** El diagrama hace referencia a que la red neuronal puede ser la base de un LLM que realiza predicciones de palabras.
* **GPU (Unidad de Procesamiento Gráfico):** Es esencial para la IA moderna, ya que realiza de manera eficiente los **cálculos matriciales** masivos requeridos por el entrenamiento en paralelo.
* **Matrices (W, b):** Los **pesos** y **sesgos** de la red se almacenan como matrices. Son los parámetros **internos** que la IA ajusta para aprender la relación entre los datos.
