Definimos la varianza como $Var=\left(\sum\limits_{i=1}^{n}a_{i}x_{i}\right)= \sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}a_{i}~a_{j}Cov(x_{i},x_{j})$

Consideramos n activar $a_{i},\dots , a_{n}$ como $\theta=(\theta_{1},\dots , \theta_{n})$ 
$a_{i}=activo i-ésimo$
$\theta_{i}=catidad ~del ~actio i-ésimo$
$Y_{ij} = costo ~por ~unidad ~del ~activo ~i-ésimo~ al ~tiempo ~t=0$ 
$t=0$ y $t=T$
$V_{i,T} =$ El costo de cada unidad del activo i-ésimo al tiempo $t=T$
$w_{i}= \frac{\theta_{i}~V_{i,0}}{\sum\limits_{i=1}^{n}\theta_{j}~V_{i,0}}$ El porcentade de dinero invertido en el activo i-ésimo

De la defincion de $w_{i}$ se tiene $\sum\limits_{i=1}^{n}w_{i}= 1$

Para calcular el retorno de la inversión tenemos la formula de la tasa de rendimiento, sin unidades:
$R_{i}= \frac{V_{i,T}-V_{i,0}}{V_{i,0}}$ la tasa de rendimiento del activo i-ésimo. Nos interesamos por $M_{i}= E(R_{i})$ y por $\sigma_{i}^{2}=Var(R_{i})$. Luego la tasa de rendimiento de todo el portafolio es $R=\sum\limits_{i=1}^{n}W_{i}R_{i}$ 

**Definición:** El rendimiento esperado de lportafolio $R_{o}$ es $\mu$ y su riesgo $\sigma^{2}$ Considerando un portafolio de 2 activos:
$$\mu = W_{1}\mu_{1}+W_{2}\mu_{2}=t\mu_{1}+(1-t)\mu_{2}$$
$$\sigma^{2}=\frac{2}{2} \frac{2}{2} w_{i}w_{j}\sigma_{i}\sigma_{j}P_{ij}= \frac{2}{2}~w_{i}~w_{j}~\sigma_{i}~\sigma_{j}P_{ij} + \sum\limits_{j=1}^{n}w_{2}~w_{j}~\sigma_{2}~\sigma_{j}~P_{2j}  = w_{i}~w_{1}\sigma_{1}~\sigma_{1}P_{11}+w_{i}w_{2}\sigma_1~\sigma_{2}~P_{12}$$
$$=w_{2}~w_{1}~\sigma_{2}~\sigma_{1}~p_{21}+w_{2}~w_{2}~\sigma_{2}\sigma_{2}p_{22}=t^{2}~\sigma_{1}^{2}+ 2t(1-t)~p_{12}~\sigma_{1}~\sigma_{2}+(1-t)^{2}\sigma_{2}^{2}$$


Sin perdida de generalidad asumimos que $0<\sigma_{1}\leq \sigma_{2}$. Si $p_{12}=0$, entonces
$$\sigma^{2}=t^{2}\sigma_{1}^{2}+(1-t)^{2}\sigma^{2}$$
$$=t^{2}\sigma_{1}^{2}+(1-2t+t^{2})\sigma_{2}^{2}$$
$$=t^{2}(\theta_{1}^{2}+\sigma_{2}^{2})+\sigma_{2}^{2}-wt\sigma_{2}^{2}$$
Luego $\frac{d}{dt}\sigma^{2}(t_{min})=0$ el t minimo debe cumplir:
$$2t(\sigma_{1}^{2} + \sigma_{2}^{2})-2\sigma_{2}^{2}= 0$$
$$t=\frac{\sigma_{2}^{2}}{\sigma_{1}^{2}\sigma_{2}^{2}}$$
Este resultado se aplica a varios activos, tomando muchos datos y numericamnte calculamos que tienen correlación a cero se invierte, por que se sabe el t de menor riesgo. La difícultad radica en encontrar esos dos activos con correlación igual a 0

### Caso general
De manera general cuando $-1<p <1$ tenemos 
$$\mu = w_{1}\mu_{1}+w_{2}\mu_{2}$$
$$\sigma^{2}=w_{1}^{2}\sigma_{1}^{2}+ w_{2}^{2}2 \sigma_{2}^{2}2 + 25(1-5) ~p~\sigma_{1}~\sigma_{2}=(\sigma_{1}^{2}+\sigma_{2}^{2}- 2 ´~\sigma_{1}~\sigma_{2})S^{2}-2\sigma_{1}~(\sigma_{1}-p~\sigma_{2}) s+\sigma_{1}^{2}$$
Parametrizando:
$$w_{1}=(1-S)$$
$$w_{2}=S $$
y $\sigma_{1}^{2}+\sigma_{2}^{2}- 2~p~\sigma_{1}\sigma_{2} = (\sigma_{1}-\sigma_{2})^{2}+2\sigma_{1}\sigma_{2}(1-p)$  y luego de esto $-2p\sigma_1\sigma_2>0$ 
$\sigma_{1}^{2}+\sigma_{2}^{2} > 2~\sigma_{1}~\sigma_{2} > 2~\rho~\sigma_{1}~\sigma_{2}$

