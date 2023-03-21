## Lineal interpolation
En matematicas, la interpolacion lineal es un metodo of curve fiting using linear polynomials to construct new data points within the range of a discrete set of known data points.

If the two points are given by the coordinates $(t_{0}, X_{T})$ and $(t_{1},X_{t})$ the linear interpolant is the straight line between these points. For a value $X_{t}$ 

## Estabilizacion de la varianza
Often, obvious aberrations are present that can contribute nonstationary as well as nonlineal behavior in observed time series. In such cases, transformations may be useful to equalize the variability over the length of a single series. A particulary useful tranformations is:
$$Y_{t}=logX_{t}$$
wich tends to suppress larger fluctuatins that occur over portions of the series where the underlying values are larger.

## Power transformations
Otras posibilidades para estabilizar la varianza son ;as transformaciones de poder en la Box-Cox family en la forma:
$$Y_{t}=\left\lbrace\begin{matrix}\frac{x^{\lambda}_{t}-1}{\lambda}&\lambda\neq 0 \\ sdsasd & \lambda=1 \end{matrix}\right.$$

## Suavizado
El metodo más conocido es el de medias moviles, podemos hacerlo usando la formula:
$$M_{t}=\sum\limits_{j=-k}^{k}d_{j}$$

## Kernel smoothing
Es un suavizado más general es un kernel de medias moviles usa una funcion de peso o kernel para la media de las observaciones:
$$M_{t}=\sum\limits_{i=1}^{T} w_{i}(t)X_{i}$$

donde
$$w_{i}(t)=\frac{K(\frac{t-i}{b})}{\sum\limits_{j=1}^{T}k(\frac{t-i}{b})}$$

