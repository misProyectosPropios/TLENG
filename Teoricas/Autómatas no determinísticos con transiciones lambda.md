## AFND con transiciones $\lambda$ 

5-upla $\langle Q, \Sigma, \delta , q_{0}, F \rangle$ donde
+ Q: conjunto finito de estados
+ $\Sigma$ alfabeto de entrada
+ $\delta$ : $Q \texttimes (\Sigma \cup \{\lambda\}) \to \mathcal{P}(Q)$ 
+ $q_{0} \in Q$ estado inicial
+ $F\subseteq Q$ conjunto de estados finales

## Relaciones

Se llama relación de $A$ en $B$ a cualquier subconjunto de $A \texttimes B$  

### Reflexiva

$$\forall a \in A \text{, } (a, a) \in R)$$

### Simétrica

$$\forall a, b \in A \text{( Si } (a,b) \in R \to (b, a) \in R)$$
### Transitiva

$$\forall a, b, c \in A \text{( Si } (a,b) \in R \text{ } \land (b,c) \in R \to (a, c) \in R)$$

### Composición

G ◦ R = {(a, c) , a ∈ A, c ∈ C : ∃b ∈ B tal que (a, b) ∈ R ∧ (b, c) ∈ G}

Es de **identidad** si:
∀a, b ∈ A, a $id_A$ b si y solo si a = b.

La relación de identidad es el **elemento de neutro** de la composición

### Relación de potencia

$$
R^n = 
\begin{cases}
\mathrm{id}_A, & n = 0,\\[4pt]
R \circ R^{\,n-1}, & n > 0.
\end{cases}
$$

### Clausura transitiva

$$R^{+} = \bigcup_{k=1}^{\infty}R^{k}$$

#### Proposición
+ $R \subseteq R^{+}$
+ $R^+$ es transitiva
+ Si $S \subseteq A \texttimes A$, $R \subseteq S$ y S transitiva, entonces $R^+ \subseteq S$


### Clausura transitivo-reflexiva

$$R^{*} = \bigcup_{i=1}^{\infty}R^{i} = R^{+} \cup \text{ }id$$

### Clausura $\lambda$

$$Cl_{\lambda}(q) = \{ p \in Q : (q, p) \in R^* \}$$

Clausura $\lambda$ de un conjunto de estados



$$Cl_{\lambda}(P) = \bigcup_{q \in P} Cl_{\lambda}(q)$$

Función transicion-sin-$\lambda$ 

$\bar{\delta} : Q \times \Sigma \to \mathcal{P}(Q),$ 
$$\bar{\delta}(q,a) = Cl_\lambda \left( \bigcup_{p \in Cl_\lambda(q)} \delta(p,a) \right)
$$

$\hat{\delta} : Q \times \Sigma^{*} \to \mathcal{P}(Q),  \qquad x \in \Sigma^{*},\ a \in \Sigma$

$$
\hat{\delta}(q,\lambda) = Cl_\lambda(q), \qquad
\hat{\delta}(q,xa) =
Cl_\lambda\left( \bigcup_{p \in \hat{\delta}(q,x)} \bar{\delta}(p,a) \right).
$$

### Lenguaje aceptado por AFND-$\lambda$ 

$$\mathcal{L}(M) = \{ x \in \Sigma^* : \hat{\bar{\delta}}(q_0, x) \text{ }  \cap \text{ } F \neq \emptyset\}$$

## Equivalencia entre AFND y AFND-$\lambda$

Dado un AFND-$\lambda$ $M$, $\exists$ AFND $M'$ tal que $\mathcal{L}(M)=\mathcal{L}(M')$ 