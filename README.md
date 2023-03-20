# Calculadora astronomía
Práctica realizada para la asignatura de "Astronomía y Geodesia" en el curso 2022-23. Consiste en una calculadora de los tiempos de visibilidad de un determinado cuerpo para todos los días del año, tomando como punto de observación el observatorio de La Palma.

La función principal es visibility_hours(), que se encarga de realizar todos los cálculos que llevamos a cabo para el caso concreto del 21 de diciembre, solo que para todos los días del año, y va guardando las horas de comienzo y fin de visibilidad en una lista. Cada elemento de la lista es una lista de tuplas (pares), para representar los intervalos de visibilidad de ese día. 

Tenemos además una función auxiliar quitarHorasSol para quitar las horas de Sol que intersecan con las horas de ARP273 sobre el horizonte, haciéndolo por casos en función de los 4 valores de orto y ocaso de ambos. También tenemos convertirHoras para convertir las horas en float (con las que trabajamos los cálculos por sencillez) a horas, minutos y segundos. Esto se utilizará en printDias, que imprime por pantalla los intervalos de visibilidad para todos los días del año en un formato legible.  

Por último, graficaIntervalos muestra en una gráfica esos intervalos de tiempo a lo largo de todo el año, igual a cómo se ve en la página de LCO. Hay que tener en cuenta que los resultados no son iguales a los de [LCO](https://lco.global/observatory/tools/visibility/), ya que en ellos están quitando no solo las horas de Sol, sino también las horas en las que H>4.6, luego nuestro intervalo de visibilidad es mayor.
