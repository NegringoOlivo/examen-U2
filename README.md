# examen-U2
Fundamentos de programación U2

Proyecto de Programación Secuencial: Cotizador de Paquetes Turísticos

Exámen de Fundamentos de Programación U2 - Marzo de 2026

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

3. Subtotal del Viaje: La suma del costo total de vuelos y el costo total de hospedaje.

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



\documentclass[12pt, a4paper]{article}

% --- UNIVERSAL PREAMBLE BLOCK ---
\usepackage[a4paper, top=2.5cm, bottom=2.5cm, left=2cm, right=2cm]{geometry}
\usepackage{fontspec}
\usepackage{amsmath}
\usepackage{enumitem}

\usepackage[spanish, bidi=basic, provide=*]{babel}

\babelprovide[import, onchar=ids fonts]{spanish}
\babelprovide[import, onchar=ids fonts]{english}

% Set default/Latin font to Sans Serif in the main (rm) slot
\babelfont{rm}{Noto Sans}
\babelfont[spanish]{rm}{Noto Sans}

% Ensure list bullets render correctly
\setlist[itemize]{label=-}

\title{Proyecto de Programación Secuencial:\\Cotizador de Paquetes Turísticos}
\author{Práctica de Fundamentos de Programación}
\date{Marzo de 2026}

\begin{document}

\maketitle

\section*{Contexto del Problema}
Una agencia de viajes requiere un sistema automatizado para generar cotizaciones rápidas para familias. El sistema debe calcular el costo total de un viaje, aplicando descuentos automáticos para los niños en los vuelos y en el hospedaje, y finalmente calcular la comisión de la agencia de viajes.

\section*{Requerimientos de Entrada}
El programa debe solicitar al usuario ingresar los siguientes datos por teclado:
\begin{itemize}
    \item Cantidad de adultos.
    \item Cantidad de niños.
    \item Días de estancia (noches de hotel).
    \item Costo estándar del vuelo (tarifa por adulto).
    \item Costo estándar de hospedaje (tarifa por noche por adulto).
\end{itemize}

\section*{Reglas de Negocio y Cálculos (Salidas Esperadas)}
El sistema procesará los datos de entrada para imprimir el desglose de la cotización basándose en las siguientes reglas y mostrará:
\begin{enumerate}
    \item \textbf{Costo total de vuelos:} Los adultos pagan la tarifa completa. Los niños tienen un descuento del $50\%$ en su vuelo. Se debe mostrar la suma total a pagar por los vuelos de toda la familia.
    \item \textbf{Costo total de hospedaje:} Los adultos pagan la tarifa completa por noche. Los niños pagan solo el $30\%$ de la tarifa de adulto por noche. Se debe mostrar el total del hotel por \textit{todas las noches} de \textit{toda la familia}.
    \item \textbf{Subtotal del Viaje:} La suma del costo total de vuelos y el costo total de hospedaje.
    \item \textbf{Comisión de la Agencia:} La agencia cobra una tarifa de servicio equivalente al $12\%$ del Subtotal del viaje.
    \item \textbf{Costo Total del Paquete:} El Gran Total a cobrar al cliente (Subtotal $+$ Comisión).
\end{enumerate}

\section*{Restricciones Técnicas y Estructura}
Para evaluar el dominio de la programación estructurada y la modularidad, se deben cumplir estrictamente las siguientes reglas:
\begin{itemize}
    \item \textbf{Cero Estructuras de Control:} Queda absolutamente prohibido el uso de \texttt{if}, \texttt{else}, \texttt{switch}, \texttt{for}, \texttt{while} o \texttt{do-while}.
    \item \textbf{Arquitectura de Dos Archivos:} La solución debe dividirse en dos archivos \texttt{.java}:
    \begin{itemize}
        \item \textbf{Archivo 1 (Clase de Herramientas/Cálculos):} Debe contener \textit{únicamente} métodos estáticos (\texttt{public static}) que realicen las operaciones matemáticas. Se sugiere crear métodos como \texttt{calcularDescuento}, \texttt{calcularCostoGrupal}, \texttt{calcularPorcentaje}, etc.
        \item \textbf{Archivo 2 (Clase Principal):} Debe contener el método \texttt{main}. Su única responsabilidad es leer los datos usando \texttt{Scanner}, invocar los métodos del Archivo 1 en el orden lógico correcto, y mostrar el desglose de resultados en consola de forma presentable.
    \end{itemize}
\end{itemize}

\end{document}
