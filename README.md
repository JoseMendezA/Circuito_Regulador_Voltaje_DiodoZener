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

![Circuito Regulador de Voltaje con Diodo Zener - Parte b](ruta/figura2.png)

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
   - $\( I_R \)$: Corriente a través de la resistencia \( R \).
   - $\( I_{L(max)} \)$ y $\( I_{L(min)} \)$: Corriente máxima y mínima a través de la carga.
   - $\( I_{Z(max)} \)$ y $\( I_{Z(min)} \)$: Corriente máxima y mínima a través del diodo Zener.

3. **Fotografía del Montaje**: Incluir fotografías del montaje experimental para documentar el proceso.

### Conclusión

Con los valores calculados, se espera que el circuito mantenga un voltaje constante de 10 V en la carga a pesar de las variaciones en la corriente de carga. Los resultados experimentales deben compararse con los valores teóricos para validar el diseño.





