# Proceso de Nacimiento y muerte
Es una cadena de Markov continua $\{x(t), t,0\}$, Nacimiento:
$$P(x_{T+T}=n+1 \mid X_{T}=n)=\int_{0}^{t}\lambda ne^{-\lambda n t}dt$$
$$P(X_{T+T}=n-1\mid X_{T}=n)=\int_{0}^{t}\mu~ n~e^{-\mu~nt}dt\rightarrow muerte$$
La matriz de transicion tiene las siguietnes caracteristicas:
$$\begin{matrix} &0&1&2&3 &\dots\\ 0&0&1&0&0&\dots \\ 1&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\dots \\ 2&0& \frac{\lambda_{2}}{\lambda_{2}+\mu}&0 &\frac{\lambda_{2}}{\lambda_{2}+\mu}&\dots \\ 3&0&0&\dots&\dots&\dots \\ \vdots&\vdots&\vdots&\vdots&\vdots&\vdots \end{matrix}$$

$p_{n}n+1 =\frac{\lambda_{n}}{\lambda_{n}+\mu_{n}}$
$P_{n},n-1=\frac{\mu_{n}}{\lambda_{u}+\mu_{u}}$
