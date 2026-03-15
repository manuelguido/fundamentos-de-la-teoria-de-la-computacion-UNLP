# Trabajo Práctico Nro 2 - La jerarquía de la Computabilidad

## Ejercicio 1. Responder breve y claramente los siguientes incisos:

### 1. ¿En qué se diferencian los lenguajes recursivos, los lenguajes recursivamente enumerables no recursivos y los lenguajes no recursivamente enumerables?

### 2. Probar que $R ⊆ RE ⊆ 𝔏$. <i>Ayuda: usar las definiciones.</i>

### 3. Dijimos en clase que el hecho de que si L es recursivo entonces LC también lo es, significa en términos de problemas que si un problema es decidible entonces también lo es el problema contrario. ¿Qué significa en términos de problemas que la intersección de dos lenguajes recursivos es también un lenguaje recursivo?

### 4. Explicar por qué no es correcta la siguiente prueba de que si L ∈ RE, también LC ∈ RE: dada una MT M que acepta L, entonces la MT M’, igual que M pero con los estados finales permutados, acepta LC.

### 5. ¿Qué lenguajes de la clase CO-RE tienen MT que los aceptan? ¿También los deciden?

### 6. Probar que el lenguaje Ʃ\* de todas las cadenas y el lenguaje vacío ∅ son recursivos. Alcanza con plantear la idea general. <i>Ayuda: encontrar MT que los decidan.</i>

### 7. Probar que todo lenguaje finito es recursivo. Alcanza con plantear la idea general. <i>Ayuda: encontrar una MT que lo decida (pensar cómo definir sus transiciones para cada una de las cadenas del lenguaje).</i>

## Ejercicio 2. Considerando la Propiedad 2 estudiada en clase:

### 1. ¿Cómo implementaría la copia de la entrada w en la cinta 2 de la MT M?

### 2. ¿Cómo implementaría el borrado del contenido de la cinta 2 de la MT M?

## Ejercicio 3. Probar:

### 1. La clase R es cerrada con respecto a la operación de unión. <i>Ayuda: la prueba es similar a la desarrollada para la intersección.</i>

### 2. La clase RE es cerrada con respecto a la operación de intersección. <i>Ayuda: la prueba es similar a la desarrollada para la clase R.</i>

## Ejercicio 4. Sean L1 y L2 dos lenguajes recursivamente enumerables de números naturales codificados en unario (por ejemplo, el número 5 se representa con 11111). Probar que también es recursivamente enumerable el lenguaje L = {x | x es un número natural codificado en unario, y existen y, z, tales que y + z = x, con y ∈ L1, z ∈ L2}. <i>Ayuda: la prueba es similar a la vista en clase, de la clausura de la clase RE con respecto a la operación de concatenación.</i>

## Ejercicio 5. Dada una MT M1 con alfabeto Γ = {0, 1, B}:

### 1. Construir una MT M2, utilizando la MT M1, que acepte, cualquiera sea su cadena de entrada, sii la MT M1 acepta al menos una cadena.

### 2. ¿Se puede construir además una MT M3, utilizando la MT M1, que acepte, cualquiera sea su cadena de entrada, sii la MT M1 acepta a lo sumo una cadena? Justificar. <i>Ayuda para la parte (1): si M1 acepta al menos una cadena, entonces existe al menos una cadena de símbolos 0 y 1, de tamaño n, tal que M1 la acepta en k pasos. Teniendo en cuenta esto, pensar cómo M2 podría simular M1 considerando todas las cadenas de símbolos 0 y 1 hasta encontrar eventualmente una que M1 acepte (¡cuidándose de los casos en que M1 entre en loop!).</i>
