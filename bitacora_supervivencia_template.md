# Bitácora de supervivencia — CitasSalud+

**Estudiante:** Ana Sofía Campos Garita
**Sección:** 11-6
**Fecha:** 27/8/26

## Escenario

Durante la ejecución de la prueba de performance (JMeter, listado de citas con
500 registros simulados — ver Anexo 1), el servidor principal de CitasSalud+
se satura y queda fuera de línea.

## 1. Identificación

<!-- ¿Cómo se detectó que el servidor había caído? ¿Qué señal o dato lo evidenció? -->
Se dectecto que el servidor se había caído debido a que dejo de dar servicios y los usuarios no podían ingresar a agendar sus citas médicas, los encargados utilizaron el comando ping para hacer la verificación de si había conectividad con el servidor


## 2. Contención

<!-- ¿Qué acción se tomó de inmediato para limitar el impacto? -->
En caso de tener activar inmediatamente la redundancia del servidor para que los usuarios no se queden sin servicio y puedan seguir accediendo a sus datos médicos, luego de eso hacer una revisión de los logs del servidor a ver que evento fue el que ocacno su caída 


## 3. Recuperación

<!-- ¿Qué acción concreta permitió que la aplicación siguiera operando para
     citas de emergencia? Esta acción debe reflejarse en un commit de este
     repositorio con un mensaje descriptivo. -->
     Se hará la activación de un servidor secundario 
     que provea los mismos servicios que el servidor principal.



**Commit de recuperación:** (Activar servidor secundario por caída del principal)

## 4. Aprendizaje / mejora

<!-- ¿Qué estrategia complementaria (respaldo, redundancia o monitoreo)
     hubiera anticipado este resultado, en relación con el criterio de
     performance del Anexo 1 (listado de citas en menos de 3 segundos)? -->
Tener un límite de citas posibles a agendar por cada usuario determinadas por las capacidades del servidor 
