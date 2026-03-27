
---

# PROGRAMACIÓN LINEAL

## Introducción

Algunos modelos de optimización tienen muchas variables de decisión y múltiples restricciones.

**Ejemplo:** Una fábrica de sillas puede fabricar 6 modelos distintos, en una cantidad de 100 por día. Cada modelo tiene una ganancia distinta para la empresa. ¿Cuál es la combinación óptima de sillas a producir para maximizar las ganancias o minimizar los costos?

*(Imagen de la página 1)*

Existen técnicas de búsqueda muy eficientes para optimizar los modelos lineales restringidos. A estos modelos optimizados se los conoce como **Programas Lineales (PL)**.

> [!important] Características de un PL
> - Siempre tiene una **función objetivo** (que deberá maximizarse o minimizarse).
> - Tiene **restricciones**.
> - Todas las funciones (objetivo y restricciones) son **funciones lineales**.

---

## Componentes de un Modelo de Programación Lineal

- **Variables de decisión:** Elementos sobre los cuales podemos interceder o cambiar.
- **Función objetivo:** Función que incluye las variables de decisión y que se desea optimizar (maximizar o minimizar).
- **Restricciones:** Limitaciones impuestas al grupo de decisiones permisibles.
- **Coeficiente:** Valores que acompañan a las variables de decisión y que contribuyen a la solución óptima.
- **Solución óptima:** Valores que toman las variables de la función objetivo para optimizar el problema.
- **Óptimo:** Es el valor que optimiza el problema de PL.

---

## Guía para la Formulación de Modelos

### 1. Definir el Objetivo
Exprese con palabras el objetivo y la función objetivo para la medición de su desempeño.

- *Ejemplo:* Maximizar las ganancias de la compañía, para el próximo mes, teniendo en cuenta que la producción no puede superar el límite que tiene la máquina embotelladora.
- *Ejemplo:* Minimizar los costos de la empresa, para los próximos seis meses, sin incumplir las restricciones que impone el sindicato.

### 2. Identificar las Variables de Decisión
Identifique verbalmente las variables de decisión.

- *Ejemplo:* Cantidad de kilos del Producto X a producir en un mes.

> [!tip] A veces pueden aparecer dudas o varias posibilidades. Es importante tener claro qué decisiones deben tomarse para optimizar la función objetivo.

### 3. Expresar las Restricciones con Palabras
Exprese cada restricción con palabras.

- *Ejemplo:* La cantidad de kilos del Producto X a procesar no puede ser mayor a 100 por día.

> [!attention] Preste especial atención al tipo de restricción:
> - `≥` (como mínimo / al menos)
> - `≤` (no mayor que / como máximo)
> - `=` (exactamente igual que)

### 4. Formulación Matemática
Al completar los pasos anteriores, invente una notación simbólica para las variables de decisión y exprese la función objetivo y cada restricción con símbolos.

---

## Tipos de Modelos de Programación Lineal

- **Modelo de Red:** Modelos en los cuales intervienen orígenes y destinos. Aplicaciones importantes en logística y distribución.
- **Modelo de Transporte:** Se utiliza para determinar la manera de asignar los productos de sus diferentes almacenes a sus clientes, para satisfacer la demanda con el menor costo de transporte posible.
- **Modelo de Asignación:** Sirve para determinar la asignación óptima de recursos (agentes de ventas a los territorios, puestos de trabajo a las máquinas, editores a los libros en producción).
- **Modelo de Planificación de la Producción:** Se utiliza para determinar la cantidad óptima a producir con el fin de maximizar las ganancias (MAX) o reducir los costos (MIN).
- **Modelo de Marketing:** Pensado para el diseño de una campaña eficaz de publicidad.

---

## Ejemplo Detallado: Problema de Planificación de la Producción (PROTRAC)

**PROTRAC, Inc.** produce dos tipos de Productos: **E** y **F**. La gerencia desea maximizar la contribución a las ganancias del mes entrante (margen de contribución = ingresos - costos variables).

