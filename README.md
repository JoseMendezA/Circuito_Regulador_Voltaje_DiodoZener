# Diseño de Circuitos Reguladores de Voltaje utilizando el Diodo Zener

## Objetivo
Diseñar analíticamente circuitos reguladores de voltaje utilizando el diodo Zener y verificar experimentalmente su operación práctica.

## Metodología
### 1. Circuito Regulador de Voltaje con Diodo Zener

Para el circuito regulador de voltaje con diodo Zener mostrado en la Figura 1, se desea diseñar analíticamente el valor de la resistencia $\( R \)$ (y su potencia) para que el voltaje en la carga sea regulado a 10 V. A continuación, se describen los pasos a seguir:

![image](https://github.com/user-attachments/assets/9d4cf275-a864-48bd-852c-41a765d33de5)


### 2. Análisis del Circuito

El circuito consta de los siguientes elementos:

- $\( V_i = 16 \, \text{V} \)$: Voltaje de entrada.
- $\( V_Z = 10 \, \text{V} \)$: Voltaje Zener (el voltaje de referencia al que el Zener regula).
- $\( R_L = 1.2 \, \text{k}\Omega \)$: Resistencia de carga.
- $\( P_{ZM} = 0.5 \, \text{W} \)$: Potencia máxima del diodo Zener.

### 3. Cálculo del Valor de la Resistencia  $\( R \)$

1. **Determinación de la Corriente de Carga $\( I_L \)$**:

```math
I_L = \frac{V_L}{R_L} = \frac{10 \, \text{V}}{1.2 \, \text{k}\Omega} = 8.33 \, \text{mA}
```

3. **Corriente del Diodo Zener $\( I_Z \)$**:
   
Para asegurar que el diodo Zener opere en la región de regulación, la corriente $\( I_Z \)$ debe ser suficiente, pero sin exceder la corriente máxima soportada por el diodo. La potencia máxima del Zener está dada por:

```math
I_{ZM} = \frac{P_{ZM}}{V_Z} = \frac{0.5 \, \text{W}}{10 \, \text{V}} = 50 \, \text{mA}
```
   
La corriente a través del Zener debe ser menor a 50 mA y mayor que cero para regular correctamente. Supongamos una corriente mínima del 10% de la corriente máxima del Zener $\( I_{Z(min)} = 5 \ \text{mA} \)$ para que el diodo opere correctamente.

5. **Corriente Total $\( I_R \)$** a través de $\( R \)$:

```math
I_R = I_L + I_Z = 8.33 \, \text{mA} + 5 \, \text{mA} = 13.33 \, \text{mA}
```

6. **Valor de la Resistencia $\( R \)$**:

```math
   R = \frac{V_i - V_Z}{I_R} = \frac{16 \, \text{V} - 10 \, \text{V}}{13.33 \, \text{mA}} \approx 450 \, \Omega
```

### 4. Cálculo de la Potencia en la Resistencia $\( R \)$

La potencia que disipa la resistencia $\( R \)$ es:

```math
P_R = I_R^2 \cdot R = (13.33 \, \text{mA})^2 \cdot 450 \, \Omega \approx 0.08 \, \text{W}
```

> [!Tip]
> Es recomendable seleccionar una resistencia con una potencia nominal mayor a la calculada, como por ejemplo, una resistencia de 0.25 W o 0.5 W para asegurar una operación segura.

## Conclusión
Hemos diseñado el valor de la resistencia $\( R \)$ y su potencia para que el voltaje en la carga sea regulado a 10 V. Se recomienda verificar experimentalmente el comportamiento del circuito construido, tomando mediciones de los voltajes y corrientes en el circuito para comparar con los valores teóricos obtenidos.

## Parte b: Circuito Regulador de Voltaje con Diodo Zener (Figura 2)

### 1. Análisis del Circuito

En esta sección, diseñaremos el valor de la resistencia $\( R \)$ para que el voltaje en la carga $\( V_L \)$ sea regulado a 10 V, considerando una variación de corriente de carga desde 0 mA hasta 80 mA.

![image](https://github.com/user-attachments/assets/37cce9c3-a8c9-4955-b909-606247606759)


### 2. Parámetros del Circuito

- **$\( V_i = 16 \, \text{V} \)$**: Voltaje de entrada.
- **$\( V_Z = 10 \, \text{V} \)$**: Voltaje Zener (voltaje de referencia).
- **$\( I_{L(min)} = 0 \, \text{mA} \)$**: Corriente mínima de carga.
- **$\( I_{L(max)} = 80 \, \text{mA} \)$**: Corriente máxima de carga.

### 3. Cálculo del Valor de la Resistencia $\( R \)$

1. **Corriente a través del Diodo Zener en Condiciones de Carga Mínima**:

   Cuando la corriente de carga $\( I_L \)$ es mínima (0 mA), toda la corriente $\( I_R \)$ pasa a través del diodo Zener. Se requiere una corriente mínima a través del Zener para que regule correctamente, supongamos $\( I_Z(min) = 5 \, \text{mA} \)$.

2. **Corriente a través del Diodo Zener en Condiciones de Carga Máxima**:

   Cuando $\( I_L = I_{L(max)} = 80 \, \text{mA} \)$, la corriente $\( I_R \)$ será la suma de la corriente de carga y la corriente mínima a través del Zener:

```math
   I_R = I_{L(max)} + I_Z(min) = 80 \, \text{mA} + 5 \, \text{mA} = 85 \, \text{mA}
```

4. **Valor de la Resistencia $\( R \)$**:

   Usamos la ley de Ohm para calcular $\( R \)$ basada en la caída de voltaje a través de la resistencia:

```math
   R = \frac{V_i - V_Z}{I_R} = \frac{16 \, \text{V} - 10 \, \text{V}}{85 \, \text{mA}} \approx 70.59 \, \Omega
```

### 4. Cálculo de la Potencia del Diodo Zener $\( P_Z \)$

La potencia disipada en el diodo Zener es un factor crítico. Debemos asegurarnos de que el diodo pueda manejar la potencia disipada en él.

1. **Corriente Máxima a través del Diodo Zener**:

   La corriente máxima a través del Zener ocurre cuando la corriente de carga es mínima:

```math
   I_{Z(max)} = I_R = 85 \, \text{mA}
```

2. **Potencia Máxima Disipada por el Diodo Zener**:

   La potencia disipada en el Zener se calcula como:

```math
   P_{Z(max)} = V_Z \cdot I_{Z(max)} = 10 \, \text{V} \cdot 85 \, \text{mA} = 0.85 \, \text{W}
```

### 5. Selección del Diodo Zener y de la Resistencia $\( R \)$

1. **Diodo Zener**:
   - Debe soportar una potencia de al menos 0.85 W. Se recomienda seleccionar un diodo Zener con una potencia nominal de 1 W o superior para mayor seguridad.

2. **Resistencia $\( R \)$**:
   - La potencia disipada por la resistencia $\( R \)$ es:

```math
     P_R = I_R^2 \cdot R = (85 \, \text{mA})^2 \cdot 70.59 \, \Omega \approx 0.51 \, \text{W}
```
   - Se recomienda utilizar una resistencia con una potencia nominal de al menos 1 W.

### 6. Montaje Experimental

1. **Montaje del Circuito**: Realizar el montaje del circuito con los valores calculados.
2. **Mediciones**: Registra los siguientes valores experimentales:
   - $\( V_L \)$: Voltaje en la carga.
   - $\( I_R \)$: Corriente a través de la resistencia $\( R \)$.
   - $\( I_{L(max)} \)$ y $\( I_{L(min)} \)$: Corriente máxima y mínima a través de la carga.
   - $\( I_{Z(max)} \)$ y $\( I_{Z(min)} \)$: Corriente máxima y mínima a través del diodo Zener.

### Paso 7: Verificación de la regulación

- Con carga mínima $(I_L = 0mA)$:
  $Iz = (16V - 10V) / 70Ω = 85.71mA$
- Con carga máxima $(I_L = 80mA)$:
  $I_z = 85.71mA - 80mA = 5.71mA$

La regulación se mantiene en ambos casos, ya que $I_z > I_{zmin}$.

3. **Fotografía del Montaje**: Incluir fotografías del montaje experimental para documentar el proceso.

### Conclusión

> [!Tip]
> - Resistencia $R: 70Ω, 2W$
> - Diodo zener: $10V, 1W$

Con los valores calculados, se espera que el circuito mantenga un voltaje constante de 10 V en la carga a pesar de las variaciones en la corriente de carga $(0\ mA \ a \ 80 \ mA)$. Los resultados experimentales deben compararse con los valores teóricos para validar el diseño.


## Parte C:

## Datos del problema:
- Voltaje de entrada (Vi): 7V a 10V
- Voltaje de salida regulado (VL): 5.1V
- Variación de corriente de carga: 0mA a 50mA

![image](https://github.com/user-attachments/assets/9b962768-d3be-4f6c-90f5-42a60f544ff5)

## Paso 1: Selección del diodo zener
Elegiremos un diodo zener con voltaje nominal de 5.1V.

## Paso 2: Cálculo de la corriente mínima del zener
Asumimos una corriente mínima del zener (Izmin) de 10% de la corriente máxima de carga:

```math
I_{zmin} = 0.1 \times 50 \, \text{mA} = 5 \, \text{mA}
```

## Paso 3: Cálculo de la corriente máxima por la resistencia R
```math
I_{Rmax} = I_{zmin} + I_{Lmax} = 5 \, \text{mA} + 50 \, \text{mA} = 55 \, \text{mA}
```

## Paso 4: Cálculo del valor de la resistencia R
Usamos el caso más desfavorable (Vi mínimo):
```math
R = \frac{V_{i(min)} - V_Z}{I_{Rmax}} = \frac{7 \, \text{V} - 5.1 \, \text{V}}{55 \, \text{mA}} \approx 34.55 \, \Omega
```
Redondeamos a un valor comercial: $R = 33Ω$

## Paso 5: Verificación de la regulación
- Con $\(V_i = 7 \, \text{V}\)$ y carga mínima $(\(I_L = 0 \, \text{mA}\))$:
  
```math
I_z = \frac{7 \, \text{V} - 5.1 \, \text{V}}{33 \, \Omega} \approx 57.58 \, \text{mA}
```

- Con $\(V_i = 10 \, \text{V}\)$ y carga máxima $(\(I_L = 50 \, \text{mA}\))$:
  
```math
I_z = \frac{10 \, \text{V} - 5.1 \, \text{V}}{33 \, \Omega} - 50 \, \text{mA} \approx 97.88 \, \text{mA}
```

La regulación se mantiene en ambos casos, ya que $I_z > I_zmin$.

## Paso 6: Cálculo de la potencia máxima de la resistencia R

```math
P_{R(max)} = \frac{(V_{i(max)} - V_Z)^2}{R} = \frac{(10 \, \text{V} - 5.1 \, \text{V})^2}{33 \, \Omega} \approx 0.73 \, \text{W}
```
Elegimos una resistencia de 1W para tener un margen de seguridad.

## Paso 7: Cálculo de la potencia máxima del diodo zener
```math
P_{zmax} = V_Z \times I_{zmax} = 5.1 \, \text{V} \times 97.88 \, \text{mA} \approx 0.499 \, \text{W}
```

Elegimos un diodo zener de 1W para tener un margen de seguridad.

## Conclusión:
> [!Tip]
> - Resistencia R: 33Ω, 1W
> - Diodo zener: 5.1V, 1W

Este diseño mantendrá un voltaje regulado de 5.1V en la carga para corrientes de 0mA a 50mA y voltajes de entrada de 7V a 10V.

## Selección de componentes comerciales:
1. Resistencia: 33Ω 1W (por ejemplo, serie MFR de Vishay)
2. Diodo zener: 1N4733A (5.1V, 1W)

## Montaje experimental:
Para realizar el montaje experimental, seguir estos pasos:
1. Conectar la fuente de alimentación variable (7V a 10V) al circuito.
2. Montar el diodo zener 1N4733A y la resistencia de 33Ω 1W.
3. Utilizar una carga variable (potenciómetro) para simular diferentes corrientes de carga.
4. Medir y registrar los valores de $V_L$, $I_R$, $I_{Lmax}$, $I_{Lmin}$, $I_{zmax}$ e $I_{zmin}$ para diferentes voltajes de entrada y corrientes de carga.

> [!Note]
> Incluir fotografías del montaje electrónico realizado para documentar el experimento.




