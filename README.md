# Proyecto de Taller de Machine Learning - Actividad 2

Este proyecto implementa un agente de inteligencia artificial que aprende a navegar en un mapa con obstáculos usando el algoritmo **Policy Gradient (REINFORCE)**.

## ¿Qué hace este proyecto?
El objetivo es entrenar a un agente para que:
1.  Salga de la posición inicial (0,0).
2.  Evite caer en los "hoyos" (obstáculos).
3.  Llegue a la meta final para ganar.
4.  Opcionalmente recoja un objeto para obtener puntos extra.

## Cómo ejecutarlo

### Opción 1: En tu computadora (Recomendado)
1.  Asegúrate de tener Python instalado.
2.  Instala las librerías necesarias ejecutando este comando en la terminal:
    ```bash
    pip install -r requirements.txt
    ```
3.  Abre el notebook:
    ```bash
    jupyter notebook notebooks/Actividad2.ipynb
    ```
4.  Dentro de Jupyter, ve al menú **Cell** -> **Run All** para ejecutar todo el código de una vez.
    *   Verás una barra de progreso del entrenamiento.
    *   Al final, verás una animación del agente moviéndose y gráficos de calor que muestran cómo aprendió la ruta.

### Opción 2: Google Colab
1.  Sube el archivo `notebooks/Actividad2.ipynb` a tu Google Drive.
2.  Ábrelo con Google Colab.
3.  Dale a "Ejecutar todas" (Ctrl+F9). No necesitas instalar nada extra.

## Estructura del Informe (Los 4 Pasos)
Si necesitan redactar el informe, aquí está la guía basada en lo que pidió el profesor:

### 1. Inteligencia
Definimos el éxito como **maximizar la recompensa total**. El agente gana puntos por llegar a la meta y pierde muchos puntos si cae en un hoyo. El alcance del proyecto es un entorno de grid 9x9 simulado.

### 2. Proceso Empresarial
El objetivo estratégico es demostrar cómo un algoritmo de aprendizaje por refuerzo puede resolver problemas de navegación autónoma aprendiendo de su propia experiencia, sin necesidad de reglas "if-else" complejas escritas a mano.

### 3. Tecnología de la IA
Usamos **Policy Gradient (REINFORCE)**. Es un método donde el agente tiene una red neuronal (o en este caso, una tabla de probabilidades) que ajusta poco a poco. Si una serie de acciones lleva a un buen resultado, aumenta la probabilidad de repetir esas acciones en el futuro.

### 4. Proceso de Cambio
La implementación está hecha en **Python** puro con **NumPy** para las matemáticas. Un riesgo potencial (Cáncer de IA) es que el agente se quede dando vueltas en círculos para no perder, pero lo solucionamos ajustando las recompensas.

## Archivos Importantes
- `notebooks/Actividad2.ipynb`: El código principal del proyecto.
- `requirements.txt`: Lista de librerías necesarias.