### Datos del Problema

1.  **Margen de Contribución:**
    - Producto E: $5000 por tonelada.
    - Producto F: $4000 por tonelada.
2.  **Procesos de Producción:** Cada producto pasa por dos departamentos (A y B).
3.  **Horas Disponibles:**
    - Departamento A: 150 horas.
    - Departamento B: 160 horas.
4.  **Horas Requeridas por Producto:**
    - **Producto E:** 10 horas en Dpto. A, 20 horas en Dpto. B.
    - **Producto F:** 15 horas en Dpto. A, 10 horas en Dpto. B.
5.  **Acuerdo Sindical (Pruebas):** Las horas de prueba no deben ser más del 10% inferior a una meta de 150 horas (es decir, mínimo 135 horas).
    - Producto E: 30 horas de prueba.
    - Producto F: 10 horas de prueba.
6.  **Política de Gerencia:** Deberá construirse al menos una F por cada tres E.
7.  **Pedido de Distribuidor:** Orden de al menos cinco toneladas entre E y F (en cualquier combinación).

### Formulación del Modelo Matemático

**Variables de Decisión:**
- `E` = Toneladas del producto E a producir por mes.
- `F` = Toneladas del producto F a producir por mes.

**Función Objetivo:**
Maximizar `z = 5000E + 4000F`

**Restricciones:**

1.  **Horas Departamento A:** `10E + 15F ≤ 150`
2.  **Horas Departamento B:** `20E + 10F ≤ 160`
3.  **Horas de Verificación (Acuerdo Sindical):** `30E + 10F ≥ 135`
4.  **Relación E - F (Política de Gerencia):** `E - 3F ≤ 0` *(Esto asegura que E/3 ≤ F, es decir, al menos una F por cada tres E)*
5.  **Demanda Mínima (Pedido Distribuidor):** `E + F ≥ 5`
6.  **No Negatividad:** `E, F ≥ 0`

---

## Solución Gráfica

### Pasos para Graficar una Desigualdad

1.  Graficar la igualdad de la función lineal.
2.  Escoger un punto de prueba `(x1, x2)`.
3.  Resolver la expresión del lado izquierdo de la desigualdad, sustituyendo el punto de prueba.
4.  Determinar si el punto de prueba satisface la desigualdad.
    - **a)** Si la satisface, entonces la recta y todos los puntos que están al mismo lado que el punto de prueba satisfacen la desigualdad.
    - **b)** Si no la satisface, entonces la recta y todos los puntos que están en el lado opuesto satisfacen la desigualdad.

*(Imagen de la página 16: "Al graficar las 5 restricciones, encontramos lo que se conoce como: Región factible")*

---

## Restricciones en la Solución Óptima

### Activas u Obligatorias
Son aquellas restricciones en las cuales, al aplicar la optimalidad, el valor del lado izquierdo es igual al valor del lado derecho.

- **Ejemplo PROTRAC:** Las restricciones de horas de los Dptos. A y B son activas.
    - `10E + 15F = 150` para `E=4.5, F=7`
    - `20E + 10F = 160` para `E=4.5, F=7`

### Inactivas
Son aquellas restricciones en las cuales, al aplicar la optimalidad, el valor del lado izquierdo **NO** es igual al valor del lado derecho.

- **Ejemplo PROTRAC:** La restricción de horas de verificación es inactiva.
    - `30E + 10F = 205`, que es mayor a 135.

*(Imagen de la página 20: "Geométricamente, una restricción activa es la que pasa por la solución óptima")*

---

## Conceptos Clave: Holgura y Excedente

En condiciones de optimalidad:

- **Holgura:** Para una restricción `≤`, es la diferencia entre el lado derecho y el lado izquierdo (cantidad no usada). Su valor es **no negativo**.
    - *Ejemplo:* En la restricción `E - 3F ≤ 0`, con `E=4.5, F=7`, la holgura es `0 - (4.5 - 21) = 16.5`.
