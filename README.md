# Nginx

## 1. Introducción
Nginx es un servidor web de alto rendimiento y proxy inverso, ampliamente utilizado por su eficiencia en la gestión de conexiones concurrentes y su baja utilización de recursos. Originalmente desarrollado como solución para el problema C10k (manejo de 10,000 conexiones simultáneas), ha ganado popularidad en aplicaciones web modernas por su capacidad para equilibrar carga, servir contenido estático rápidamente y actuar como proxy para aplicaciones dinámicas.

En la empresa Servicios Web RC, S.A., se ha planteado la migración desde Apache a Nginx con el objetivo de mejorar el rendimiento y la escalabilidad de los servicios ofrecidos.

---

## 2. Comparativa con Apache

Para la comparativa con Apache tendremos en cuenta los siguientes aspectos:

1. **Arquitectura**:  
   - Apache utiliza un modelo basado en procesos o hilos (dependiendo del módulo MPM configurado). Esto implica que cada conexión requiere un hilo o proceso dedicado, lo que puede generar un mayor uso de recursos en escenarios con muchas conexiones concurrentes.  
   - Nginx, en cambio, se basa en un modelo asincrónico y dirigido por eventos, lo que le permite manejar múltiples conexiones simultáneamente dentro de un solo hilo, utilizando significativamente menos recursos.

2. **Gestión de conexiones**:  
   - Apache no es tan eficiente cuando se trata de manejar conexiones concurrentes, especialmente en grandes volúmenes.  
   - Nginx está diseñado específicamente para manejar miles de conexiones concurrentes de manera eficiente.

3. **Consumo de recursos**:  
   - Apache suele requerir más memoria RAM y CPU, especialmente en configuraciones de alta carga.  
   - Nginx tiene un consumo de recursos más reducido, lo que lo hace ideal para entornos con limitaciones de hardware.

4. **Rendimiento en contenido estático**:  
   - Apache es rápido al servir contenido estático, pero no tanto como Nginx.  
   - Nginx destaca por su velocidad y eficiencia al manejar archivos estáticos como imágenes, CSS y JavaScript.

5. **Configuración**:  
   - Apache ofrece flexibilidad extrema en sus configuraciones, pero esto puede hacerlo más complejo de gestionar.  
   - Nginx tiene una configuración más sencilla y estructurada, lo que facilita su administración.

6. **Módulos**:  
   - Apache cuenta con una amplia variedad de módulos dinámicos que pueden activarse o desactivarse sin necesidad de recompilar el servidor.  
   - En Nginx, algunos módulos requieren recompilación para ser añadidos, lo que puede limitar su flexibilidad.

7. **Casos de uso**:  
   - Apache se utiliza comúnmente en aplicaciones dinámicas que requieren configuraciones muy específicas.  
   - Nginx se emplea frecuentemente como proxy inverso, balanceador de carga o servidor para contenido estático.

8. **Documentación y comunidad**:  
   - Apache tiene una documentación muy extensa y una comunidad consolidada debido a su larga trayectoria.  
   - Nginx también cuenta con buena documentación, aunque es algo menos extensa comparada con Apache.

---

## 3. Esquema de red

A continuación, se presenta un esquema básico de red para implementar Nginx como servidor web y proxy inverso:

   - Clientes: Usuarios que acceden al servicio web.

   - Servidor Nginx: Actúa como proxy inverso, distribuyendo las peticiones a los servidores backend.

   - Servidores Backend: Procesan las peticiones dinámicas y generan las respuestas necesarias.

Nginx se posiciona como un punto central en la red, manejando las conexiones y distribuyendo las cargas de manera eficiente para maximizar el rendimiento del sistema.


