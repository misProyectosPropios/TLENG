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

Falso, podes tener máquinas de Turing que para reconocer una palabra por ejemplo, pero haga un millón de transiciones * tamaño de la palabra, mientras que la cadena sea 1.

Ejemplo:
Reconoce todo el lenguaje, pero hace 1.000.000 de transiciones siempre
```S++
Z1 := 1.000.000
Z1 := Z1 * X1
while Z1 != 0:
	Z1--
Y := 1
```

7.7 - 

Verdadero.

El automata que se genera por revertir la función de transición sigue siendo un AF, posiblemente no determinístico, pero, acepta un lenguaje regular. Ahora, si acepta un lenguaje regular, podemos hacer la intersección entre $M^r$ y $M$ y obtenemos un autómata regular (VAMOS!!)

8  - Respuesta

8 - 1

Falso, contra ejemplo HALT. Es una función total de $\mathbb{N}\to\mathbb{N}$, pero no es total computable (ni siquiera es computable).

8 - 2

Sip, devuelve true siempre porque vimos que todas las funciones parcialmente computables las podemos poner en biyección con los naturales (si no hay pass al final)

8 - 3

Debe de serlo, no pensé mucho la respuesta

8 - 4

Diría que sí, suponiendo que no hay $\lambda$

9  - **Pregunta**

Sea $A$ el conjunto más pequeño que contiene a todos los conjuntos finito, y está clausurado por union finita intersección finita, y complemento. Mostrar que $A$ está incluido en el conjunto de todos los lenguajes Regulares, pero no coinciden.

 **Respuesta**

$A$ = Set of finites sets of languages / Tiene unión finita, intersección finita y complemento computables (sino consideramos eso, no tiene sentido).

Ahora, vemos queremos ver que:
+ está incluido en el conjunto de todos los lenguajes regulares
+ $\exists$ $L$ lenguaje /   $L \in R \land L \notin A$

Veamos si está incluido en el conjunto de los lenguajes regulares

Como son conjuntos finitos, pueden ser aceptados por un AFD, entonces son regulares.

Ahora, como solamente son conjuntos finitos, podemos ver que un conjunto *infinito* **SÍ** pertenece a los regulares, pero no a $A$ (al ser infinito). Por ejemplo, usemos el lenguaje

$$\{ A^n \text{ }| \text{ } n \geq 0\}$$

que es infinito y regular, pero no está en $A$, al ser infinito

10  - Respuesta

1 - 

Verdadero

```S++
Z1 := psi_x1(X3)
Z2 := psi_x2(X3)
Y := Z1 and Z2
```

Ambos determinan si pertenece ó (se cuelga o no pertenece). Si ambos pertenecen, va a pertenecer

2 - 

Sí, podemos hacer un programa en S++ que compute todos los elementos que pertenecen a la clausura de Kleene, sino no pertenece

```S++
X1 := programa que computa el conjunto c.e.
X2 := palabra a averiguar si pertenece al c.e.
----
# se puede hacer esto sin problemas
for (t, p) do {
	# p
	Z1 := Subcadenas
	Z2 := STEP(X1, t, Z1)
	Z3 := R(SNAP(X1, t,Z1))[0]
	if Z2 and Z3 break;
}
Y := 1
```

3 - 

11  - Respuesta

1. Sí, sería computable.

Demostración:

Con esta función, logramos minimizar los inputs sin problemas

```S++
X1 = programa a minimizar
---

function noSonIguales(Z1, X1) {
	X2 = Halt(X1, 0) = Halt(x2, 0)
	if x2 = 0 {
		Z2 := 0
		while STEP(X1, Z2, 0) = 0 and STEP(Z1, Z2, 0) = 0 {
			Z2++
		}
		Z2 := R(SNAP(X1, Z2, 0))[0] = R(SNAP(Z1, Z2, 0))[0]
	}
	Y := !Z2 
}

Z1 := 0

while Z1 < X1 and noSonIguales(Z1, X1)) {
	Z1++
}
Y := Z1

```


2.

Sí, es computable

**Demostración**:

Para ser computable como aceptadora de palabras debe haber una función total computable que devuelve 1 o 0 según si pertenece al string o no.

Entonces, ya estaría 

12  - Respuesta

13  - Respuesta

14  - Respuesta

15  - Respuesta

16  - Respuesta

17  - Respuesta

18  - Respuesta

19  - **Pregunta**

Si $A  \subseteq \mathbb{N}$ es computable entonces no es decidible si $A$ es vacío.

 **Respuesta**

Podemos pensarlo como conjunto. Eso sería: 

$$ A = \{ x \in \Sigma^* \text{ }| \text{ } \phi_x  = 0 \}$$

Esto es un conjunto de indices?

Es trivial?

+ Existe un caso que lo cumple?

Sí, la función en S++ tal que
  
```S++
Y := 0
```

+ Existe un caso que no lo cumple?

Sí, la función en S++ tal que
  
```S++
Y := 1
```

Ahora, tenemos que ver si es un conjunto de índices:

Para ser un conjunto de índices si para todo par de programas $P$ y $Q$, tales que $\psi_P^{(1)}  = \psi_Q^{(1)}$ y $\#(P) \in C$, se cumple que $\#(Q) \in C$ .

Sea P y Q tal que $\#(P) \in C \land \psi_P^{(1)}  = \psi_Q^{(1)}$ 

$A = \{ x \in \Sigma^* \text{ }| \text{ } \phi_x  = 0 \}$, $\rightarrow$ $P \in A \to \phi_P  = 0$. 
Sabemos que $\phi_Q = \phi_P \to \phi_Q = 0$. Entonces, $Q \in A$

Ahora, como es un conjunto de índices, podemos concluir que no es decidible saber si es vacío o no