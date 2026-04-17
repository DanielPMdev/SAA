# UT5 — CNN: Cálculo de Dimensiones y Parámetros

## Fórmulas de referencia

$$W_{out} = \frac{W_{in} - F + 2P}{S} + 1$$

$$\text{Params} = (F \times F \times C_{in} + 1) \times K$$

| Variable | Significado |
|----------|-------------|
| $W_{in}$ | Ancho / alto de entrada |
| $F$ | Tamaño del filtro |
| $P$ | Padding |
| $S$ | Stride |
| $C_{in}$ | Canales de entrada (ej. 3 para RGB) |
| $K$ | Número de filtros (profundidad de salida) |

> **Regla de oro:** si $W_{out}$ no es un número entero → stride incompatible → configuración inválida.  
> **Max Pooling:** nunca tiene parámetros (0). La profundidad $D$ siempre se conserva igual a la entrada.

---

## Capas de Convolución

---

### Ejercicio 1

**Input:** $32 \times 32 \times 3$ — 10 filtros de $6 \times 6$, stride $S=1$, padding $P=2$

**Volumen de salida:** $31 \times 31 \times 10$  
**Número de parámetros:** $1090$

**Cálculo:**

$$W = \frac{32 - 6 + 2 \times 2}{1} + 1 = \frac{30}{1} + 1 = 30 + 1 = 31$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 31 \qquad D = K = 10$$

$$\text{Params} = (6 \times 6 \times 3 + 1) \times 10 = 109 \times 10 = 1090$$

---

### Ejercicio 2

**Input:** $32 \times 32 \times 3$ — 10 filtros de $6 \times 6$, stride $S=2$, padding $P=2$

**Volumen de salida:** $16 \times 16 \times 10$  
**Número de parámetros:** $1090$

**Cálculo:**

$$W = \frac{32 - 6 + 2 \times 2}{2} + 1 = \frac{30}{2} + 1 = 15 + 1 = 16$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 16 \qquad D = K = 10$$

$$\text{Params} = (6 \times 6 \times 3 + 1) \times 10 = 109 \times 10 = 1090$$

---

### Ejercicio 3

**Input:** $32 \times 32 \times 3$ — 10 filtros de $6 \times 6$, stride $S=3$, padding $P=2$

**Volumen de salida:** $11 \times 11 \times 10$  
**Número de parámetros:** $1090$

**Cálculo:**

$$W = \frac{32 - 6 + 2 \times 2}{3} + 1 = \frac{30}{3} + 1 = 10 + 1 = 11$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 11 \qquad D = K = 10$$

$$\text{Params} = (6 \times 6 \times 3 + 1) \times 10 = 109 \times 10 = 1090$$

---

### Ejercicio 4 ⚠️ Stride incompatible

**Input:** $32 \times 32 \times 3$ — 10 filtros de $6 \times 6$, stride $S=4$, padding $P=2$

**Volumen de salida:** ❌ Inválido  
**Número de parámetros:** $1090$ (los parámetros se calculan igual, pero la capa no es aplicable)

**Cálculo:**

$$W = \frac{32 - 6 + 2 \times 2}{4} + 1 = \frac{30}{4} + 1 = 7{,}5 + 1 = 8{,}5 \quad \Rightarrow \text{No entero: Inválido}$$

---

### Ejercicio 5 ⚠️ Stride incompatible

**Input:** $32 \times 32 \times 3$ — 10 filtros de $5 \times 5$, stride $S=2$, padding $P=2$

**Volumen de salida:** ❌ Inválido  
**Número de parámetros:** $760$ (calculable pero la capa no es aplicable)

**Cálculo:**

$$W = \frac{32 - 5 + 2 \times 2}{2} + 1 = \frac{31}{2} + 1 = 15{,}5 + 1 = 16{,}5 \quad \Rightarrow \text{No entero: Inválido}$$

$$\text{Params} = (5 \times 5 \times 3 + 1) \times 10 = 76 \times 10 = 760$$

---

## Capas de Max Pooling

> En Max Pooling: **no hay parámetros** y la profundidad $D$ **se conserva** siempre.  
> Se usa $P = 0$ por defecto (sin padding).

---

### Ejercicio 6 ⚠️ Stride incompatible

**Input:** $224 \times 224 \times 64$ — filtro $6 \times 6$, stride $S=5$

**Volumen de salida:** ❌ Inválido  
**Parámetros:** $0$

$$W = \frac{224 - 6 + 0}{5} + 1 = \frac{218}{5} + 1 = 43{,}6 + 1 = 44{,}6 \quad \Rightarrow \text{No entero: Inválido}$$

---

### Ejercicio 7

**Input:** $224 \times 224 \times 64$ — filtro $2 \times 2$, stride $S=1$

**Volumen de salida:** $223 \times 223 \times 64$  
**Parámetros:** $0$

$$W = \frac{224 - 2 + 0}{1} + 1 = \frac{222}{1} + 1 = 222 + 1 = 223$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 223 \qquad D = 64 \text{ (se conserva)}$$

---

### Ejercicio 8 ⚠️ Stride incompatible

**Input:** $224 \times 224 \times 64$ — filtro $113 \times 113$, stride $S=2$

**Volumen de salida:** ❌ Inválido  
**Parámetros:** $0$

$$W = \frac{224 - 113 + 0}{2} + 1 = \frac{111}{2} + 1 = 55{,}5 + 1 = 56{,}5 \quad \Rightarrow \text{No entero: Inválido}$$

---

### Ejercicio 9

**Input:** $224 \times 224 \times 64$ — filtro $4 \times 4$, stride $S=2$

**Volumen de salida:** $111 \times 111 \times 64$  
**Parámetros:** $0$

$$W = \frac{224 - 4 + 0}{2} + 1 = \frac{220}{2} + 1 = 110 + 1 = 111$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 111 \qquad D = 64 \text{ (se conserva)}$$

---

### Ejercicio 10

**Input:** $224 \times 224 \times 64$ — filtro $112 \times 112$, stride $S=4$

**Volumen de salida:** $29 \times 29 \times 64$  
**Parámetros:** $0$

$$W = \frac{224 - 112 + 0}{4} + 1 = \frac{112}{4} + 1 = 28 + 1 = 29$$

$$H = \text{imagen cuadrada} \Rightarrow H_{out} = 29 \qquad D = 64 \text{ (se conserva)}$$

---

## Resumen de resultados

| Ej. | Tipo | Input | F | S | P | Volumen salida | Parámetros |
|-----|------|-------|---|---|---|----------------|------------|
| 1 | Conv | 32×32×3 | 6 | 1 | 2 | 31×31×10 | 1090 |
| 2 | Conv | 32×32×3 | 6 | 2 | 2 | 16×16×10 | 1090 |
| 3 | Conv | 32×32×3 | 6 | 3 | 2 | 11×11×10 | 1090 |
| 4 | Conv | 32×32×3 | 6 | 4 | 2 | ❌ Inválido | — |
| 5 | Conv | 32×32×3 | 5 | 2 | 2 | ❌ Inválido | — |
| 6 | MaxPool | 224×224×64 | 6 | 5 | 0 | ❌ Inválido | 0 |
| 7 | MaxPool | 224×224×64 | 2 | 1 | 0 | 223×223×64 | 0 |
| 8 | MaxPool | 224×224×64 | 113 | 2 | 0 | ❌ Inválido | 0 |
| 9 | MaxPool | 224×224×64 | 4 | 2 | 0 | 111×111×64 | 0 |
| 10 | MaxPool | 224×224×64 | 112 | 4 | 0 | 29×29×64 | 0 |
