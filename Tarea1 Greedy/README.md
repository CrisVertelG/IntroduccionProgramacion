# Tarea 1 - Algoritmos Greedy

**Curso:** Análisis de algoritmos  
**Institución:** Instituto Tecnológico Metropolitano (ITM)  
**Periodo:** 2026-2  
**Lenguaje:** Python

---

## 1. 860. Lemonade Change

**Problema:** [860. Lemonade Change - LeetCode](https://leetcode.com/problems/lemonade-change/)

**Criterio Greedy:** Se procesa cada cliente en orden de llegada. Cuando un cliente paga con un billete de 20, se prioriza devolver un billete de 10 y uno de 5 para conservar la mayor cantidad posible de billetes de 5 para futuros cambios. Si no es posible, se utilizan tres billetes de 5. Si no se puede devolver el cambio exacto, se retorna `False`.

**Complejidad:**
- Tiempo: O(n), porque se recorre la lista una sola vez.
- Espacio: O(1), porque se utilizan únicamente variables auxiliares.

**Evidencia de Accepted:**

[Ver captura de Lemonade Change](Evidencia/LemonChange.png)

---

## 2. 455. Assign Cookies

**Problema:** [455. Assign Cookies - LeetCode](https://leetcode.com/problems/assign-cookies/)

**Criterio Greedy:** Se ordenan los niños y las galletas de menor a mayor. En cada paso se intenta asignar la galleta más pequeña que pueda satisfacer al niño menos exigente que todavía no ha recibido una. Si la galleta no es suficiente, se prueba con una más grande. Así se maximiza la cantidad de niños satisfechos.

**Complejidad:**
- Tiempo: O(n log n + m log m), debido al ordenamiento de las dos listas y su posterior recorrido.
- Espacio: O(n + m), considerando la memoria auxiliar utilizada por el ordenamiento.

Donde n representa la cantidad de niños y m la cantidad de galletas.

**Evidencia de Accepted:**

[Ver captura de Assign Cookies](Evidencia/Cookies.png)
