Cada problema esta definido por cierto parametros, los parametros de este problema son; C,A, b.
Estos valores se obtienen observando mediante promedios u otras formas, no hay una matriz dada.

Supongamos que el método simplex produce una base óptima B. Describiremos como hacer uso de condiciones de optimalidad con el fin de econtrar una nueva solución, si alguna parte de los parametros inciales es modificada (c, A, b).

De manera más precisa consideramos las siguientes variaciones. 
- Posible cambio en el vector C
- Posible cambio en el vector b
- Posible cambio en la matriz A
- Añadir una nueva actividad (nueva incognita)
- Añadir una nueva constante

### Cambio en el vector de costo
Dada una solución óptima factible, supongamos que uno (o más) de las variables se cambia de Ck a C'k.
Tenemos el problema:
Minimiza cx
Ax = b
x $\geq$ 0
Lo que cambia seria el cx. 

#### Caso 1:
$X_{k}$ no básica 
en este caso $C=(C_{B},C_{N})^{T}$ lo podemos dibidir en su parte basica y en su parte no básica $X'=(X'_{B}, 0)^{T}$  esto significa: $CX=C_{B}X_{B} + C_{N}0$ el $C_{B}$ no varia. 
En este caso $C_{B}$ no es afectada y por tanto $Z_{j} = C_{B}B^{-1}a_{j}$ no es afectado para ningún j. Por tanto $Z_{k}-C_{k}$ es reemplazado por $Z_{k}-C'_{k}$. Notece que $Z_{k}-C_{k} \leq 0$ esto es una condicion de optimalidad.
Si $Z_{k}-C'_{k} = (Z_{k}-C_{k}) + (C_{k}-C'_{k})$ es positivo

Teniendo la tabla del metodo simplez como 

|1|$Z_{1}-C_{1}$|**$\dots,Z_{k}-C_k$** | $Z_{n}-C_{n}$|$C_{x}$|
|--|--|--|--|--|
|0|$Y_{1}$|**$Y_{k}$**| $Y_{n}$|$\overline{b}$|

Entonces vemos que toda la parte de la tabla no se ha modificado, solo una parte del vector c, el unico que se ha modificado es la columna $Z_{k}-C'_{k}$ si el número que resulta de $Z_{k}-C'_{k} = (Z_{k}-C_{k}) + (C_{k}-C'_{k})$  es negativo sigue cumpliendo la respuesta, si es mayor que cero esta columna utilizamos la columna para seguir haciendo el pivote.

Entonces $X_{k}$ debe entrar a la base de otra forma el punto $X^{*}$ (la solución optima inicial) sigue siendo óptima.

#### Caso 2:
$X_{k}$ es básico, digamos $X_{k}= X_{Bt}$ en este caso $C_{Bt}$ es remplazado por $C'_{bt}~~sea ~Z'_{j}$ el nuevo valor de $Z_{j}$. Entonces $Z'_{j}-C_{j}$ se calcula como$$Z'_{j}-C_{j}= C'_{B}B^{-1}a_{j}-c_{j}=(C_{B}B^{-1}a_{j}-c_{j}) + (0,0,\dots,C'_{Bt} - C_{Bt}, 0,\dots,0)~Y_{j}=(Z_{j}-c_{j})+(C'_{Bt}-C_{Bt}) Y_{tj}$$
$Y_{j} = B^{-1}a_{j}$ 
