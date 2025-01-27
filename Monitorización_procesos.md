## MONITORIZACIÓN DE PROCESOS

En la administración de sistemas informáticos y redes, la monitorización
de procesos es una tarea fundamental para garantizar el rendimiento,
estabilidad y seguridad de los servidores. Linux ofrece varias
herramientas en línea de comandos para monitorizar el hardware: CPU,
memoria, uso de disco duro y red.

# 1. Comando ps
   
El comando ps proporciona una instantánea de los procesos en
ejecución. Es útil para obtener información específica sobre
procesos.

Sintaxis básica:

ps [opciones]
Opciones comunes:

● ps sin opciones:

![ps](img/Ps_sin_opciones.png)

● ps a:

![ps_a](img/ps_a.png)

● ps aux:

![ps_aux](img/ps_aux.png)

● ps -C nano <nombre>: 

# 2. Comando top

El comando top permite monitorizar el sistema en tiempo real y
detectar procesos que consumen muchos recursos,
proporcionando una vista dinámica y en tiempo real de los
procesos en ejecución y el uso de recursos del sistema (CPU,
memoria y procesos en ejecución).
Sintaxis básica:

top [opciones]
Opciones comunes:

● top T:

![top_t](img/Top_T.png)

● top M:

![top_m](img/Top_M.png)

● top P:

!![top_r](img/Top_P.png)


● top p:

● top R:

![top_r](img/Top_R.png)

● top U:

![top_u](img/Top_U.png)

● top q:


● top k:

![top_k](img/Top_k.png)

# 3. Comando htop

htop es una versión mejorada y más amigable de top, con una
interfaz interactiva y funcionalidad adicional.

Sintaxis básica:
htop [opciones]
Opciones:

● htop -u <usuario>:

![Htop_U](img/Htop_U.png)

● htop --tree:

![Htop_tree](img/Htop_tree.png)

● htop -p <PID1,PID2>:

![Htop_tree](img/htop_P.png)

Atajos de Teclado:

● F2 (Setup) - Configuración

![htop_f2.png](img/htop_f2.png)

● F3 (Search) - Búsqueda

![htop_f3.png](img/htop_f3.png)

● F4 (Filter) - Filtro

![htop_f4.png](img/htop_f4.png)

● F5 (Tree) - Vista en árbol



● F6 (Sort) - Ordenar

![htop_f6.png](img/htop_f6.png)

● F9 (Kill) - Terminar un Proceso

# 4. Comando atop

atop es una herramienta avanzada para monitorizar no solo
procesos, sino también otros recursos del sistema, como disco, red
y memoria.

Uso básico:
● Ejecutar en tiempo real:

atop

![atop](img/atop.png)

● Consultar registros guardados:

atop -r archivo_de_registratop

![atop_r](img/atop_r.png)
