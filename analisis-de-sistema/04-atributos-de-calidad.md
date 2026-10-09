# 04. Atributos de calidad

| ID | Atributo | Escenario | Respuesta medible |
|---|---|---|---|
| AC01 | Rendimiento | El pasajero toca “Buscar moto”. | La solicitud llega a conductores cercanos en menos de 3 segundos. |
| AC02 | Tiempo real | El conductor se desplaza durante un viaje. | Ubicación cada 3 a 5 segundos sin recargar la pantalla. |
| AC03 | Tolerancia a cortes | El teléfono pierde datos brevemente. | Recupera del servidor el viaje vigente sin duplicarlo. |
| AC04 | Disponibilidad | Operación mensual normal. | 99.5 % mensual para funciones propias y degradación controlada ante fallas externas. |
| AC05 | Escalabilidad | Crece el piloto. | Soportar 2 000 conductores y 300 viajes simultáneos, verificado con carga. |
| AC06 | Seguridad | Una app modificada intenta cambiar saldo o estado. | Rechazar todas las escrituras no autorizadas y registrar el intento. |
| AC07 | Privacidad | Soporte revisa un caso. | Datos ocultos por defecto; enlaces de documentos de máximo cinco minutos; acceso auditado. |
| AC08 | Usabilidad | Una persona solicita una moto. | Acción principal en tres toques; botones de 48 dp y contraste AA. |
| AC09 | Eficiencia | Conductor conectado ocho horas. | Menos de 60 MB de datos y frecuencia GPS acorde al estado. |
| AC10 | Compatibilidad | Instalación en gama baja. | Inicio menor a 4 segundos en Android 9 con 2 GB y paquete menor a 40 MB. |
| AC11 | Auditoría | Se revisa recarga, sanción o configuración. | Reconstruir actor, fecha, motivo y valores; conservar dos años. |
| AC12 | Recuperación | Ocurre pérdida de datos. | Copia diaria por treinta días y restauración probada mensualmente. |
| AC13 | Mantenibilidad | Cambia el proveedor de mapas. | Sustituir adaptadores sin reescribir reglas ni pantallas. |

Estas metas deben comprobarse con telemetría, carga, pruebas de seguridad y simulaciones de desconexión antes del lanzamiento.
