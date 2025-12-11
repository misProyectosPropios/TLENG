1 - Respuesta

Un algoritmo sería: hacer la resta de cada lenguaje y verificar si son vacíos

2 - Respuesta

Una posibilidad
+ Hacer un automata que acepte todo el lenguaje y verificar si denotan el mismo lenguaje 
Otra posibilidad:
+ Minimizarlo y verificar si es de tamaño 1 con un estado final

3  - Respuesta

Le aplico DFS. Si veo un ciclo, sé que va a ser infinito, pues al haber un ciclo puede recorrerlo por una cantidad ilimitada de veces, generando que pueda tener infinitas cadenas.

4  - Respuesta

Analicemos la situación:

+ 2 estados que pueden ser finales o no finales. Es decir $2^2$ opciones
+ $2 * 2$ flechas. Cada una de estas apunta hacia si mismo o hacia el otro estado, es decir:
	+ $4^2$ opciones

Juntando los 2 datos, tenemos que la cantidad de opciones es:
+ $2^2 * 4^2$

5  - Respuesta

5.1 - Respuesta - En clase

Supongamos que no fue así.

Es decir

Sea AFD A mínimo y por la suposición, $\bar{A}$ no es mínimo
#TODO

6  - Respuesta

No lo llegamos a ver, investigar más adelante

7  - Respuesta

7.1 -

Correcto, si tiene algún estado trampa es simplemente agregar más información, si no tiene estado trampa, entonces 

+ Desenrollamos por pumping algún ciclo y listo
+ Agregamos estados inaccesibles y listo
+ Agregamos más estados 

7.2 - 

Falso. Contra-ejemplo

La clausura de Kleene es regular y como subconjunto tiene el conjunto de Halt que no es computable

7.3 -

Mismo argumento de antes con Halt de nuevo

7.4 - 

Sip, eso es lo hermoso de estos

7.5 -

Sip, son las mejores máquinas de pila que hay

7.6 - 

Falso, podes tener máquinas de Turing que para reconocer una palabra por ejemplo, hagan un millón de transiciones, mientras que la cadena sea 1.

Ejemplo:
Reconoce todo el lenguaje, pero hace 1.000.000 de transiciones siempre
```S++
Z1 := 1.000.000
while Z1 != 0:
	Z1--
Y := 1
```

7.7 - 

Verdadero.

El automata que se genera por revertir la función de transición sigue siendo un AF, posiblemente no determinístico, pero, acepta un lenguaje regular. Ahora, si acepta un lenguaje regular, podemos hacer la intersección entre $M^r$ y $M$ y obtenemos un autómata regular (VAMOS!!)

8  - Respuesta

Falso,

9  - Respuesta

10  - Respuesta

11  - Respuesta

12  - Respuesta

13  - Respuesta

14  - Respuesta

15  - Respuesta

16  - Respuesta

17  - Respuesta

18  - Respuesta

19  - Respuesta

