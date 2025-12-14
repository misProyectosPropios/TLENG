# Ejercicio 1

Sea $\Sigma$ un alfabeto. Sea $L \subseteq \Sigma^*$ un lenguaje regular.
Sea $S \subseteq \Sigma^*$ el lenguaje que resulta de intercalar cada palabra de $L$ con su reversa y sea:

$$
S = \left\{
a_2 \dots a_{n}, a_{1}
\;\middle|\;
a_1 a_3 \dots a_{2n-1} \in L,\;
a_2 a_4 \dots a_{2n} \in L^R
\right\}.$$

Decidir si $S$ es regular y demostrarlo

*Ayuda*: dar un AF que acepta $S$ o demostrar que $S$ no es regular

## Respuesta

Supongamos que $S$ es regular. Entonces, particularmente para el lenguaje $A^{N}B^{M} \text{ } | \text{ } N < M$ podemos  usarlo como lenguaje para la demostración.

Ahora, tomemos una 

# Ejercicio 2

Sea $\Sigma$ un alfabeto, y sea $A \subseteq \Sigma^*$ computable y sea $B \subseteq \Sigma^*$ computablemente enumerable. Demostrar que $A^* \cap B^*$ es computablemente enumerable.

Ayuda: Recordar que $\mathbb{N}$ tiene relación 1 a 1 con $\Sigma^*$
Ayuda: Dar las funciones características de $A$, $A^*$, $B$, $B^*$


