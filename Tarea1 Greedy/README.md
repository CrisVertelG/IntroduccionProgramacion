# Tarea 1 - Algoritmos Greedy

**Curso:** Análisis de algoritmos  
**Institución:** Instituto Tecnológico Metropolitano (ITM)  
**Lenguaje:** Python

## 1. 860. Lemonade Change
Enlace:https://leetcode.com/problems/lemonade-change/
Criterio Greedy
Se recorren los clientes en el orden de llegada, llevando un registro de los billetes de 5 y 10 disponibles.
Cuando un cliente paga con 20, se prioriza entregar un billete de 10 y uno de 5, ya que esta combinación permite conservar más billetes de 5 para futuros clientes. Si no es posible, se entregan tres billetes de 5.
Si no se puede devolver el cambio exacto, el algoritmo retorna `False`. Si todos los clientes pueden ser atendidos, retorna `True`.


2. 455. Assign Cookies

Enlace: LeetCode - Assign Cookies](https://leetcode.com/problems/assign-cookies/
Criterio Greedy
Se ordenan las listas de niños y galletas de menor a mayor. Después, se recorren las galletas intentando satisfacer primero al niño con menor exigencia.
Si el tamaño de la galleta es suficiente para satisfacer al niño actual, se le asigna y se avanza al siguiente. Si no es suficiente, se prueba con una galleta más grande.
De esta manera se utilizan las galletas más pequeñas posibles para cada niño, reservando las más grandes para quienes tienen mayor exigencia.

