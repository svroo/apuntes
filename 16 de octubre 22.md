
### Computation of Maximum likelihood estimate
Maximiza $p(d|\theta)$ : $(\theta_{1},\dots, \theta_{M}) = arg~max_{\theta_{1},\dots,\theta_{M}}~~p(d|\theta)=arg~max_{\theta_{1},\dots,\theta_{M}}~~\prod_{i=1}^{M} \theta_{i}^{c(w_{i},d)}$ 
Max. log-likelihood

$$p(w_{i}|\theta)=\frac{(w_{i},d)}{\sum_{i=1}^{M}(w_{i},d)}=\frac{c(w_{i},d)}{|d|}$$

#### What does the Topic look like?
d = text mining paper
can we get rid of these common words?

#### Generate d Using two word Distributions
d = text mining papel
``` mermaid
flowchart RL
A[Topic \theta_d] --> d
B[Background \theta_b] --> d

C[Topic choise] --> A 
C-->B
```
where topic choise = $p(\theta_{d}) + p(\theta_{B})=1$ dado que $p(\theta_{d})=0.5$ y $p(\theta_{B})=0.5$ 

$$p(the)= p(\theta_{d})~~p(the|\theta_{d}) + p(\theta_{B})~~p(the|\theta_{B}) = 0.5*0.000001+0.5*0.03$$
$$p(tex)= p(\theta_{d})~~p(tex|\theta_{d}) + p(\theta_{B})~~p(the|\theta_{B}) = 0.5*0.04+0.5*0.04$$

Formally defines the following generative model:
$$w\rightarrow p(w)= p(\theta_{d})~~p(w|\theta_{d}) + p(\theta_{B})~~p(w|\theta_{B})$$
what if p = 1

#### Likelihood function:
$$p(d|\varLambda)=\prod_{i=1}^{|d|}p(x_{i}|\varLambda)=\prod_{i=1}^{|d|}[p(\theta_{d}) ~p(x_{i}|\theta_{d}) + p(\theta_{B})~p(x_{i}|\theta_{B})]$$
Ecuacion lineal:
$$0.5*p(text|\theta_{d})+0.5*0.1=0.5*p(the|\theta_{d})+0.5*0.9$$
quedando p(text|$\theta_{d}$) = 0.9 >> the = p(the|$\theta_{d}$) = 0.1

from $\theta_{d}~~(Z=0)$  $p(\theta_{d})~p(text|\theta_{d})$ 
para calcular si la palabra esta en $\theta_{d}$ o en $\theta_{B}$ usamos una variable Z
|$\theta_{d}$|$\theta_B$|
|--|--|
|$z=0$|$z=1$|

p(text|$\theta_d$)
p(text|$\theta_{B}$)

$$p(z=0|w=text ) = ~\frac{p(\theta_{d})~p(text|\theta_{d})}{p(\theta_{d})~p(text|\theta_{d})+p(\theta_{B}) p(text|\theta_{B})}$$

#### The expectation-Maximization (EM) Algoithm
$$p^{n}=\frac{p(\theta_{d}) p^{n}(w|\theta_{d})} {p(\theta_{d})p^{(n)} (w|\theta_{d}) +p(\theta_{B}) p(w|\theta_{B})} ~~\rightarrow E-step$$

how likely w is from $\theta_{d}$

$$p^{(n+1)} (w|\theta_{d})=\frac{c(w,d)p^{(n)} (z=0|w )}{\sum_{w' \in V} c(w',d)p^{(n)} (z=0|w' )}~~\rightarrow M-step$$

|word|#|p(w$\mid \theta_B$)|Iteracion 1| | Iteracion 2| | Iteracion 3| |
|--|--|--|--|--|--|--|--|--|
| | | |P(w$\mid \theta$)| p(z=0$\mid$w)|p(w$\mid \theta$)|p(z=0$\mid$w)|p(w$\mid\theta$)|p(z=0$\mid$w)| 
|The|4|0.5|**0.25**|0.33|**0.20**|0.29|**0.18**|0.26|
|Paper| 2|0.3|**0.25**|0.45|**0.14**|0.32|**0.10**|0.25|
|Text| 4|0.1|**0.25**|0.71|**0.44**|0.81|**0.50**|0.93|
|Mining|2|0.1|**0.25**|0.71|**0.22**|0.69|**0.22**|0.69|
|Long-likelihood |||| -16.96||-16.13||-16.02|

