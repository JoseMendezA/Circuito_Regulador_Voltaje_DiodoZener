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
   
La corriente a través del Zener debe ser menor a 50 mA y mayor que cero para regular correctamente. Supongamos una corriente mínima $\( I_{Z(min)} = 5 \ \text{mA} \)$ para que el diodo opere correctamente.

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
Hemos diseñado el valor de la resistencia \( R \) y su potencia para que el voltaje en la carga sea regulado a 10 V. Se recomienda verificar experimentalmente el comportamiento del circuito construido, tomando mediciones de los voltajes y corrientes en el circuito para comparar con los valores teóricos obtenidos.

