## Lema (*"Pumping"*, Scott & Rabin 1959, Bar Hillel, Perles & Shamir 1961)

Sea $L$ un lenguaje regular. Existe una longitud $n$ tal que  
$\forall \text{ }z \in L$  con $|z| \ge n$ existe $u, v, w \in \Sigma^*$ tales que

$$
z = u v w,
$$
$$
|uv| \le n,
$$
$$
|v| \ge 1,$$
$$
\forall i \ge 0,\quad u v^i w \in L.
$$