- **Excedente:** Para una restricción `≥`, es la diferencia entre el lado izquierdo y el lado derecho (cantidad sobrante). Su valor es **no negativo**.
    - *Ejemplo:* En la restricción `30E + 10F ≥ 135`, con `E=4.5, F=7`, el excedente es `205 - 135 = 70`.

> [!summary] Resumen
> - Una restricción de igualdad siempre es activa.
> - Una restricción de desigualdad puede ser activa o inactiva.
> - El valor de la holgura o excedente es **cero** si y solo si la restricción es **activa**.
> - Si el valor es **positivo**, la restricción es **inactiva**.

---

## El Método Simplex

### Convertir el Modelo para Simplex
Para optimizar mediante el Método Simplex, se deben convertir las restricciones de desigualdad en igualdades, añadiendo **variables de holgura (SH)** y **variables de excedente (SE)**.

- **Variables de Holgura (`SH`):** Se agregan (`+`) a las restricciones `≤`.
- **Variables de Excedente (`SE`):** Se restan (`-`) a las restricciones `≥`.

Estas nuevas variables cumplen con la condición de no negatividad y no aparecen en la función objetivo (coeficiente 0).

### Modelo PROTRAC Convertido

**Función Objetivo:**
`Maximizar z = 5000E + 4000F + 0*SH1 + 0*SH2 + 0*SH3 + 0*SE1 + 0*SE2`

**Restricciones (en forma de igualdad):**
1.  `10E + 15F + SH1 = 150`  (SH1: holgura de horas Dpto. A)
2.  `20E + 10F + SH2 = 160`  (SH2: holgura de horas Dpto. B)
3.  `30E + 10F - SE1 = 135`  (SE1: excedente de horas de verificación)
4.  `E - 3F + SH3 = 0`        (SH3: holgura de la relación E-F)
5.  `E + F - SE2 = 5`         (SE2: excedente de la demanda mínima)
6.  `E, F, SH1, SH2, SH3, SE1, SE2 ≥ 0`

### Valores Óptimos de Holgura/Excedente (para E=4.5, F=7)

- `SH1 = 150 - (10*4.5 + 15*7) = 0` → **Activa**
- `SH2 = 160 - (20*4.5 + 10*7) = 0` → **Activa**
- `SH3 = 0 - (4.5 - 3*7) = 16.5` → **Inactiva**
- `SE1 = (30*4.5 + 10*7) - 135 = 70` → **Inactiva**
- `SE2 = (4.5 + 7) - 5 = 6.5` → **Inactiva**

---

## Soluciones Degeneradas y No Degeneradas

- **Vértice Degenerado:** Cualquier vértice en el que el número de variables positivas es **menor** que el número de restricciones.
    - Si la solución óptima está en un vértice degenerado, se dice que es una **solución degenerada**.
- **Vértice No Degenerado:** Cuando el número de variables positivas es **exactamente igual** al número de restricciones.
    - Si la solución óptima está en un vértice no degenerado, se dice que es una **solución no degenerada**.

**Ejemplo PROTRAC:** La solución es **no degenerada**.
- **Gráficamente:** Dos rectas de restricción activas se intersectan en el vértice óptimo.
- **Analíticamente:** Hay 5 variables positivas (`E, F, SH3, SE1, SE2`) y el número de restricciones es 5.

---

## Filosofía del Método Simplex

El método simplex es, en esencia, un proceso equivalente al de escalar una colina.

1.  Encuentra una solución en un vértice.
2.  Examina todos los vértices inmediatamente vecinos.
3.  Plantea la pregunta: *“Si me traslado a uno de esos vértices, ¿mejorará el valor de la función objetivo?”*
4.  Si la respuesta es afirmativa, se traslada a dicho vértice y repite el proceso.
5.  Cuando la respuesta es negativa (no hay vecino que mejore la solución), el algoritmo concluye, habiendo encontrado el óptimo.