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
| descuento | 18,00 € | 6,00 € |
| total | 123,42 € | 137,94 € |

- **Línea del error y explicación:** la línea 26, `descuento = base * 0.05;`. Con el `=` el 5 % del socio machaca el 10 % que ya estaba calculado en vez de sumarse, y por eso el descuento se queda en 6 €.
- **Corrección:** cambiar el `=` por `+=`, que queda `descuento += base * 0.05;`. Así se suman los dos descuentos y con 60, 2 y s da 123,42 €.
- **Mi propia prueba:** auriculares, precio 25, cantidad 4, socio s → total 114,95 €. Lo he elegido porque la base sale justo 100 € y, como no supera 100, no se aplica el 10 %, solo el 5 % del socio: (100 − 5) × 1,21 = 114,95 €.

Captura del depurador: capturas/reto3.png

## Reto 4 · Reutilización
- Métodos creados y para qué sirve cada uno:
- `calcularDescuento(double base, boolean socio)`: le paso la base y si es socio, y me devuelve el descuento total (el 10 % si la base pasa de 100 € y un 5 % más si es socio).
- `aplicarIVA(double importe)`: le paso un importe y me lo devuelve con el 21 % de IVA sumado. En el main ahora solo pido los datos y llamo a los métodos. Con 60, 2 y s sigue dando 123,42 €.
- ¿Qué ventaja tiene frente al código anterior?
El main queda más corto y se entiende mejor, porque cada cálculo tiene su nombre. Si cambia una regla (por ejemplo el IVA o el descuento de socio) solo hay que cambiarla en un sitio, y los métodos se pueden reutilizar en otras partes del programa sin copiar el código.

## Reto 5 · ¿Qué lenguaje elegirías?
- Caso A (web de la tienda): usaría un lenguaje interpretado, como JavaScript. Es portable, porque funciona en cualquier navegador sin instalar nada, y es el adecuado para este tipo de proyecto, porque es una web.
- Caso B (propuesta en ensamblador): no lo haría, seguiría con Java. El ensamblador no es portable, porque depende del procesador y no funcionaría en cualquier ordenador, y el coste de desarrollo sería mucho mayor para una calculadora que ya va rápida.
