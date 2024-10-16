# Segundo Parcial Paradigmas de Programación

## 1. Modelamiento de un Perceptrón en NetLogo

El objetivo de esta punto es implementar y simular un perceptrón en NetLogo. El perceptrón es un modelo simple de una red neuronal que puede clasificar datos linealmente separables. Utilizando el entorno de NetLogo, simularás el aprendizaje de un perceptrón para clasificar un conjunto de datos.

### Requisitos:

A. **Interfaz gráfica en NetLogo:**
   - Diseña una interfaz con sliders para ajustar los valores de:
     - Tasa de aprendizaje.
     - Número de iteraciones.
   - Botones para:
     - Iniciar la simulación del aprendizaje.
     - Restablecer la simulación.

B. **Modelo del Perceptrón:**
   - Implementa el algoritmo del perceptrón que pueda clasificar puntos en un plano 2D.
   - El perceptrón debe tener dos entradas y un valor de sesgo (bias).
   - Los pesos de las entradas deben actualizarse utilizando la regla de actualización basada en la tasa de aprendizaje.
   - Inicializa los pesos y el sesgo en valores aleatorios.

C. **Entrenamiento:**
   - Genera puntos en el plano 2D (turtles en NetLogo) que representen los datos de entrenamiento. Deben ser linealmente separables.
   - Asigna etiquetas (1 o -1) a los puntos según su posición respecto a una línea de separación (la frontera de decisión).
   - Durante el entrenamiento, ajusta los pesos del perceptrón para aprender a clasificar correctamente los puntos.
   
D. **Visualización:**
   - Muestra los puntos y la línea de decisión actualizada en tiempo real durante el entrenamiento.
   - Cambia el color de los puntos correctamente clasificados a verde y los incorrectamente clasificados a rojo.
   
E. **Evaluación:**
   - Después de que el perceptrón se entrene, verifica su rendimiento clasificando un nuevo conjunto de puntos de prueba.
   - Muestra el porcentaje de puntos clasificados correctamente.

### Entregables:
- Código completo de NetLogo con el modelo de perceptrón.
- Capturas de pantalla de la simulación mostrando el entrenamiento y la clasificación de los datos.
- Un informe de una página explicando cómo funciona el perceptrón y cómo fue implementado en NetLogo, incluyendo los resultados obtenidos.

## 2. Implementación de una Calculadora Basada en el Paradigma de Agentes

El objetivo de esta punto es implementar una calculadora utilizando el paradigma de agentes. En este enfoque, cada operación aritmética (suma, resta, multiplicación, división, etc.) será manejada por un agente autónomo. Estos agentes deben comunicarse entre sí para resolver expresiones matemáticas complejas.

### Descripción del Problema

Vas a diseñar una calculadora distribuida en la que cada operación es gestionada por un **agente**. Cada agente será responsable de una operación específica y debe interactuar con otros agentes cuando se le solicite realizar una operación combinada.

A. **Agentes:**
   - Crea un conjunto de agentes, donde cada uno sea responsable de una operación:
     - **Agente Suma**: Gestiona las sumas.
     - **Agente Resta**: Gestiona las restas.
     - **Agente Multiplicación**: Gestiona las multiplicaciones.
     - **Agente División**: Gestiona las divisiones.
     - **Agente Potencia**: Gestiona las operaciones de potencia.
     - **Agente Entrada/Salida**: Recibe las expresiones del usuario, las envía a los agentes adecuados y presenta el resultado final.
   
B. **Funcionalidad del Sistema:**
   - El agente **Entrada/Salida** debe recibir una expresión matemática (por ejemplo, `2 + 3 * 4 - 5`) y distribuir las operaciones entre los agentes correspondientes.
   - Los agentes deben trabajar de manera autónoma, coordinándose entre ellos para resolver expresiones más complejas, como aquellas que requieren manejar precedencia de operadores.
   - El agente **Entrada/Salida** debe recibir las respuestas de los agentes de operación y devolver el resultado final al usuario.

C. **Requisitos de Implementación:**
   - Utiliza un lenguaje de programación que soporte el paradigma de agentes (Mesa en Python).
   - Asegúrate de que los agentes puedan manejar cálculos básicos, así como expresiones más complejas que involucren varias operaciones.
   - Los agentes deben poder gestionar la precedencia de operaciones (por ejemplo, multiplicación y división antes que suma y resta).
   - Permite que la calculadora maneje números enteros y decimales.

D. **Comunicación entre Agentes:**
   - Utiliza un mecanismo de comunicación para que los agentes intercambien mensajes (por ejemplo, cuando el agente **Suma** necesita el resultado de una multiplicación para completar su cálculo).
   - Cada agente debe ser capaz de esperar su turno para recibir los datos necesarios antes de realizar su operación.

### Entregables:
- Código completo de la calculadora basada en agentes.
- Capturas de pantalla o una descripción de cómo funciona la comunicación entre agentes durante el cálculo de una expresión.
- Un informe explicando la arquitectura del sistema, cómo interactúan los agentes y qué mecanismos de comunicación utilizan.

## 3. Implementación de una Calculadora Científica usando el Paradigma de Objetos en Kotlin

El objetivo de este punto es desarrollar una aplicación que implemente una **calculadora científica** utilizando el paradigma de **Programación Orientada a Objetos (POO)** en **Kotlin**. Esta calculadora debe ser capaz de realizar operaciones aritméticas básicas, así como operaciones avanzadas propias de una calculadora científica (trigonometría, potencias, logaritmos, etc.).

### Descripción del Problema

Vas a diseñar una calculadora científica que debe cumplir con los principios de **encapsulamiento**, **herencia**, y **polimorfismo**. La aplicación debe tener una interfaz amigable para el usuario y permitirle realizar cálculos precisos.

### Requisitos:

A. **Clases y Objetos:**
   - Crea una clase base llamada `Calculadora` que contenga las operaciones básicas:
     - Suma
     - Resta
     - Multiplicación
     - División
   - Implementa métodos en la clase `Calculadora` que permitan realizar estas operaciones, asegurando el manejo de posibles excepciones (como la división por cero).
   
B. **Herencia y Extensión de Funcionalidades:**
   - Crea una clase derivada llamada `CalculadoraCientifica` que herede de `Calculadora` y extienda las funcionalidades agregando:
     - Funciones trigonométricas: seno, coseno, tangente.
     - Potencias y raíces.
     - Logaritmos (base 10 y base e).
     - Funciones exponenciales.
     - Conversión de grados a radianes y viceversa.

C. **Polimorfismo:**
   - Utiliza polimorfismo para implementar sobrecarga de operadores o métodos que permitan realizar cálculos con distintos tipos de datos (números enteros, decimales).

D. **Manejo de Excepciones:**
   - Implementa manejo de excepciones para manejar errores comunes, como la introducción de entradas no válidas o la división por cero.
   - Muestra mensajes claros y concisos al usuario cuando ocurran estos errores.

E. **Funcionalidades adicionales:**
   - Implementa la capacidad de evaluar expresiones completas (por ejemplo, `2 + 3 * sin(45) - log(10)`).
   - Permite que el usuario guarde un valor en la memoria y lo recupere más tarde (funciones de Memoria M+, M-, MR).

### Entregables:
- Código completo de la calculadora científica en Kotlin.
- Capturas de pantalla mostrando el funcionamiento de la calculadora, con ejemplos de cálculos básicos y avanzados.
- Un informe explicando cómo aplicaste los principios de la Programación Orientada a Objetos (encapsulamiento, herencia, polimorfismo) en la solución.

