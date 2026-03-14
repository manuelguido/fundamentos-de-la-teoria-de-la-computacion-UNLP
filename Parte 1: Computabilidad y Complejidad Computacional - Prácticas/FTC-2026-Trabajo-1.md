# Trabajo Práctico Nro 1 - La máquina de Turing (MT)

## Conceptos clave para entender mejor la práctica

**Aclaración:** Esta práctica se enfoca en **MTs que resuelven problemas de decisión**.

### ¿Qué es un Lenguaje?

Un **lenguaje** es simplemente un conjunto de cadenas (secuencias de símbolos) que cumplen una regla específica.

**Ejemplo:**

- Alfabeto: Σ = {a, b}
- Lenguaje L = {cadenas que tienen igual cantidad de 'a' y 'b'}
- Entonces L = {ab, ba, aabb, abab, baba, ...}

Un lenguaje es la colección de todas las cadenas que satisfacen esa regla.

### ¿Qué es una Máquina de Turing?

Una **MT es un dispositivo teórico** que:

1. Lee símbolos de una cinta
2. Cambia de estado según lo que lee
3. Escribe símbolos en la cinta
4. Se mueve por la cinta
5. **Acepta o rechaza** la cadena (responde SÍ o NO)

**Visualización simple:**

```
Estado: q0
Cinta: [a][b][a][b][_]
       ↑
```

La MT lee, decide qué hacer, se mueve, y eventualmente acepta o rechaza.

### ¿Cómo una MT "resuelve" un Problema?

La MT acepta exactamente las cadenas que pertenecen al lenguaje:

**Ejemplo:**

- **Problema:** "¿Esta cadena tiene igual cantidad de 'a' y 'b'?"
- **MT:** Lee la cadena y dice SÍ (acepta) o NO (rechaza)
- **Lenguaje L(M):** El conjunto de todas las cadenas que la MT acepta

Por eso: **problema = lenguaje**. Son dos formas de decir lo mismo.

**Otra forma de interpretarlo:** La MT es como un verificador automático que lee una entrada y decide si pertenece o no a un lenguaje específico.

---

## Ejercicio 1. Responder breve y claramente los siguientes incisos:

### 1. ¿En qué se diferencia un problema de búsqueda de un problema de decisión?

Un problema de búsqueda es aquel para el cual existe una MT la cual pueda retornar una solución (podría existir mas de una) y pueda retornar NO en caso de que no exista.

Un problema de decisión es aquel para el cual existe una máquina de turing que responde SI o NO

### 2. ¿Por qué en el caso de los problemas de decisión, podemos referirnos indistintamente a problemas y lenguajes?

Una MT que resuelve un problema de decisión acepta exactamente las cadenas que satisfacen el problema. El lenguaje L(M) que acepta es el conjunto de soluciones del problema, por eso problema y lenguaje son lo mismo.

La idea central es: problema de decisión = lenguaje que reconoce la MT que lo resuelve. Son dos formas de ver lo mismo.

### 3. El problema de satisfactibilidad de las fórmulas booleanas, en su forma de decisión, es: “Dada una fórmula φ, ¿existe una asignación A de valores de verdad que la hace verdadera?” Enunciar el problema de búsqueda asociado.

Dada una fórmula booleana φ, encuentre una asignación A de valores de verdad que haga verdadera la fórmula φ, o retorne NO si no existe tal asignación.

### 4. Otra visión de MT es la que genera un lenguaje (visión generadora). En el caso del problema del inciso anterior, ¿qué lenguaje generaría la MT de visión generadora que resuelve el problema?

Una MT de visión generadora es aquella que genera (produce) cadenas de un lenguaje, en lugar de solo reconocerlas. Es decir, explícitamente produce todas las cadenas que pertenecen a un lenguaje.

Una MT generadora para ese problema generaría el lenguaje:

$L(M) = {A₁, A₂, A₃, ... | cada Aᵢ es una asignación de valores de verdad que hace verdadera la fórmula φ}$

El lenguaje L(M) está formado por todas las asignaciones de valores de verdad que satisfacen la fórmula φ, generadas secuencialmente.

**Ejemplo**: Si $φ = (x ∨ ¬y)$:

Genera: $(x=T,y=T)$, $(x=T,y=F)$, $(x=F,y=F)$, ... (todas las asignaciones excepto $x=F,y=T$)

### 5. ¿Qué postula la Tesis de Church-Turing?

La tesis de Church-Turing afirma que todo problema computable se puede resolver con una máquina de Turing.

### 6. ¿Cuándo dos MT son equivalentes? ¿Y cuándo dos modelos de MT son equivalentes?

Dos MT son equivalentes cuando reconocen el mismo lenguaje. Dos modelos de MT son equivalentes si, dada una MT de un modelo, existe una MT equivalente en el otro modelo.

**Explicación con ejemplos:**

- **Dos MTs equivalentes:** Una MT M₁ que acepta ${a^N b^n | n ≥ 0}$ y una MT M₂ que también acepta ${a^n b^n | n ≥ 0}$ son equivalentes, aunque usen estrategias diferentes. Ambas reconocen el mismo lenguaje.

- **Dos modelos equivalentes:** Una MT determinística (MTD) de 1 cinta y una MT no determinística (MTN) de 2 cintas son modelos equivalentes porque cualquier lenguaje que reconozca una MTN puede ser reconocido por una MTD equivalente (posiblemente con más pasos).

## Ejercicio 2. Dado el alfabeto $Ʃ = {0, 1}$:

### 1. Obtener el conjunto Ʃ* y el lenguaje incluido en Ʃ* con cadenas de a lo sumo 2 símbolos.

### 2. Sea el lenguaje $L = {0^n 1^n | n ≥ 0}$. Obtener los lenguajes $Ʃ^* ⋂ L$, $Ʃ^* ⋃ L$ y $L^C$ respecto de $Ʃ^*$.

## Ejercicio 3. En clase se mostró una MT no determinística (MTN) que acepta las cadenas de la forma han o hbn, con n ≥ 0. Construir (describir la función de transición) una MT determinística (MTD) equivalente.

## Ejercicio 4. Describir la idea general de una MT con varias cintas que acepte, de la manera más eficiente posible (menor cantidad de pasos), el lenguaje $L = {a^n b^n c^n | n ≥ 0}$.

## Ejercicio 5. Explicar cómo una MT sin el movimiento S (el no movimiento) puede simular (ejecutar) otra que sí lo tiene.

## Ejercicio 6. En clase se construyó una MT con 2 cintas que acepta $L = {w | w ∈ {a, b}^* y w es un palíndromo}$. Construir una MT equivalente con 1 cinta. Ayuda: la solución que vimos para aceptar el lenguaje de las cadenas $a^n b^n$, con $n ≥ 1$, puede ser un buen punto de partida.

## Ejercicio 7. Construir una MT que calcule la resta de dos números. Ayuda: se puede considerar la idea de solución propuesta en clase.

## Ejercicio 8. Construir una MT que genere todas las cadenas de la forma anbn, con $n ≥ 1$. Ayuda: se puede considerar la idea de solución propuesta en clase.
