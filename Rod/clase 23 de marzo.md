## Selección de modelo
lo mas importante para la validacion es la seleccion de modelo. Que modelo se comporta mejor o la configuración de todos los parametros que tenemos para entrenar nuestro modelo.

Usamos el conjunto de entrenamiento $D_{train}$ para enseñar a nuestra hipotesis final $g_m$ para cada modelo. Ahora evaluamos cada modelo en el conjunto de validacion para obtener el error de validacion $E_{1,}\cdots, E_{M}$ donde:
$$E_{m}= E_{out}(g_{m}):~~m=1,\cdots ,M$$
El error de validacion estimado como error de salida.

De todos nuestros m modelos esperamos que sea el que mejor se comporte con los datos que nunca haya visto. entonces para $H_{m}$ es nuestro mejor modelo y se debe decumplir que: $E_{in}\leq E_{m}$ 

### Cross Validation
Validations relies on the following chain of reasoning.
$$E_{out}(g)\approx E_{out}(g^{-})\approx E_{out}(g^{-})$$
wich highlights the dilemma we face in trying to select K. We eould like to choose k as small as possible in order to minimize the discrepancy between $E_{out}(g^{-})$ and $E_{out}(g^{-})$ ideally $k=1$. The validation error $E_{out}(g^{-})$ will still be an ubiased estimate of $E_{out}(g^{-})$ (g is trained on N-1 points), but ir will be so unrealiable as to be useless since it is based on only onde data proint. This brings us to the cross balidation estimate of out-of-sample error.

We will focus on the *leave-one-out* version

