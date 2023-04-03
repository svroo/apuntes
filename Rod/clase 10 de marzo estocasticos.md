# Processos Estocásticos
Definición de un proceso estocástico es una familia de variables aleatorias $\{N_{t}:t\in T.X_{t}\in S\}$. Donde T es un conjunto de indices y S conjunto de estados

```{python}
import random
import Matplotlib.pyplot as plt

def random_walk(x, time):
	TS=[0]: x=[0]

	for ts in range(1, time+1):
		TS.append(ts)
		rand = random.choice(x)
		step = X[ts-1]+rand
		x.append(step)

plt.figure(figsize=(8,6))
plt.plot(TS, x, label='Random walk')

plt.xlabel('time')
plt.ylabel("walk")
plt.show()

if __name__ = '__main__':
	randomwalk([-1,1], 50)
```

#### Definición de Caminata aleatoria
Caminata aleatoria (simple) es un proceso aestocastico discreto $T(z_{t},s\leq z)$ 
$$P(X_{n}=J\mid X_{n-1} =i)=\left\lbrace\begin {matrix} p,&j=i+1\\ q, & J=i-1 \\ 0, & en~caso~contrario\end{matrix} \right.$$

$X_{n}= x_{0}+\epsilon_{1}+\dots+\epsilon_{n}$ son variables de Bernoulli y calculamos su valor esperado como:
$\mathbb{E}[X_{n}]=\mathbb{E}\left[x_{0}+\sum\limits_{i=1}^{n}\epsilon_{1}\right] =\mathbb{E}[x_{0}]+\sum\limits_{i=1}^{n}\mathbb{E}[\epsilon_{i}]] = x_{0}+ \sum\limits_{i=1}^{n}\mathbb{E}[\epsilon_{1}]$ y obtenemos:
$\mathbb{E}[\epsilon_{i}]=1*p+(-1)*q=p-q~~~(i=1,2,\dots,n)$
$\mathbb{E}[X_{n}]=n(p-q)$
$var(X_{n})=\sum\limits_{i=1}^{n} var(\epsilon_{i})$
$var(\epsilon_{i}) =\mathbb{E}[\epsilon_{i}^{2}]-\mathbb{E}[\epsilon_{i}]^{2}$
$\mathbb{E}[\epsilon_{i}^{2}]=1^{2}*p+(-1)^{2}q=p+q=1$
$\mathbb{E}[\epsilon_{i}] ^{2}=p-q$
$var=1-(p-1)^{2}~~~~q=1-p$
$=1-(2p-1)^{2}=1-(4p^{2}-4p+1)=1-4p^{2}+4p-1=4p-4p^{2}=4p(1-p)$
$var=4npq$

La variable $X_{n}$ se puede escribir como pasos a la derecha menos pasos a la izquierda.
$X_{}=R_{n}-L_{n}~~ y~n=R_{n}+L_{n}$
$X_{n}+ n =2R_{n}\sum\limits_{i=1}^{n}\epsilon_{i}$

:a suma de n variables Bernulli se distribuye como una Binomial con parametro p y n
$$R_{n}=\frac{x_{n}+n}{2}=\frac{1}{2}(y_{n}+n)+\frac{1}{2}\sum\limits_{i=1}^{n}(\epsilon_{i}+1)=\sum\limits_{i=1}^{n}\left(\frac{\epsilon_{i}+1}{2} \right)$$
$$$$
$$P(X_{n}=x \mid X_{0}=0 )=P\left(R_{n}=\frac{x=2}{2}\right)=\begin{pmatrix}n \\ \frac{x+2}{2}\end{pmatrix} p^{{\frac{x+2}{2}}} q^{(n-\frac{k+2}{2})} n-\left[\frac{x+2}{2} \right]=$$
$$=n-\frac{x}{2}-\frac{n}{2}=\frac{n}{2}-\frac{x}{2}=\frac{n-x}{2}$$

$$P(X_{n}=x\mid X_{0}=0)=\begin{pmatrix}n\\\frac{n+x}{2}\end{pmatrix}p^{\frac{n+x}{2}}q^{\frac{n-x}{2}}$$

Modificar probabilidad python