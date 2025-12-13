# Teórica 1

1. Dado un AFD $M = \langle Q, \Sigma, \delta, q_0, F\rangle$ , y sea a un símbolo de Σ. Construir otro AFD $M ′$ que acepte el lenguaje $\mathcal{L} = \{ax \in \Sigma^{*} : x \in \mathcal{L}(M )\}$
2. Indicar verdadero o falso y justificar
	1.  Si AFD $M = \langle Q, \Sigma, \delta, q_0, F\rangle$ es un AFD entonces reconoce al menos $|Q|$ palabras distintas, es decir $\#\mathcal{L}(M) \geq |Q|$ 
	2. Si AFD $M = \langle Q, \Sigma, \delta, q_0, F\rangle$ es un AFD, entonces todas las palbras de $\mathcal{L}(M)$ tienen longitud menor o igual que $|Q|^2$
3. ¿Cuántos AFD hay con |Q| = 2 y |Σ| = 3?
4. ¿qué pasa si revierto todas las flechas de un AFD ?
5. ¿qué pasa si invierto estados finales con no finales de un AFND?
# Respuestas 1

1- Respuesta
Dado el $M = \langle Q, \Sigma, \delta, q_0, F\rangle$
Para construir otro AFD $M = \langle Q, \Sigma, \delta_m, q_{0_m}, F\rangle$, podríamos agregar un estado $x_{n + 1}$ 

+ $Q_m$ = $\{Q \cup \{x_{n + 1}\} , x_{n + 2}\}\}$
+ $q_{0_m}$ = $x_{n + 1}$
+ $\delta_m = \delta$ 
	+ junto con $x_{n +1}$ iría a $q_0$ en caso de ser $a$ y sino, iría a $x_{n + 2}$
	+ $x_{n + 2}$ todas las cadenas apuntan hacía si mismo

2 - Respuesta
	1. Falso
	   Puedo tener un autómata de 1 estado sin estados finales y de esa forma, se lenguaje es 0, mientras que el tamaño del autómata es 1 
	2. Falso
	   Como sabemos que $AFD \equiv AFND$, podemos hacer un autómata para la clausura de Kleene con un autómata de 1 estado. Este conjunto tiene $\infty \geq 1^2$ ,

3 - Respuesta

Tenemos:
+ 2 estados
+ 3 símbolos

Sabemos que 
+ La función $\delta$ tiene que estar completa definida. Entonces para cada estado debe haber una flecha para cada símbolo del elemento ($2 * 3$), ahora, estas flechas tienen 2 opciones apuntar hacia sí mismo o apuntar hacia el otro estado. 
	+ Por lo tanto: $2^(2 * 3)$
+ Los estados pueden ser finales o no finales
	+ $2^2$ opciones

Multiplicando ambos resultados nos quedan ($2^2 * 2^{2 * 3}$)


4 - Respuesta:

+ Si revierto todas las flechas de un AFD, me puede quedar un AFND

5 - Respuesta:

+ Si invierto estados finales con no finales obtendría el complemento del lenguaje regular.
# Teórica 2

1. Dado un AFND $M = \langle Q, \Sigma, \delta, q_0, F\rangle$ , y sea a un símbolo de Σ. Construir otro AFND-$\lambda$ $M′$ tal que  $\mathcal{L}(M) = \mathcal{L}(M')$ y tiene un único estado final
2. Indicar si es verdadero o falso y justificar
3. ¿Se puede acotar superiormente cuantas transiciones requiere la aceptación de una palabra en un AFND-$\lambda$?
4. ¿Puede haber ciclos de transiciones-λ?

# Respuestas 2

1 - Respuesta

Podemos construir un AFND con un estado más en donde todos los estados finales de M apunten por medio de una $\lambda$ hacia ese único estado final del $M'$ obteniendo de esa forma un único estado final

2 - Respuesta

2.1 -

2.2 - 

3 - No, si llega a haber un ciclo de transiciones $\lambda$ puede no terminar nunca. Si no hay ciclos, entonces sería exponencial.
Si no llega a haber ciclos de transiciones $\lambda$ entonces, la cota superior sería $2^n$

4 - Como haber puede haber, pero decidimos cortarlos haciendo un BFS. y si hay ciclos, los sacamos 

