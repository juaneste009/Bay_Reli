---
title       : Confiablidad Bayesiana
subtitle    : Una breve introducci�n
author      : Juan Esteban Mej�a Villegas
job         : Estad�stico
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, mathjax]   # {quiz}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Contenido

> 1. Confiabilidad.
> 2. Estad�stica Bayesiana.
> 3. Confiabilidad Bayesiana.

---

## Confiablidad

La confiabilidad es la propiedad de que algo funcione de forma correcta cuando se quiere usar.

Estad�sticamente se define como la probabilidad que un sistema funcione de forma adecuada para lo cual fue desarrollado; se establece un per�odo de tiempo y un conjunto de condiciones para su funcionamiento. La confiablidad puede ser expresada como una funci�n del tiempo.

El an�lisis de confiablidad com�nmente se define bajo respuesta binaria, es decir, �xito/falla; pero es igual de importante analizar los per�odos de tiempo, denominados *tiempo de vida* o *tiempo de falla*.

Algunas razones para recolectar datos de Confiabilidad es evaludar las caracter�stias de los materiales, predecir el tiempo de falla del producto, comparar con competidores, etc.

Las caractar�stica de los datos de Confiabilidad pueden ser: datos censurados (se establece un per�odo para el estudio), datos con respuesta binaria (positiva).

---

## Confiabilidad (Cont.)

En la estad�stica cl�sica com�nmente se utilizan distribuciones exponencial, lognormal, Weibull, gamma y gamma inversa.

En la figura de abajo podemos observar la funci�n de densidad de probabilidad de una variable aleatoria $exp(2)$:

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1-1.png)

---

## Confiablidad (Cont.)

En el an�lisis de Confiabilidad la m�trica m�s usada es su distribuci�n de *tiempo de falla* y los datos de los cuales se tiene informaci�n es acerca de los tiempos de falla y variables explicativas que dar�n informaci�n adicional al modelo.

La funci�n de *tiempo de falla* puede ser caracterizada por:

> 1. Funci�n de distribuci�n acumulada: nos da la probabilidad de que una unidad falle en el tiempo $t$ o antes. $$F(t) = P(T \leq t)$$

> 2. Funci�n de densidad de probabilidad: se usa para representar la frecuenca relativa de los tiempos de falla en funci�n del tiempo. $$F(t) = \int_0^t f(x)dx$$

---

## Confiablidad (Cont.)

> 3. Funci�n de supervivencia: tambi�n conocida como funci�n de confiabilidad, nos da la probabilidad de que una unidad funcione m�s all� del tiempo $t$. $$ s(t) = P(T > t) = 1- F(t) = \int_t^{\infty} f(x)dx$$

> 4. Funci�n Hazard: conocida como tasa de riesgo, expresa la posibilidad a fallar en el siguiente intervalo de tiempo definido.

> 5. Y otras como: funci�n de Hazard acumulada, raz�n Hazard promedio, funci�n cuantil y distribuci�n cualtil.

---

## Estad�stica Bayesiana

La estad�stica Bayesiana en los �ltimos a�os a tomado mucha fuerza con el desarrollo de la computaci�n dado que es altamente demandante en simulaciones computacionales. �ltimamente a tomado mucha relevancia ya que se pueden resolver problemas que con m�todos cl�sicos no ha sido posible.

La implementaci�n de m�todos Bayesianos permite representar lo que creemos acerca de los datos en una distribuci�n apriori, luego cuando podemos analizar los datos recolectados lo que creemos va ser actualizado con la distribuci�n aposteriori.

---

## Estad�stica Bayesiana - Distribuci�n apriori

Las distribuciones apriori se pueden clasificar en:

> 1. Apriori propia: es una distribuci�n que asigna pesos no negativos y que suman o integran hasta uno, a todos los valores posibles del par�metro.

> 2. Apriori No Informativa/Informativa: una distribuci�n apriori no informativa refleja una ignorancia totl o un conocimiento limitado sobre el par�metro de inter�s. Caso contrario con la informativa, va expresar informaci�n que conocemos, la dificultad est� en la identificaci�n, selecci�n y justificaci�n de la distribuci�n apriori.

> 3. Apriori Conjugada: al proceder a su actualizaci�n mediante la informaci�n muestral, la distribuci�n aposteriori es igual a la apriori.

---

## Confiabilidad Bayesiana

En Confiabilidad Bayesiana, la modelaci�n estad�stica consta de dos partes:

1. La funci�n de verosimilitud: tipicamente construida de la distribuci�n muestral, definida por la funci�n de densidad de probabilidad asumida de la data, de la cual no se conocen los par�metros.
2. La distribuci�n apriori: se obtiene antes de analizar la data experimental y representa el conocimiento que tenemos de los datos.

En el an�lisis Bayesiano, la *funci�n de verosimilitud* y la *distribuci�n apriori* son la base para la estimaci�n de los par�metros e inferencia.

La estad�stica Bayesiana permite el uso de informaci�n que va m�s all� de la data experimental, esto se conoce como *probabilidad subjetiva*, por lo general se usa otra informaci�n relevante acerca de los par�metros de confiablidad desconocidos. Esta informaci�n es extremandamente �til y es un componente muy poderoso en el enfoque Bayesiano.

---

## Confiabilidad Bayesiana (Cont.)

Despu�s que lo datos de la prueba han sido obtenidos, la *distribuci�n aposteriori* describe completamente la incertidumbre asociada a los par�metros; la *distribuci�n aposteriori* se calcula v�a **Teorema de Bayes** usando la *funci�n de verosimilitud* y la *distribuci�n apriori*. La sucuencia l�gica de los m�todos Bayesianos para el an�lisis de Confiablidad hace que sea f�cil de describir, f�cil de interpretar y usar.

Un ejemplo de una distribuci�n apriori y una aposteriori se puede ver a continuaci�n.

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png)

---

### Bibliograf�a

J.C. Correa Morales. Introduci�n a la Estad�stica Bayesiana. Escuela de Estad�stica, Universidad Nacional de Colombia, Sede Medell�n. 2008.

M.C. Jaramillo Elorza. Notas de clase: Estad�stica Industrial II. Escuela de Estad�stica, Universidad Nacional de Colombia, Sede Medell�n 2015.

M.S. Hamada, A.G. Wilson, C.S. Reese and H.F. Martz. Bayesian Reliability, Springer Series in Statistics. 2008.
