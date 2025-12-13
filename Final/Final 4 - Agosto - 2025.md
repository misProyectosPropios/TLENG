## **Ejercicio 1.**
Sea $\Sigma$ un alfabeto. Sea $L \subseteq \Sigma^*$ un lenguaje regular.
Sea $S \subseteq \Sigma^*$ el lenguaje que resulta de intercalar cada palabra de $L$ con su reversa:

$$
S = \left\{
a_1 \dots a_{2n}
\;\middle|\;
a_1 a_3 \dots a_{2n-1} \in L,\;
a_2 a_4 \dots a_{2n} \in L^R
\right\}.$$

Decidir si $S$ es regular y demostrarlo (dar un autómata finito que lo reconoce o demostrar que no es regular).

## Respuesta:

Supongamos que S es regular, entonces por pumping, tenemos que existe una descomposición en $u$, $v$, $w$ con las restricciones de pumping.


Ahora, tomaremos el lenguaje regular $AB^{2N}$. Este lenguaje al aplicarle pumping.