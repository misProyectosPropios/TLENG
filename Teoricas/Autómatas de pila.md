## Alfabeto y lenguaje
### Alfabeto
Conjunto finito, no vacío, de símbolos.

### Palabra
Sobre el **alfabeto Σ**: la **concatenación** de los **elementos** de una **secuencia finita** de símbolos. También la llamamos cadena o string.

**Palabra nula λ**: no tiene símbolos

### Clausura de Kleene

Definimos: $\Sigma^{i}$ como todas las combinaciones de las palabras con un tamaño de palabra de $i$

 $$ \Sigma^{*} = \bigcup_{i \geq 0} \Sigma^{i}$$
Todas las palabras pertenecen a este conjunto
### Clausura positiva del alfabeto Σ

$$ \Sigma^{+} = \bigcup_{i \geq 1} \Sigma^{i}$$

### Cardinalidad del Conjunto $\Sigma^{i}$

+ Conjunto Σ tiene |Σ| elementos.
+ Tiene $|\Sigma|^{i}$ 
+ Conjunto $\Sigma^{*}$ es numerable
	+ Le definimos un orden lexicográfico a los elementos y a las palabras por tamaño.
	+ Entonces, todas las palabras van a tener un orden desde el 0 hasta el |tamaño de palabra|

## AFD

5-upla $\langle Q, \Sigma, \delta , q_{0}, F \rangle$ donde
+ Q: conjunto finito de estados
+ $\Sigma$ alfabeto de entrada
+ $\delta$ : $Q \texttimes \Sigma \to Q$ función de transición
+ $q_{0} \in Q$ estado inicial
+ $F\subseteq Q$ conjunto de estados finales


### Función de transición generalizada:

Definimos

$\Sigma : Q \texttimes \Sigma^{*} \to Q$ 
+  $\hat{\delta}$  (q, λ) = q
+ $\hat{\delta} (q, xa)$ = $\delta (\hat{\delta} (q, x) , a )$ con $x \in \Sigma^{*}$ y $a \in \Sigma$
### Lenguaje aceptado por un AFD

$\mathcal{L}(M) = \{x \in \Sigma^{*} : \hat{\delta} (q_{0}, x) \in F\}$ 

## AFND

5-upla $\langle Q, \Sigma, \delta , q_{0}, F \rangle$ donde
+ Q: conjunto finito de estados
+ $\Sigma$ alfabeto de entrada
+ $\delta$ : $Q \texttimes \Sigma \to \mathcal{P}(Q)$ 
+ $q_{0} \in Q$ estado inicial
+ $F\subseteq Q$ conjunto de estados finales

### Función de transición generalizada

Definimos

$\hat{\Sigma} : Q \texttimes \Sigma^{*} \to Q$ 
+  $\hat{\delta}$  (q, λ) = $\{q\}$
+ $\hat{\delta} (q, xa)$ = $\{p \in Q : \exists r \in \hat{\delta} (q, x) \land p \in \delta(r, a))$ con $x \in \Sigma^{*}$ y $a \in \Sigma$
### Lenguaje aceptado por un AFD

$\mathcal{L}(M) = \{x \in \Sigma^{*} : \hat{\delta} (q_{0}, x) \cap F \neq \emptyset \}$ 
## Equivalencia entre AFND y AFD (Racing & Scott)

Dado un AFND $M$, $\exists$ AFD $M'$ tal que $\mathcal{L}(M)=\mathcal{L}(M')$ 

### Demostración 
Por inducción

