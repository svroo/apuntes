
#### Large-sample Distribution of the ACF

Bajo las condiciones generales si $X_{t}$ es ruido blanco, entonces para n large la muestra ACF$\hat{P_{x}}(H)$ para $h=1,2,\cdots,h$ donde h is fixed but arbitrary is aproximately normally distributed with zero mean and standerd deviation given by:
$$\sigma_{\hat{p_{X}}} = \frac{1}{\sqrt{P}} $$

### Cross-functions Estimations
El estimador de la función de covarianza $\gamma~XY(h)$ esta dada por:
$$\hat{\gamma}XY(h)=\frac{}{}$$

### Correlacion cruzada
$$\sigma_{\hat{p_{XY}}} = \frac{1}{\sqrt{P}} $$

## Regresión lineal 

Vamos a asumir una serie de tiempo $X_{t}$ para $t=1,\cdots,n$ es influenciada por una coleccion de entradas o series independientes, dicho, $Z_{t}^{(1)},Z_{t}^{(2)},\cdots,Z_{t}^{(9)}$  esta assumption, necessary for applying la regresion lineal convencional, podemos expresar esta relacion como:
$$X_{t}=\beta_{0}+\beta_{1}Z_{t}^{(1)}+\cdots+\beta_{1}Z_{t}^{(q)}+W_{t}$$

o expresada en forma de vector:
$$X_{t}=\beta^{T}Z_{T}+W_{T}$$
donde $\beta=[\beta_{0}\cdots,\beta_{q}]^{T}$ y $Z=[t,Z_{t}^{(1)},\cdots,Z_{t}^{(q)}]^{T}$

Modelo OLS
$$\Delta_{\beta}=\frac{1}{N}$$

Después de la optimización (Ordinary least Squares), we can get the optimal weights $\beta$ defined as:
$$\hat{\beta}=(Z^{t}*Z -Z^{T}X)$$

## Analisis de la varianza (ANOVA)
Varius competing models are of interest to osilate or select the best subset of independent variables. Suppose a proposed model specifies that only a susbet $r<q$ intependent variables, say $Z_{t-r}=Z_{t}^{(1)},\cdots,Z_{t}^{(r)}$   



## The Expected Value

The expected value of a random variable with a finite number of outcomes is a weighted average of all possible outcomes. In the case of a continuum of possible outcomes, the expectation is defined by integration.

$$ \mu_{X_t}=\mathbb{E}[X_t] = \int_{x=-\infty}^{\infty} x f_t(x) dx $$

### Expected Value of Some Statistical Models

Excercises.

Assume that all white noises $W_i \sim \mathcal{N}(0, \sigma_W)$, and then compute

1.  the expected value of the moving averages model defined by

$$ V_t=\frac{1}{3}[W_{t-1} + W_t + W_{t+1}] $$

1.  the expected value of the random walk with drift model defined by

$$ X_t=\delta t + \sum_{j=1}^{t}W_j $$

## Autocovariance

The autocovariance function measures the linear dependence between two points on the same series observed at diﬀerent times, and it is defined as:

$$ \gamma_X(s,t) = \gamma_X(t, s) = \text{cov}(X_s, X_t) = \mathbb{E}[(X_s-\mu_s)(X_t-\mu_t)] $$

What is the covariance of $X_t$ with itself?

### Autocovariance of Some Statistical Models

Excercises.

Assume that all white noises $W_i \sim \mathcal{N}(0, \sigma_W)$.

1.  Compute the autocovariance of white noise model

$$ \text{cov}(W_s,W_t) $$

1.  Proof the equality written below of the autocovariance of a moving average model

$$ \text{cov}(V_s, V_t) = cov\left\{ \frac{1}{3}(W_{s-1} + W_s + W_{s+1}), \frac{1}{3}(W_{t-1} + W_t + W_{t+1}) \right\} = \begin{cases} \frac{3}{9} \sigma^2_W & s=t \\ \frac{2}{9} \sigma^2_W & |s-t|=1 \\ \frac{1}{9} \sigma^2_W & |s-t|=2 \\ 0 & |s-t|>0 \end{cases} $$

## Autocorrelation

The autocorrelation function measures the linear predictability of the series at time $t$, say $X_t$, using only the value at time $s$, say $X_s$, and it is defined as:

$$ \rho_X(s,t) = \frac{\gamma_X(s,t)}{\sqrt{\gamma_X(s,s) \gamma_X(t,t)}} $$

What is the correlation of $X_t$ with itself?

### Autocorrelation Bound

Excercise.

The the Cauchy-Schwarz inequality establish that given two random variables, $X$ and $Y$, with a common probability space. Then:

$$ |\mathbb{E}[XY]| \leq \sqrt{\mathbb{E}[X^2]\mathbb{E}[Y^2]} $$

Using the Cauchy-Schwarz inequality, prove that:

$$ -1 \leq \rho(s,t) \leq 1 $$

## Cross-Variance Function

Often, we would like to measure the predictability of another series $Y_t$ from the series $X_s$. Assuming both series have ﬁnite variances, we define the cross-variance function between two series, $X_s$ and $Y_t$ as

$$ \gamma_{XY}(s,t)=\text{cov}(X_s, Y_t)= \mathbb{E}[(X_s-\mu_{X_s})(Y_t-\mu_{Y_t})] $$

Why could be important to mix the analysis of two time series?

## Cross-Correlation Function

The cross-correlation function between two series, $X_s$ and $Y_t$ is given by

$$ \rho_{XY}(s,t)= \frac{\gamma_{XY}(s,t)}{\sqrt{\gamma_X(s,s) \gamma_Y(t,t)}} $$