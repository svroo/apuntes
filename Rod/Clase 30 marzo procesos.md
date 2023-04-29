# Proceso de Nacimiento y muerte
Es una cadena de Markov continua $\{x(t), t,0\}$, Nacimiento:
$$P(x_{T+T}=n+1 \mid X_{T}=n)=\int_{0}^{t}\lambda ne^{-\lambda n t}dt$$
$$P(X_{T+T}=n-1\mid X_{T}=n)=\int_{0}^{t}\mu~ n~e^{-\mu~nt}dt\rightarrow muerte$$
La matriz de transicion tiene las siguietnes caracteristicas:
$$\begin{matrix} &0&1&2&3 &\dots\\ 0&0&1&0&0&\dots \\ 1&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\frac{\lambda_{1}}{\lambda_{1}+\mu}&0&\dots \\ 2&0& \frac{\lambda_{2}}{\lambda_{2}+\mu}&0 &\frac{\lambda_{2}}{\lambda_{2}+\mu}&\dots \\ 3&0&0&\dots&\dots&\dots \\ \vdots&\vdots&\vdots&\vdots&\vdots&\vdots \end{matrix}$$

$p_{n}n+1 =\frac{\lambda_{n}}{\lambda_{n}+\mu_{n}}$
$P_{n},n-1=\frac{\mu_{n}}{\lambda_{u}+\mu_{u}}$

$P(T_{B}< T_{D})$ 
$$\int_{0}^{\infty}\int_{x}^{\infty}\mu e^{\mu y}~dy ~\lambda e^{\lambda x}=\int_{0}\lambda e^{\lambda x}~e^{\mu x}~dx$$
$$[-e^{\mu y}]=e^{-\mu x}$$
$$x\int_{0}^{\infty}e^{-(x+\mu)x}~dx=\lambda\left[-\frac{1}{(\lambda+\mu)}\right]e^{-(\lambda+\mu )}$$
$$=\lambda\left[\frac{1}{(x+\mu)} e^{-(x+\mu)x}\right]_{0} ^{\infty}=\frac{\lambda}{\lambda+\mu}$$
$$P(T_{D}< T_{B})=1-\frac{\lambda}{\lambda+\mu}=\frac{\lambda+\mu}{\lambda+\mu}-\frac{\lambda}{\lambda+\mu} =\frac{\lambda +\mu -\lambda}{\lambda+\mu}=\frac{\mu}{\lambda+\mu}$$
$$f_{min}(T_{B}\leq t, T_{B}<T_{D})+P(T_{D}\leq t, T_{D}<T_{B}):$$
$$\int_{0}^{t}\int_{o}^{\infty}\lambda e^{-\lambda x}\mu e^{-\mu y}~dy~dx+\int_{0}^{t}\int_{y}^{\infty}\lambda e^{-\lambda x}\mu e^{-\lambda y}~dx~dy$$
$$\int_{o}^{t}\lambda e^{-\lambda~x}e^{-\mu~x}~dx+\int_{0}^{t}e^{-\mu~y}\lambda e^{-x~y}~dy=\int(\lambda+\mu)e^{-(\lambda+\mu)T}$$
$$dt=1-e^{-(\lambda+u)t}$$
$$\mathbb{E}[x(t)]=\sum\limits_{n=0}^{\infty}nP(t)$$
$$Var(x_{t})=\sum\limits_{n=0}^{\infty}n^{2}P(n(t))-\mathbb{E}[x(t)]^{2}$$

### Sistema de Ecuaciones de kolmogorov
La ecuación de Chapman-Kolmogórov es una identidad sobre las distribuciones de probabilidad conjunta de los diferentes conjuntos de coordenadas en un proceso estocástico.
$$P_{0}(t)=\lambda_{0}P_{0}(t) +\mu_{1}P_{1}(t)$$
$$P_{n}(t) =\lambda_{n-1}P_{n-1}(t)+\mu_{n+1}P_{n+1}-(\lambda x_{n}+\mu_{n}) P_{n}(t)$$
$$P_{n0}(0)=1$$
