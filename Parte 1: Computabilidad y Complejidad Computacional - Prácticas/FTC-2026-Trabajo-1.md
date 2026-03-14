# Trabajo Práctico Nro 1 - La máquina de Turing (MT)

## Ejercicio 1. Responder breve y claramente los siguientes incisos:

### 1. ¿En qué se diferencia un problema de búsqueda de un problema de decisión?

### 2. ¿Por qué en el caso de los problemas de decisión, podemos referirnos indistintamente a problemas y lenguajes?

### 3. El problema de satisfactibilidad de las fórmulas booleanas, en su forma de decisión, es: “Dada una fórmula φ, ¿existe una asignación A de valores de verdad que la hace verdadera?” Enunciar el problema de búsqueda asociado.

### 4. Otra visión de MT es la que genera un lenguaje (visión generadora). En el caso del problema del inciso anterior, ¿qué lenguaje generaría la MT de visión generadora que resuelve el problema?

### 5. ¿Qué postula la Tesis de Church-Turing?

### 6. ¿Cuándo dos MT son equivalentes? ¿Y cuándo dos modelos de MT son equivalentes?

## Ejercicio 2. Dado el alfabeto $Ʃ = {0, 1}$:

### 1. Obtener el conjunto Ʃ* y el lenguaje incluido en Ʃ* con cadenas de a lo sumo 2 símbolos.

### 2. Sea el lenguaje $L = {0^n 1^n | n ≥ 0}$. Obtener los lenguajes $Ʃ^* ⋂ L$, $Ʃ^* ⋃ L$ y $L^C$ respecto de $Ʃ^*$.

## Ejercicio 3. En clase se mostró una MT no determinística (MTN) que acepta las cadenas de la forma han o hbn, con n ≥ 0. Construir (describir la función de transición) una MT determinística (MTD) equivalente.

## Ejercicio 4. Describir la idea general de una MT con varias cintas que acepte, de la manera más eficiente posible (menor cantidad de pasos), el lenguaje $L = {a^n b^n c^n | n ≥ 0}$.

## Ejercicio 5. Explicar cómo una MT sin el movimiento S (el no movimiento) puede simular (ejecutar) otra que sí lo tiene.

## Ejercicio 6. En clase se construyó una MT con 2 cintas que acepta $L = {w | w ∈ {a, b}^* y w es un palíndromo}$. Construir una MT equivalente con 1 cinta. Ayuda: la solución que vimos para aceptar el lenguaje de las cadenas $a^n b^n$, con $n ≥ 1$, puede ser un buen punto de partida.

## Ejercicio 7. Construir una MT que calcule la resta de dos números. Ayuda: se puede considerar la idea de solución propuesta en clase.

## Ejercicio 8. Construir una MT que genere todas las cadenas de la forma anbn, con $n ≥ 1$. Ayuda: se puede considerar la idea de solución propuesta en clase.
