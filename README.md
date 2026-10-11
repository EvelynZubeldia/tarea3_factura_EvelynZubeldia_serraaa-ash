# Tarea 3 · La factura bajo el microscopio
Pareja: Evelyn y Antonio · GitHub: EvelynZubeldia, serraaa-ash

## Reto 1 · Compilar desde la terminal
- Comando usado y resultado (captura: capturas/reto1.png)
- ¿Qué es Factura.java? Es el código fuente escrito en lenguaje java que tiene las instrucciones que dice como debe funcionar el programa 
-¿Y Factura.class? Es el archivo compilado que contiene el bytecode. No está pensado para ser leido por personas sino para ser interpretado y jecutado por la maquina virtual de Java.
-¿Quién ejecuta el .class? Lo ejecuta la máquina virtual de Java.
- ¿Por qué no se ha generado Factura.class la primera vez? No se ha generado porque el código de factura.java tiene errores de sintaxis por lo que el compilador se detiene al encontrar errores para no generar un archivo ejecutable defectuoso.

## Reto 2 · Errores de compilación
| Nº | Línea | Mensaje de javac | Tipo (léxico / sintaxis / semántica) | Corrección |
|----|-------|------------------|--------------------------------------|------------|
| 1  |linea 15. factura.java:15:error:illegal character "#". Error léxico  
| 2  |linea 17. factura.java:17:error:expected ";". Error de sintaxis
| 3  |linea 28. ifactura.java:28:error: incompatible types: possible lossy conversation from double to int. 
Captura del programa funcionando: capturas/reto2.png

## Reto 3 · Depuración del error lógico
| Variable | Valor esperado | Valor real |
|----------|----------------|------------|
| descuento |               |            |
| total     |               |            |
- Línea del error y explicación:
- Corrección:
- Mi propia prueba (producto, precio, cantidad, socio → total):
Captura del depurador: capturas/reto3.png

## Reto 4 · Reutilización
- Métodos creados y para qué sirve cada uno:
- ¿Qué ventaja tiene frente al código anterior?

## Reto 5 · ¿Qué lenguaje elegirías?
- Caso A (web de la tienda):
- Caso B (propuesta en ensamblador):
