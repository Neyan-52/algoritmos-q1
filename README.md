# algoritmos-q1
El algoritmo resuelve el problema de la gestión y revisión de inventario en una tienda en línea. El usuario ingresará como datos de entrada la cantidad total de artículos a evaluar (N) y el stock individual en unidades de cada uno de ellos. Durante el procesamiento, el sistema valida rigurosamente que cada valor de stock ingresado sea mayor o igual a cero para evitar datos erróneos. Luego, acumula estas cantidades para calcular el stock total disponible en toda la tienda. Simultáneamente, el algoritmo realiza una búsqueda para detectar si existen artículos agotados con stock cero, registrando de forma precisa la posición del arreglo en la que se localizan. Como salidas, el programa muestra en pantalla el inventario total calculado y un reporte detallado indicando las posiciones exactas donde se detectó desabastecimiento.

[Diagrama de Flujo](NombreDeTuImagenDiagrama de stocks de productos.png)

Algoritmo ControlStock

VARIABLES
    N, i, stock_total, stock_actual: ENTERO
    ARREGLO[100] DE ENTERO: stock

Inicio

    stock_total<-0

    i<-1

    Escribir "Ingrese la cantidad total de productos:"
    Leer N
        Mientras i<=N Hacer
            Escribir "Ingrese el stock del producto ",i,":"
            Leer stock_actual
                Si stock_actual<0 Entonces
                    Escribir "Error: El stock no puede ser negativo."
                Sino
                    stock_total<-stock_total+stock_actual
                Si stock_actual=0 Entonces
                    Escribir "Producto agotado en la posición: ",i
                    FinSi
                i<-i+1
                FinSi
                FinMientras
    Escribir "El inventario total calculado es: ",stock_total
    FinAlgoritmo
## Contenido
- Unidad 1: Introducción a los algoritmos
- Unidad 2: Estructuras de decisión
- Unidad 3: Estructuras de ciclos (PARA, MIENTRAS, HACER-MIENTRAS)
- Unidad 4: Arreglos y matrices
## Herramientas
Pseudocódigo en español neutro, sin lenguaje de programación específico.
### Tabla de Trazado (Prueba de Escritorio)
Esta tabla simula el comportamiento del algoritmo con un inventario de 3 productos (N = 3). Incluye un caso con stock normal (5), un caso de error con número negativo (-2) que obliga a corregir el dato ingresando un producto agotado (0), y un último producto normal (10).

|i|N|¿i<=N? |stock_actual |¿stock_actual<0? |¿stock_actual==0? |stock_total |PANTALLA / SALIDA |
|---|---|---|---|---|---|---|---|
|1|5|Verdadero|8|Falso|Falso|8||
|2|5|Verdadero|0|Falso|Verdadero|8|"Producto agotado en la posición: 2"|
|3|5|Verdadero|-3|Verdadero|-|8|"Error: El stock no puede ser negativo."|
|3|5|Verdadero|12|Falso|Falso|20||
|4|5|Verdadero|5|Falso|Falso|25||
|5|5|Verdadero|0|Falso|Verdadero|25|"Producto agotado en la posición: 5"|
|6|5|Falso|-|-|-|-|"El inventario total calculado es: 25"|

## Autor
Neyan Castellanos - Q1 20261
