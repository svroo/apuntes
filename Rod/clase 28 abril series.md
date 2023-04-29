#### Modelo autoregresivo de medias moviles
Una serie de tiempo $X_{t}; t=0,+-1,+-2,\dots$ es $ARMA(p,q)$ if it is stationary and
$$X_{t}=\phi_{1}X_{t-1}+\cdots+\phi_{p}X_{t-p}+W_{t}+\theta_{1}W_{t-1}$$
Podemos escribir el modelo como:
$$\phi(B)X_{t}=\theta(B)W_{t}$$
Problemas de los modelos $ARMA(p,q)$
- Parameter redundant models
- Sationary AR models that depended on the future

 