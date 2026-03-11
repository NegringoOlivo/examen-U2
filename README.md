# examen-U2
Fundamentos de programación U2

Proyecto de Programación Secuencial:
Cotizador de Paquetes Turísticos
Exámen de Fundamentos de Programación U2
Marzo de 2026
Contexto del Problema
Una agencia de viajes requiere un sistema automatizado para generar cotizaciones rá-
pidas para familias. El sistema debe calcular el costo total de un viaje, aplicando des-
cuentos automáticos para los niños en los vuelos y en el hospedaje, y finalmente cal-
cular la comisión de la agencia de viajes.
Requerimientos de Entrada
El programa debe solicitar al usuario ingresar los siguientes datos por teclado:
- Cantidad de adultos.
- Cantidad de niños.
- Días de estancia (noches de hotel).
- Costo estándar del vuelo (tarifa por adulto).
- Costo estándar de hospedaje (tarifa por noche por adulto).
Reglas de Negocio y Cálculos (Salidas Esperadas)
El sistema procesará los datos de entrada para imprimir el desglose de la cotización
basándose en las siguientes reglas y mostrará:
1. Costo total de vuelos: Los adultos pagan la tarifa completa. Los niños tienen un
descuento del 50% en su vuelo. Se debe mostrar la suma total a pagar por los
vuelos de toda la familia.
2. Costo total de hospedaje: Los adultos pagan la tarifa completa por noche. Los
niños pagan solo el 30% de la tarifa de adulto por noche. Se debe mostrar el total
del hotel por todas las noches de toda la familia.
3. Subtotal del Viaje: Lasumadelcostototaldevuelosyelcostototaldehospedaje.
1
4. Comisión de la Agencia: La agencia cobra una tarifa de servicio equivalente al
12% del Subtotal del viaje.
5. Costo Total del Paquete: El Gran Total a cobrar al cliente (Subtotal + Comisión).
Restricciones Técnicas y Estructura
Para evaluar el dominio de la programación estructurada y la modularidad, se deben
cumplir estrictamente las siguientes reglas:
- Cero Estructuras de Control: Quedaabsolutamenteprohibidoelusodeif,else,
switch, for, while o do-while.
- Arquitectura de Dos Archivos: La solución debe dividirse en dos archivos .java:
- Archivo 1 (Clase de Herramientas/Cálculos): Debecontenerúnicamente mé-
todosestáticos(public static)querealicenlasoperacionesmatemáticas.Se
sugierecrearmétodoscomocalcularDescuento,calcularCostoGrupal,calcularPorcent
etc.
- Archivo 2 (Clase Principal): Debecontenerelmétodomain.Suúnicarespon-
sabilidad es leer los datos usando Scanner, invocar los métodos del Archivo
1 en el orden lógico correcto, y mostrar el desglose de resultados en consola
de forma presentable.
