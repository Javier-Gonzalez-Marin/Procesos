# Nginx

## 1. Introducción
Nginx es un servidor web de alto rendimiento y proxy inverso, ampliamente utilizado por su eficiencia en la gestión de conexiones concurrentes y su baja utilización de recursos. Originalmente desarrollado como solución para el problema C10k (manejo de 10,000 conexiones simultáneas), ha ganado popularidad en aplicaciones web modernas por su capacidad para equilibrar carga, servir contenido estático rápidamente y actuar como proxy para aplicaciones dinámicas.

En la empresa Servicios Web RC, S.A., se ha planteado la migración desde Apache a Nginx con el objetivo de mejorar el rendimiento y la escalabilidad de los servicios ofrecidos.

---

## 2. Comparativa con Apache

| Característica            | Apache                             | Nginx                              |
|---------------------------|-------------------------------------|-------------------------------------|
| **Arquitectura**          | Basado en procesos/hilos (MPM)     | Basado en eventos asincrónicos      |
| **Gestión de conexiones** | Cada conexión requiere un hilo o proceso | Manejo eficiente con un solo hilo para múltiples conexiones |
| **Consumo de recursos**   | Mayor consumo de RAM y CPU         | Consumo reducido de RAM y CPU       |
| **Contenido estático**    | Rápido pero menos eficiente que Nginx | Excelente para servir contenido estático |
| **Configuración**         | Flexible pero más complejo         | Sencillo y estructurado            |
| **Módulos**               | Más extensos y dinámicos           | Menos módulos y requiere recompilación para añadir algunos |
| **Uso común**             | Aplicaciones dinámicas con muchas configuraciones específicas | Proxy inverso, balanceo de carga y contenido estático |
| **Documentación y Comunidad** | Muy amplia y consolidada        | Amplia, aunque algo menos extensa que Apache |

---

## 3. Esquema de red

A continuación, se presenta un esquema básico de red para implementar Nginx como servidor web y proxy inverso:

